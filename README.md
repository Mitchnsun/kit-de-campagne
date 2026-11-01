# Kit de campagne

Contenu facultatif du jeu **Moi Président**, téléchargé à part depuis l'app. **Le jeu se joue en entier sans lui** : le kit ne change aucun résultat.

_English below._

## Contenu

| Partie | Contenu |
| --- | --- |
| Illustrations | Une image WebP par carte d'événement, nommée d'après l'identifiant de la carte |
| Données des Dossiers | Les chiffres, les séries, les points « À savoir » (en français et en anglais) et le fond de carte des départements |

Chaque partie paraît en éditions datées et numérotées (« Édition de novembre 2026, n° 1 »). Sans les illustrations, la carte d'événement s'affiche sans image ; sans les données, la zone « Dossiers » s'ouvre sans chiffres.

## Où sont les fichiers

Dans les [Releases](https://github.com/Mitchnsun/kit-de-campagne/releases) de ce dépôt, pas dans son arborescence.

- Chaque Release contient un `manifest.json`. Il donne, pour chaque partie, ses éditions, de la plus récente à la plus ancienne. Pour chacune : la version minimale de l'app qui sait la lire, ses crédits et sa licence, et chacun de ses fichiers avec sa taille et son empreinte SHA-256. Un fichier qui n'a pas changé peut rester dans une Release précédente.
- L'app lit le manifeste de la dernière Release : `https://github.com/Mitchnsun/kit-de-campagne/releases/latest/download/manifest.json`
- Les Releases sont immuables : une édition publiée ne change plus. Une correction paraît dans la Release suivante.
- Chaque Release porte un tag `kit-france-AAMM-NNNN` : l'année et le mois (`2611` pour novembre 2026), puis un numéro augmenté de un à chaque Release. `kit-france-2611-0001`, puis `kit-france-2611-0002` si la suivante sort aussi en novembre, puis `kit-france-2612-0003` en décembre.
- Comment publier une édition : [`RELEASE.md`](RELEASE.md).
- Le kit ne contient que des images et des fichiers JSON, aucun code exécutable.

## Comment les illustrations sont faites

Elles sont générées par IA. Les fichiers d'origine, lourds, ne sont pas dans le dépôt.

- [`illustrations/`](illustrations/) contient l'image validée de chaque carte, telle que la Release la publie, dont [`oldTweet.webp`](illustrations/polemic/oldTweet.webp), qui sert de référence de style.
- [`prompts/`](prompts/) contient le [gabarit de prompt](prompts/gabarit.md), le [modèle de fiche](prompts/modele-fiche.md) et la fiche de chaque image : son prompt, l'outil, la date, les retouches et la relecture.

Dans les deux dossiers, images et fiches sont rangées par catégorie d'événement, sous le nom que la catégorie a dans le moteur du jeu : `illustrations/polemic/oldTweet.webp` et `prompts/polemic/oldTweet.md`.

| Dossier | Catégorie dans le jeu |
| --- | --- |
| `affair` | Affaire |
| `attack` | Attaque |
| `breakthrough` | Coup de projecteur |
| `buzz` | Buzz |
| `crisis` | Crise |
| `farFetched` | Incroyable |
| `media` | Opportunité médiatique |
| `polemic` | Polémique |
| `sponsorships` | Parrainages |
| `support` | Offre de soutien |
| `team` | Crise d'équipe |

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

Each part comes out in dated, numbered editions ("November 2026 edition, no. 1"). Without the illustrations, the event card shows no image; without the data, the Briefings area opens without figures.

### Where the files are

In this repository's [Releases](https://github.com/Mitchnsun/kit-de-campagne/releases), not in its tree.

- Each Release holds a `manifest.json`. For each part it gives its editions, newest first. For each one: the oldest app version that can read it, its credits and licence, and every file with its size and SHA-256 hash. A file that has not changed may stay in an earlier Release.
- The app reads the manifest of the latest Release: `https://github.com/Mitchnsun/kit-de-campagne/releases/latest/download/manifest.json`
- Releases are immutable: a published edition never changes. A correction comes out in the next Release.
- Each Release is tagged `kit-france-AAMM-NNNN`: the year and month (`2611` for November 2026), then a number one higher at every Release. `kit-france-2611-0001`, then `kit-france-2611-0002` if the next one also comes out in November, then `kit-france-2612-0003` in December.
- How to publish an edition: [`RELEASE.md`](RELEASE.md) (in French).
- The kit holds only images and JSON files, no executable code.

### How the illustrations are made

They are AI-generated. The original files, which are heavy, are not in the repository.

- [`illustrations/`](illustrations/) holds the validated image of each card, as the Release publishes it, among them [`oldTweet.webp`](illustrations/polemic/oldTweet.webp), the style reference.
- [`prompts/`](prompts/) holds the [prompt template](prompts/gabarit.md), the [sheet model](prompts/modele-fiche.md) and the sheet of each image: its prompt, the tool, the date, the retouches and the review. These working files are in French.

In both folders, images and sheets are filed by event category, under the category's name in the game's engine: `illustrations/polemic/oldTweet.webp` and `prompts/polemic/oldTweet.md`. The table above gives each category's name in the game.

### Privacy

The app only contacts this repository for the kit: when the player opens its page, downloads it or updates it, and, once the kit is installed, at most once a week when the game starts, to find out whether a new edition exists. It sends no account, identifier or cookie. Like any server, GitHub receives the IP address of the device that downloads: see [GitHub's privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

### Licences

See [LICENSE](LICENSE). In short: each figure keeps the licence of its source, the layout of the data and the prompts are under the Open Licence 2.0, and this repository grants no licence to reuse the illustrations.

### Reporting an error

This repository has no issues. For an error in an image or a figure, write to the contact given in the game's legal notice.
