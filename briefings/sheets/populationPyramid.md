# `populationPyramid` · Pyramide des âges

**Vérifiée le 02/11/2026** : double vérification sur le web, chiffres conformes (section « Double vérification ») ; les « À savoir » reformulés d'après elle (le champ des habitants, le libellé du statut provisoire, la dernière classe d'âge).

| Champ | Valeur |
| --- | --- |
| Indicateur | `populationPyramid`, dossier « Électorat » (`electorate`), page de type pyramide, ticket #22 de l'app (statut `planned` : les chiffres et la fiche avant la page) |
| Données | `briefings/data/populationPyramid.json`, écrit par `yarn briefings populationPyramid` le 2026-11-02 |
| Sources | Insee, « Bilan démographique 2025 - Tableaux rétrospectifs », https://www.insee.fr/fr/statistiques/8721185 (en français seulement ; l'Insee Première n° 2087 a une page anglaise, résumé seulement : https://www.insee.fr/en/statistiques/8726555), parue le 13/01/2026 : POP3 `3_Pop1janv_age.xlsx` (âge détaillé, un onglet par année) et POP5 `5_Pop1janv_grands_grages.xlsx` (onglet FR-Ensemble) ; Licence Ouverte 2.0 |
| Séries | `population` : population au 1er janvier, France, POP5, annuel, 1991 à 2026, 36 points, 2024 à 2026 provisoires ; `share75` : part des 75 ans ou plus dans la population, calculée sur POP5 (11,1 % en 2026) |
| Pyramides | `pyramids` : hommes et femmes par âge révolu de 0 à la classe ouverte, pour 1991 (France hors Mayotte, « 100 ou plus »), 2006 (France hors Mayotte, « 105 ou plus ») et 2026 (France, « 105 ou plus », provisoire), les années que donne #22 en exemple ; la somme des âges égale le total de l'onglet, et 2026 égale le total de POP5 |
| Chiffre clé | 69 081 996 habitants au 1er janvier 2026 (« 69,1 millions »), en hausse après 68,9 millions |
| Contrôle | La pyramide de 2026 redonne la répartition des 18 ans ou plus que #22 a vérifiée : 17,4 / 23,2 / 23,8 / 21,7 / 13,9 % (18-29 / 30-44 / 45-59 / 60-74 / 75 ans ou plus) ; la vérification la retrouve par l'outil pyramide et l'Insee Première n° 2087 |
| Règles | Le champ et la dernière classe d'âge viennent de l'onglet de chaque année ; le statut, de la mention « Estimation provisoire arrêtée à fin 2025 » de l'onglet et des « (p) » de POP5, qui doivent concorder. Les années de la pyramide sont un choix à confirmer par le PO (#22 dit « par exemple ») |
| Première édition | À remplir à la publication |

## « À savoir »

