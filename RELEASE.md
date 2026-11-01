# Publier une édition du kit

Chaque édition du kit de campagne est une **Release** de ce dépôt. Le jeu lit une seule adresse, le manifeste de la dernière Release :

```
https://github.com/Mitchnsun/kit-de-campagne/releases/latest/download/manifest.json
```

Les Releases sont **immuables** : une fois publiée, une Release ne change plus, ni ses fichiers ni son tag. Une erreur ne se corrige donc pas sur place : elle se corrige par une révision (voir « Corriger une édition publiée »). Le service du kit est décrit dans le dépôt de l'app, à la section « KitProvider Context » de `docs/ARCHITECTURE.md`.

## Ce qu'une Release contient

- **Un tag `edition-AAAA-MM`**, le mois de l'édition : `edition-2026-11`. Une révision du même mois prend `-2`, puis `-3`, jusqu'à `-9` : `edition-2026-11-2`.
- **Les fichiers de l'édition**, à plat : une image `<id-de-la-carte>.webp` par carte d'événement.
- **`manifest.json`**, écrit par `yarn kit:build`. Il donne pour chaque partie la liste de ses éditions, de la plus récente à la plus ancienne. Pour chaque édition, il donne :
  - la version minimale de l'app qui la lit ;
  - l'adresse de ses fichiers ;
  - ses crédits ;
  - la taille et l'empreinte SHA-256 de chaque fichier.

  Les éditions plus anciennes restent dans le manifeste, et leurs fichiers dans leur propre Release. Une app trop ancienne pour la dernière édition télécharge ainsi la dernière qu'elle sait lire.

Ne jamais supprimer une Release publiée : des joueurs peuvent encore en dépendre.

## Une fois pour toutes

- Le réglage **« Enable release immutability »** est coché : _Settings › General › Releases_.
- Le dépôt de l'app (`Mitchnsun/moi-president`) et celui-ci sont clonés côte à côte, dans le même dossier : `yarn kit:build` lit `../kit-de-campagne/prompts` par défaut. Un autre dossier se donne avec `--illustrations chemin/vers/prompts`.
- Dans le dépôt de l'app, Node (version de `.nvmrc`) et Yarn par Corepack sont installés : `corepack enable`, puis `yarn install`.
- L'outil [`gh`](https://cli.github.com/) est installé et connecté, avec les droits d'écriture sur ce dépôt : `gh auth login`.

## 1. Vérifier les images

Chaque image de l'édition est dans [`prompts/`](prompts/), avec sa fiche relue et validée. Elle est exportée selon le [gabarit](prompts/gabarit.md) : WebP de qualité 75, 1290 × 726 px (ou 1290 × 860 px pour une image restée en 3:2). Mettre à jour les deux dépôts :

```bash
git -C kit-de-campagne pull
git -C moi-president pull
```

## 2. Préparer l'édition

Dans le dépôt de l'app :

```bash
cd moi-president
```

**Première édition :**

```bash
yarn kit:build --edition 2026-11
```

**Édition suivante :** partir du manifeste de la dernière Release, pour garder les éditions précédentes.

```bash
gh release download --repo Mitchnsun/kit-de-campagne --pattern manifest.json --dir /tmp/kit-precedent
yarn kit:build --edition 2027-03 --previous /tmp/kit-precedent/manifest.json
```

Le script :

- **vérifie chaque image** : un WebP de 1290 × 726 ou 1290 × 860 px, 400 Kio au plus. Une image hors règle fait échouer le script, qui dit pourquoi ;
- **copie les images et écrit `manifest.json`** dans `dist/kit/`, ou dans le dossier donné par `--out`, puis donne le nombre d'images et leur poids total en Mo ;
- **relit le manifeste comme l'app le lira** : un manifeste que l'app refuserait (une adresse hors des Releases de ce dépôt, une version mal écrite) fait échouer le script, et rien n'est à publier ;
- **liste les cartes du jeu sans image**, sans échouer : une carte sans image reste jouable ;
- **liste les images dont le nom n'est l'`id` d'aucune carte**, sans échouer : par exemple une carte d'une branche pas encore fusionnée. Relire la liste : une faute de frappe dans un nom y apparaît aussi, et l'image ne s'afficherait jamais.

