# `<id>` · <titre de l'indicateur>

À copier en `briefings/sheets/<id>.md` (par exemple `briefings/sheets/inflation.md`), l'`id` étant celui de l'indicateur dans le registre de l'app (`briefings/registry.ts`), puis à remplir. Les chiffres vont en `briefings/data/<id>.json`, écrits par `yarn briefings <id>` dans le dépôt de l'app, et les points « À savoir » en `briefings/notes/<id>.json`. Supprimer cette ligne.

**Vérifiée le JJ/MM/AAAA** : double vérification sur le web, sans écart non expliqué (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `<id>`, dossier « <nom du dossier> » (`<briefing>`), page de type <série, pyramide, carte, comparaison, scrutin, volets>, ticket #NN de l'app |
| Données | `briefings/data/<id>.json`, écrit par `yarn briefings <id>` le AAAA-MM-JJ ; ou saisi à la main depuis <document> le AAAA-MM-JJ |
| Sources | Producteur, « titre de la publication », page d'origine, fichier ou API, licence |
| Séries | `<id-de-série>` : <ce qu'elle mesure>, identifiant du producteur, première et dernière période, nombre de points |
| Chiffre clé | Valeur, période, tendance par rapport à la période précédente |
| Règles | Ce que le script garde ou écarte (chiffres définitifs seulement, dernière année, départements…) |
| Première édition | `kit-france-AAMM-NNNN` |

## « À savoir »

Chaque point de `briefings/notes/<id>.json`, en français, avec la source qui le soutient. Deux à quatre points, autant en anglais.

1. Le point. Source : <URL>.

## Double vérification

Faite le JJ/MM/AAAA par <qui : un agent Claude (modèle Sonnet) qui cherche sur le web, ou une personne>, sans passer par la source du script : d'autres publications du producteur, d'autres diffuseurs (Eurostat, OCDE…), la presse.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | | | | Conforme / Écart expliqué / Écart / Non trouvé |

Verdicts : un « Écart » non expliqué bloque l'entrée de l'indicateur dans une édition. « Non trouvé » dit où l'on a cherché.

**Conclusion.** En une phrase.

**Pages consultées**, avec leur date de consultation.

## Mises à jour

Aucune. Sinon, pour chaque nouvelle récupération : la date, ce qui a changé (nouvelle période, révision, changement de source) et la vérification refaite.

## Relecture

- [ ] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [ ] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [ ] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