1. Habitants au 1er janvier, toutes nationalités, âge en années révolues (Insee Première n° 2087) ; l'électorat est un autre ensemble (Insee Focus n° 378 et n° 328).
2. « Champ : France hors Mayotte jusqu'en 2013, France à partir de 2014 » (note de POP5, Insee Première n° 2087).
3. « Données provisoires arrêtées à fin 2025 » (libellé public de l'Insee, plutôt que « résultats provisoires ») ; révision constatée : le 1er janvier 2025 valait 68 605 616 en novembre 2025 et vaut 68 851 996 dans le bilan 2025.
4. « 100 ou plus » de 1991 à 1998, « 105 ou plus » ensuite (onglets de POP3 ; tableau T6 de l'édition 2020) ; aucune page de l'Insee n'énonce la rupture, la note dit seulement que les classes ne se comparent pas telles quelles.

Non repris : l'écart entre les enfants de 0 an au 1er janvier 2026 (598 115) et les naissances de 2025 (environ 645 000), que la vérification relève dans toutes les sources de l'Insee ; la page ne dira pas « nés en 2025 ». L'écart d'Eurostat (30 000 à 44 000 de plus sur les totaux), un autre périmètre.

À savoir pour la suite : 1991 existe en deux ventilations par sexe et âge chez l'Insee (le total est le même ; 93 personnes réparties autrement entre Melodi et l'outil pyramide) ; le kit garde celle de POP3. Les fichiers POP1 et POP6 ont été remplacés après la parution (26/02 et 18/06/2026), pas POP3 ni POP5.

À actualiser : le bilan démographique paraît chaque année en janvier (aucune date annoncée pour 2027).

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans relire POP3 ni POP5. Son rapport, tel quel :

Date du contrôle : 2026-11-02. Méthode : sources web uniquement. Je n'ai relu ni POP3 (`3_Pop1janv_age.xlsx`) ni POP5 (`5_Pop1janv_grands_grages.xlsx`), ni aucun fichier de `/home/user`.

### Routes utilisées

| Route | Ce que c'est | Statut vis-à-vis du snapshot |
|---|---|---|
| **Melodi** `DS_ESTIMATION_POPULATION` (API JSON, sans clé) | Tranches de 5 ans, dernière classe 95+, statut `OBS_STATUS_FR` (PROV / D) | Autre canal Insee, mêmes estimations |
| **Outil pyramide interactif** (5014911), fichier `data/FR/donnees_pyramide_act.csv` | Âges simples 0 à 99 (99 = « 99 ans ou plus »), 1991 à 2026, les deux sexes | Autre fichier Insee, âges simples : c'est la route la plus utile |
| **Insee Première n° 2087** (8719824), figure 6a (page HTML et `ip2087.xlsx`) | Pyramide 2006 / 2016 / 2026 par âge simple, arrondie au millier, jusqu'à « 105 ou plus » | Autre publication Insee |
| `demo-pop-france.xlsx` (page 5225246) | Population au 1er janvier 1990-2026, en milliers | Autre fichier Insee |
| Édition 2020 du tableau T6 (`fe_t6.xlsx`, page 6327222) | Prédécesseur de POP3 (autre édition, publiée le 11/07/2022), âges simples 1991-2021 | Ce n'est **pas** POP3 : je l'ai utilisé seulement pour le libellé de la dernière classe d'âge et le champ par année (point 6, point 7) et comme second témoin de 1991 |
| **Eurostat** `demo_pjan` et `demo_pjangroup` (API de diffusion) | France (code FR), âges simples jusqu'à 100+ | Série transmise par l'Insee à Eurostat, périmètre légèrement différent (voir point 1) |
| Pages Insee : IP 2108, Insee Références 8612506, 8331297, mentions légales, Focus 328, blog | Contexte, statuts, champ, licence, électorat | Pages elles-mêmes lues (HTML brut), pas des résumés |

Limite à garder en tête : Melodi, l'outil, l'IP 2087, Eurostat et les anciennes éditions viennent tous de la production statistique de l'Insee. Ils prouvent que le fichier a été lu et recopié sans erreur, pas que l'Insee n'a pas fait d'erreur en amont.

Les résumés de moteur de recherche ne sont jamais la seule source d'une valeur de ce rapport, sauf là où c'est dit (point 8, prochaine parution).

---

### 1. Population totale au 1er janvier

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Total 2026 | 69 081 996 | 69 081 996 (statut PROV). IP 2087 fig. 1 : « 69 082 » milliers, « p » | Melodi `https://api.insee.fr/melodi/data/DS_ESTIMATION_POPULATION?GEO=2026-FRANCE-F&TIME_PERIOD=2026&EP_MEASURE=POP_JAN_1ST` ; somme des âges du CSV de l'outil `https://www.insee.fr/fr/outil-interactif/5014911/data/FR/donnees_pyramide_act.csv` ; `https://www.insee.fr/fr/statistiques/8719824` | Conforme |
| Hommes 2026 | 33 551 197 | 33 551 197 | Melodi (SEX=M) ; CSV de l'outil (somme) | Conforme |
| Femmes 2026 | 35 530 799 | 35 530 799 | Melodi (SEX=F) ; CSV de l'outil (somme) | Conforme |
| Total 2025 | 68 851 996 | 68 851 996 (PROV). IP 2087 : « 68 852p » | Melodi (TIME_PERIOD=2025) ; CSV de l'outil ; IP 2087 fig. 1 | Conforme |
| Total 2024 | 68 638 377 | 68 638 377 (PROV). IP 2087 : « 68 638p » | idem (TIME_PERIOD=2024) | Conforme |
| Total 1991 | 58 280 135 | 58 280 135 (D). `demo-pop-france.xlsx` : 58 280 milliers. Tableau T6 édition 2020 : somme des âges = 58 280 135 | Melodi ; CSV de l'outil ; `https://www.insee.fr/fr/statistiques/fichier/5225246/demo-pop-france.xlsx` ; `https://www.insee.fr/fr/statistiques/fichier/6327222/fe_t6.xlsx` | Conforme |
| Total 2006 | 63 186 117 | 63 186 117 (D). `demo-pop-france.xlsx` : 63 186 milliers | Melodi ; CSV de l'outil ; `demo-pop-france.xlsx` | Conforme |
| Chiffre clé « 69,1 millions », en hausse sur 2025 | « 69,1 millions », en hausse | « la population résidant en France est estimée à 69,1 millions d'habitants » ; « +0,25 % sur un an » ; 66,8 millions en métropole et 2,3 millions dans les DOM | `https://www.insee.fr/fr/statistiques/8719824` (texte de la page) ; synthèse Insee Résultats `https://www.insee.fr/fr/statistiques/8998999` | Conforme |
| Total 2026, contrôle Eurostat | (sans objet) | Eurostat ne publie pas encore 2026 pour FR (dernier millésime : 2025). 2025 : 68 882 600 ; 2024 : 68 669 303 ; 2006 : 63 229 635 ; 1991 : 58 313 439 (drapeau « p » pour 2024-2025) | `https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/demo_pjan?format=JSON&geo=FR&time=2025&time=2024` ; `.../demo_pjangroup?...&time=1991&time=2006` | Écart expliqué (hypothèse) : Eurostat est au-dessus de l'Insee de +30 604 (2025), +30 926 (2024), +43 518 (2006), +33 304 (1991). Le total diffère mais le 75+ ne diffère que de 0,9 à 3,6 mille, donc l'écart est un périmètre, pas une erreur. Explication probable, non confirmée par une source : le « FR » d'Eurostat inclurait Saint-Martin (et Saint-Barthélemy avant 2012) alors que l'Insee écrit « Les données de la Guadeloupe sont hors Saint-Martin » (`https://www.insee.fr/fr/statistiques/8331297`) |
| Révision du 1er janvier 2025 | (sans objet) | 68,6 millions dans « France, portrait social » (18/11/2025, millésime Bilan 2024 : hommes 33 279 211 + femmes 35 326 405 = 68 605 616) contre 68 851 996 dans le Bilan 2025 : +246 380 | `https://www.insee.fr/fr/statistiques/8612506` | Écart expliqué : révision d'une estimation provisoire (sert à la note 3) |
| Répartition par sexe en 1991 (non fournie dans votre liste) | non vérifiable | Hommes / femmes : Melodi 28 374 865 / 29 905 270 ; CSV de l'outil et T6 édition 2020 : 28 374 772 / 29 905 363. Le total est identique, mais 93 personnes changent de sexe d'une route à l'autre, et les tranches de 5 ans de 1991 diffèrent de quelques dizaines à 287 personnes (femmes 95+) | Melodi ; CSV de l'outil ; `fe_t6.xlsx` | Écart (mineur, entre sources Insee) : si le snapshot garde la ventilation 1991 par sexe ou par âge, vérifier laquelle des deux versions il reprend. 2006, 2024, 2025 et 2026 sont identiques à l'unité près dans Melodi et dans l'outil |

### 2. Personnes de 75 ans ou plus

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 75+ au 1er janvier 2026 (effectif) | 7 686 082 | 7 686 082 = somme Melodi des cinq tranches 75-79 (3 362 849) + 80-84 (1 931 997) + 85-89 (1 354 060) + 90-94 (766 177) + 95+ (270 999). Même valeur en sommant les âges 75 à 99+ du CSV de l'outil. Hommes 3 145 476, femmes 4 540 606 | Melodi (AGE=Y75T79 à Y_GE95) ; CSV de l'outil | Conforme |
| Part en 2026 | 11,1 % | 11,126 % calculé ; 11,1 % dans l'IP 2087 (fig. 6b : « 2026p … 11,1 ») ; 11,1 dans Melodi (`EP_MEASURE=PT_IN_POP`, AGE=Y_GE75) | `https://www.insee.fr/fr/statistiques/8719824` ; Melodi | Conforme |
| Part en 2025 | 10,8 % | 10,775 % calculé ; 10,8 (IP 2087 fig. 6b, « 2025p ») ; 10,8 (Melodi PT_IN_POP, PROV) | idem | Conforme |
| Part en 1991 | 6,6 % | 6,562 % calculé ; 6,6 (Melodi PT_IN_POP, D). Eurostat : 3 825 324 / 58 313 439 = 6,56 % | Melodi ; CSV de l'outil ; `demo_pjangroup` | Conforme |
| Pour mémoire | (non demandé) | 2006 : 8,2 % (IP 2087 et Melodi) ; 2024 : 10,4 % ; Eurostat 2025 : 75+ = 7 421 381 contre 7 419 063 Insee | idem | Conforme |

Remarque : l'effectif 75+ de 1991 est 3 824 237 dans Melodi et 3 824 412 dans le CSV de l'outil et dans le T6 édition 2020 (écart de 175 personnes, sans effet sur la part de 6,6 %).

### 3. Répartition des 18 ans et plus en cinq tranches (2026)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 18-29 ans | 17,4 % | 17,39 % (9 605 750 sur 55 229 330) | CSV de l'outil (âges simples, somme des âges 18 à 29) `https://www.insee.fr/fr/outil-interactif/5014911/data/FR/donnees_pyramide_act.csv` | Conforme |
| 30-44 ans | 23,2 % | 23,18 % (12 799 763) | idem | Conforme |
| 45-59 ans | 23,8 % | 23,79 % (13 138 290) | idem | Conforme |
| 60-74 ans | 21,7 % | 21,73 % (11 999 445) | idem | Conforme |
| 75 ans ou plus | 13,9 % | 13,92 % (7 686 082) | idem | Conforme |

Les cinq valeurs arrondies à une décimale du fichier sont celles que donne le calcul exact sur les âges simples. La somme des cinq vaut bien 100,0 %.

Détail du recoupement, trois routes :

| Tranche | Fichier | Âges simples exacts (CSV de l'outil) | IP 2087 fig. 6a (milliers arrondis, somme des deux sexes) | Melodi 5 ans, 18-19 ans estimé à 2/5 de la tranche 15-19 | Melodi 5 ans, 18-19 ans calé sur l'IP (38,9 % de la tranche 15-19) |
|---|---|---|---|---|---|
| 18-29 | 17,4 | 17,39 | 17,39 | 17,46 | 17,39 |
| 30-44 | 23,2 | 23,18 | 23,18 | 23,16 | 23,18 |
| 45-59 | 23,8 | 23,79 | 23,79 | 23,77 | 23,79 |
| 60-74 | 21,7 | 21,73 | 21,73 | 21,71 | 21,73 |
| 75+ | 13,9 | 13,92 | 13,92 | 13,91 | 13,92 |
| Effectif 18+ | (non fourni) | 55 229 330 | 55 226 000 | 55 274 350 | 55 228 963 |

Comment s'en approcher avec Melodi seul : seules les tranches 30-44, 45-59, 60-74 et 75+ s'alignent sur des tranches de 5 ans (elles sont exactes : 12 799 763 / 13 138 290 / 11 999 445 / 7 686 082). Le 18-29 dépend de la part des 18-19 ans dans la tranche 15-19. Si cette part est de 0,3 / 0,4 / 0,5, la part des 18-29 ans vaut 16,81 / 17,46 / 18,10 %. Avec l'hypothèse naïve de 2/5 on tombe à 17,46 %, soit +0,06 point par rapport au fichier. Avec la part réelle (38,9 %, tirée de l'IP 2087) on retrouve 17,39 %. Les âges simples sont donc nécessaires pour trancher ; Melodi seul ne suffit pas pour la décimale du 18-29 (il donne 17,4 à 17,5).

### 4. Quelques âges simples en 2026 et les classes ouvertes

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Âge 0, hommes | 305 209 | 305 209. IP 2087 fig. 6a : 305 (milliers) | CSV de l'outil (ANNEE=2026, SEXE=M, AGE=0) ; `https://www.insee.fr/fr/statistiques/8719824` ; `https://www.insee.fr/fr/statistiques/fichier/8719824/ip2087.xlsx` (onglet Figure 6a, identique à la page) | Conforme |
| Âge 0, femmes | 292 906 | 292 906. IP 2087 fig. 6a : 293 | idem | Conforme |
| Âge 0, total | (déduit : 598 115) | 598 115 | idem | Conforme |
| Classe « 105 ans ou plus » en 2026 | (valeur du fichier non fournie) | IP 2087 fig. 6a, ligne « 105 ou plus » : femmes 2 (milliers), hommes 0. Valeur non arrondie : introuvable pour 2026. Ordre de grandeur de l'édition précédente (Bilan 2024, 1er janvier 2025, non arrondie) : hommes 309, femmes 1 146 | `https://www.insee.fr/fr/statistiques/8719824` ; `https://www.insee.fr/fr/statistiques/8612506` | Non trouvé (valeur exacte). Cohérent à l'arrondi près |
| Centenaires (100 ans ou plus) en 2026 | (à chercher) | **37 000** « En 2026, le nombre de centenaires en France est estimé à 37 000 » et « la part des hommes parmi les centenaires … 15 % en 2026 » (IP 2108, juin 2026, texte de la page). En sommant les lignes 100 à 105+ de la fig. 6a de l'IP 2087 : femmes 32 + hommes 5 = 37 (milliers, somme de valeurs arrondies, donc ±2). Eurostat 2025 (classe ouverte Y_OPEN = 100+) : 34 979 (hommes 5 318, femmes 29 661) | `https://www.insee.fr/fr/statistiques/9004289` ; `https://www.insee.fr/fr/statistiques/8719824` ; `https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/demo_pjan?format=JSON&geo=FR&time=2025` | Conforme (arrondi au millier). Aucune source ne donne le 100+ 2026 à l'unité. À noter : l'IP 2108 est une publication de projections, l'estimation 2026 y sert de point de départ, je n'ai pas vu de phrase la reliant explicitement au bilan du 13/01/2026 |
| Dernière classe du CSV de l'outil | (sans objet) | L'âge 99 de l'outil vaut « 99 ans ou plus » : femmes 48 944 = somme IP 99 à 105+ (17+12+8+5+3+2+2 = 49 milliers) ; Melodi 95+ = 270 999 = somme des âges 95 à 99 du CSV | CSV de l'outil ; Melodi | Information : l'outil ne permet pas d'isoler les centenaires |

Observation hors périmètre (pas une erreur du snapshot) : l'effectif à 0 an au 1er janvier 2026 (598 115) est inférieur d'environ 47 000 aux 645 000 naissances estimées de 2025 (IP 2087). Le même écart existe pour 2025 (613 622 à 0 an selon l'outil, contre 660 800 naissances en 2024) et pour 2024 (629 245 à 0 an selon Eurostat, contre 677 800 naissances en 2023). Il est présent dans l'outil, dans l'IP 2087 et dans Eurostat (Melodi n'a pas d'âge simple). Je n'ai pas trouvé d'explication publiée. À ne pas présenter comme « les enfants nés en 2025 » sans réserve.

### 5. Statuts provisoire / définitif

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2024, 2025, 2026 provisoires | « estimations provisoires » (« résultats provisoires à fin 2025 ») | Melodi : `OBS_STATUS_FR = PROV` pour 2024, 2025, 2026. Page Insee : « p : données provisoires arrêtées à fin 2025 », « Note : données 2024 à 2026 provisoires arrêtées à fin 2025 ». IP 2087 : « Note : Données provisoires pour 2026 » | Melodi ; `https://www.insee.fr/fr/statistiques/5225246` ; `https://www.insee.fr/fr/statistiques/8719824` | Conforme sur le fond. Écart de formulation : le libellé public est « données provisoires arrêtées à fin 2025 », je n'ai pas trouvé « résultats provisoires à fin 2025 » (cette tournure est peut-être dans le fichier, que je n'ai pas lu) |
| 1991 et 2006 définitifs | définitifs | Melodi : `OBS_STATUS_FR = D` pour 1991 et 2006 (et pour toutes les années jusqu'en 2023). IP 2087, « Sources » : jusqu'à 2023 (France hors Mayotte), « les niveaux de population sont définitifs et directement issus du recensement » ; pour les années suivantes la population « est provisoire » | Melodi ; `https://www.insee.fr/fr/statistiques/8719824` | Conforme. Nuance de l'IP 2087 : le niveau « définitif » s'appuie sur le recensement jusqu'en 2023 pour la France hors Mayotte et jusqu'en 2017 pour Mayotte |

### 6. Dernière classe d'âge des tableaux annuels

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 1991 à 1998 | « 100 ans ou plus » | Édition 2020 du T6 : dernière ligne « 100 ou plus » dans chacune des feuilles 1991, 1992, …, 1998 (101 lignes d'âge : 0 à 99 puis 100+) | `https://www.insee.fr/fr/statistiques/fichier/6327222/fe_t6.xlsx` (page `https://www.insee.fr/fr/statistiques/6327222`) | Conforme (via l'édition 2020, pas via POP3) |
| 1999 à 2026 | « 105 ans ou plus » | Même fichier : « 105 ou plus » de 1999 à 2021 (106 lignes : 0 à 104 puis 105+). IP 2087 fig. 6a : « 105 ou plus » pour 2006, 2016 et 2026 | `fe_t6.xlsx` ; `https://www.insee.fr/fr/statistiques/fichier/8719824/ip2087.xlsx` | Conforme |
| Autres sources | (sans objet) | Melodi s'arrête à 95+, le CSV de l'outil à 99+, Eurostat regroupe tout en 100+ (Y_OPEN, sans rupture en 1999). Aucune ne contredit, aucune ne confirme directement | Melodi ; outil ; Eurostat | Information |

Je n'ai pas trouvé de phrase de l'Insee qui énonce la rupture de 1998-1999 ; elle se lit dans le libellé de la dernière ligne de chaque feuille.

### 7. Champ

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Libellé du champ | « Champ : France hors Mayotte jusqu'en 2013, France à partir de 2014 » | IP 2087 fig. 6b, mot pour mot : « Champ : France hors Mayotte jusqu'en 2013 et France à partir de 2014 » (autres figures de la même publication : « jusqu'en 2013 et France à partir de 2014 » ; les figures 2a et 2b portent une coquille « jusqu'en 2014 et France à partir de 2014 »). Page 5225246 et son xlsx : « France hors Mayotte jusqu'en 2013 et y compris Mayotte à partir de 2014 ». Page 8331297 : « Mayotte, devenu un département d'outre-mer, est intégré au champ France à partir de l'année 2014. Les données concernant Mayotte ne sont pas incluses au champ France pour les années précédentes » | `https://www.insee.fr/fr/statistiques/8719824` ; `https://www.insee.fr/fr/statistiques/fichier/5225246/demo-pop-france.xlsx` ; `https://www.insee.fr/fr/statistiques/8331297` | Conforme (ponctuation près : « et » au lieu de la virgule) |
| Champ des feuilles de l'édition 2020 du T6 | (sans objet) | 1991-2010 : « Champ : France » ; 2011-2013 : « France hors Mayotte » ; 2014-2021 : « France inclus Mayotte » | `fe_t6.xlsx` | Information : avant 2011 « France » voulait dire France hors Mayotte |
| Cohérence avec les valeurs | (sans objet) | Rupture visible : 65 564 756 au 1er janvier 2013 (hors Mayotte) puis 66 130 873 au 1er janvier 2014 (avec Mayotte). L'IP précise « France hors Mayotte en 2006 » pour la pyramide 2006 | Melodi ; `https://www.insee.fr/fr/statistiques/8719824` | Conforme |
| Nuance Eurostat | (sans objet) | Eurostat intègre Mayotte « with the statistics on population on 1 January 2015 » (Insee : 1er janvier 2014) | `https://ec.europa.eu/eurostat/cache/metadata/en/demo_pop_esms.htm` | Écart expliqué : définition propre à Eurostat, à ne pas mélanger avec le champ Insee |
| Présence sur la page 8721185 | (sans objet) | La page elle-même ne contient aucune mention « Champ » (lue en HTML brut). Le champ est dans les fichiers et dans l'IP 2087 | `https://www.insee.fr/fr/statistiques/8721185` | Non trouvé sur la page (trouvé ailleurs) |

### 8. Parution, prochaine édition, licence

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Date de parution de la page 8721185 | 13/01/2026 (« Paru le ») | « Paru le : 13/01/2026 », « Janvier 2026 ». Même date pour l'IP 2087 et pour la page 5225246. Melodi : `issued` = 2026-01-13T11:00 | `https://www.insee.fr/fr/statistiques/8721185` ; `https://www.insee.fr/fr/statistiques/8719824` ; `https://api.insee.fr/melodi/catalog/DS_ESTIMATION_POPULATION` | Conforme |
| Avertissements affichés sur la page | (non mentionnés) | Deux fichiers ont été remplacés après la parution : POP1 le 26/02/2026 (solde naturel 2024 de la France métropolitaine : -737 au lieu de +737) et POP6 le 18/06/2026 (âge moyen et âge médian 2021 : 42,0 et 41,0 ans au lieu de 41,5 et 40,6). POP3 et POP5 ne sont pas cités | `https://www.insee.fr/fr/statistiques/8721185` | Information : « Paru le 13/01/2026 » reste la date de parution, mais si le kit reprend POP1 ou POP6 ou l'archive complète, la « date de mise à jour » diffère. Melodi : jeu de données `modified` = 2026-08-05 (je n'ai pas identifié ce qui a changé, les valeurs comparées sont identiques au fichier) |
| Prochaine édition « mi-janvier 2027 » | « mi-janvier 2027 » | Aucune date annoncée trouvée. La page 8721185 n'en porte pas. Le blog de l'Insee écrit « Comme chaque année en janvier, l'Insee a publié le 13 janvier 2026 le bilan démographique ». Le calendrier de diffusion de l'Insee est une application JavaScript, inaccessible ici. Deux recherches web (résumés de moteur) n'ont trouvé aucune annonce du « Bilan démographique 2026 » | `https://blog.insee.fr/france-2025-plus-de-deces-que-de-naissances/` ; recherches web | Non trouvé. « Janvier 2027 » est une attente fondée sur le rythme annuel, pas une date annoncée. Écrire « attendue en janvier 2027 » ou « chaque janvier », pas « mi-janvier 2027 » comme fait établi |
| Licence | Licence Ouverte 2.0 ; « Source : Insee » et la date | Page des mentions légales : « Sauf mention contraire, les informations publiques diffusées sur ce site (données, bases de données, publications, fichiers téléchargeables) sont mises à disposition sous la Licence Ouverte / Open Licence version 2.0 (Etalab). Cette licence autorise la réutilisation libre, y compris à des fins commerciales, sous réserve de mentionner la source sous la forme « Source : Insee », de mentionner la date de dernière mise à jour des données lorsque celle-ci est connue et de ne pas altérer le sens des informations ou induire en erreur quant à leur interprétation » | `https://www.insee.fr/fr/information/2008466` (page lue en direct) | Conforme. La page 8721185 ne porte pas la licence ; elle renvoie aux « Mentions légales et crédits » du pied de page. Aucune « mention contraire » vue sur cette page |

### 9. Versions anglaises

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Page 8721185 en anglais | `https://www.insee.fr/en/statistiques/8721185` renvoie 404 | 404 confirmé. Aucune page anglaise des tableaux rétrospectifs trouvée : les identifiants voisins `/en/statistiques/8721187`, `8721189`, `8721191`, `8721207`, `8721209` sont aussi en 404. Seul lien anglais dans l'en-tête : le bouton de langue du site (`/langue/en`) | `https://www.insee.fr/en/statistiques/8721185` (404) | Conforme (404) ; équivalent anglais : Non trouvé |
| Insee Première n° 2087 en anglais | (à chercher) | **Existe** : « Demographic report 2025 », Insee Première n° 2087, January 2026, sous l'identifiant **8726555**. Contenu : résumé en anglais seulement (69,1 millions, +0,25 %, 22 % de 65 ans ou plus, 645 000 naissances, 651 000 décès, solde naturel de -6 000) ; pas de tableaux, pas de lien vers un PDF ou un xlsx anglais. Trouvé d'abord par recherche web, puis lu sur la page elle-même (HTTP 200). `/en/statistiques/8719824` renvoie 404 | `https://www.insee.fr/en/statistiques/8726555` ; (aussi accessible avec `?sommaire=8721209`) | Trouvé |
| Autres supports bilingues | (sans objet) | Melodi : libellés français et anglais dans le catalogue. Outil pyramide : bouton EN/FR et exports « Actual data (CSV) / Projected data (CSV) » | `https://api.insee.fr/melodi/catalog/DS_ESTIMATION_POPULATION` ; `https://www.insee.fr/fr/outil-interactif/5014911/pyramide.htm` | Information |

Remarque sur l'outil pyramide : la page HTML porte encore le titre « Pyramide des âges au 1er janvier 2025 » et son `settings.js` traite 2024-2026 comme « projetées », alors que son CSV contient bien les valeurs du Bilan 2025 pour 2024-2026 (identiques à Melodi). Ne pas s'en servir comme preuve du statut provisoire.

---

### Les quatre notes « À savoir »

**(1) « La pyramide compte les habitants au 1er janvier, âge en années révolues ; ce n'est pas l'électorat (les inscrits par âge sont une autre source). »**

Confirmé. Support : l'IP 2087 écrit « la population résidant en France » et « Note : L'âge est celui au 1er janvier » (fig. 6b) ; la figure 6a de l'xlsx est titrée « Âge au 1er janvier (en année) » ; le tableau POP3 est présenté sur la page 8721185 comme « par sexe et âge détaillé (en années révolues) ». L'électorat est bien une autre source : le Répertoire électoral unique, géré par l'Insee, et l'Insee Focus n° 328 (mai 2024, `https://www.insee.fr/fr/statistiques/8192479`) publie les inscrits par âge. Cet Insee Focus montre pourquoi les deux ne se superposent pas : 49,5 millions d'inscrits début mai 2024, dont 1,6 million résidant hors de France et 269 000 citoyens d'un autre pays de l'UE résidant en France, alors que 95 % des Français en âge de voter (France métropolitaine et DOM) sont inscrits. À titre de repère, la population de 18 ans ou plus résidant en France au 1er janvier 2026 est de 55,2 millions.

Proposition de formulation : « La pyramide compte les personnes résidant en France au 1er janvier, quelle que soit leur nationalité, avec l'âge en années révolues à cette date. Elle ne décrit pas l'électorat : les inscrits sur les listes électorales (Répertoire électoral unique) sont une autre source, avec un autre champ. » Le mot « habitants » est acceptable (l'Insee l'emploie) ; « personnes résidant en France » est plus proche de la source.

**(2) « Champ : France hors Mayotte jusqu'en 2013, France y compris Mayotte depuis 2014. »**

Confirmé, mot pour mot dans l'IP 2087 (fig. 6b) et dans la note de bas de tableau de `demo-pop-france.xlsx` (« France hors Mayotte jusqu'en 2013 et y compris Mayotte à partir de 2014 »). Points à signaler : la rupture est visible dans les totaux (65 564 756 en 2013, 66 130 873 en 2014) ; Eurostat, lui, intègre Mayotte un an plus tard (1er janvier 2015) ; une coquille de l'Insee (« jusqu'en 2014 ») figure dans les figures 2a et 2b de l'IP 2087. Éventuel ajout : l'Insee précise « Les données de la Guadeloupe sont hors Saint-Martin » (page 8331297, estimations régionales et départementales).

