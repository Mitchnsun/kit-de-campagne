# `workingHours` · La durée du travail

**Vérifiée le 25/11/2026** : relue par un second agent, mais sur la même source : aucune autre publication de la même mesure n'a été trouvée (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `workingHours`, dossier « Travail et retraites » (`work`), page de type série, ticket #540 de l'app |
| Données | `briefings/data/workingHours.json`, écrit par `yarn briefings workingHours` le 2026-11-25 |
| Sources | Eurostat, « Average actual weekly hours worked in the main job of persons who worked in this job during the reference week by professional status, full-time/part-time employment and economic activity (NACE Rev. 2) » (`lfsa_ewhan2`), https://ec.europa.eu/eurostat/databrowser/view/lfsa_ewhan2/default/table?lang=fr ; API https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/lfsa_ewhan2?format=JSON&lang=fr&geo=FR&geo=EU27_2020&nace_r2=TOTAL&wstatus=EMP&worktime=TOTAL&age=Y15-64&sex=T&unit=HR (puis `worktime=FT` et `PT`) ; politique de réutilisation d'Eurostat (mention de la source). Le titre du registre s'arrête avant « (NACE Rev. 2) (2008-2026) » : un titre de source tient en 200 caractères |
| Séries | Heures effectivement travaillées par semaine dans l'emploi principal, personnes de 15 à 64 ans ayant travaillé dans la semaine de référence, tous statuts, toutes activités, 2008 à 2025, 18 points chacune : `france`, `europeanUnion` (ensemble), `franceFullTime`, `europeanUnionFullTime` (temps plein), `francePartTime`, `europeanUnionPartTime` (temps partiel) ; ruptures (`b`) : France 2014, 2021, 2024 ; UE 2021 ; drapeau `d` (définition différente) sur la France ; mise à jour d'Eurostat du 30/10/2026 |
| Chiffre clé | 35,5 h en 2025, en baisse (35,6 h en 2024) ; l'UE à côté, 35,7 h |
| Règles | Toutes les années d'Eurostat ; le script échoue sur un autre jeu de données (début du libellé), une réponse manquante, une année manquante, un territoire absent ou une valeur hors de 5 à 60 h |
| Première édition | La prochaine édition du kit |

## « À savoir »

1. 35,5 et 35,7 h, 38,1 et 38,7 h à temps plein, en 2025 : lus dans `briefings/data/workingHours.json`.
2. Les heures habituelles : Eurostat, `lfsa_ewhun2`, mêmes filtres, 2025 : France 37,0 h (`d`), UE 37,0 h, lus par l'API le 25/11/2026, https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/lfsa_ewhun2?format=JSON&lang=fr&geo=FR&geo=EU27_2020&nace_r2=TOTAL&wstatus=EMP&worktime=TOTAL&age=Y15-64&sex=T&unit=HR .
3. Code du travail, art. L3121-27 (« La durée légale de travail effectif des salariés à temps complet est fixée à trente-cinq heures par semaine. ») et L3121-28 (« Toute heure accomplie au delà de la durée légale hebdomadaire ou de la durée considérée comme équivalente est une heure supplémentaire qui ouvre droit à une majoration salariale ou, le cas échéant, à un repos compensateur équivalent. »), lus sur le Code du travail numérique le 25/11/2026 : https://code.travail.gouv.fr/code-du-travail/l3121-27 et https://code.travail.gouv.fr/code-du-travail/l3121-28 .
4. Les drapeaux `b` et `d` : réponse de l'API d'Eurostat, repris dans les ruptures des séries.

## Double vérification

Faite le 25/11/2026 par un agent Claude (modèle Sonnet), sans passer par le script (rapport `dossiers2/A-series.md` de la session).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| France 2025, ensemble | 35,5 h | 35,5 h | Eurostat, `lfsa_ewhan2`, relu par l'agent de recherche (même source que le script) | Conforme, même source |
| France 2025, temps plein | 38,1 h | 38,1 h | Idem | Conforme, même source |
| UE 2025, temps partiel | 21,4 h | 21,4 h | Idem | Conforme, même source |
| Durée effective selon l'Insee | | Non trouvée | Insee, pages de l'enquête Emploi (recherche de l'agent) | Non trouvé : seule la source d'Eurostat est reprise |

**Conclusion.** Les valeurs du fichier sont celles d'Eurostat ; aucune publication de l'Insee de la même mesure n'a été trouvée pour un second recoupement.

**Pages consultées** le 25/11/2026 : celles du tableau.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande : celle des autres jeux d'Eurostat du kit.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
