# `schools` · Éducation (page composite)

La page « Éducation » (#32) n'a pas de fichier : ses trois parties ont le leur (`pisaScores`, `earlySchoolLeavers`, `educationSpending`, PO, 02/11/2026). Cette fiche porte la double vérification commune aux trois.

**Vérifiée le 02/11/2026** : aucun chiffre faux ; corrections portées sur les notes des parties (voir leurs fiches).

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans relire les trois fichiers de la DEPP ni appeler le jeu Eurostat du script. Son rapport, tel quel :

Date de la vérification : 2026-11-02. Méthode : sources web uniquement. Aucun fichier sous `/home/user` lu ou modifié. Les trois XLSX de la DEPP et le jeu `edat_lfse_14` de l'API Eurostat n'ont pas été lus ni appelés.

### Légende de fiabilité des sources

- **[direct]** : document, fichier ou API lu en entier par moi (PDF, JSON, Excel, HTML récupéré).
- **[moteur]** : valeur qui ne vient que du résumé d'un moteur de recherche (page non lisible : 403 ou hôte bloqué). À traiter comme non vérifiée.
- **[calcul]** : calcul que j'ai fait à partir de valeurs [direct].

Deux précisions de méthode à connaître :

1. Pour PISA, les valeurs décimales viennent de l'annexe Excel **de l'OCDE** (StatLink `https://stat.link/mrq53f`, tableaux I.B1.2a.1 à 3 et 36 à 38, et `https://stat.link/3r8tyd`, figure I.1.5), pas du XLSX de la DEPP. C'est une source indépendante du script.
2. Pour Eurostat, je n'ai pas appelé `edat_lfse_14`. J'ai appelé `sdg_04_10` (« Early leavers from education and training by sex », indicateur ODD 4.10). **Ce n'est pas une source indépendante des données** : son annotation `DISSEMINATION_SOURCE_DATASET` indique `EDAT_LFSE_14`. Il vérifie donc l'extraction du script (filtres, années, drapeaux), pas Eurostat lui-même. Pour l'indépendance, j'ai ajouté deux témoins plus anciens : le graphique de Statistics Explained (extraction avril 2026) et la page Insee (extraction Eurostat du 14/10/2025).

---

### 1. PISA 2025 : scores moyens, erreurs-types, écart à la moyenne OCDE

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| France, compréhension de l'écrit | 456.33 (3.24) | 456.33453 (S.E. 3.24423) ; arrondi 456 | OCDE, annexe Excel, tableau I.B1.2a.2 [direct] `https://stat.link/mrq53f` ; OCDE Vol. I, tableau I.1 [direct] ; note pays OCDE, graphique 3 [direct] ; NI 26.40 [direct] | Conforme |
| France, mathématiques | 457.66 (3.00) | 457.65501 (S.E. 2.99509) ; arrondi 458 | OCDE, tableau I.B1.2a.3 [direct] `https://stat.link/mrq53f` ; Vol. I tableau I.1 ; NI 26.40 | Conforme |
| France, sciences | 483.42 (3.21) | 483.42120 (S.E. 3.20594) ; arrondi 483 | OCDE, tableau I.B1.2a.1 [direct] ; Vol. I tableau I.1 ; NI 26.39 ; note pays OCDE | Conforme |
| Moyenne OCDE, lecture | 460.94 (0.45) | 460.94416 (S.E. 0.44637) ; arrondi 461 | OCDE, tableau I.B1.2a.2 [direct] ; Vol. I tableau I.1 | Conforme |
| Moyenne OCDE, mathématiques | 463.02 (0.42) | 463.02078 (S.E. 0.42482) ; arrondi 463 | OCDE, tableau I.B1.2a.3 [direct] ; Vol. I tableau I.1 | Conforme |
| Moyenne OCDE, sciences | 481.91 (0.44) | 481.90834 (S.E. 0.43835) ; arrondi 482 | OCDE, tableau I.B1.2a.1 [direct] ; Vol. I tableau I.1 | Conforme |
| Nombre de pays de la moyenne « OCDE » 2025 | 38 | 38 pays de l'OCDE et 53 partenaires (91 au total) ; figures NI libellées « OCDE - 38 » | OCDE Vol. I, résumé et figures [direct] `https://www.oecd.org/content/dam/oecd/en/publications/reports/2026/09/pisa-2025-results-volume-i_5265bfb1/73451bc5-en.pdf` ; NI 26.40 [direct] | Conforme |
| Chiffres arrondis de l'issue #32 | maths 458 (OCDE 463), lecture 456 (461), sciences 483 (482) | Identiques (Vol. I tableau I.1 : France 483 / 456 / 458 ; OCDE 482 / 461 / 463) | OCDE Vol. I, tableau I.1 [direct] | Conforme |
| France vs moyenne OCDE, lecture : écart significatif ? | non précisé | Écart −4,61. S.E. de l'écart ≈ 3,19 (corrigé du poids de la France dans la moyenne). z = −1,45, p ≈ 0,15. **Non significatif.** | [calcul] sur tableau I.B1.2a.2 ; confirmé par la cellule non colorée (France) du tableau I.1 de l'OCDE [direct] ; NI 26.40 : « dans la moyenne de l'OCDE (461) » [direct] ; note pays OCDE : « proches de la moyenne » [direct] | Conforme |
| France vs moyenne OCDE, mathématiques | non précisé | Écart −5,37. S.E. ≈ 2,95. z = −1,82, p ≈ 0,07. IC95 % de l'écart [−11,1 ; +0,4]. **Non significatif, mais à la limite.** | [calcul] sur tableau I.B1.2a.3 ; cellule non colorée du tableau I.1 [direct] ; NI 26.40 : « dans la moyenne de l'OCDE (463 points) » [direct] | Conforme (limite) |
| France vs moyenne OCDE, sciences | non précisé | Écart +1,51. S.E. ≈ 3,15. z = +0,48, p ≈ 0,63. **Non significatif.** | [calcul] sur tableau I.B1.2a.1 ; tableau I.1 ; NI 26.39 : « dans la moyenne des pays de l'OCDE (482) » [direct] | Conforme |

Notes sur le test de significativité :

- Formule utilisée : S.E.(écart)² = S.E.(France)² × (1 − 2/38) + S.E.(OCDE)², pour tenir compte du fait que la France entre dans la moyenne de 38 pays. Sans cette correction, on obtient z = −1,41 (lecture), −1,77 (maths), +0,47 (sciences) : mêmes conclusions.
- J'ai validé la méthode sur d'autres pays : mes z reproduisent la coloration du tableau I.1 de l'OCDE (par exemple Slovénie en maths, 460 : z = −2,59, cellule grisée donc « significativement inférieure » ; Hongrie en maths, 459 : z = −1,43, cellule non colorée).
- Les intervalles de confiance à 95 % de la France contiennent la moyenne OCDE dans les trois domaines : lecture [450,0 ; 462,7] contient 460,94 ; maths [451,8 ; 463,5] contient 463,02 (de très peu) ; sciences [477,1 ; 489,7] contient 481,91.
- Le tableau I.1 de l'OCDE (page 28 du Vol. I) colore la moyenne de la France comme « non significativement différente de la moyenne de l'OCDE » dans les trois domaines et en résolution informatique de problèmes (497 vs 500). Seule la part d'élèves très performants (9,8 % contre 11,9 %) est colorée « inférieure ».
- Le dossier de presse du ministère (08/09/2026) écrit : « Les élèves français restent dans la moyenne de l'OCDE en sciences et en compréhension de l'écrit. En mathématiques, leur score baisse davantage que la moyenne de l'OCDE. » Il ne dit pas « dans la moyenne » pour les maths, alors que la NI 26.40 le dit. Pas de contradiction chiffrée, seulement une formulation différente.

**Réponse à la question 1 : non, la France n'est significativement différente de la moyenne OCDE dans aucun des trois domaines** (mathématiques : p ≈ 0,07, donc proche du seuil).

---

### 2. PISA : historique France et OCDE-24

#### 2.1 Valeurs France (annexe OCDE, tableaux I.B1.2a.36 à 38 [direct], `https://stat.link/mrq53f`)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| France, lecture 2000 | 504.7 | 504.742 (S.E. 2.73) | Tableau I.B1.2a.37 [direct] ; graphique 2 de la note pays OCDE (505) [direct] | Conforme |
| France, lecture 2022 | 473.9 | 473.852 (S.E. 3.07) | Tableau I.B1.2a.37 [direct] | Conforme |
| France, lecture 2025 | 456.3 | 456.335 | Tableau I.B1.2a.37 [direct] | Conforme |
| France, maths 2003 | 510.8 | 510.799 (S.E. 2.50) | Tableau I.B1.2a.38 [direct] ; NI 26.40 figure 5 (511) [direct] | Conforme |
| France, maths 2022 | 473.9 | 473.944 (S.E. 2.49) | Tableau I.B1.2a.38 [direct] | Conforme |
| France, maths 2025 | 457.7 | 457.655 | Tableau I.B1.2a.38 [direct] | Conforme |
| France, sciences 2006 | 495.2 | 495.220 (S.E. 3.36) | Tableau I.B1.2a.36 [direct] | Conforme |
| France, sciences 2022 | 487.2 | 487.225 (S.E. 2.73) | Tableau I.B1.2a.36 [direct] | Conforme |
| France, sciences 2025 | 483.4 | 483.421 | Tableau I.B1.2a.36 [direct] | Conforme |

#### 2.2 Valeurs OCDE-24 (moyenne à périmètre constant)

La DEPP calcule une moyenne sur **24 pays** (NI 26.40, note de la figure 5 ; NI 26.39, figure 2 ; dossier de presse : « moyenne à périmètre constant de 24 pays »). L'OCDE publie, elle, une moyenne à périmètre constant sur **23 pays** (« OECD average-23 », définie page 21 du Vol. I : les 38 membres moins Autriche, Chili, Colombie, Costa Rica, Estonie, Israël, Lituanie, Luxembourg, Pays-Bas, Slovaquie, Slovénie, Espagne, Türkiye, Royaume-Uni, États-Unis). Je n'ai pas pu identifier quel pays supplémentaire la DEPP inclut.

| Élément | Valeur du fichier (OCDE-24) | OCDE average-23 (OCDE) | Écart | Source | Verdict |
|---|---|---|---|---|---|
| Lecture 2000 | 499.2 | 499.534 | +0,3 | Tableau I.B1.2a.37 [direct] ; figure I.1.5 `https://stat.link/3r8tyd` [direct] ; dossier de presse (graphique, lecture visuelle ≈ 499) [direct] | Écart expliqué (périmètre 24 contre 23) |
| Lecture 2022 | 481.9 | 481.932 | 0,0 | idem ; dossier de presse : 482 [direct] | Conforme |
| Lecture 2025 | 465.9 | 465.830 | −0,1 | idem ; dossier de presse : 466 [direct] | Conforme |
| Maths 2003 | 502.3 | 502.125 | −0,2 | Tableau I.B1.2a.38 [direct] ; NI 26.40 : « 502 points pour la moyenne de l'OCDE » [direct] | Conforme |
| Maths 2022 | 480.6 | 480.290 | −0,3 | idem ; dossier de presse : 481 [direct] | Écart expliqué (périmètre) |
| Maths 2025 | 469.7 | 469.383 | −0,3 | idem ; dossier de presse : 470 [direct] | Écart expliqué (périmètre) |
| Sciences 2006 | 503.1 | 502.744 | −0,4 | Tableau I.B1.2a.36 [direct] | Écart expliqué (périmètre) |
| Sciences 2022 | 490.9 | 490.864 | 0,0 | idem ; dossier de presse : 491 [direct] | Conforme |
| Sciences 2025 | 486.4 | 485.936 | −0,5 | idem ; dossier de presse : 486 [direct] | Écart expliqué (périmètre) |

Aucun écart ne dépasse 0,5 point, et tous les arrondis à l'unité coïncident avec le dossier de presse du ministère (`https://www.education.gouv.fr/sites/default/files/document/pisa-2025-une-baisse-des-r-sultats-commune-l-ocde-un-rel-vement-poursuivre-520338.pdf`, créé le 08/09/2026). Les valeurs du fichier sont donc cohérentes avec le calcul de la DEPP ; la différence avec l'OCDE tient au nombre de pays.

#### 2.3 Baisses depuis 2022, chiffre clé, cycle

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Baisse en lecture 2022-2025 | −18 | −17,52 (S.E. 4,60), **significative** ; −18 dans Vol. I tableau I.1 (en gras) et NI 26.40 | Tableau I.B1.2a.37 [direct] ; NI 26.40 [direct] | Conforme |
| Baisse en maths 2022-2025 | −16 | −16,29 (S.E. 4,08), **significative** ; −16 dans le tableau I.1 (en gras), NI 26.40, dossier de presse | Tableau I.B1.2a.38 [direct] | Conforme |
| Baisse en sciences 2022-2025 | −4 | −3,80 (S.E. 5,24), **non significative** (z = −0,73) ; tableau I.1 : −4 non en gras ; DEPP : « résultats stables » (NI 26.39) ; dossier de presse : « quasi stable » ; note pays OCDE : « à peu près équivalents à ceux de 2022 en sciences » | Tableau I.B1.2a.36 [direct] ; NI 26.39 [direct] ; note pays [direct] | Écart expliqué : chiffre exact, mais ce n'est pas une baisse statistiquement établie |
| Chiffre clé : « 458 points en maths, −16 points sur 2022 » | 458 ; −16 | 458 (457,66) ; −16 (−16,29). Pour mémoire, la moyenne OCDE baisse de 9 points (OECD average-35 et NI 26.40) | Vol. I tableau I.1 ; NI 26.40 ; dossier de presse | Conforme |
| Rang | non fourni | Sciences −1 place, lecture +1 place, maths −8 places (par rapport à 2022) | Dossier de presse, p. 5 [direct] | Information utile (non utilisée) |
| Cycle de 4 ans | « le cycle passe à 4 ans » | Oui. NCES (US Department of Education) : « Since 2000, PISA has been conducted every three years and will move to a four-year cycle starting after 2025. » PISA 2029 est le 10e cycle, domaine majeur : lecture, domaine innovant : culture médiatique et IA. | NCES `https://nces.ed.gov/surveys/pisa/` [direct] ; ACER, 01/04/2026 `https://www.acer.org/news/article/acer-to-deliver-pisa-2029-with-novel-focus-on-ai-and-media-literacy` [direct] ; document OCDE « PISA 2029 – Working with the International Contractors » [direct] ; document de consultation OCDE « PISA 2029 Preliminary technical information for potential bidders » : « From PISA 2029 onwards, PISA will become a four year-cycle » **[moteur uniquement : `search.oecd.org` est bloqué dans cette session]** | Conforme (le « 4 ans » est solide via NCES) |
| Prochaine édition : « 2029 » | « next 2029 » | **2029 est l'année de passation, pas de publication.** Brochure OCDE « PISA 2029 » : 2028 pré-test, **2029 collecte de la passation principale, 2030 analyse, rapport et publication des résultats**. Précédent : PISA 2025 passé en 2025, résultats publiés le 08/09/2026. | Brochure OCDE `https://www.naer.edu.tw/upload/1/14/doc/5466/附件1-PISA2029Brochure.pdf` (timeline, copyright OCDE 2025, « Restricted Use ») [direct] ; ACER `https://www.acer.org/au/pisa` (Vol. I publié le 08/09/2026) [direct] | **Écart** (voir note PISA 4 ci-dessous) |
| Vocabulaire des notes DEPP | — | Les NI 26.39 et 26.40 et le dossier de presse écrivent encore « Tous les trois ans depuis 2000 » ; le Vol. I OCDE (avant-propos) écrit « Now every three years ». C'est la description du passé, pas une contradiction. | NI 26.40, NI 26.39, Vol. I p. 3 [direct] | Information |

Points d'attention PISA :

- La moyenne OCDE-24 de 2025 est plus haute que la moyenne OCDE-38 de la table 2025 : lecture 465,9 contre 460,9 (+5,0), maths 469,7 contre 463,0 (+6,7), sciences 486,4 contre 481,9 (+4,5). Un joueur qui compare 463 (maths, table) et 469,7 (maths, historique) verra deux « moyennes OCDE » différentes. La note PISA 3 est donc utile et mérite d'être précise.
- La NI 26.40 mesure les évolutions « 2022-2025 » avec une moyenne « OCDE-37 » (figure 2, moyenne de 37 pays) et l'OCDE avec « OECD average-35 » ; les deux donnent −14 (lecture) et −9 (maths) pour l'OCDE.
- Données de qualité : la note pays de l'OCDE précise que « En France, toutes les données ont respecté les normes de qualité fixées par le PISA et ont été validées pour publication » [direct]. (Un résumé de moteur de recherche affirmait le contraire : il est faux.)

---

### 3. Sortants précoces (Eurostat, 18-24 ans) : France et UE27_2020

Source des valeurs trouvées : API Eurostat, jeu `sdg_04_10`, `updated: 2026-10-30T23:00:00+0100`, requête `geo=FR&geo=EU27_2020&sex=T` [direct], `https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/sdg_04_10?format=JSON&lang=en&geo=FR&geo=EU27_2020&sex=T`. **Rappel : jeu dérivé de `edat_lfse_14`.**

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| France 2025 | 7.2 % (d) | 7.2 %, drapeau `d` | API `sdg_04_10` [direct] | Conforme à Eurostat au 30/10/2026 |
| France 2024 | 7.9 % (b, d) | 7.9 %, drapeau `bd` | API `sdg_04_10` [direct] | Conforme à Eurostat au 30/10/2026. **Écart expliqué** avec la page Insee (7,7 %, extraction 14/10/2025) : révision |
| France 2013 | 9.7 % (b) | 9.7 %, drapeau `b` | API `sdg_04_10` [direct] ; Insee, fichier xlsx 9,7 [direct] | Conforme |
| France 2006 | 12.7 % | 12.7 %, sans drapeau | API `sdg_04_10` [direct] ; Insee xlsx 12,7 [direct] | Conforme |
| UE 2025 | 9.1 % | 9.1 %, sans drapeau | API `sdg_04_10` [direct] ; Eurostat Statistics Explained (extraction avril 2026) 9,1 [direct] ; Euronews 16/06/2026 [direct] | Conforme |
| UE 2024 | 9.6 % | 9.6 %, sans drapeau | API `sdg_04_10` [direct] | Conforme à Eurostat au 30/10/2026. **Écart expliqué** avec la page Insee (9,4 %, extraction du 14/10/2025) : révision |
| UE 2006 | 15.2 % (b) | 15.2 %, drapeau `b` | API `sdg_04_10` [direct] ; Insee xlsx 15,2 [direct] | Conforme |
| Ruptures de série France (b) | 2013, 2014, 2021, 2024 | `b` en 2013, 2014, 2021 (`bd`), 2024 (`bd`) ; **et aussi 2003** (hors fenêtre du fichier si la série commence en 2006) | API `sdg_04_10` [direct] | Conforme (2003 absent du fichier, donc à ignorer ou à signaler selon la fenêtre) |
| Ruptures de série UE (b) | 2006, 2014, 2021 | `b` en 2003, 2006, 2014, 2021 | API `sdg_04_10` [direct] | Conforme (même remarque pour 2003) |
| Drapeau `d` France | « depuis 2021 » | `d` ou `bd` pour 2021, 2022, 2023, 2024, 2025 (et pas avant) | API `sdg_04_10` [direct] | Conforme |
| Signification de `d` | à expliquer | Étiquette officielle Eurostat : « definition differs (see metadata) » ; en français « définition différente (voir métadonnées) » ; `bd` = « break in time series, definition differs (see metadata) ». **Je n'ai trouvé aucune explication publiée de la différence de définition propre à la France** (voir 3.1). | API `sdg_04_10`, bloc `extension.status.label` (EN et FR) [direct] | Non trouvé (la cause exacte) |
| Date de mise à jour | 30/10/2026 | `updated` et `DISSEMINATION_TIMESTAMP_DATA` : 2026-10-30 à 23:00 (UTC+1) | API `sdg_04_10` [direct] | Conforme |
| France 2025, témoin plus ancien | — | **7,0 %** (extraction avril 2026, UE 9,1 %) | Eurostat Statistics Explained, « Early leavers from education and training », données du graphique 2025 `https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Early_leavers_from_education_and_training` [direct] | **Écart expliqué (révision de 7,0 à 7,2 entre avril et octobre 2026)** |

#### 3.1 Comparaison avec la page Insee 2407835

Page : `https://www.insee.fr/fr/statistiques/2407835` [direct], « Sortants précoces et diplômés du supérieur dans l'Union européenne », **paru le 24/10/2025**, « Données annuelles de 2006 à 2024 », source « Eurostat (extraction du 14 octobre 2025), EU-LFS » ; fichier `https://www.insee.fr/fr/statistiques/fichier/2407835/cond-educ-sortie-precoce-dip-ue.xlsx` [direct].

- France : 2006 = 12,7 ; 2013 = 9,7 ; 2014 = 8,8 ; 2021 = 7,8 ; 2022 = 7,6 ; 2023 = 7,6. **Tous identiques** aux valeurs Eurostat du 30/10/2026. **2024 = 7,7** contre 7,9 aujourd'hui.
- UE : 2006 = 15,2 ; 2013 = 11,8 ; 2014 = 11,1 ; 2021 = 9,7 ; 2022 = 9,6 ; 2023 = 9,6. **Identiques.** **2024 = 9,4** contre 9,6 aujourd'hui.
- La page Insee ne contient pas 2025 (elle n'a pas été mise à jour) et ne porte aucun drapeau.
- Conclusion : l'écart est une **révision Eurostat de +0,2 point pour 2024 (France et UE)**, plus une révision de +0,2 pour la France en 2025 (7,0 en avril 2026, 7,2 en octobre 2026). Je n'ai trouvé aucune source qui explique ces révisions. L'apparition du drapeau `b` sur 2024 pour la France laisse penser à un changement méthodologique, mais c'est une hypothèse.
- Définition Insee : « part des sortants précoces (diplômés au plus du brevet qui ne suivent aucune formation) au sein des 18-24 ans » [direct]. Même concept qu'Eurostat.

#### 3.2 Ce que disent les sources sur les ruptures

- **UE 2014** : passage à la CITE 2011 (séries jusqu'en 2013 en CITE 1997). Métadonnées Eurostat `sdg_04_10_esmsip2` [direct].
- **UE 2021 (tous les pays)** : entrée en vigueur du règlement (UE) 2019/1700 (IESS). Métadonnées `sdg_04_10_esmsip2` [direct].
- **France 2013 et 2014** : refonte du questionnaire de l'enquête Emploi en 2013 (questions sur la formation non formelle étoffées, de une à quatre questions ; meilleure mesure du diplôme), puis passage du champ « France métropolitaine » à « France hors Mayotte » à partir de 2014 (quatre DOM ajoutés). Sources : DEPP, document de travail 2019-M01 [direct] `https://www.education.gouv.fr/sites/default/files/document/Am%C3%A9lioration%20des%20estimations%20de%20la%20part%20de%2018-24%20ans%20peu%20dipl%C3%B4m%C3%A9s%20et%20hors%20formation%20et%20du%20flux%20de%20sortants%20de%20formation%20initiale%20sans%20dipl%C3%B4me,%20%C3%A0%20partir%20de%20l%E2%80%99enqu%C3%AAte%20Emploi-270177.pdf` ; Insee, fiche F6 « Formations et emploi » 2025 [direct] `https://www.insee.fr/fr/statistiques/fichier/8305510/BFE2025-F6.pdf`.
- **France 2021** : refonte de l'enquête Emploi pour se conformer au règlement IESS (DEPP 2019 : « En 2021, le questionnaire de l'enquête Emploi sera à nouveau remanié ») [direct].
- **France 2003** : rupture indiquée dans le graphique d'Inégalités.fr, série du ministère de l'Éducation (« Rupture de série en 2003 ») [direct]. Eurostat la signale aussi (`b` en 2003 pour la France et l'UE).
- **France 2024** : cause non documentée dans les sources consultées.
- **Drapeau `d` depuis 2021** : cause non documentée (voir ci-dessus). Les métadonnées `edat1_esms` et `lfsa_esms` d'Eurostat [direct] ne mentionnent pas la France à ce sujet.

---

### 4. Dépense intérieure d'éducation (DIE), France

Source principale : NI 26.42, `https://www.education.gouv.fr/sites/default/files/document/educationnationaledepp-ni-2026-42pdf-520993.pdf` [direct, PDF de 4 pages].

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| DIE 2025, provisoire | 199,2 Md€ | « estimée à titre provisoire à 199,2 milliards d'euros » | NI 26.42 p. 2 [direct] ; Banque des Territoires/Localtis [direct] | Conforme |
| DIE 2025, euros constants 2025 | 199,17 Md€ | 199 172 M€ (figure 3) | NI 26.42, figure 3 [direct] | Conforme |
| Part du PIB 2025 | 6,7 % (6,66) | « 6,7 % en 2025, une part stable par rapport à 2024 ». Décimale non publiée dans la note. Contrôle [calcul] : 199,172 / 2 991,1 (PIB 2025, Insee, paru le 29/05/2026) = 6,659 % | NI 26.42 [direct] ; Insee `https://www.insee.fr/fr/statistiques/8988793` [direct] | Conforme (6,66 recoupé par calcul) |
| DIE 2024, euros 2025 | 198,9 Md€ | 198 900 M€ (figure 3) | NI 26.42, figure 3 [direct] | Conforme |
| Part du PIB 2024 | 6,70 % | La note dit « stable » et précise que 2024 a été « légèrement révisé à la baisse (moins de 0,1 point) dans les comptes définitifs 2024 ». Contrôle [calcul] : 198,9 / 1,011 = 196,74 Md€ courants ; PIB 2024 = 2 991,1 / 1,019 = 2 935,3 Md€ (Insee : +1,9 % en valeur) ; ratio 6,70 % | NI 26.42 [direct] ; Insee [direct] | Conforme (recoupé par calcul) |
| 1980, euros constants | 91,0 Md€ | « de 91,0 milliards d'euros en 1980 à 199,2 milliards d'euros en 2025 » (en euros constants). RERS 2026 : 90 005 M€ aux prix 2024, ce qui donne 91,0 aux prix 2025 (déflateur 2025 : +1,1 %) | NI 26.42 p. 2 [direct] ; RERS 2026, chap. 10 [direct] | Conforme. **À préciser : euros constants 2025**, pas courants (29,4 Md€ courants en 1980) |
| Part du PIB 1980 | 6,58 % | RERS 2026, tableau 10.01 : **6,6 %** pour 1980 (arrondi). La décimale 6,58 n'est publiée ni dans la note ni dans le chapitre. | RERS 2026, chap. 10 [direct] `https://www.education.gouv.fr/sites/default/files/document/10-budget-couts-et-financementpdf-519303.pdf` | Conforme à l'arrondi, décimale non vérifiable |
| Hausse en euros courants | +2,4 Md€ (+1,2 %) | « hausse de 2,4 milliards d'euros par rapport à 2024 en euros courants (+ 1,2 %) » | NI 26.42 p. 1 [direct] ; Localtis [direct] | Conforme |
| Hausse en euros constants | +0,3 Md€ (+0,1 %) | « ramenée à 0,3 milliard en euros constants, soit + 0,1 % » (199 172 − 198 900 = 272 M€) | NI 26.42 p. 1 et 2 [direct] | Conforme |
| DIE 2024 dans une autre publication | non fourni | RERS 2026 chap. 10 (publié le 27/07/2026) : **197,1 Md€ en 2024 provisoire, 6,8 % du PIB**. Même chiffre dans Insee « France, portrait social » (paru le 18/11/2025). | RERS 2026 [direct] ; Insee `https://www.insee.fr/fr/statistiques/8612572` [direct] | **Écart expliqué** : provisoire de 2025 remplacé par les comptes définitifs 2024 dans la NI 26.42 (≈ 196,7 Md€ courants, 6,70 %) |
| Banque des Territoires (recoupement) | — | 199,2 Md€ « un record » ; +2,4 Md€ (+1,2 %) ; 6,7 % stable ; État 55 % ; collectivités 23 % (communes 57 %, régions 27 %, départements 16 % de cette part) | `https://www.banquedesterritoires.fr/depenses-deducation-la-france-flirte-avec-les-200-milliards-deuros-en-2025` [direct] | Conforme |
| Anomalie dans le PDF de la NI 26.42 | — | **La métadonnée « Title » du PDF dit « En 2025, 199,2 milliards d'euros consacrés à l'éducation, soit 6,4 % du PIB »**, alors que le corps du texte, la citation (« soit 6,7% du PIB ») et la page web disent 6,7 %. | Métadonnées PDF (`pdfinfo`) [direct] | **Écart** (sans conséquence sauf si un script lit le titre du PDF) |

Répartition du financement 2025 (NI 26.42, figure 2 [direct]) : État 55,3 %, collectivités territoriales 22,9 % (communes 13,1, départements 3,6, régions 6,1), autres administrations publiques 3,6 %, ménages 7,9 %, entreprises 10,4 %. Ce sont des parts du **financement initial**.

RERS 2026 [direct] : en 2024, l'État assure 55,2 % du financement initial et **53,1 % du financement final** (après transfert des bourses aux ménages) ; collectivités 23,0 % et 22,9 %.

---

### 5. Dates et licences

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Date des notes DEPP | « Septembre 2026 » | NI 26.39, 26.40 et 26.42 portent « Septembre 2026 » en en-tête et en pied | PDF des notes [direct] | Conforme |
| Publication des notes PISA | 08/09/2026 | PISA 2025 Vol. I « Released 8 September 2026 » (ACER) ; Wikipédia : « released on 8 September 2026 » ; presse (Euronews FR 08/09/2026, Digischool). Le dossier de presse du ministère est créé le 08/09/2026 à 07:53 UTC. | `https://www.acer.org/au/pisa` [direct] ; `https://en.wikipedia.org/wiki/Programme_for_International_Student_Assessment` [direct] ; PDF dossier de presse [direct] | Conforme. La page web de la DEPP (403) n'a pas pu être lue |
| Date des fichiers PISA | 04/09/2026 | NI 26.40 : `Last-Modified` 04/09/2026 11:40 GMT, créé le 03/09, modifié le 04/09. NI 26.39 : créé et modifié les 03 et 04/09. La note pays OCDE : `Last-Modified` 07/09/2026 09:47 GMT. | en-têtes HTTP et `pdfinfo` [direct] | Conforme (le fichier précède la publication de quatre jours : embargo) |
| Date de publication de la NI 26.42 | fichier du 23/09/2026 | Fichier : créé le 23/09/2026 08:37 UTC, modifié 14:54 UTC, `Last-Modified` 23/09/2026 14:55 GMT. **Banque des Territoires/Localtis (article du 29/09/2026) écrit : « note de la Depp publiée le 29 septembre 2026 ».** Je n'ai pas pu confirmer sur le site du ministère (403). | PDF [direct] ; `https://www.banquedesterritoires.fr/depenses-deducation-la-france-flirte-avec-les-200-milliards-deuros-en-2025` [direct] | **Écart expliqué** : mise en ligne technique le 23/09, publication probable **le 29/09/2026** (une seule source de presse). Pour le kit, « Septembre 2026 » reste exact et prudent |
| Licence des publications DEPP | « Licence Ouverte ? » | Les trois PDF ne portent **aucune mention de licence** [direct, recherche dans le texte]. Le site du ministère indique « Sauf mention contraire, tous les contenus de ce site sont sous licence etalab-2.0 » (Licence Ouverte 2.0). **[moteur uniquement : la page `education.gouv.fr/bulletin-officiel` répond 403 ; le résumé cite la phrase.]** Conditions de la Licence Ouverte 2.0 lues en direct : réutilisation libre, y compris commerciale ; obligation de mentionner la source (a minima le nom du concédant) et la date de dernière mise à jour ; pas d'impression de caution de l'administration. | `https://www.data.gouv.fr/pages/legal/licences/etalab-2.0` [direct] | Conforme avec réserve (statut Etalab 2.0 : [moteur] seulement) |
| Licence des données Eurostat | réutilisation avec « Source : Eurostat » | Avis de copyright Eurostat : « Reuse of statistical data, metadata, publications, and other dissemination tools published on this website for commercial or non-commercial purposes is authorised provided the source is acknowledged. » Exceptions : données d'autres sources (non commerciales seulement), logos. Si on modifie les données, il faut l'indiquer et ajouter une clause de non-responsabilité d'Eurostat. Base : décision du 12/12/2011 (2011/833/UE). | `https://ec.europa.eu/eurostat/help/copyright-notice` [direct] | Conforme |
| Licence des données OCDE-PISA (non demandée) | — | Publications PISA 2025 sous CC BY 4.0 (« Attribution – you must cite the work » ; une adaptation doit être signalée comme telle). | Vol. I et note pays OCDE, pages de copyright [direct] | Information |

---

### 6. Versions anglaises

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Notes DEPP en anglais | aucune attendue | Aucune trouvée. Les PDF sont entièrement en français, sans résumé anglais [direct]. La recherche n'a renvoyé aucune version anglaise [moteur]. | PDF des trois notes [direct] | Conforme (aucune) |
| Page Eurostat en anglais | `…/databrowser/view/edat_lfse_14/default/table?lang=en` | L'URL répond 200 en `lang=en` et `lang=fr`, mais c'est une coque JavaScript (≈ 8,6 ko, sans titre ni données dans le HTML). Le jeu a un titre anglais (« Early leavers from education and training by labour status ») [moteur] et l'API renvoie des libellés en EN et FR [direct]. | URL citée [direct pour le code de retour] ; API `sdg_04_10` `lang=en` et `lang=fr` [direct] | Conforme (la page existe en anglais et en français, mais elle n'est pas lisible sans navigateur) |
| Note pays OCDE en anglais | — | Existe : `https://www.oecd.org/en/publications/pisa-2025-results-volume-i-country-notes_2d4ff9ea-en/france_6d229453-en` (URL vue dans les résultats de recherche, page en 403 pour moi) [moteur]. Le Vol. I complet est en anglais [direct]. | — | Information |

---

### Les douze notes « À savoir » : vérification et corrections proposées

#### PISA

1. **« Les scores ont des marges d'erreur (erreurs-types) : un écart de quelques points peut ne pas être significatif. »** Conforme. Exemple chiffré disponible : la France est à 456 en lecture et la moyenne OCDE à 461, soit −5 points, non significatif (p ≈ 0,15). En maths, −5 points aussi, mais p ≈ 0,07 : à la limite. Texte proposé : « Chaque score est une estimation avec une marge d'erreur de l'ordre de ±6 points pour la France. Un écart de quelques points avec la moyenne de l'OCDE n'est donc pas forcément significatif. »
2. **« La baisse touche toute l'OCDE. »** À nuancer. Depuis 2022, la moyenne OCDE baisse de 14 points en lecture et de 9 en maths, mais de 3 seulement en sciences (Vol. I, tableau I.1) ; en lecture, seuls huit pays n'accusent pas de baisse, et en maths seule la Türkiye progresse (NI 26.40). En maths, la France recule plus que l'OCDE (−16 contre −9) ; en lecture aussi (−18 contre −14). Texte proposé : « Le recul touche presque tous les pays de l'OCDE en lecture et en mathématiques. En sciences, il est faible et la France est stable. »
3. **« La moyenne OCDE diffère entre le tableau 2025 (38 pays) et l'historique (24 pays présents à chaque cycle depuis 2000). »** Conforme, à préciser : « 24 pays » est le calcul de la DEPP (l'OCDE publie une moyenne comparable sur 23 pays, à moins d'un demi-point près). Les deux moyennes de 2025 ne sont pas comparables entre elles : 463 contre 469,7 en maths, 461 contre 465,9 en lecture, 482 contre 486,4 en sciences.
4. **« Le cycle passe à 4 ans : prochains résultats en 2029 ; l'axe du graphique ne part pas de 0. »** **À corriger : les prochains résultats ne seront pas publiés en 2029.** PISA 2029 sera *passé* en 2029 (lecture en domaine majeur) et ses résultats sont prévus en **2030** (brochure OCDE, calendrier). Texte proposé : « Le cycle passe à 4 ans : la prochaine enquête (PISA 2029) sera passée en 2029, ses résultats sont attendus en 2030. » La mention sur l'axe qui ne part pas de 0 est une remarque de présentation que ces sources ne contredisent pas.

#### Sortants précoces

1. **Définition.** Conforme. Eurostat : personnes de 18 à 24 ans dont le diplôme le plus élevé est au plus de niveau collège (CITE 2011 niveaux 0 à 2) et qui n'ont suivi aucun enseignement ni formation (formelle ou non formelle) au cours des quatre semaines précédant l'enquête. Insee : « diplômés au plus du brevet qui ne suivent aucune formation ». Une formation non formelle (stage, cours particulier, sport ou loisir encadré) compte comme « en formation ».
2. **Ruptures de série en 2013, 2014, 2021 et 2024 pour la France.** Conforme aux drapeaux `b` (plus 2003, hors fenêtre). Causes documentées : 2013 et 2014 (refonte du questionnaire de l'enquête Emploi, puis extension à quatre DOM, source DEPP/Insee), 2021 (refonte liée au règlement européen IESS, rupture pour tous les pays). **2024 : cause non documentée dans les sources trouvées** ; le texte ne doit donc pas en donner la raison.
3. **« Depuis 2021, la France suit une définition différente de celle de l'UE (drapeau d). »** Non vérifiable dans le détail. Eurostat indique seulement « definition differs (see metadata) ». Je n'ai trouvé aucune source qui dise en quoi. Texte proposé, prudent : « Eurostat signale depuis 2021 que la définition appliquée à la France diffère légèrement de la définition européenne standard (indicateur « d »). La comparaison avec les autres pays reste utile, mais approximative. » Ne pas avancer d'explication (période de quatre semaines, questionnaire, etc.) sans source.
4. **« La source est l'enquête Emploi (un échantillon). »** Conforme (Eurostat : enquête européenne sur les forces de travail ; moyennes annuelles de données trimestrielles). À ajouter : **les valeurs sont révisées**. La France 2024 est passée de 7,7 % (octobre 2025) à 7,9 % (octobre 2026) ; la France 2025 de 7,0 % (avril 2026) à 7,2 % (octobre 2026) ; l'UE 2024 de 9,4 % à 9,6 %. L'enquête interroge des ménages ordinaires (les personnes vivant en communauté ne sont pas interrogées, DEPP 2019).

#### Dépense intérieure d'éducation

1. **« Définition de la DIE (tous les agents économiques, France, métropole et DOM). »** Largement conforme. Insee : « l'ensemble des agents économiques, administrations publiques centrales et locales, entreprises et ménages », dépenses « sur le territoire national » [direct]. Les sources écrivent « Champ : France » [direct]. La formule « métropole et DOM » vient de l'ancienne rédaction de la DEPP **[moteur uniquement]** ; les éditions récentes écrivent « France ». Texte proposé : « Elle additionne les dépenses de tous les acteurs (État, collectivités, entreprises, ménages) pour l'éducation en France. »
2. **« 2025 est provisoire. »** Conforme (« estimée à titre provisoire »). À ajouter : 2024 a lui-même été révisé (197,1 Md€ provisoires, 6,8 % du PIB, remplacés par les comptes définitifs : 198,9 Md€ aux prix 2025, 6,7 %).
3. **« Euros constants de 2025. »** Conforme. Les euros constants sont obtenus avec le prix du PIB (+1,1 % en 2025), déflateur international (collecte UOE).
4. **« L'État finance environ 55 %, les collectivités 23 %. »** Conforme, mais **en financement initial** (55,3 % et 22,9 % en 2025). En financement final (après transfert des bourses aux ménages), l'État assure 53,1 % en 2024 (RERS 2026). Texte proposé : « L'État finance environ 55 % de la dépense, les collectivités territoriales environ 23 % (financement initial). »

---

### Conclusion : écarts d'abord

#### Écarts à traiter

1. **Note PISA 4 : « prochains résultats en 2029 » est inexact.** 2029 est l'année de passation ; les résultats sont prévus en 2030 (brochure OCDE, calendrier). Le passage à un cycle de 4 ans est confirmé (NCES ; document OCDE de consultation [moteur seulement]).
2. **PDF de la NI 26.42 : métadonnée « Title » à 6,4 % du PIB**, contre 6,7 % partout ailleurs (corps du texte, citation, titre de la page web). À ignorer, mais à ne pas utiliser comme source de titre.
3. **Sciences −4 points depuis 2022 : chiffre exact, mais non significatif** (−3,80, S.E. 5,24). DEPP, dossier de presse et OCDE parlent de stabilité. À ne pas présenter comme une baisse. À l'inverse, −18 (lecture) et −16 (maths) sont significatifs.
4. **Note PISA 2 : « la baisse touche toute l'OCDE » à nuancer** (−14 lecture, −9 maths, −3 sciences ; seule la Türkiye progresse en maths).
5. **Sortants précoces : révisions Eurostat.** France 2024 : 7,9 % aujourd'hui contre 7,7 % sur la page Insee citée. UE 2024 : 9,6 % contre 9,4 %. France 2025 : 7,2 % contre 7,0 % en avril 2026. Les valeurs du fichier sont **conformes à Eurostat au 30/10/2026**, mais ne coïncident pas avec la page Insee de comparaison, qui date d'octobre 2025. Il faut l'indiquer si le kit renvoie à cette page.
6. **Drapeau `d` : explication non trouvée.** La note 3 des sortants précoces ne doit pas inventer de cause.
7. **Date de publication de la NI 26.42 : 29/09/2026 (presse) contre 23/09/2026 (fichier).** Une seule source de presse. « Septembre 2026 » est sûr.

#### Écarts expliqués

- OCDE-24 (DEPP) contre OECD average-23 (OCDE) : au plus 0,5 point ; tous les arrondis concordent avec le dossier de presse du ministère.
- DIE 2024 : 197,1 Md€ / 6,8 % (RERS 2026, provisoire) contre 198,9 Md€ aux prix 2025 / 6,7 % (NI 26.42, comptes définitifs). Le 1980 à 91,0 Md€ est en euros constants 2025.
- Rupture 2003 présente chez Eurostat pour la France et l'UE, absente du fichier (hors fenêtre).

#### Non vérifié ou limité

- Erreurs-types, OECD average et valeurs décimales PISA : **vérifiées** dans l'annexe Excel de l'OCDE.
- DIE 1980 à 6,58 % : seul l'arrondi 6,6 % est publié. 6,66 % (2025) et 6,70 % (2024) : recoupés par calcul avec le PIB Insee, pas publiés par la DEPP.
- Licence Etalab 2.0 du site du ministère : [moteur] seulement.
- Mention « métropole et DOM » : [moteur] seulement.
- Pages HTML d'education.gouv.fr, d'eduscol et d'oecd.org : 403. `search.oecd.org` : hôte non autorisé dans cette session. À autoriser si l'on veut lire directement le document de consultation PISA 2029.
- Erreurs relevées dans des résumés de moteur de recherche (à ne pas reprendre) : un résumé affirmait que les normes d'échantillonnage n'étaient pas respectées pour la France (faux, la note pays dit le contraire) ; un autre présentait la France « sous la moyenne » en lecture et en maths (les écarts ne sont pas significatifs) ; un titre de presse parlait d'une « hausse » des sortants précoces de l'UE à 9,1 % (le chiffre baisse par rapport à 9,6 %).

---

### URL consultées (2026-11-02)

Lues en direct :

- `https://www.education.gouv.fr/sites/default/files/document/depp-ni-2026-40pisa-mathspdf-520231.pdf`
- `https://www.education.gouv.fr/sites/default/files/document/depp-ni-2026-39pisa-sciencespdf-520225.pdf`
- `https://www.education.gouv.fr/sites/default/files/document/educationnationaledepp-ni-2026-42pdf-520993.pdf`
- `https://www.education.gouv.fr/sites/default/files/document/pisa-2025-une-baisse-des-r-sultats-commune-l-ocde-un-rel-vement-poursuivre-520338.pdf`
- `https://www.oecd.org/content/dam/oecd/fr/publications/reports/2026/09/pisa-2025-results-volume-i-country-notes_88d1164e/france_69779694/9840dc6b-fr.pdf`
- `https://www.oecd.org/content/dam/oecd/en/publications/reports/2026/09/pisa-2025-results-volume-i_5265bfb1/73451bc5-en.pdf`
- `https://stat.link/mrq53f` (annexe B1, chapitre 2, tableaux I.B1.2a.1 à 50 ; OCDE)
- `https://stat.link/3r8tyd` (données du chapitre 1, figure I.1.5 ; OCDE)
- `https://stat.link/xgs41b` (chapitre 2 ; téléchargé, non exploité)
- `https://www.oecd.org/content/dam/oecd/en/about/programmes/edu/pisa/pisa-database/survey-implementation-tools/pisa-2029/PISA_2029_Working_with_the_International_Contractors_(Public_version).pdf`
- `https://www.naer.edu.tw/upload/1/14/doc/5466/附件1-PISA2029Brochure.pdf` (brochure OCDE PISA 2029)
- `https://www.acer.org/news/article/acer-to-deliver-pisa-2029-with-novel-focus-on-ai-and-media-literacy`
- `https://www.acer.org/au/pisa`
- `https://nces.ed.gov/surveys/pisa/`
- `https://en.wikipedia.org/wiki/Programme_for_International_Student_Assessment`
- `https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/sdg_04_10?format=JSON&lang=en&geo=FR&geo=EU27_2020&sex=T` (et `lang=fr`)
- `https://ec.europa.eu/eurostat/cache/metadata/en/sdg_04_10_esmsip2.htm`, `.../edat1_esms.htm`, `.../lfsa_esms.htm`
- `https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Early_leavers_from_education_and_training`
- `https://ec.europa.eu/eurostat/statistics-explained/SEPDF/cache/94764.pdf`
- `https://ec.europa.eu/eurostat/databrowser/view/edat_lfse_14/default/table?lang=en` (et `lang=fr`) : coque JavaScript, code de retour seulement
- `https://ec.europa.eu/eurostat/help/copyright-notice`
- `https://www.insee.fr/fr/statistiques/2407835` et `https://www.insee.fr/fr/statistiques/fichier/2407835/cond-educ-sortie-precoce-dip-ue.xlsx`
- `https://www.insee.fr/fr/statistiques/8305510` et `https://www.insee.fr/fr/statistiques/fichier/8305510/BFE2025-F6.pdf`
- `https://www.insee.fr/fr/statistiques/8612572`
- `https://www.insee.fr/fr/metadonnees/definition/c2093`
- `https://www.insee.fr/fr/statistiques/8988793`
- `https://www.education.gouv.fr/sites/default/files/document/10-budget-couts-et-financementpdf-519303.pdf` (RERS 2026, chapitre 10)
- `https://www.education.gouv.fr/sites/default/files/document/Am%C3%A9lioration%20des%20estimations%20...-270177.pdf` (DEPP, document de travail 2019-M01)
- `https://www.banquedesterritoires.fr/depenses-deducation-la-france-flirte-avec-les-200-milliards-deuros-en-2025`
- `https://www.data.gouv.fr/pages/legal/licences/etalab-2.0`
- `https://www.euronews.com/my-europe/2026/06/16/education-where-in-the-eu-has-the-most-early-school-dropouts`, `https://fr.euronews.com/my-europe/2026/06/16/le-decrochage-scolaire-en-baisse-en-europe`
- `https://www.brusselstimes.com/2222484/early-school-leavers-in-the-eu-rise-to-9-1-amid-struggles`
- `https://www.inegalites.fr/De-moins-en-moins-de-jeunes-sans-diplome`

Inaccessibles (403, hôte bloqué ou coque JavaScript), valeurs éventuelles [moteur] :

- Pages HTML `education.gouv.fr/depp/...` (NI 26.39, 26.40, 26.42, calendrier des publications, `bulletin-officiel`, mentions légales), `eduscol.education.gouv.fr`, `data.education.gouv.fr`.
- Pages HTML `oecd.org` (communiqué de presse, rapport complet, page pays), `search.oecd.org` (hôte non autorisé).
- `https://ec.europa.eu/eurostat/about-us/policies/copyright` (404 ; remplacée par `/help/copyright-notice`).

Recherches web (résumés de moteur, utilisées comme pistes, jamais comme preuve sauf mention) : PISA 2025 moyennes et cycle de 4 ans ; sortants précoces 2025 ; licence Etalab du site du ministère ; définition DIE « métropole et DOM » ; publication de la NI 26.42 ; version anglaise des NI.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
