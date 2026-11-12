# `youthActivity` · L'emploi des jeunes et les NEET (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart de valeur ; réserves de lecture reprises ci-dessous (« le plus haut depuis 1990 » réservé à la moyenne 2025, deux NEET de nature différente). La licence des sources n'a pas été vérifiée (voir « Relecture »).

**Le 2e trimestre 2026.** Les dernières valeurs des trois séries trimestrielles (2e trimestre 2026 : taux d'emploi 33,8 %, taux d'activité 43,1 %, NEET 13,3 %) sont celles que l'Insee publiait au 09/11/2026 ; l'Insee publie le 3e trimestre le 10/11/2026 à 7 h 30 : la prochaine édition du kit les remplacera, et les trimestres passés peuvent être révisés.

| Champ | Valeur |
| --- | --- |
| Indicateur | `youthActivity`, dossier « Travail et retraites » (`work`), volet « Emploi et NEET » de la page composite `youthEmployment` (voir `youthEmployment.md`), page de type série, recherche du 09/11/2026 |
| Données | `briefings/manual/youthActivity.json`, saisi à la main le 2026-11-09 : les séries trimestrielles de la BDM recopiées des fichiers SDMX téléchargés par la contre-vérification (identiques aux valeurs du rapport de recherche, comparées par programme), les autres valeurs depuis les publications ci-dessous |
| Sources | 1. Insee, « Au deuxième trimestre 2026, le taux de chômage augmente de 0,2 point et atteint 8,3 %, Informations rapides n° 192 », https://www.insee.fr/fr/statistiques/9032359, série https://www.insee.fr/fr/statistiques/serie/011818685, `etalab-2.0`. 2. Insee, « Une photographie du marché du travail en 2025, Insee Première n° 2096 », https://www.insee.fr/fr/statistiques/8901327, `etalab-2.0`. 3. Insee, « Le marché du travail en 2025 : l'emploi marque le pas, le chômage augmente à nouveau », vue d'ensemble d'Emploi, chômage, revenus du travail, édition 2026, https://www.insee.fr/fr/statistiques/8733111, PDF https://www.insee.fr/fr/statistiques/fichier/8733111/ECRT2026-VE.pdf, `etalab-2.0`. 4. Eurostat, « Young persons neither in employment nor in education and training by labour status (NEET rates) » (`edat_lfse_20`), https://ec.europa.eu/eurostat/databrowser/view/edat_lfse_20/default/table?lang=fr, licence Eurostat. 5. Eurostat, « Employment and labour force by sex and age - annual data » (`lfsi_emp_a`), https://ec.europa.eu/eurostat/databrowser/view/lfsi_emp_a/default/table?lang=fr, licence Eurostat, pour le taux d'activité de 2019 que cite une réponse |
| Dates de publication | 2026-08-07 (IR n° 192, mise à jour BDM du 07/08/2026) ; 2026-03-25 (Insee Première 2096) ; 2026-07-02 (vue d'ensemble) ; 2026-10-30 (`edat_lfse_20`) ; 2026-11-06 (`lfsi_emp_a`) |
| Séries | `employmentRate` : taux d'emploi des 15-24 ans, CVS, BDM 011818685, 2003-T1 à 2026-T2, 94 points (32,0 au 1er trimestre 2003, 33,8 au 2e trimestre 2026). `activityRate` : taux d'activité des 15-24 ans, BDM 011818679, mêmes trimestres (39,6 puis 43,1). `neet` : part des 15-29 ans ni en emploi ni en formation, BDM 011818639, mêmes trimestres (10,8 puis 13,3 ; 15,8 au 2e trimestre 2020). `employmentRateYear` et `activityRateYear` : moyennes 2025 (34,5 ; 43,0). `workStudyShare` : part des 15-24 ans en emploi qui sont en alternance ou en stage, 2025 (30,5). `neetEurostat`, `neetWanting`, `neetNotWanting` : NEET d'Eurostat en France, ensemble, souhaitant travailler, ne souhaitant pas travailler, 2019 à 2025, ruptures en 2021 et 2024 (12,9 ; 8,9 ; 4,1 en 2025). `neetNotWantingEu` : UE à 27, ne souhaitant pas travailler, 2019 à 2025, rupture en 2021 (4,1 en 2025) |
| Chiffre clé | 33,8 % des 15-24 ans en emploi au 2e trimestre 2026, en baisse (34,1 % au 1er trimestre) ; à côté, le taux d'activité (43,1 %) et la part en alternance ou en stage (30,5 %, 2025) |
| Règles | Saisie à la main. Quatre vues : « Emploi et activité » (deux lignes trimestrielles depuis 2003), « Moyenne annuelle » (barres 2025 ; la note cite « son plus haut niveau depuis 1990 » pour la moyenne 2025 seulement), « NEET, Insee » (le plus haut point trouvé dans les données), « NEET, Eurostat » (l'ensemble et ceux qui ne souhaitent pas travailler, le tableau avec ceux qui le souhaitent et l'UE). Les deux NEET sont dans des vues séparées, jamais comparés. Les drapeaux « d » d'Eurostat (définition différente pour la France) sont dans la note de la vue ; les drapeaux « b » sont des ruptures (`breaks`). Non saisis : le NEET d'Eurostat avant 2019, le taux d'emploi en alternance des 15-64 ans (2,3 %), le halo et le sous-emploi des 15-24 ans, les taux d'emploi et d'activité des 15-29 ans d'Eurostat |
| Première édition | À remplir à la publication |

## « À savoir »

1. Valeurs du 2e trimestre 2026 remplacées le 10 novembre 2026 ; « son plus haut niveau depuis 1990 » vaut pour la moyenne 2025 (43,0 %), pas pour le 2e trimestre 2026 (43,1 %), le 4e trimestre 2025 (43,5 %) étant plus haut. Source : vue d'ensemble de l'édition 2026 (« Le taux d'activité des 15-24 ans atteint 43,0 % en 2025, son plus haut niveau depuis 1990 et 0,7 point de plus qu'en 2024. ») ; BDM 011818679 (2025-T4 43.5 ; 2026-T1 43.3 ; 2026-T2 43.1).
2. L'alternance de l'enquête Emploi compte les contrats d'apprentissage, de professionnalisation et les stages : 30,5 % n'est pas un nombre de contrats d'apprentissage ; l'Insee relie la hausse de 2021 et 2022 à l'apprentissage. Source : Insee Première 2096 (« 30,5 % d'entre eux sont en alternance ou en stage ») ; IR n° 192 (« L'emploi en alternance regroupe ici les contrats d'apprentissage, les contrats de professionnalisation et les stages. ») ; vue d'ensemble (« Sa hausse a été forte en 2021 et 2022 (+5,2 points au total), portée notamment par l'essor de l'apprentissage »).
3. Le NEET de l'Insee (13,3 %, trimestriel, Mayotte comprise) et celui d'Eurostat (12,9 % en 2025, annuel) ne sont pas la même mesure ; pic de 15,8 % au 2e trimestre 2020. Source : IR n° 192 (« la part des jeunes de 15 à 29 ans qui ne sont ni en emploi, ni en formation, ni en études (NEET) est stable, à 13,3 % ») ; BDM 011818639 ; Eurostat `edat_lfse_20` (FR 2025 : 12.9, drapeau « d »).
4. Eurostat sépare les NEET qui souhaitent travailler de ceux qui ne le souhaitent pas (4,1 % des 15-29 ans en France comme dans l'UE en 2025) ; pas de motif ; ruptures en 2021 et 2024. Source : Eurostat `edat_lfse_20`, `wstatus=NWANT` (FR 2025 : 4.1 « d » ; EU27_2020 : 4.1) et `WANT`.

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/youthActivity.json` (clé `claims`). Source de chaque chiffre de la réponse :

1. « On entend que les jeunes ne veulent plus travailler. » « Aucune statistique officielle ne mesure l'envie de travailler » : constat de la recherche et de la contre-vérification (aucune série de ce genre chez l'Insee ni chez Eurostat). 43,0 % en 2025 et « son plus haut niveau depuis 1990 » : vue d'ensemble de l'édition 2026 (Insee). 37,8 % en 2019 : Eurostat, `lfsi_emp_a` (`indic_em=ACT`, Y15-24 ; Eurostat donne aussi 43,0 % pour la France en 2025, même valeur que l'Insee). « L'Insee relie cette hausse notamment à l'apprentissage » : vue d'ensemble (« portée notamment par l'essor de l'apprentissage »). 4,1 % (2025), 4,3 % (2019) et 4,1 % pour l'UE : Eurostat, `edat_lfse_20`, `wstatus=NWANT`.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-jeunes.md` : séries de la BDM retéléchargées par l'API SDMX, API d'Eurostat rouverte, PDF lus avec `pdftotext`.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, taux d'emploi | 33,8 % (2026-T2) | IR 192 : « -0,3 point parmi les 15-24 ans, à 33,8 % » ; BDM 011818685 `2026-Q2 33.8 DEF` | https://www.insee.fr/fr/statistiques/9032359 | Conforme |
| Taux d'activité | 43,1 % (2026-T2) | IR 192 : « le taux d'activité des 15-24 ans diminue de 0,2 point, à 43,1 % » ; BDM 011818679 | idem | Conforme |
| Séries trimestrielles | 3 × 94 valeurs | Identiques valeur par valeur aux séries du rapport (contre-vérification) ; recomparées le 09/11/2026 aux fichiers SDMX téléchargés : identiques | https://www.insee.fr/fr/statistiques/serie/011818685 (et 011818679, 011818639) | Conforme |
| Moyennes 2025 | 34,5 % ; 43,0 % | IP 2096 : « À 34,5 %, il demeure 4,6 points au-dessus de son niveau de 2019 » ; vue d'ensemble : « atteint 43,0 % en 2025, son plus haut niveau depuis 1990 » | https://www.insee.fr/fr/statistiques/8901327 ; https://www.insee.fr/fr/statistiques/fichier/8733111/ECRT2026-VE.pdf | Conforme, avec réserve : la formule vaut pour la moyenne 2025, pas pour le 2e trimestre 2026 |
| Alternance ou stage | 30,5 % (2025) | IP 2096, figure 3 | https://www.insee.fr/fr/statistiques/8901327 | Conforme |
| NEET de l'Insee | 13,3 % ; pic 15,8 % | IR 192 : « stable, à 13,3 % » ; BDM : 13,0 au 2e trimestre 2025, 12,4 au 4e trimestre 2019 (refait) | https://www.insee.fr/fr/statistiques/9032359 | Conforme |
| NEET d'Eurostat | 2019 à 2025, 4 séries | API `edat_lfse_20` (NEMP, WANT, NWANT ; FR et EU27_2020), drapeaux « b », « d », « bd » | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/edat_lfse_20?format=JSON&lang=en&sex=T&age=Y15-29&wstatus=NWANT&training=NO_FE_NO_NFE&unit=PC&sinceTimePeriod=2019 | Conforme, avec réserve : définition différente pour la France, ruptures |
| Taux d'activité 2019 (Eurostat) | 37,8 % (réponse) | API `lfsi_emp_a` : FR 2019 37.8 ; 2025 43.0 « d » | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/lfsi_emp_a?format=JSON&lang=en&sex=T&age=Y15-24&indic_em=ACT&unit=PC_POP&sinceTimePeriod=2019 | Conforme |

**Conclusion.** Aucun chiffre du fichier n'est faux ; « le plus haut depuis 1990 » n'est attaché qu'à la moyenne 2025, et les deux NEET restent séparés.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus.

## Réserves

- Les apprentis et les étudiants qui travaillent au moins une heure dans la semaine sont en emploi au sens du BIT : le taux d'emploi des 15-24 ans monte avec l'alternance.
- Le NEET de l'Insee et celui d'Eurostat ne se comparent pas ; la moyenne des quatre trimestres 2025 de l'Insee (12,95 %, calculé) est proche du chiffre annuel d'Eurostat (12,9 %), sans être la même mesure.
- « Ne souhaite pas travailler » ne donne pas de motif (santé, charge de famille…), et ces deux sous-catégories ne sont qu'une partie de la décomposition du NEET.
- Les valeurs du 2e trimestre 2026 seront remplacées à la prochaine édition.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert la BDM, l'API d'Eurostat et les publications.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Insee : Licence Ouverte 2.0, mention « Source : Insee » et date de dernière mise à jour (https://www.insee.fr/fr/information/2008466) ;
  - Eurostat : réutilisation permise, commerciale comprise, mention « Source : Eurostat » et modifications signalées (https://ec.europa.eu/eurostat/help/copyright-notice).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
