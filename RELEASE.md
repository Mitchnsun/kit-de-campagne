# Publier une édition du kit

Chaque édition du kit de campagne est une **Release** de ce dépôt. Le jeu lit une seule adresse, le manifeste de la dernière Release :

```
https://github.com/Mitchnsun/kit-de-campagne/releases/latest/download/manifest.json
```

Les Releases sont **immuables** : une fois publiée, une Release ne change plus, ni ses fichiers ni son tag. Une erreur ne se corrige donc pas sur place : elle se corrige par la Release suivante (voir « Corriger une édition publiée »). Le service du kit est décrit dans le dépôt de l'app, à la section « KitProvider Context » de `docs/ARCHITECTURE.md`.

## Ce qu'une Release contient

- **Un tag `kit-france-AAMM-NNNN`**, qui est aussi l'identifiant de l'édition :
  - `AAMM`, l'année et le mois de la Release : `2611` pour novembre 2026 ;
  - `NNNN`, son numéro, augmenté de un à chaque Release du kit, quelle que soit la partie qui change.

  Par exemple : `kit-france-2611-0001` pour la première, `kit-france-2611-0002` si la suivante sort aussi en novembre, puis `kit-france-2612-0003` en décembre. Le jeu range les éditions par numéro, et affiche « Édition de novembre 2026, n° 2 ».
- **Les fichiers de l'édition**, à plat : une image `<id-de-la-carte>.webp` par carte d'événement pour les illustrations, un fichier `<id>.json` par indicateur publié pour les données des Dossiers.
- **`manifest.json`**, écrit par `yarn kit:build`. Il donne pour chaque partie la liste de ses éditions, de la plus récente à la plus ancienne. Pour chaque édition, il donne :
  - la version minimale de l'app qui la lit ;
  - l'adresse de ses fichiers ;
  - ses crédits ;
  - la taille et l'empreinte SHA-256 de chaque fichier.

  Les éditions plus anciennes restent dans le manifeste, et leurs fichiers dans leur propre Release. Une app trop ancienne pour la dernière édition télécharge ainsi la dernière qu'elle sait lire.

Ne jamais supprimer une Release publiée : des joueurs peuvent encore en dépendre.

## Une fois pour toutes

- Le réglage **« Enable release immutability »** est coché : _Settings › General › Releases_.
- Le dépôt de l'app (`Mitchnsun/moi-president`) et celui-ci sont clonés côte à côte, dans le même dossier : `yarn kit:build` lit `../kit-de-campagne/illustrations` et `../kit-de-campagne/briefings` par défaut, et `yarn briefings` écrit dans `../kit-de-campagne/briefings/data`. D'autres dossiers se donnent avec `--illustrations`, `--briefings` et `--out`.
- Dans le dépôt de l'app, Node (version de `.nvmrc`) et Yarn par Corepack sont installés : `corepack enable`, puis `yarn install`.
- L'outil [`gh`](https://cli.github.com/) est installé et connecté, avec les droits d'écriture sur ce dépôt : `gh auth login`.

## 1. Vérifier les images

Chaque image de l'édition est dans [`illustrations/`](illustrations/), rangée dans le dossier de la catégorie de sa carte (`illustrations/polemic/oldTweet.webp`), et sa fiche relue et validée est au même endroit sous [`prompts/`](prompts/) (`prompts/polemic/oldTweet.md`). L'image est exportée selon le [gabarit](prompts/gabarit.md) : WebP de qualité 75, 1290 × 726 px (ou 1290 × 860 px pour une image restée en 3:2). Mettre à jour les deux dépôts :

```bash
git -C kit-de-campagne pull
git -C moi-president pull
```

## 2. Préparer l'édition

Dans le dépôt de l'app :

```bash
cd moi-president
```

Choisir l'identifiant : le mois de la Release, puis le numéro qui suit celui de la dernière Release. Les étapes suivantes le reprennent.

**Les parties** : par défaut, l'édition ne prépare que les illustrations. `--parts briefings` ne prépare que les données des Dossiers (voir « Les données des Dossiers »), `--parts illustrations,briefings` les deux. Avec `--previous`, une partie laissée de côté garde ses éditions précédentes, qui pointent toujours vers la Release qui porte leurs fichiers : un joueur ne retélécharge que ce qui a changé.

