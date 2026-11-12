# `housingConstruction` · Construire des logements (saisi à la main)

**Vérifiée le 10/11/2026** : double vérification sur le web, aucun écart de valeur ; les sommes annuelles et sur douze mois refaites sur le CSV de DiDo (297 mois bruts et 297 corrigés relus). Réserves reprises ci-dessous (sommes calculées, estimations révisables, deux traitements). La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `housingConstruction`, dossier « Pouvoir d'achat et logement » (`purchasingPower`), volet « Construire » de la page composite `housing` (voir `housing.md`), page de type série, recherche du 09/11/2026 |
| Données | `briefings/manual/housingConstruction.json`, saisi à la main le 2026-11-10 depuis le CSV de DiDo (millésime 2026-10) et la page de résultats du SDES |
| Sources | 1. SDES, « Construction de logements : résultats à fin septembre 2026 (France entière) », https://www.statistiques.developpement-durable.gouv.fr/construction-de-logements-resultats-fin-septembre-2026-france-entiere, données DiDo « Logements autorisés et commencés, séries mensuelles », fichier « Données mensuelles nationales - Logements » https://data.statistiques.developpement-durable.gouv.fr/dido/api/v1/datafiles/175486a6-76a3-4c6c-a34b-aeb96758910b/csv?millesime=2026-10&withColumnName=true&withColumnDescription=true, Licence Ouverte 2.0 (non vérifiée). 2. Ministère de la Ville et du Logement, « Projet de loi relance logement, dossier de presse », https://www.ecologie.gouv.fr/sites/default/files/documents/DP_PJL-Relance-logement.pdf, p. 5 et p. 10, citation seulement |
| Dates de publication | 2026-10-28 (page du SDES et millésime DiDo 2026-10) ; 2026-06-24 (date de couverture du dossier de presse) |
| Séries | `started` et `authorised` : logements commencés et autorisés par an, 2002 à 2025, 24 points chacune, somme des 12 mois bruts « Tous Logements » (colonnes `LOG_COM` et `LOG_AUT`, `NAT_SERIES` = Brute), calculée (2024 : 264 705 commencés, le plus bas de la série ; 2025 : 268 428 et 378 435). `authorisedTwelveMonths` (377 834, publié par le SDES) et `startedTwelveMonths` (318 419, somme des 12 mois CVS-CJO, calculée) : un point chacune, septembre 2026, pour octobre 2025 à septembre 2026 |
| Chiffre clé | 268 428 logements commencés en 2025 (somme calculée), en hausse (264 705 en 2024) ; à côté, les autorisés de 2025 (378 435) |
| Règles | Saisie à la main. Deux vues : « Par an » (commencés et autorisés, 2002-2025), « Sur douze mois » (deux barres). 2026 partiel (neuf mois) n'est pas saisi. Le −5,1 % des commencés sur douze mois (calculé) est dans une note, « calculé ». L'objectif du Gouvernement est cité dans les notes, jamais comme une barre. Non saisis : l'investissement en logement neuf (compte du logement), les mois de septembre 2026 |
| Première édition | À remplir à la publication |

## « À savoir »

1. Chaque année est une somme des douze mois, calculée ; 264 705 commencés en 2024, le plus bas de la série, qui commence en 2002 (calculé). Source : CSV DiDo, somme des 12 mois bruts refaite par la contre-vérification ; la page du SDES : « séries de données mensuelles depuis 2002 sont disponibles ».
2. « D'octobre 2025 à septembre 2026, 377 834 logements ont été autorisés à la construction, soit 9,1 % de moins que la moyenne des cinq années précédentes » ; 318 419 commencés, somme calculée. Source : page du SDES (phrase recopiée) ; somme CVS-CJO refaite (377 834 retrouvé à l'unité, −9,14 % refait ; 318 419 par la même méthode).
3. « Produire 2 millions de logements d'ici 2030 » ; « Près de 400 000 logements par an dont près de 125 000 logements sociaux » ; un objectif ; « produire » inclut la remise sur le marché de logements rénovés. Source : dossier de presse, p. 5 (phrases recopiées) ; p. 10 : « pour atteindre plus de 400 000 logements par an ». Le projet de loi a été présenté en Conseil des ministres le 24 juin 2026 ; son sort parlementaire n'a pas été vérifié.
4. Estimations révisables ; Sitadel3 a remplacé Sitadel2 en mars 2026 et révisé 2013 et après ; 2002-2012 de l'ancien traitement. Source : page du SDES (« Données estimées en date réelle », révisables) ; précautions des chiffres `logementsAutorises12m` et `logementsCommences2024` du rapport final (« Sitadel3 a remplacé Sitadel2 en mars 2026 » ; « Sitadel3 (mars 2026) ne révise que 2013 et après, 2002-2012 viennent de l'ancien traitement »).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Aucune affirmation : « On ne construit plus » est mixte (on construit, mais moins), écartée par le rapport final.

## Double vérification

Faite le 10/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-logement.md` : CSV de DiDo retéléchargé, sommes refaites par programme ; page du SDES et dossier de presse relus.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 268 428 (2025) | Somme des 12 mois bruts 2025 = 268 428 | CSV DiDo | Conforme (somme calculée) |
| Le plus bas | 264 705 (2024) | Plus bas des années complètes 2002-2025 (puis 2025 : 268 428 ; 2023 : 302 366) | CSV DiDo | Conforme, avec réserve : la série commence en 2002 |
| Séries 2002-2025 | 2 × 24 valeurs | Valeurs du rapport comparées une à une | CSV DiDo | Conforme |
| Autorisés sur 12 mois | 377 834 | Phrase du SDES ; somme CVS-CJO à l'unité | https://www.statistiques.developpement-durable.gouv.fr/construction-de-logements-resultats-fin-septembre-2026-france-entiere | Conforme |
| Commencés sur 12 mois | 318 419 | Somme CVS-CJO ; −5,1 % par la méthode du SDES | CSV DiDo | Conforme, avec réserve : calculé |
| Objectif | « Près de 400 000 logements par an » | Dossier de presse, p. 5 | https://www.ecologie.gouv.fr/sites/default/files/documents/DP_PJL-Relance-logement.pdf | Conforme, avec réserve : un objectif |

**Conclusion.** Aucun chiffre du fichier n'est faux ; les sommes sont calculées et dites telles.

**Pages consultées** le 10/11/2026 : les URL ci-dessus.

## Réserves

- Les séries annuelles sont des sommes calculées des mois publiés : le SDES ne publie pas ces totaux dans sa page.
- Les derniers mois sont des estimations en date réelle, révisables ; 2002-2012 et 2013 et après ne viennent pas du même traitement.
- L'objectif est celui d'un dossier de presse ; le document écrit aussi « plus de 400 000 » (p. 10).

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a refait les sommes sur le CSV.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - SDES : licence ouverte du décret n° 2017-638, réutilisation commerciale permise, mention « Service des données et études statistiques (SDES) » et date de dernière mise à jour (https://www.statistiques.developpement-durable.gouv.fr/mentions-legales) ;
  - citation seule : Ministère de la Ville et du Logement (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