**La version minimale de l'app** est par défaut celle du dépôt de l'app, dans `package.json`. On la change avec `--min-app-version 0.2.0`, seulement quand l'édition demande une app plus récente : un nouveau format de fichier, une nouvelle partie. Les éditions précédentes restent alors proposées aux apps plus anciennes.

## 3. Essayer l'édition avant de la publier (conseillé)

Préparer une copie dont les fichiers sont servis par un serveur local, puis lancer l'app sur ce kit :

```bash
yarn kit:build --edition 2026-11 --out dist/kit-essai --base-url http://localhost:8080/
npx serve dist/kit-essai --cors -l 8080
# dans un autre terminal
EXPO_PUBLIC_KIT_URL=http://localhost:8080 yarn web
```

Sur un téléphone, remplacer `localhost` par l'adresse IP de l'ordinateur sur le réseau local. Ouvrir la page « Kit de campagne », télécharger les illustrations, puis vérifier quelques cartes. Cette copie d'essai ne se publie jamais : ses adresses sont locales, et une app publiée la refuserait (elle n'accepte que les Releases de ce dépôt, et ignore `EXPO_PUBLIC_KIT_URL`). `--base-url` ne sert qu'à cet essai.

## 4. Créer la Release en brouillon

Toujours en brouillon d'abord : une Release publiée ne se modifie plus.

```bash
gh release create edition-2026-11 --repo Mitchnsun/kit-de-campagne --target master \
  --draft --title "Édition de novembre 2026" --notes "Les illustrations des 36 cartes d'événement."
gh release upload edition-2026-11 dist/kit/* --repo Mitchnsun/kit-de-campagne
```

Les notes disent ce qui change pour le joueur : de nouvelles cartes illustrées, des images refaites, une version minimale de l'app plus récente.

## 5. Vérifier le brouillon

```bash
gh release view edition-2026-11 --repo Mitchnsun/kit-de-campagne --json assets --jq '.assets | length'
```

Le nombre de fichiers est celui des images, plus un pour `manifest.json`. Vérifier aussi que le manifeste joint est bien celui de `dist/kit/` : même taille, même date.

## 6. Publier

```bash
gh release edit edition-2026-11 --repo Mitchnsun/kit-de-campagne --draft=false --latest
```

Le tag est créé à ce moment, sur `master`. La Release ne peut plus changer.

## 7. Vérifier en ligne

```bash
curl -sL https://github.com/Mitchnsun/kit-de-campagne/releases/latest/download/manifest.json | head -20
```

Le manifeste lu doit être celui de la nouvelle édition. Dans l'app :

- **un joueur qui a déjà un kit** voit « Nouvelle édition » dans le tiroir, au plus tard une semaine après, ou tout de suite en ouvrant la page du kit ;
- **un nouveau joueur** télécharge directement la nouvelle édition.

Ensuite, remplir « Première édition » (`edition-2026-11`) dans la fiche de chaque image entrée dans cette édition.

## Corriger une édition publiée

Une Release publiée ne se corrige pas. Pour une image fausse ou un fichier manquant, publier une révision du même mois à partir du manifeste publié :

```bash
gh release download edition-2026-11 --repo Mitchnsun/kit-de-campagne --pattern manifest.json --dir /tmp/kit-precedent
yarn kit:build --edition 2026-11-2 --previous /tmp/kit-precedent/manifest.json
```

Puis reprendre à l'étape 4 avec le tag `edition-2026-11-2`. La révision passe avant l'édition qu'elle corrige. Les joueurs qui ont l'édition fautive voient « Nouvelle édition » et téléchargent la révision.

## Plus tard : les données des Dossiers

La seconde partie du kit, les données des Dossiers, aura ses propres éditions dans le même manifeste. Une Release qui ne change qu'une partie garde l'autre telle quelle : avec `--previous`, ses éditions sont recopiées et pointent toujours vers la Release qui porte leurs fichiers.