**Première édition :**

```bash
EDITION=kit-france-2611-0001
yarn kit:build --edition $EDITION
```

**Édition suivante :** partir du manifeste de la dernière Release, pour garder les éditions précédentes. Si la dernière est `kit-france-2611-0001` :

```bash
EDITION=kit-france-2612-0002
gh release download --repo Mitchnsun/kit-de-campagne --pattern manifest.json --dir /tmp/kit-precedent
yarn kit:build --edition $EDITION --previous /tmp/kit-precedent/manifest.json
```

Le script :

- **vérifie l'identifiant** : `0001` sans `--previous`, sinon le numéro qui suit le plus haut du manifeste précédent, et un mois qui n'est pas avant celui de la dernière Release. Un numéro sauté ou répété, ou un `--previous` oublié, fait échouer le script ;
- **vérifie chaque image** : un WebP de 1290 × 726 ou 1290 × 860 px, 400 Kio au plus, rangé dans le dossier de la catégorie de sa carte. Une image hors règle, ou rangée ailleurs, fait échouer le script, qui dit pourquoi. Dans la Release, les images sont à plat : le manifeste ne connaît pas les dossiers ;
- **copie les images et écrit `manifest.json`** dans `dist/kit/`, ou dans le dossier donné par `--out`, puis donne le nombre d'images et leur poids total en Mo ;
- **relit le manifeste comme l'app le lira** : un manifeste que l'app refuserait (une adresse hors des Releases de ce dépôt, une version mal écrite) fait échouer le script, et rien n'est à publier ;
- **liste les cartes du jeu sans image**, sans échouer : une carte sans image reste jouable ;
- **liste les images dont le nom n'est l'`id` d'aucune carte**, sans échouer : par exemple une carte d'une branche pas encore fusionnée. Relire la liste : une faute de frappe dans un nom y apparaît aussi, et l'image ne s'afficherait jamais.

**La version minimale de l'app** est par défaut celle du dépôt de l'app, dans `package.json`. On la change avec `--min-app-version 0.2.0`, seulement quand l'édition demande une app plus récente : un nouveau format de fichier, une nouvelle partie. Les éditions précédentes restent alors proposées aux apps plus anciennes.

## 3. Essayer l'édition avant de la publier (conseillé)

Préparer une copie dont les fichiers sont servis par un serveur local, puis lancer l'app sur ce kit :

```bash
yarn kit:build --edition $EDITION --out dist/kit-essai --base-url http://localhost:8080/
npx serve dist/kit-essai --cors -l 8080
# dans un autre terminal
EXPO_PUBLIC_KIT_URL=http://localhost:8080 yarn web
```

Pour une édition suivante, ajouter le même `--previous` qu'à l'étape 2 : le numéro y est vérifié de la même façon. Sur un téléphone, remplacer `localhost` par l'adresse IP de l'ordinateur sur le réseau local. Ouvrir la page « Kit de campagne », télécharger les illustrations, puis vérifier quelques cartes. Cette copie d'essai ne se publie jamais : ses adresses sont locales, et une app publiée la refuserait (elle n'accepte que les Releases de ce dépôt, et ignore `EXPO_PUBLIC_KIT_URL`). `--base-url` ne sert qu'à cet essai.

## 4. Créer la Release en brouillon

Toujours en brouillon d'abord : une Release publiée ne se modifie plus.

```bash
gh release create $EDITION --repo Mitchnsun/kit-de-campagne --target master \
  --draft --title "Édition de novembre 2026, n° 1" --notes "Les illustrations des 36 cartes d'événement."
gh release upload $EDITION dist/kit/* --repo Mitchnsun/kit-de-campagne
```

Le titre reprend le nom que le jeu affiche : le mois et le numéro. Les notes disent ce qui change pour le joueur : de nouvelles cartes illustrées, des images refaites, une version minimale de l'app plus récente.

## 5. Vérifier le brouillon

```bash
gh release view $EDITION --repo Mitchnsun/kit-de-campagne --json assets --jq '.assets | length'
```

Le nombre de fichiers est celui des images, plus un pour `manifest.json`. Vérifier aussi que le manifeste joint est bien celui de `dist/kit/` : même taille, même date.

## 6. Publier

```bash
gh release edit $EDITION --repo Mitchnsun/kit-de-campagne --draft=false --latest
```

