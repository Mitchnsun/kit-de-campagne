# `seniorEmployment` · L'emploi des 55-64 ans

**Vérifiée le 25/11/2026** : double vérification sur le web, sans écart non expliqué (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `seniorEmployment`, volet de « Retraites » (`pensions`), dossier « Travail et retraites » (`work`), page de type série, ticket #540 de l'app |
| Données | `briefings/data/seniorEmployment.json`, écrit par `yarn briefings seniorEmployment` le 2026-11-25 |
| Sources | Eurostat, « Employment and activity by sex and age - annual data » (`lfsi_emp_a`), https://ec.europa.eu/eurostat/databrowser/view/lfsi_emp_a/default/table?lang=fr ; API https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/lfsi_emp_a?format=JSON&lang=fr&geo=FR&geo=EU27_2020&indic_em=EMP_LFS&sex=T&age=Y55-64&unit=PC_POP ; politique de réutilisation d'Eurostat (mention de la source) |
| Séries | `france` : taux d'emploi des 55-64 ans, France, 2003 à 2025, 23 points, drapeau `d` (définition différente) de 2021 à 2025 ; `europeanUnion` : UE à 27, 2009 à 2025, 17 points ; mise à jour d'Eurostat du 06/11/2026 |
| Chiffre clé | 61,7 % en 2025, en hausse (60,3 % en 2024) ; l'UE à côté, 66,4 % |
| Règles | Toutes les années d'Eurostat ; un drapeau `b` devient une rupture de la série ; le script échoue sur un autre jeu de données, une année manquante, un territoire absent ou un taux hors de 10 à 100 % |
| Première édition | La prochaine édition du kit |

## « À savoir »

1. 61,7 % et 66,4 % en 2025, 38,2 % en 2003 : lus dans `briefings/data/seniorEmployment.json`.
2. La définition du taux d'emploi au sens du BIT et celle du taux de chômage (chômeurs rapportés aux actifs) : Insee, définitions, https://www.insee.fr/fr/metadonnees/definition/c1159 (emploi au sens du BIT) et https://www.insee.fr/fr/metadonnees/definition/c1687 (taux de chômage).
3. Insee, BDM `011818719`, « Personnes en emploi (taux d'emploi) au sens du BIT - Ensemble des 55 à 64 ans - France entière - Données CVS », trimestriel, 2026-T3 : 62,0, mise à jour du 10/11/2026, https://www.insee.fr/fr/statistiques/serie/011818719 (lue par l'API de la BDM le 25/11/2026). Le drapeau `d` : réponse de l'API d'Eurostat.

## Double vérification

Faite le 25/11/2026 par un agent Claude (modèle Sonnet), sans passer par l'API du script (rapport `dossiers2/A-series.md` de la session), et relue par l'agent principal sur la BDM.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| France 2025 | 61,7 % | 61,75 % (moyenne des quatre trimestres de 2025, CVS) | Insee, BDM `011818719` | Conforme |
| France 2019 | 54,5 % (`lfsi_emp_a`) | 53,1 % (`lfsa_ergan`) | Eurostat, `lfsa_ergan` | Écart expliqué : deux jeux d'Eurostat, ruptures traitées différemment avant 2021 ; le script n'en lit qu'un |
| UE 2025 | 66,4 % | 66,4 % | Eurostat, `lfsi_emp_a`, page du jeu | Conforme |

**Conclusion.** Le taux d'Eurostat concorde avec la série trimestrielle de l'Insee.

**Pages consultées** le 25/11/2026 : celles du tableau.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande : celle des autres jeux d'Eurostat du kit.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
