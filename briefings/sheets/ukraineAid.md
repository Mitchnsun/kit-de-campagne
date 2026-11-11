# `ukraineAid` · L'aide de la France à l'Ukraine (saisi à la main)

**Vérifiée le 11/11/2026** : le fichier de Kiel et le rapport du ministère ont été rouverts et chaque chiffre contrôlé ; recoupement entre les deux sources par une publication tierce (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `ukraineAid`, dossier « Défense et Europe » (`defence`), page de type comparaison, ticket #349 de l'app |
| Données | `briefings/manual/ukraineAid.json`, saisi à la main le 2026-11-11 depuis le fichier de Kiel (version 31) et le rapport du ministère |
| Sources | 1. Kiel Institute for the World Economy, « Ukraine Support Tracker », version 31 (aide du 24/01/2022 au 31/08/2026, page datée « Update October 8, 2026 »), page https://www.kielinstitut.de/topics/war-against-ukraine/ukraine-support-tracker/, fichier https://www.kielinstitut.de/fileadmin/Dateiverwaltung/IfW-Publications/fis-import/bc5059ba-ef38-4f08-988a-746a03905a6c-Ukraine_Support_Tracker__Release_31.xlsx, aucune licence indiquée, citation demandée (ci-dessous), citation seule. 2. Ministère des Armées et des Anciens combattants, « Rapport au Parlement 2026 sur les exportations d'armement de la France », 12/08/2026 (date de création du PDF), https://www.defense.gouv.fr/sites/default/files/ministere-armees/Rapport%20au%20Parlement%202026%20sur%20les%20exportations%20d%E2%80%99armement%20de%20la%20France%20(12082026).pdf, citation seule, en français seulement |
| Séries | Kiel, feuille « Country Summary (€) », ligne « France », en milliards d'euros, période 2026-08, un point chacune : `kielMilitary` 6,2316 ; `kielFinancial` 0,7994 ; `kielHumanitarian` 0,8756 ; `kielTotal` 7,9066 (allocations) ; `kielCommitMilitary` 8,5473 ; `kielCommitFinancial` 0,8144 ; `kielCommitHumanitarian` 0,9756 ; `kielCommitTotal` 10,3373 (engagements). Ministère : `ministryMilitary` 6,5 Md€, période 2025-12 (rapport, p. 34) |
| Chiffre clé | 7,9066 Md€ alloués par la France (aide bilatérale, Kiel, au 31/08/2026), sans tendance saisie ; à côté, les engagements de Kiel et l'estimation du ministère |
| Règles | Saisie à la main, chiffres arrondis à 4 décimales (le fichier en donne davantage : 7,9066323…). Les allocations (livrées ou affectées) et les engagements (promesses) de Kiel et l'estimation du ministère ne sont jamais additionnés ni mis dans un même bloc. Aide bilatérale seulement : l'aide de l'Union est comptée à part par Kiel |
| Première édition | À remplir à la publication |

## Citation demandée par l'institut de Kiel

Feuille « ReadMe » du fichier, § 1, « Citation » : « When using the data, please cite it as follows: Christoph Trebesch, Arianna Antezza, Yana Balanchuk, Pietro Bomprezzi, Katelyn Bushnell, Daniel Cherepinskiy, Catarina Chambino, Zakarias Sjöberg Dahlén, Jakob Drews, Yelmurat Dyussimbinov, Celina Ferrari, Gabriele Ferretti, Jonas Fey, Andre Frank, Pascal Frank, Lukas Franz, Nathanael Frey, Manon Funke, Max Funke, Caspar Gerland, Ettore Goffi, Leon Haziraj, Tilmann Hogrefe, Giuseppe Irto, Felicia Jäckel, Kateryna Kuzmuk, Ivan Kharitonov, Bharath Kumar, Federico Mellace, Taro Nishikawa, Javier Ospital, Ekaterina Rebinskaya, Christopher Schade, Stefan Schramm, Jonas Schweigard, Jannis Stagge, Annalena Tetzner & Leon Weiser (2026). "The Ukraine Support Tracker: Which countries help Ukraine and how?" Kiel Working Paper, No. 2218, 1-75. »

La publication du registre abrège la liste des 38 auteurs en « Christoph Trebesch et al. (2026) » : choix à confirmer par le PO.

## « À savoir »

1. Kiel : aide bilatérale de la France du 24/01/2022 au 31/08/2026, 7,91 Md€ alloués (militaire 6,23 ; financière 0,80 ; humanitaire 0,88), 10,34 Md€ engagés. Source : feuille « Country Summary (€) », ligne « France » ; page de Kiel (« Update October 8, 2026 »).
2. Définitions de Kiel : « We report allocations as our primary metric. Commitments of future aid are reported in auxiliary figures. » ; « Military assistance includes all types of weapons and military equipment alongside items donated to the Ukrainian army as well as financial assistance tied for military purposes. » ; l'aide de l'Union est dans le fichier sous « EU (Commission and Council) » et « European Investment Bank ». Source : feuille « ReadMe », § 2.
3. Ministère : « Entre le 24 février 2022 et le 31 décembre 2025, le soutien militaire de la France peut être estimé à une valeur totale de 6,5 Md€, incluant les engagements de la France au titre du financement de la FEP (le financement français correspond à environ 18 % des engagements des États membres et pourrait atteindre jusqu'à 2,1 Md€ sur toute la période). » Source : rapport, p. 34.
4. Définitions et périodes différentes, jamais additionnées. Source : les deux ci-dessus.

Les quatre points en anglais disent la même chose que le français.

## Double vérification

Faite le 11/11/2026 par un agent Claude (modèle Opus) : le fichier ouvert avec `openpyxl`, le rapport avec `pdftotext`, un article de presse.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Allocations de Kiel | 6,2316 ; 0,7994 ; 0,8756 ; 7,9066 | 6,231602… ; 0,7994 ; 0,875629… ; 7,906632… ; la somme des trois est le total | fichier de Kiel, « Country Summary (€) », ligne « France » | Conforme (arrondi à 4 décimales) |
| Engagements de Kiel | 8,5473 ; 0,8144 ; 0,9756 ; 10,3373 | 8,547316… ; 0,8144 ; 0,975629… ; 10,337345… | idem | Conforme (arrondi) |
| Ministère | 6,5 Md€ | « 6,5 Md€ », 24/02/2022 au 31/12/2025, incluant les engagements au titre de la FEP | rapport, p. 34 (`pdftotext`) | Conforme |
| Kiel par un tiers | 7,9 ; dont 6,2 militaire, 0,9 humanitaire, 0,8 financier | « Bilateral aid allocated, of which 6.2 military, 0.9 humanitarian and 0.8 financial » ; 7,9 Md€, 0,3 % du PIB | https://www.revueconflits.com/?p=65984 (17/10/2026) | Conforme, arrondi à la décimale |
| Ministère par un tiers | 6,5 | « 6.5 billion cumulative at the end of 2025 » | idem | Conforme |
| Kiel contre ministère | — | Kiel valorise le matériel fourni à son prix de marché, avec une décote selon l'inflation, et ne compte pas la formation des soldats ukrainiens, que Paris inclut dans son total (article ci-dessus) | idem | Écart expliqué : définitions différentes, 6,23 contre 6,5 Md€ ne se comparent pas |

**Conclusion.** Aucun chiffre saisi n'est faux ; les deux sources diffèrent par la définition et par la période, ce que la page dit.

**Pages consultées** le 11/11/2026 : le fichier, le rapport, la page de Kiel, l'article de la Revue Conflits (résumé de la page lue par un outil).

## Réserves

- Les engagements de Kiel sont des promesses, non de l'aide versée.
- L'estimation du ministère comprend des engagements à la Facilité européenne pour la paix jusqu'à 2,1 Md€.
- Aucune licence n'est indiquée par Kiel : citation seule.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : le fichier et le rapport ont été rouverts, un tiers recoupe les deux.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Kiel : aucune licence, citation demandée et reprise ci-dessus ; ministère : licence non cherchée.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