Proposition de formulation : inchangée. Facultatif : « (1991 et 2006 sont donc hors Mayotte ; 2024 à 2026 incluent Mayotte) ».

**(3) « 2024 à 2026 sont des estimations provisoires, révisées chaque janvier. »**

Confirmé pour le statut (Melodi : PROV pour 2024-2026 et D jusqu'à 2023 ; page 5225246 : « données 2024 à 2026 provisoires arrêtées à fin 2025 »). « Révisées chaque janvier » est exact en pratique, mais une précision manque : une estimation provisoire change à chaque nouveau bilan démographique, et devient définitive quand le recensement de l'année correspondante est disponible. Exemple chiffré : le 1er janvier 2025 valait 68,6 millions (68 605 616) dans la publication de novembre 2025 et vaut 68 851 996 dans le Bilan 2025 (+246 380).

Proposition de formulation : « Les chiffres de 2024 à 2026 sont des estimations provisoires (données arrêtées à fin 2025). L'Insee les révise à chaque bilan démographique, publié en janvier, jusqu'à ce que le recensement les rende définitifs ; ceux de 1991 à 2023 sont définitifs. »

**(4) « La dernière classe d'âge : 100 ans ou plus jusqu'en 1998, 105 ans ou plus depuis 1999. »**

Confirmé, mais seulement par l'édition 2020 du tableau T6 (libellé de la dernière ligne de chaque feuille : « 100 ou plus » de 1991 à 1998, « 105 ou plus » de 1999 à 2021) et par l'IP 2087 pour 2006 et 2026 (« 105 ou plus »). Je n'ai pas lu POP3 et aucune page Insee ne décrit cette rupture. L'effet pratique à signaler : les classes ne sont pas comparables telles quelles ; pour suivre les centenaires dans le temps, il faut additionner les âges 100 à 104 et la classe 105+ à partir de 1999.

Proposition de formulation : « Dans les tableaux annuels, la dernière classe d'âge regroupe les 100 ans ou plus jusqu'en 1998 et les 105 ans ou plus depuis 1999 (les âges 100 à 104 sont détaillés depuis cette date). »

---

### Conclusion

**Écarts et points à corriger, par ordre d'importance**

1. **Prochaine édition « mi-janvier 2027 » : non trouvée.** Aucune date n'est annoncée dans ce que j'ai pu lire. Seul le rythme annuel (« Comme chaque année en janvier ») le soutient. Écrire « attendue en janvier 2027 », ou retirer « mi-».
2. **Fichiers corrigés après parution.** POP1 (26/02/2026) et POP6 (18/06/2026) ont été remplacés. POP3 et POP5 ne sont pas concernés d'après l'avertissement de la page, mais si le kit cite une « date de mise à jour », 13/01/2026 est la date de parution, pas celle de ces deux corrections.
3. **Sexe et âge en 1991 : deux versions Insee.** Totaux identiques (58 280 135), mais Melodi sépare 93 personnes différemment du CSV de l'outil et du T6 édition 2020 (tranches de 5 ans : jusqu'à 287 personnes). Sans effet sur « 6,6 % » ni sur le total ; à vérifier si le snapshot garde la ventilation 1991.
4. **Libellé du statut.** Le public Insee écrit « données provisoires arrêtées à fin 2025 », pas « résultats provisoires à fin 2025 ». Le fond est exact.
5. **Page 8721185 incomplète pour votre sourcing.** Elle ne porte ni « Champ », ni licence, ni date de prochaine parution. Le champ vient de l'IP 2087 et des fichiers, la licence des mentions légales du site.
6. **Version anglaise.** Pas de page anglaise de 8721185 (404 confirmé). L'IP 2087 existe en anglais sous un autre identifiant : `https://www.insee.fr/en/statistiques/8726555`, résumé seulement.
7. **Observation sur l'âge 0 :** 598 115 enfants de 0 an au 1er janvier 2026 pour 645 000 naissances en 2025 (écart d'environ 47 000, présent aussi en 2024 et 2025, dans l'outil, l'IP 2087 et Eurostat). Cela n'invalide pas le snapshot ; ne pas l'étiqueter « nés en 2025 » sans réserve.

