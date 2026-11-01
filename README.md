# Kit de campagne

Contenu facultatif du jeu **Moi Président**, téléchargé à part depuis l'app. **Le jeu se joue en entier sans lui** : le kit ne change aucun résultat.

_English below._

## Contenu

| Partie | Contenu |
| --- | --- |
| Illustrations | Une image WebP par carte d'événement, nommée d'après l'identifiant de la carte |
| Données des Dossiers | Les chiffres, les séries, les points « À savoir » (en français et en anglais) et le fond de carte des départements |

Chaque partie paraît en éditions datées (« Édition de novembre 2026 »). Sans les illustrations, la carte d'événement s'affiche sans image ; sans les données, la zone « Dossiers » s'ouvre sans chiffres.

## Où sont les fichiers

Dans les [Releases](https://github.com/Mitchnsun/kit-de-campagne/releases) de ce dépôt, pas dans son arborescence.

- Chaque Release contient un `manifest.json`. Il donne, pour chaque partie, son édition, la version minimale de l'app qui sait la lire, ses crédits et sa licence, et chacun de ses fichiers avec sa taille et son empreinte SHA-256. Un fichier qui n'a pas changé peut rester dans une Release précédente.
- L'app lit le manifeste de la dernière Release : `https://github.com/Mitchnsun/kit-de-campagne/releases/latest/download/manifest.json`
- Les Releases sont immuables : une édition publiée ne change plus. Une correction paraît dans une nouvelle édition.
- Le kit ne contient que des images et des fichiers JSON, aucun code exécutable.

## Comment les illustrations sont faites

Elles sont générées par IA. Le dossier [`prompts/`](prompts/) contient le [gabarit de prompt](prompts/gabarit.md), la fiche de chaque image (son prompt, l'outil, la date, les retouches et la relecture) et l'image validée, dont [`oldTweet.webp`](prompts/oldTweet.webp), qui sert de référence de style. Les fichiers d'origine, lourds, ne sont pas dans le dépôt.

## Confidentialité

L'app ne contacte ce dépôt que pour le kit : quand le joueur ouvre sa page, le télécharge ou le met à jour, et, une fois le kit installé, au plus une fois par semaine à l'ouverture du jeu, pour savoir si une nouvelle édition existe. Elle n'envoie ni compte, ni identifiant, ni cookie. Comme tout serveur, GitHub reçoit l'adresse IP de l'appareil qui télécharge : voir la [déclaration de confidentialité de GitHub](https://docs.github.com/fr/site-policy/privacy-policies/github-general-privacy-statement).

## Licences

Voir [LICENSE](LICENSE). En bref : chaque chiffre garde la licence de sa source, la mise en forme des données et les prompts sont sous Licence Ouverte 2.0, et ce dépôt n'accorde aucune licence de réutilisation sur les illustrations.

## Signaler une erreur

Ce dépôt n'a pas d'issues. Pour une erreur dans une image ou un chiffre, écrivez au contact indiqué dans les « Mentions légales » du jeu.

---

## English

Optional content for the game **Moi Président**, downloaded separately from the app. **The whole game can be played without it**: the kit changes no result.

### Contents

| Part | Contents |
| --- | --- |
| Illustrations | One WebP image per event card, named after the card's identifier |
| Briefing data | The figures, the series, the "Good to know" notes (in French and English) and the map of the départements |

Each part comes out in dated editions ("November 2026 edition"). Without the illustrations, the event card shows no image; without the data, the Briefings area opens without figures.

### Where the files are

In this repository's [Releases](https://github.com/Mitchnsun/kit-de-campagne/releases), not in its tree.

- Each Release holds a `manifest.json`. For each part it gives the edition, the oldest app version that can read it, its credits and licence, and every file with its size and SHA-256 hash. A file that has not changed may stay in an earlier Release.
- The app reads the manifest of the latest Release: `https://github.com/Mitchnsun/kit-de-campagne/releases/latest/download/manifest.json`
- Releases are immutable: a published edition never changes. A correction comes out in a new edition.
- The kit holds only images and JSON files, no executable code.

### How the illustrations are made

They are AI-generated. The [`prompts/`](prompts/) folder holds the [prompt template](prompts/gabarit.md), the sheet of each image (its prompt, the tool, the date, the retouches and the review) and the validated image, among them [`oldTweet.webp`](prompts/oldTweet.webp), the style reference. The original files, which are heavy, are not in the repository. These working files are in French.

### Privacy

The app only contacts this repository for the kit: when the player opens its page, downloads it or updates it, and, once the kit is installed, at most once a week when the game starts, to find out whether a new edition exists. It sends no account, identifier or cookie. Like any server, GitHub receives the IP address of the device that downloads: see [GitHub's privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

### Licences

See [LICENSE](LICENSE). In short: each figure keeps the licence of its source, the layout of the data and the prompts are under the Open Licence 2.0, and this repository grants no licence to reuse the illustrations.

### Reporting an error

This repository has no issues. For an error in an image or a figure, write to the contact given in the game's legal notice.