Le tag est créé à ce moment, sur `master`. La Release ne peut plus changer.

## 7. Vérifier en ligne

```bash
curl -sL https://github.com/Mitchnsun/kit-de-campagne/releases/latest/download/manifest.json | head -20
```

Le manifeste lu doit être celui de la nouvelle édition. Dans l'app :

- **un joueur qui a déjà un kit** voit « Nouvelle édition » dans le tiroir, au plus tard une semaine après, ou tout de suite en ouvrant la page du kit ;
- **un nouveau joueur** télécharge directement la nouvelle édition.

Ensuite, remplir « Première édition » (par exemple `kit-france-2611-0001`) dans la fiche de chaque image entrée dans cette édition.

## Corriger une édition publiée

Une Release publiée ne se corrige pas. Pour une image fausse ou un fichier manquant, publier la Release suivante, comme une édition suivante (étape 2), même dans le même mois. Après `kit-france-2611-0001` :

```bash
EDITION=kit-france-2611-0002
gh release download --repo Mitchnsun/kit-de-campagne --pattern manifest.json --dir /tmp/kit-precedent
yarn kit:build --edition $EDITION --previous /tmp/kit-precedent/manifest.json
```

Puis reprendre à l'étape 4. La nouvelle édition passe avant celle qu'elle corrige. Les joueurs qui ont l'édition fautive voient « Nouvelle édition » et la téléchargent ; un téléchargement qui avait échoué passe à la nouvelle.

## Les données des Dossiers

La seconde partie du kit a ses propres éditions dans le même manifeste. Elle se prépare ainsi, avant les étapes 2 à 7.

1. **Récupérer les chiffres**, dans le dépôt de l'app : `yarn briefings --all`. Chaque script écrit `briefings/data/<id>.json` dans ce dépôt, ou échoue en disant pourquoi (une colonne, une série ou une page qui a changé) sans rien écrire pour cet indicateur. Relire ce qui a changé : `git -C ../kit-de-campagne diff --stat`, puis chaque chiffre clé.
   Le fond de carte ne change qu'avec un nouveau millésime des contours de l'IGN : `yarn briefings:map` le récrit alors dans `briefings/basemap/` (le millésime est dans le script, `LAYER`), et sa fiche note la mise à jour.
2. **Mettre à jour les fiches** : pour chaque indicateur dont les chiffres changent, une ligne dans « Mises à jour » de sa fiche, et la double vérification refaite sur les nouveaux chiffres. Revoir ses « À savoir » si la source signale une rupture ou une révision.
3. **Fusionner** ces changements sur `master` par une PR de ce dépôt.
4. **Préparer l'édition** avec la partie `briefings` :

   ```bash
   yarn kit:build --edition $EDITION --parts briefings --previous /tmp/kit-precedent/manifest.json
   ```

   Le script prend chaque indicateur publié dans l'app (`briefings/registry.ts`), réunit son instantané et ses « À savoir », joint le fond de carte (`departments.json`, demandé dès qu'une carte est publiée), et refuse l'édition s'il manque l'un des deux, si une source n'est pas celle du registre, si un « À savoir » manque dans une langue ou n'en suit pas la typographie. Un fichier d'un indicateur pas encore publié dans l'app est écarté, avec un avertissement. « Données au … », sur l'accueil des Dossiers, est la plus ancienne des dates de récupération.

   Il liste aussi, sans échouer, les indicateurs dont une série a pris du retard sur le jour du build : un dernier point à trois mois ou plus pour une série mensuelle, deux trimestres pour une trimestrielle, trois ans pour une annuelle (les scrutins passés n'y sont jamais). Chaque ligne dit comment rafraîchir l'indicateur : `yarn briefings <id>`, ou une saisie à la main d'après sa fiche. Le rythme de la source peut expliquer un retard (une enquête publiée deux ans après, PISA tous les trois ans) : relire la liste, rafraîchir ce qui peut l'être, et joindre la liste à la PR de l'édition.
5. **La version minimale de l'app** : la première édition des données attend la version de l'app qui ouvre la zone Dossiers. La donner avec `--min-app-version`.

Puis reprendre aux étapes 3 à 7. À l'essai (étape 3), ouvrir la zone Dossiers et quelques pages d'indicateurs.
