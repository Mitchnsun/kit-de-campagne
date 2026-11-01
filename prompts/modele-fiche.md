# `<id-de-la-carte>` · <titre de la carte>

À copier en `prompts/<id-de-la-carte>.md` (par exemple `prompts/marketGaffe.md`), puis à remplir. Le prompt suit le [gabarit](gabarit.md). Supprimer cette ligne.

**Validée par le PO le JJ/MM/AAAA**, au premier essai (ou à l'essai N, ou après une retouche). Elle sert telle quelle en clair et en sombre.

![<titre de la carte>](<id-de-la-carte>.webp)

| Champ | Valeur |
| --- | --- |
| Carte | `<id>`, catégorie `<kind>` (<nom de la catégorie dans le jeu>) |
| Style | Reportage dessiné ; ce qui s'écarte du style, s'il y a lieu |
| Ton | Observateur / Ironique / Tendu / Chaleureux, ou plus précis |
| Date | AAAA-MM-JJ |
| Outil | ChatGPT, ChatGPT Images <version> ; mode et effort : … |
| Conversation | Lien de la conversation (il ne s'ouvre qu'avec le compte qui l'a créée) |
| Format rendu | L × H (16:9) : export en 1290 × 726 px depuis le PNG d'origine, WebP de qualité 75, NNN Ko, sans recadrage |
| Fichier d'origine | Nom du fichier, et où il est rangé (hors du dépôt) |
| Première édition | `edition-AAAA-MM` |

## Texte de la carte

> **<titre de la carte>**
>
> Le texte de la carte, en français, tel que le jeu l'affiche.

## Le moment choisi

La scène en quelques phrases : le lieu, le moment, qui fait quoi, où est le candidat.

## Prompt complet

Dans une nouvelle conversation, avec [`oldTweet.webp`](oldTweet.webp) comme seule image de référence (ou les images jointes, dans l'ordre) :

```
Le prompt envoyé, en entier.
```

### Message de correction

Facultatif : chaque message envoyé ensuite dans la même conversation, en entier, et l'essai qu'il a donné.

## Décisions prises sur cette image

Facultatif : ce que le PO a décidé, et ce qui s'écarte du prompt ou du gabarit. Une ressemblance voulue se note ici : « d'après une photo de famille du PO, avec l'accord de la personne, confirmé par le PO », sans nom ; ni la photo ni le portrait ne vont dans le dépôt.

## Essais écartés

Aucun. Sinon, pour chaque essai : la date et ce qui n'allait pas.

## Retouches

Aucune. Sinon, chaque retouche faite sur une copie : texte effacé, main corrigée, recadrage…

## Relecture

Faite et validée par le PO le JJ/MM/AAAA.

- [ ] Aucun texte lisible : journaux, pancartes, enseignes, plans, tampons, écrans.
- [ ] Aucun sosie d'une personne réelle, hors une ressemblance voulue notée plus haut.
- [ ] Le candidat du joueur est hors champ ; toute image de lui (affiche, tract, double) n'a ni visage ni genre.
- [ ] Mains, visages et foules sans défaut visible à 343 px de large.
- [ ] Aucune couleur ni aucun logo de parti. Drapeaux, écharpes et Marianne seulement pour signaler un lieu ou un élu officiel. Des personnes variées par l'âge, le corps, l'origine et la coiffure.
- [ ] En 3:2 : rien d'important dans les 80 px du haut et du bas.
- [ ] Lisible sur la page de l'événement, en clair et en sombre.
