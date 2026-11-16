# `youthUnemployment` · Le chômage des jeunes, taux et part (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart de valeur ; réserves de lecture reprises ci-dessous (titre BDM trompeur de la part de chômage, maximum de 28,0 % de la série, qui remonte à 1975 (relu le 16/11/2026), Céreq à ne pas comparer à l'Insee). La licence des sources n'a pas été vérifiée (voir « Relecture »).

**Le 3e trimestre 2026** (rafraîchi le 16/11/2026, Mitchnsun/moi-president#439). Les valeurs trimestrielles sont celles du 3e trimestre 2026 (21,0 % et 9,0 %) et du 2e trimestre révisé (21,5 % et 9,3 %), publiées par l'Insee le 10/11/2026 (Informations rapides n° 270) et relues dans la BDM le 16/11/2026 : les mêmes que la page du chômage (`data/unemployment.json`, 10/11/2026) et la question du débat (21 %). L'Insee publie le 4e trimestre le 16/02/2027 à 7 h 30 : la prochaine édition du kit les remplacera.

| Champ | Valeur |
| --- | --- |
| Indicateur | `youthUnemployment`, dossier « Travail et retraites » (`work`), volet « Chômage des jeunes » de la page composite `youthEmployment` (voir `youthEmployment.md`), page de type comparaison, recherche du 09/11/2026 |
| Données | `briefings/manual/youthUnemployment.json`, saisi à la main le 2026-11-09 depuis les publications ci-dessous et la BDM de l'Insee ; le 3e trimestre 2026 saisi le 2026-11-16 (`retrievedOn`) |
| Sources | 1. Insee, « Au troisième trimestre 2026, le taux de chômage s’établit à 8,2 %, en hausse de 0,4 point sur un an, Informations rapides n° 270 », https://www.insee.fr/fr/statistiques/9118603 (avant le 16/11/2026 : n° 192 du 2e trimestre, https://www.insee.fr/fr/statistiques/9032359), série https://www.insee.fr/fr/statistiques/serie/011818548 (page anglaise de la série), licence `etalab-2.0`. 2. Insee, « Une photographie du marché du travail en 2025, Insee Première n° 2096 », https://www.insee.fr/fr/statistiques/8901327, PDF https://www.insee.fr/fr/statistiques/fichier/8901327/ip2096.pdf, `etalab-2.0`. 3. Insee, « Évolution du chômage », Emploi, chômage, revenus du travail, édition 2026, https://www.insee.fr/fr/statistiques/8733053, classeur https://www.insee.fr/fr/statistiques/fichier/8733053/ECRT2026_F8.xlsx, `etalab-2.0`. 4. Insee, « Inégalités face au chômage », même édition, https://www.insee.fr/fr/statistiques/8733055, `etalab-2.0`. 5. Insee, « Chômage en phase d'insertion professionnelle », Formations et emploi, édition 2025, https://www.insee.fr/fr/statistiques/8305516, `etalab-2.0`. 6. Céreq, « Enquête 2024 auprès de la Génération 2021. S'insérer dans un monde instable : le diplôme reste une valeur sûre », Céreq Bref n° 487-488, https://www.cereq.fr/sites/default/files/2026-07/Bref_487-488_OK.pdf, licence « citation seule ». Toutes en français seulement (pages anglaises en 404 le 09/11/2026) |
| Dates de publication | 2026-11-10 (IR n° 270) ; 2026-03-25 (Insee Première 2096) ; 2026-07-02 (deux fiches de l'édition 2026) ; 2025-02-12 (Formations et emploi) ; 2026-07-07 pour le Céreq : la date de publication n'est pas dans le PDF, c'est la date de création du fichier |
| Séries | `youthRate` : taux de chômage des 15-24 ans, CVS, BDM 011818548, 2e et 3e trimestres 2026 (21,5 ; 21,0). `youthShare` : part de chômage des 15-24 ans, CVS, BDM 011818613, mêmes trimestres (9,3 ; 9,0). `youthRateYear` et `youthShareYear` : moyennes 2025 (19,8 ; 8,5), Insee Première 2096 et fiche « Évolution du chômage ». `rate1524`, `rate2549`, `rate50plus`, `rateAll` : taux de chômage par âge, moyennes annuelles 2019 à 2025, 7 points chacune, figure 1 du classeur F8 (15-24 ans 20,8 à 19,8 ; ensemble 8,5 à 7,7) |
| Ventilations | `byDiploma` (2025, tous âges, figure 1 de « Inégalités face au chômage ») : aucun diplôme ou brevet 14,7 ; CAP-BEP 7,6 ; baccalauréat 9,1 ; bac+2 ou plus 5,3 ; ensemble 7,7. `afterStudies` (2023, sortis depuis 1 à 4 ans, figure 1 de « Chômage en phase d'insertion professionnelle ») : 42,4 ; 17,5 ; 18,2 ; bac+2 11,0 ; bac+3/4 10,7 ; bac+5 ou plus 6,8 ; ensemble 14,2. `cereq` (période « 2024 », enquête 2024 auprès de la Génération 2021, tableau 1) : non-diplômés 40 ; CAP-BEP 25 ; bac 18 ; bac+2 13 ; bac+3/4 13 ; master 9 ; bac+8 6 ; ensemble 16 |
| Chiffre clé | 21,0 % des actifs de 15 à 24 ans au chômage au 3e trimestre 2026, en baisse (21,5 % au 2e trimestre révisé) ; à côté, la part de chômage, 9,0 % |
| Règles | Saisie à la main. Quatre vues : « Taux ou part » (un groupe par période, le taux et la part côte à côte, les deux définitions de l'Insee dans la note), « Par âge » (2019 à 2025, l'ensemble hachuré), « Par diplôme » (tous âges en 2025, puis 1 à 4 ans après les études en 2023), « Trois ans après » (Céreq). La série 1980-2023 par diplôme (figure 2a) n'est pas saisie : selon l'Insee, ses années ne se comparent que par périodes (2003-2013, puis depuis 2014), et son champ change en 2014 (France métropolitaine, puis France hors Mayotte) : elle n'est pas homogène, seule la dernière année est montrée. Non saisis : le taux 1 à 4 ans après les études de 2025 tous diplômes (16,6 %), le halo et le sous-emploi des 15-24 ans, les chômeurs qui n'ont jamais travaillé, le chômage de longue durée des jeunes, les taux d'emploi du Céreq par diplôme (seuls 74 % pour l'ensemble, dans une note) |
| Première édition | À remplir à la publication |

## « À savoir »

1. Valeurs du 3e trimestre 2026 publiées le 10 novembre 2026, le 2e trimestre révisé avec elles, le 4e trimestre attendu le 16 février 2027 ; estimations d'enquête, ±0,3 point pour le taux d'ensemble, marge non publiée et plus large pour les 15-24 ans. Source : IR n° 270 (« La prochaine publication, portant sur le quatrième trimestre 2026, est prévue le 16 février 2027 à 7h30. » ; « Estimation à +/- 0,3 point près du niveau du taux de chômage et de son évolution d'un trimestre à l'autre. ») ; précaution du rapport final (`jeunesTauxChomageT2`).
2. Une personne en études qui ne cherche pas d'emploi est inactive : elle compte dans la part, pas dans le taux ; part de chômage de 8,5 % pour les 15-24 ans en 2025 contre 6,2 % pour les 25-49 ans. Source : fiche « Évolution du chômage » (« peu de jeunes sont comptabilisés comme actifs. Aussi, rapporté à l'ensemble de la population (actifs et inactifs), l'écart avec leurs aînés est plus réduit : la part de chômage est de 8,5 % pour les 15-24 ans, contre 6,2 % parmi les 25-49 ans. »).
3. Les taux par diplôme de 2025 portent sur tous les âges ; le croisement 1 à 4 ans après les études s'arrête à 2023 ; la série depuis 1980 change de questionnaire (2013, 2021) et de champ (2014). Source : « Inégalités face au chômage » (« en 2025, le taux de chômage atteint 14,7 % parmi les actifs ayant au plus le brevet des collèges, contre 5,3 % parmi les diplômés du supérieur ») ; « Chômage en phase d'insertion professionnelle » (« À la suite des changements de questionnaires en 2013 puis en 2021, les données ont été rétropolées afin de rendre comparables les années 2003-2013 d'une part, les années 2014 et ultérieures d'autre part »).
4. Le Céreq suit 773 000 primo-sortants de 2021, interrogés de septembre 2024 à janvier 2025 ; 74 % en emploi ; évolutions relatives ; à ne pas comparer à l'Insee. Source : Céreq Bref 487-488 (« 773 000 individus ayant quitté pour la première fois le système éducatif en 2021 » ; « 31 000 jeunes ont été interrogés entre septembre 2024 et janvier 2025 » ; « après trois ans de vie active, 74 % des jeunes de la Génération 2021 sont en emploi »).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/youthUnemployment.json` (clé `claims`). Source de chaque chiffre de la réponse :

1. « On entend qu'un jeune sur quatre est au chômage. » 21,0 % (taux, 3e trimestre 2026) : IR n° 270 et BDM 011818548. « Un peu plus d'un sur cinq » : calculé (21,0 %), et dit « calculé ». 9,0 % (part) : BDM 011818613. « Le taux a dépassé 25 % en 2009 et 2010, puis de mi-2012 à fin 2016, avec un maximum de 28,0 % au 4e trimestre 2012 » : BDM 011818548 (série 2003-T1 à 2026-T2, relue par la contre-vérification ; 25,0 au 2e trimestre 2012, de 26,1 au 3e trimestre 2012 à 25,3 au 4e trimestre 2016 ; relue le 16/11/2026 dans la série mise à jour le 10/11/2026, qui remonte à 1975 : de 26,1 au 3e trimestre 2012 à 25,2 au 4e trimestre 2016, maximum 28,0 au 4e trimestre 2012, 24,0 au plus avant 2003). Le maximum est aussi celui de la série depuis 1975 (24,0 au plus avant 2003). Le taux a aussi dépassé 25 % aux 2e, 3e et 4e trimestres 2009 (25,2, 25,5, 25,3) et au 3e trimestre 2010 (25,5) : la réponse le dit (contre-vérification du 16/11/2026).
2. « On entend que le diplôme ne protège plus du chômage. » 14,7 % et 5,3 % (2025, tous âges) : « Inégalités face au chômage ». 42,4 % et 6,8 % (2023, 1 à 4 ans après les études) : « Chômage en phase d'insertion professionnelle », figure 1. 40 %, 9 % et 16 % (Génération 2021, trois ans après) : Céreq Bref 487-488, tableau 1. Les trois mesures sont nommées chacune avec leur producteur et leur population ; elles ne sont pas comparées entre elles.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-jeunes.md` : séries de la BDM retéléchargées par l'API SDMX, PDF lus avec `pdftotext`, classeur F8 lu avec openpyxl.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, taux 15-24 ans | 21,6 % (2026-T2) ; 21,2 % (2026-T1) | BDM 011818548 `2026-Q2 21.6 DEF` ; IR 192 : « le taux de chômage des 15-24 ans rebondit : +0,4 point, à 21,6 % » | https://www.insee.fr/fr/statistiques/9032359 | Conforme |
| Part de chômage | 9,3 % ; 9,2 % | BDM 011818613 `2026-Q2 9.3` ; refait : 21,6 % × 43,1 % = 9,3 % (calculé) ; moyenne des quatre trimestres 2025 (8,2 ; 8,2 ; 8,3 ; 9,4) = 8,5 %, la part publiée pour 2025 | https://www.insee.fr/fr/statistiques/serie/011818613 | Conforme, avec réserve : le titre BDM dit « part dans la population de 15 ans ou plus », la valeur est rapportée aux 15-24 ans |
| Moyennes 2025 | 19,8 % ; 8,5 % | IP 2096 : « atteint 19,8 % » ; « jusqu'à 8,5 % pour les 15-24 ans » ; classeur F8 : 19.8 et 8.5 | https://www.insee.fr/fr/statistiques/8901327 | Conforme |
| Taux par âge 2019-2025 | 4 × 7 valeurs | Classeur F8, figure 1, relu cellule par cellule | https://www.insee.fr/fr/statistiques/fichier/8733053/ECRT2026_F8.xlsx | Conforme |
| Par diplôme, tous âges | 14,7 / 7,6 / 9,1 / 5,3 / 7,7 | Cellules de la figure 1 de la fiche | https://www.insee.fr/fr/statistiques/8733055 | Conforme |
| 1 à 4 ans après, 2023 | 7 valeurs | Cellules de la figure 1 ; texte : « 42 % parmi les peu ou pas diplômés [...] 7 % pour les diplômés de niveau bac+5 ou plus » | https://www.insee.fr/fr/statistiques/8305516 | Conforme |
| Céreq, Génération 2021 | 8 valeurs | Tableau 1 : « Non-diplômé ... 40 » ; « Ensemble ... 16 » ; interrogation entre septembre 2024 et janvier 2025 | https://www.cereq.fr/sites/default/files/2026-07/Bref_487-488_OK.pdf | Conforme, avec réserve : date de publication non lue (PDF du 07/07/2026), évolutions relatives |

**Conclusion.** Aucun chiffre du fichier n'est faux ; le taux et la part de chômage sont toujours affichés avec leur définition.

**Rafraîchissement du 16/11/2026** (Mitchnsun/moi-president#439) : relu par l'agent qui a fait la mise à jour (série BDM retéléchargée par l'API SDMX, « LAST_UPDATE 2026-11-10 » ; page de l'IR n° 270 lue). Double vérification faite le 16/11/2026 par un agent Claude (modèle Sonnet) qui a rouvert l'IR n° 270 et les deux séries de la BDM : aucune valeur fausse ; deux formulations reprises (le maximum de 28,0 % vaut aussi depuis 1975 ; le taux a aussi dépassé 25 % en 2009 et 2010).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Taux 15-24 ans, 3e trimestre 2026 | 21,0 % | BDM 011818548 `2026-Q3 21.0 DEF` ; IR 270 : « le taux de chômage diminue pour les 15-24 ans (-0,5 point, à 21,0 %) » ; tableau : « 15-24 ans 21,5 21,0 » | https://www.insee.fr/fr/statistiques/9118603 | Conforme (contre-vérifié le 16/11/2026 par un agent Claude, modèle Sonnet, sur l’IR n° 270 et la BDM) |
| Taux 15-24 ans, 2e trimestre 2026 révisé | 21,5 % | BDM 011818548 `2026-Q2 21.5 DEF` ; IR 270, colonne 2026T2 : 21,5 | https://www.insee.fr/fr/statistiques/serie/011818548 | Conforme (contre-vérifié le 16/11/2026 par un agent Claude, modèle Sonnet, sur l’IR n° 270 et la BDM) |
| Part de chômage, 2e et 3e trimestres 2026 | 9,3 % ; 9,0 % | BDM 011818613 `2026-Q2 9.3`, `2026-Q3 9.0` (l'IR n° 270 ne la donne pas) | https://www.insee.fr/fr/statistiques/serie/011818613 | Conforme (contre-vérifié le 16/11/2026 par un agent Claude, modèle Sonnet, sur l’IR n° 270 et la BDM) |
| Publication | IR n° 270, 2026-11-10 | « Informations rapides N° 270 », « Paru le 10/11/2026 », « Prochaine parution le : 16/02/2027 à 07h30 » | https://www.insee.fr/fr/statistiques/9118603 | Conforme (contre-vérifié le 16/11/2026 par un agent Claude, modèle Sonnet, sur l’IR n° 270 et la BDM) |

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus.

## Réserves

- Le taux de chômage des 15-24 ans n'est pas la part des jeunes au chômage : le `readFirst` du volet et la note du bloc le disent.
- Le maximum de 28,0 % (4e trimestre 2012) est celui de la série trimestrielle depuis 1975 (24,0 au plus avant 2003).
- Les taux du Céreq ne se comparent pas à ceux de l'Insee (autre population, autre date, autre source).
- Les valeurs du 3e trimestre 2026 seront remplacées à la prochaine édition (4e trimestre publié le 16/02/2027).

## Mises à jour

- 16/11/2026 (Mitchnsun/moi-president#439) : le 3e trimestre 2026, publié par l'Insee le 10/11/2026 (Informations rapides n° 270), pour que le volet, la page du chômage (`data/unemployment.json`) et la question du débat disent le même chiffre. `youthRate` : 21,5 (2e trimestre, révisé de 21,6) et 21,0 (3e trimestre) ; `youthShare` : 9,3 et 9,0 ; chiffre clé 21,0 % au 3e trimestre 2026, en baisse ; la 1re source passe du n° 192 au n° 270 (registre de l'application mis à jour dans la même PR, #439) ; le 1er « À savoir » et la 1re réponse de « Ce qu'on entend » suivent. Les autres valeurs ne changent pas. La double vérification de ces chiffres est à faire (voir le tableau).

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert les publications et la BDM.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Insee : Licence Ouverte 2.0, mention « Source : Insee » et date de dernière mise à jour (https://www.insee.fr/fr/information/2008466) ;
  - citation seule : Céreq (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