**Conforme, sans réserve :** tous les totaux (2026 avec les deux sexes, 2025, 2024, 1991, 2006), le 75+ (effectif et parts 2026, 2025, 1991), la répartition 18+ en cinq tranches (recalculée à partir des âges simples : 17,39 / 23,18 / 23,79 / 21,73 / 13,92), l'âge 0 hommes et femmes, les statuts provisoire et définitif, le libellé du champ, la date du 13/01/2026, la licence, les deux libellés de dernière classe d'âge (via l'édition 2020, pas POP3), la « 69,1 millions » en hausse.

**Centenaires 2026 :** 37 000 selon l'Insee (IP 2108) ; 32 000 femmes et 5 000 hommes en sommant les cellules arrondies de l'IP 2087. Pas de valeur exacte à l'unité.

Les quatre notes sont justes. Les reformulations proposées plus haut précisent la note (1) (personnes résidant en France, toutes nationalités), la note (3) (révision à chaque bilan, définitif quand le recensement est disponible) et la note (4) (les classes ne sont pas comparables telles quelles).

---

### URL consultées (2026-11-02)

**Insee, pages et fichiers**
- https://www.insee.fr/fr/statistiques/8721185 (page lue en HTML brut ; aussi `?sommaire=8721209`)
- https://www.insee.fr/fr/statistiques/8719824 (Insee Première n° 2087, page HTML)
- https://www.insee.fr/fr/statistiques/fichier/8719824/ip2087.xlsx (onglet Figure 6a comparé à la page : 106 lignes identiques)
- https://www.insee.fr/en/statistiques/8726555 (version anglaise de l'IP 2087)
- https://www.insee.fr/en/statistiques/8721185 , /en/statistiques/8719824 , /en/statistiques/8721187 , /8721189 , /8721191 , /8721207 , /8721209 (tous 404)
- https://www.insee.fr/fr/statistiques/5014911 (redirige vers https://www.insee.fr/fr/outil-interactif/5014911/pyramide.htm) ; fichiers `settings.js`, `scripts/functions.js`, `data/FR/donnees_pyramide_act.csv` et `data/FR/donnees_pyramide_proj.csv` (identiques)
- https://www.insee.fr/fr/statistiques/5225246 et https://www.insee.fr/fr/statistiques/fichier/5225246/demo-pop-france.xlsx
- https://www.insee.fr/fr/statistiques/9004289 (Insee Première n° 2108, projections de population, juin 2026)
- https://www.insee.fr/fr/statistiques/8998999 (Insee Résultats, synthèse, 15/06/2026)
- https://www.insee.fr/fr/statistiques/8612506 (Insee Références, France portrait social, 18/11/2025)
- https://www.insee.fr/fr/statistiques/8331297 (estimation de la population au 1er janvier 2025, séries régionales et départementales)
- https://www.insee.fr/fr/statistiques/2012692 (estimations par sexe et âge au 1er janvier 2026, départements ; non exploité)
- https://www.insee.fr/fr/statistiques/6327222 et https://www.insee.fr/fr/statistiques/fichier/6327222/fe_t6.xlsx (édition 2020 de T6, prédécesseur de POP3) ; https://www.insee.fr/fr/statistiques/5390418 (édition 2019, page seulement)
- https://www.insee.fr/fr/statistiques/8192479 (Insee Focus n° 328, électeurs inscrits, mai 2024)
- https://www.insee.fr/fr/information/2008466 (mentions légales et crédits)
- https://blog.insee.fr/france-2025-plus-de-deces-que-de-naissances/
- https://www.insee.fr/fr/information/2410168 (sans rapport : « Économie et Statistique »), https://www.insee.fr/fr/calendrier (erreur 500), https://www.insee.fr/fr/information/8168551 (404)

**Melodi (API Insee)**
- https://api.insee.fr/melodi/data/DS_ESTIMATION_POPULATION?GEO=2026-FRANCE-F&TIME_PERIOD=2026&EP_MEASURE=POP_JAN_1ST (et les mêmes requêtes pour 2025, 2024, 2006, 1991 ; `EP_MEASURE=PT_IN_POP`)
- https://api.insee.fr/melodi/catalog/DS_ESTIMATION_POPULATION

**Eurostat**
- https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/demo_pjan (geo=FR, 2024 et 2025, tous âges et sexes)
- https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/demo_pjangroup (geo=FR, 1991, 2006, 2024, 2025, 75+)
- https://ec.europa.eu/eurostat/cache/metadata/en/demo_pop_esms.htm

**Recherches web (résumés de moteur, non utilisés comme source unique)**
- « Insee mentions légales réutilisation des données licence ouverte 2.0 … » : a mené à la page des mentions légales, ensuite lue directement.
- « Insee Demographic Overview 2025 … Insee Première 2087 English » : a mené à `/en/statistiques/8726555`, ensuite lu directement.
- « Insee centenaires 1er janvier 2026 … » : a mené à l'IP 2108 (9004289), ensuite lu directement (37 000).
- « Insee bilan démographique 2026 date de publication janvier 2027 … » et « Insee "Bilan démographique 2026" parution janvier 2027 » : aucun résultat annonçant la date. Seule valeur issue d'un résumé de moteur sans page confirmant : l'absence d'annonce.
- « nombre d'inscrits sur les listes électorales par tranche d'âge … » : a mené à l'Insee Focus n° 328, ensuite lu directement.
- « … 105 ans ou plus … 100 ans ou plus jusqu'en 1998 … » : n'a trouvé aucune explication de la rupture ; la vérification est passée par l'édition 2020 de T6.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
