# `urbanRural` · Urbain et rural

**Vérifiée le 02/11/2026** : double vérification sur le web, sans écart sur les chiffres (section « Double vérification ») ; les « À savoir » reformulés d'après elle (ce qui a changé en 2020 et en 2025, Mayotte, l'affirmation sur l'absence de total national).

| Champ | Valeur |
| --- | --- |
| Indicateur | `urbanRural`, dossier « Électorat » (`electorate`), page de type carte, ticket #23 de l'app (statut `planned` : les chiffres et la fiche avant la page) |
| Données | `briefings/data/urbanRural.json`, écrit par `yarn briefings urbanRural` le 2026-11-02 |
| Sources | Insee, « La grille de densité 2025 », https://www.insee.fr/fr/information/8571524 (en français seulement ; la définition a une page anglaise : https://www.insee.fr/en/metadonnees/definition/c2343), fichier `fichier_diffusion_2026.xlsx`, onglet « Maille communale », « Mise en ligne le 15/05/2026 », géographie au 01/01/2026 ; Licence Ouverte 2.0 ; la carte cite aussi « IGN, ADMIN EXPRESS COG CARTO PE » (`departments.json`) |
| Série | `ruralPopulationShare` : part de la population vivant dans une commune rurale (`DENS` = 3), 2023, 32,092 % |
| Carte | `ruralPopulationShare` des 101 départements, de Paris (0 %) à la Creuse (88,8 %) ; l'Ain à 48,2 % (le `P_RURAL` de l'onglet départemental, 52,5 %, compte les carreaux ruraux, pas les communes) |
| Valeurs par catégorie | `communesByDensity` et `populationByDensity` (3 niveaux, `DENS`), `communesByDensity7` et `populationByDensity7` (7 niveaux, `DENS7`), en nombres : 87,7 / 10,3 / 2,0 % des communes et 32,1 / 30,8 / 37,2 % de la population (rural / urbain intermédiaire / urbain dense), comme #23 les a calculés |
| Chiffre clé | 32,1 % de la population vit dans une commune rurale ; une seule grille, pas de tendance |
| Règles | Le script additionne les 34 875 communes ; il vérifie le libellé de chaque niveau et que chaque niveau à 7 postes tombe dans son niveau à 3 postes (1 → dense ; 2, 3, 4 → intermédiaire ; 5, 6, 7 → rural) ; le département se déduit du code commune (3 caractères pour les codes 97) |
| Dates | Le fichier dit « Mise en ligne le 15/05/2026 » ; la page de la grille affiche « Dernière mise à jour : 06/05/2026 » et parle encore de « géographie 2025 » : le kit garde la date du fichier, celui qu'il lit |
| Première édition | À remplir à la publication |

## « À savoir »

1. Classement selon la répartition de la population sur le territoire de la commune (définition c2343), pas sa densité moyenne ; la population municipale 2023 vaut 2017 pour Mayotte (68 350 798 = 68 094 280 pour les 100 autres départements + 256 518 à Mayotte).
2. La vérification n'a trouvé aucun total national de l'Insee pour la grille 2025 ; la note ne dit pas qu'il n'existe pas, elle dit que les parts sont additionnées commune par commune.
3. Le rural se définit par la densité depuis 2020 (décision de 2020, publiée en avril 2021) ; avant, hors unité urbaine. Sur le recensement 2018, la population rurale passe de 20,8 % (hors unité urbaine) à 32,7 % (densité), d'après la DEPP. La phrase d'abord prévue, « la grille 2025 ne se compare pas aux précédentes », était trop forte : l'Insee attribue les écarts au changement de source (recensement 2021 au lieu de Fideli 2018). Le passage de 4 niveaux à 3 + 7 date de 2022, pas de 2025.
4. Aires d'attraction des villes et unités urbaines : deux autres zonages (pages de l'Insee citées par #23).

À actualiser : à la prochaine grille de densité (elle change avec le millésime du recensement).

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans resommer le fichier de la grille. Son rapport, tel quel :

Date des vérifications : 2026-11-02. Contrôle indépendant par le web, sans relire ni resommer le fichier `fichier_diffusion_2026.xlsx` ni aucun fichier sous `/home/user`.

Modes de lecture, indiqués pour chaque source dans la liste finale :

- **[page lue]** : page ou PDF téléchargé en entier puis converti en texte, passage relu.
- **[extrait]** : réponse d'un outil de lecture qui résume la page (le texte cité vient de cette réponse, pas d'une relecture de la page entière).
- **[moteur]** : seulement un résumé de moteur de recherche, la page n'a pas pu être ouverte.
- **[calcul]** : calcul refait ici à partir de chiffres lus.

### Synthèse : écarts d'abord

| # | Point | Verdict |
|---|-------|---------|
| A | « Les niveaux sont passés de 4 (ou 6/7) à 3 et 7 » en 2025 | **Écart.** Ce passage date de la grille 2022 (4 niveaux en 2019-2020, puis 3 niveaux + 7 niveaux en 2022). La grille 2025 garde 3 + 7 niveaux. Ce qui change en 2025 : la source (recensement 2021 au lieu de Fideli 2018). Aucun « 6 niveaux » trouvé. |
| B | Note (3) : « la grille 2025 ne se compare pas aux précédentes » | **Écart de formulation.** L'Insee ne l'écrit pas : il écrit que les évolutions 2022 → 2025 « s'expliquent principalement par le changement de source et de millésime ». La vraie rupture de série documentée est celle de la définition du rural en 2020 (hors unité urbaine, puis densité). |
| C | « Mise en ligne le 15/05/2026 » | **Écart non expliqué (mineur).** La page de l'Insee affiche « Dernière mise à jour : 06/05/2026 », soit avant le 15/05/2026 ; elle n'a pas de date de mise en ligne. |
| D | `P_RURAL` départemental (Ain 52,5 %) contre part des habitants des communes rurales (Ain 48,2 %) | **Écart expliqué.** La note complémentaire de l'Insee agrège des parts de population par catégorie de carreaux (« clusters »), pas par type de commune. Les deux mesures diffèrent. |
| E | Total 68 350 798 libellé « population municipale 2023 » | **Conforme, avec une réserve.** Total = 68 094 280 (France hors Mayotte, 2023) + 256 518 (Mayotte, recensement 2017) : **Mayotte n'a pas de population 2023**. |
| F | Vocabulaire « faible densité / très faible densité » | **À nuancer.** « Peu dense / très peu dense » est le vocabulaire de l'ancienne grille à 4 niveaux (encore repris par le décret 2025-438 et le Sénat). La page 2025 de l'Insee ne parle que de « communes rurales ». |
| G | Non trouvé sur le web | Parts nationales exactes de la grille 2025 (ni Insee ni autre) ; codes numériques `DENS7` 1 à 7 ; valeur exacte Creuse 88,8 % ; page anglaise de la grille 2025 (n'existe pas). |

Tout le reste (libellés, emboîtement, définition avant 2020, mai 2025, géographie 2026, licence, 34 875 communes) est confirmé.

---

### 1. Totaux nationaux (population municipale 2023, 34 875 communes)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Nombre de communes au 1er janvier 2026 | 34 875 | 34 875, « stable » : aucune commune nouvelle créée en 2025 (loi : pas de fusion l'année précédant les municipales). Même total au 1er janvier 2025. | [S19](https://www.collectivites-locales.gouv.fr/files/files/Etudes-et-statistiques/OFGL/2026/Annexes%206%20%C3%A0%208.pdf) [page lue] | Conforme |
| Population totale | 68 350 798 | Insee, populations de référence 2023 (réf. 1er janvier 2023, limites communales au 1er janvier 2025, en vigueur au 1er janvier 2026, décret 2025-1362 du 26 décembre 2025) : somme des 100 départements = **68 094 280** (France hors Mayotte) ; + Mayotte 256 518 (recensement 2017) = **68 350 798**, exactement. La DGCL arrondit à « 68,4 millions » (France métropolitaine + DOM). | [S17](https://www.insee.fr/fr/statistiques/8680659) [extrait] + somme [calcul] ; [S17b](https://www.insee.fr/fr/statistiques/8681011) [page lue] ; [S18](https://insee.fr/fr/statistiques/3284395) [page lue] ; [S19](https://www.collectivites-locales.gouv.fr/files/files/Etudes-et-statistiques/OFGL/2026/Annexes%206%20%C3%A0%208.pdf) [page lue] | Conforme |
| Millésime de Mayotte | « PMUN23 » | L'Insee n'a pas de population 2023 pour Mayotte : « Le dernier recensement général à Mayotte a été réalisé en 2017 », nouvelles populations attendues fin 2026 (cyclone Chido). L'égalité exacte du total montre que le fichier reprend 256 518 pour Mayotte (déduction, non écrite telle quelle sur le web). | [S17b](https://www.insee.fr/fr/statistiques/8681011) [page lue] | Écart expliqué |
| Rural (DENS = 3) | 87,7 % des communes (≈ 30 585) ; 32,1 % de la population | **Aucune publication de l'Insee ou autre trouvée avec ces parts pour la grille 2025.** Ordres de grandeur d'autres millésimes : grille 2022, recensement 2018, géographie 2021 : 88,0 % des communes (30 772 sur 34 965) et 32,7 % de la population ; 2017 : 30 775 communes, 88 %, 32,8 % de la population (« un tiers ») ; grille 2022 avec populations 2021 : France hors Mayotte 32,6 %, France métropolitaine 33,2 %. | [S5](https://www.insee.fr/fr/statistiques/fichier/6686472/DT2022-18_Document_travail_Grille_de_densite.pdf) [page lue] ; [S6](https://www.insee.fr/fr/statistiques/5039991) [page lue] ; [S12](https://www.insee.fr/fr/statistiques/fichier/8259620/lm_ind_26_C10.pdf) [page lue] ; [S16](https://www.education.gouv.fr/sites/default/files/2025-04/la-d-finition-de-la-ruralit-par-l-insee-et-les-volutions-de-la-typologie-des-communes-rurales-et-urbaines-de-la-depp-pdf-avril-2025--439881.pdf) [page lue] | Non trouvé (valeur exacte) ; ordre de grandeur cohérent (−0,6 pt de population par rapport à 2022) |
| Urbain intermédiaire (DENS = 2) | 10,3 % des communes ; 30,8 % de la population | Grille 2022 (2018) : 3 417 communes, 9,8 % ; 19 636 374 habitants, 29,3 %. | [S5](https://www.insee.fr/fr/statistiques/fichier/6686472/DT2022-18_Document_travail_Grille_de_densite.pdf) [page lue] | Non trouvé (exact) ; écart de +0,5 et +1,5 pt avec 2022, plausible (autre source, autre année de population) |
| Urbain dense (DENS = 1) | 2,0 % des communes (≈ 698) ; 37,2 % de la population | Grille 2022 (2018) : 774 communes, 2,2 % ; 25 448 138 habitants, 38,0 %. Insee Focus n° 169 (2019) : « 38 % de la population française vit dans une commune densément peuplée ». | [S5](https://www.insee.fr/fr/statistiques/fichier/6686472/DT2022-18_Document_travail_Grille_de_densite.pdf) [page lue] ; [S8](https://www.insee.fr/fr/information/6439600) [page lue] | Non trouvé (exact) ; −0,8 pt avec 2022, plausible |
| Cohérence interne | 2,0 + 10,3 + 87,7 = 100,0 ; 37,2 + 30,8 + 32,1 = 100,1 | Écart d'arrondi seulement. | [calcul] | Conforme |
| « L'Insee ne publie aucun total national par commune » | — | La page de la grille 2025 ne donne aucun total national par niveau ; elle propose un fichier de compositions communales, plus les niveaux par département, bassin de vie et EPCI. Les seules parts nationales par niveau publiées par l'Insee concernent des grilles précédentes (Insee Références 2021 pour 2017 ; Insee Focus n° 169 de 2019 ; document de travail 2022-18 pour 2018). **Un seul recoupement national pour 2025** : le dossier Insee Pays de la Loire n° 16 dit que les bourgs ruraux regroupent « 32 % de la population [de la région], contre 15 % en France » : le fichier donne 15,1 %. | [S1](https://www.insee.fr/fr/information/8571524) [page lue] ; [S10](https://www.insee.fr/fr/statistiques/fichier/8887956/pa_ind_16_12.pdf) [page lue] | Conforme (absence non contredite, mais « non trouvé » ne prouve pas « n'existe pas ») |
| « Un tiers de la population vit dans une commune rurale » | — | Insee Références 2021 : « Avec un tiers de sa population vivant dans une commune rurale, la France occupe une position médiane en Europe » (33 % en 2017 ; 28 % pour l'UE à 28 en 2015 ; Pologne 45 %). | [S6](https://www.insee.fr/fr/statistiques/5039991) [page lue] | Conforme |

### 2. Les sept niveaux (DENS7)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Libellés des 7 niveaux | Grands centres urbains ; Centres urbains intermédiaires ; Petites villes ; Ceintures urbaines ; Bourgs ruraux ; Rural à habitat dispersé ; Rural à habitat très dispersé | Mêmes libellés (« grands centres urbains », « centres urbains intermédiaires », « ceintures urbaines », « petites villes », « bourgs ruraux », « rural à habitat dispersé », « rural à habitat très dispersé »). Une présentation Insee abrège « Centres intermédiaires ». | [S4](https://www.insee.fr/fr/statistiques/fichier/8571524/note_complementaire.pdf) [page lue] ; [S10](https://www.insee.fr/fr/statistiques/fichier/8887956/pa_ind_16_12.pdf) [page lue] ; [S11](https://www.senat.fr/fileadmin/cru-1759398938/Office_et_delegations/Collectivites_territoriales/Controle/2024-2025/Presentation_INSEE.pdf) [page lue] | Conforme |
| Codes 1 à 7 | 1 à 7 dans l'ordre ci-dessus | **Aucune page web ne donne les codes numériques.** Recoupements : (a) le tableau du dossier Pays de la Loire liste les 7 libellés dans l'ordre du fichier (3 = Petites villes, 4 = Ceintures urbaines) ; (b) l'ordre de la classification Eurostat de niveau 2 est le même : villes ; villes denses (= centres urbains intermédiaires) ; villes semi-denses (= petites villes) ; banlieues / périurbain (= ceintures) ; villages (= bourgs ruraux) ; rural dispersé ; rural très dispersé ; (c) les ordres de grandeur du document de travail 2022-18 (petites villes 2,6 % des communes, ceintures 5,6 %) collent aux parts du fichier pour les codes 3 (2,7 %) et 4 (5,7 %). **Attention** : les textes de l'Insee (document de travail, page 2022, note complémentaire) listent plutôt « centres urbains intermédiaires, ceintures urbaines, petites villes » : ne pas inverser 3 et 4 en recopiant ces listes. | [S10](https://www.insee.fr/fr/statistiques/fichier/8887956/pa_ind_16_12.pdf) ; [S21](https://ec.europa.eu/eurostat/statistics-explained/SEPDF/cache/108903.pdf) ; [S5](https://www.insee.fr/fr/statistiques/fichier/6686472/DT2022-18_Document_travail_Grille_de_densite.pdf) [pages lues] | Non trouvé (codes) ; recoupé (ordre) |
| Emboîtement 7 → 3 | 1 → dense ; 2, 3, 4 → intermédiaire ; 5, 6, 7 → rural | Confirmé : « les communes densément peuplées restent identiques [...] nommées grands centres urbains » ; au sein des communes de densité intermédiaire : centres urbains intermédiaires, ceintures urbaines, petites villes ; au sein des communes rurales : bourgs ruraux, rural à habitat dispersé, rural à habitat très dispersé. Même tableau dans la présentation de l'Insee au Sénat (9 octobre 2025). | [S4](https://www.insee.fr/fr/statistiques/fichier/8571524/note_complementaire.pdf) ; [S11](https://www.senat.fr/fileadmin/cru-1759398938/Office_et_delegations/Collectivites_territoriales/Controle/2024-2025/Presentation_INSEE.pdf) ; [S5](https://www.insee.fr/fr/statistiques/fichier/6686472/DT2022-18_Document_travail_Grille_de_densite.pdf) [pages lues] | Conforme |
| Parts de la population (7 niveaux) | 37,2 / 14,3 / 6,1 / 10,3 / 15,1 / 14,6 / 2,4 % | Grille 2022 (2018), recalculé à partir des effectifs du document de travail : 38,0 / 13,2 / 6,0 / 10,1 / 15,3 / 14,9 / 2,5 % (les % imprimés dans ce document diffèrent par endroits des % recalculés : 5,6 et 10,5 pour petites villes et ceintures). **Bourgs ruraux : « 15 % en France » dans la grille 2025** (dossier Pays de la Loire). Sous-totaux du fichier : 14,3 + 6,1 + 10,3 = 30,7 (30,8 annoncé : arrondi) ; 15,1 + 14,6 + 2,4 = 32,1. | [S5](https://www.insee.fr/fr/statistiques/fichier/6686472/DT2022-18_Document_travail_Grille_de_densite.pdf) [page lue + calcul] ; [S10](https://www.insee.fr/fr/statistiques/fichier/8887956/pa_ind_16_12.pdf) [page lue] | Conforme (ordres de grandeur) ; non trouvé (valeurs exactes) |
| Parts des communes (7 niveaux) | 2,0 / 1,8 / 2,7 / 5,7 / 14,5 / 52,4 / 20,7 % | Grille 2022 (2018) : 2,2 / 1,6 / 2,6 / 5,6 / 14,6 / 52,6 / 20,8 %. Sous-totaux du fichier : 1,8 + 2,7 + 5,7 = 10,2 (10,3 annoncé) ; 14,5 + 52,4 + 20,7 = 87,6 (87,7 annoncé) : arrondis. | [S5](https://www.insee.fr/fr/statistiques/fichier/6686472/DT2022-18_Document_travail_Grille_de_densite.pdf) [page lue + calcul] | Conforme (ordres de grandeur) ; non trouvé (valeurs exactes) |

Point d'attention : le dossier Pays de la Loire résume les niveaux avec des seuils d'habitants (« grands centres urbains : communes les plus densément peuplées de 50 000 habitants ou plus », « bourgs ruraux : 500 à 4 999 habitants »). Ce sont des raccourcis de rédaction régionale, pas la définition de l'Insee, fondée sur la part de population dans les types de carreaux. À ne pas reprendre dans le jeu.

### 3. Départements (part de la population vivant dans une commune rurale)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Ain | 48,2 % (≈ 327 400 sur 679 344 habitants) | Insee Analyses Auvergne-Rhône-Alpes n° 113 (12/02/2021, recensement 2017, ancienne grille à 4 niveaux) : 311 600 habitants sur 643 400 dans les communes peu et très peu denses, soit **48 %**. Autre millésime, même ordre de grandeur. | [S14](https://www.insee.fr/fr/statistiques/5040213) [page lue] ; population 2023 : [S17](https://www.insee.fr/fr/statistiques/8680659) [extrait] | Conforme (ordre de grandeur) ; valeur exacte non retrouvée |
| Ain, `P_RURAL` départemental | 52,5 % | La note complémentaire de l'Insee agrège par la formule P_k du territoire = Σ P_k × PMUN, avec des catégories 1 et 2 qualifiées de « clusters urbains » (« plus de 80 % de la population appartient à la catégorie 1 ou 2 de la grille de densité (clusters urbains) »). La page de la grille parle de « la répartition de la population communale dans les trois catégories de densité de niveau 1 ». Ces catégories sont donc des parts de population par type de **carreaux**, pas le type de la commune : `P_RURAL` ≠ part des habitants des communes rurales. Le fichier de la page a été corrigé le 22/07/2025 sur la « part de population à la maille départementale dans le rural ». Conséquence : avec P_RURAL = 52,5 % (> 50 %), la règle de l'Insee pour un territoire donne « rural » au niveau du département Ain, alors que 48,2 % seulement de ses habitants vivent dans une commune rurale. La lecture exacte de la colonne ne peut être confirmée que dans le fichier (non relu ici). | [S4](https://www.insee.fr/fr/statistiques/fichier/8571524/note_complementaire.pdf) ; [S1](https://www.insee.fr/fr/information/8571524) [pages lues] | Écart expliqué |
| Paris | 0 % | Paris est une commune unique (2 103 778 habitants en 2023, selon l'Insee) : par construction « commune dense » (plus de 50 % de la population en centre urbain). Aucune page lue ne le dit en une phrase. | [S17](https://www.insee.fr/fr/statistiques/8680659) [extrait] (population seulement) | Conforme (par construction), non sourcé directement |
| Creuse, valeur et rang | 88,8 %, le plus élevé | Insee Analyses Occitanie n° 133 (21/04/2023) : le Gers (84 % de ses habitants dans une commune rurale) est « au troisième rang des départements français les plus ruraux **après la Creuse et la Lozère** ». Lozère : 83,9 % et Gers : 83,2 % dans le dossier Occitanie n° 26 (grille 2022, population 2021). La Creuse (115 527 habitants en 2023) est donc en tête, au-dessus de 84 %. **La valeur 88,8 % n'a pas été retrouvée.** | [S15](https://www.insee.fr/fr/statistiques/7344780) [extrait] ; [S12](https://www.insee.fr/fr/statistiques/fichier/8259620/lm_ind_26_C10.pdf) [page lue] | Conforme (rang) ; valeur exacte non trouvée |

Autres départements, pour comparer aux valeurs du fichier (**grille et millésime différents, attendre quelques points d'écart**) :

- Occitanie, grille 2022, population 2021 (S12) : Lozère 83,9 % ; Gers 83,2 % ; Lot 80,9 % ; Aveyron 69,7 % ; Tarn-et-Garonne 63,4 % ; Ariège 60,7 % ; Aude 53,8 % ; Hautes-Pyrénées 52,5 % ; Tarn 44,8 % ; Gard 34,9 % ; Pyrénées-Orientales 31,7 % ; Haute-Garonne 23,5 % ; Hérault 22,9 % ; France hors Mayotte 32,6 % ; France métropolitaine 33,2 %.
- Auvergne-Rhône-Alpes, grille à 4 niveaux, recensement 2017 (S14) : Ain 48 % ; Allier 56 % ; Ardèche 59 % ; Cantal 74 % ; Drôme 45 % ; Isère 34 % ; Loire 32 % ; Haute-Loire 67 % ; Puy-de-Dôme 43 % ; Rhône 11 % ; Savoie 45 % ; Haute-Savoie 29 % ; région 35 %.
- Pays de la Loire, grille 2025, population 2022 (S10) : 49 % de la population en commune rurale, 51 % en commune urbaine.

### 4. Grille 2025 contre grille 2022

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| La grille 2025 remplace celle de 2022 | oui | « La grille de densité 2025 remplace la précédente, qui datait de 2022. » La page 2022 : « Depuis mai 2025, une nouvelle grille de densité a remplacé la grille 2022. » | [S1](https://www.insee.fr/fr/information/8571524) ; [S8](https://www.insee.fr/fr/information/6439600) [pages lues] | Conforme |
| Source des données | recensement 2021, pas Fideli 2018 | « Les données de population sont issues du recensement de la population carroyé (RP 2021) » ; « Les évolutions s'expliquent principalement par le changement de source et de millésime des données (RP 2021 au lieu de Fideli 2018). » La page 2022 : Fideli 2018. | [S1](https://www.insee.fr/fr/information/8571524) ; [S8](https://www.insee.fr/fr/information/6439600) [pages lues] | Conforme |
| « Les niveaux sont passés de 4 (ou 6/7) à 3 et 7 » | — | **Pas en 2025.** Grille 2019 / 2020 (Fideli 2018) : 4 niveaux (dense, intermédiaire, peu dense, très peu dense) ; grille 2010 : 4 niveaux (population 2010). Grille 2022 : 3 niveaux + 7 niveaux, « la subdivision de l'espace rural en 3 catégories remplace la précédente subdivision en 2 catégories » (document de travail 2022-18, paru le 05/01/2023). Grille 2025 : 3 niveaux + 7 niveaux, comme 2022. Aucun « 6 niveaux » trouvé (Eurostat parle de six sous-classes de niveau 2 en plus des villes : peut-être l'origine). | [S9](https://www.insee.fr/fr/information/2114627) ; [S8](https://www.insee.fr/fr/information/6439600) ; [S5](https://www.insee.fr/fr/statistiques/6686472) ; [S21](https://ec.europa.eu/eurostat/statistics-explained/SEPDF/cache/108903.pdf) [pages lues] | **Écart** |
| Ce qui change exactement en 2025 | — | Source et millésime (RP 2021 au lieu de Fideli 2018). Le dossier Insee Pays de la Loire n° 16 écrit « méthodologie redéfinie par l'Insee en 2025 » (formule régionale, absente de la page nationale). Mise à jour annuelle : « ne consiste pas à ré-estimer le niveau de densité de chaque commune, mais seulement à affecter les communes dans leur nouvelle géographie à un niveau de densité "2021" » (donc le niveau reste celui de 2021 pour les géographies 2022 à 2026). Reclassements réels : en Occitanie, 4 086 communes rurales (grille 2022, géographie 2024) contre 4 052 (grille 2025, géographie 2025). Pas de liste nationale des reclassements trouvée. | [S10](https://www.insee.fr/fr/statistiques/fichier/8887956/pa_ind_16_12.pdf) ; [S12](https://www.insee.fr/fr/statistiques/fichier/8259620/lm_ind_26_C10.pdf) ; [S13](https://www.insee.fr/fr/statistiques/8646270) [pages lues] | Conforme (source) ; non trouvé (détail méthodologique) |
| Les grilles 2022 et 2025 se comparent-elles ? | « ne se comparent pas » | Aucun texte de l'Insee ne dit « ne se comparent pas ». Il dit que les évolutions viennent surtout du changement de source. Les deux grilles ont la même nomenclature (3 + 7 niveaux) : on peut les comparer en connaissant l'effet de source, sans en tirer une évolution du territoire. | [S1](https://www.insee.fr/fr/information/8571524) [page lue] | **Écart de formulation** |

### 5. Définition du rural en 2020

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Avant 2020 | rural = hors unité urbaine | « Jusqu'en 2020, l'Insee définissait le rural comme l'ensemble des communes n'appartenant pas à une unité urbaine » (unité urbaine : au moins 2 000 habitants, bâti continu, pas de coupure de plus de 200 m). DEPP : « Jusqu'en 2020, les communes rurales étaient définies par l'Insee comme les communes en dehors d'une unité urbaine. » | [S6](https://www.insee.fr/fr/statistiques/5039991) ; [S16](https://www.education.gouv.fr/sites/default/files/2025-04/la-d-finition-de-la-ruralit-par-l-insee-et-les-volutions-de-la-typologie-des-communes-rurales-et-urbaines-de-la-depp-pdf-avril-2025--439881.pdf) [pages lues] | Conforme |
| Depuis 2020 | rural = densité | « Les territoires ruraux désignent désormais l'ensemble des communes peu denses ou très peu denses d'après la grille communale de densité. » Décision d'un groupe de travail en 2020 (Cnis, commission Territoires du 26 novembre 2020 ; Comité interministériel aux ruralités du 14 novembre 2020), publication de l'Insee Références le **29/04/2021**. Présentation Insee (Sénat, 9 octobre 2025) : « Depuis 2020, c'est la notion de densité de population qui est retenue **au niveau européen** ». Sénat (question du 30/10/2025) : en métropole, rurales = « peu denses » ou « très peu denses » en application de l'article 8 du décret n° 2025-438 du 20 mai 2025 (contenu du décret : résumé de moteur seulement). | [S6](https://www.insee.fr/fr/statistiques/5039991) ; [S16](https://www.education.gouv.fr/sites/default/files/2025-04/la-d-finition-de-la-ruralit-par-l-insee-et-les-volutions-de-la-typologie-des-communes-rurales-et-urbaines-de-la-depp-pdf-avril-2025--439881.pdf) ; [S11](https://www.senat.fr/fileadmin/cru-1759398938/Office_et_delegations/Collectivites_territoriales/Controle/2024-2025/Presentation_INSEE.pdf) [pages lues] ; [S24](https://www.senat.fr/questions/base/2025/qSEQ25100755S.html) [extrait] | Conforme (« depuis 2020 » : décidé en 2020, publié en avril 2021) |
| Effet sur les chiffres | — | DEPP (recensement 2018) : communes rurales 78,3 % → 88 % ; population rurale 20,8 % → 32,7 %. « Il n'est pas possible de comparer directement les résultats sur l'ancienne et la nouvelle définition du rural. » C'est la rupture de série documentée. | [S16](https://www.education.gouv.fr/sites/default/files/2025-04/la-d-finition-de-la-ruralit-par-l-insee-et-les-volutions-de-la-typologie-des-communes-rurales-et-urbaines-de-la-depp-pdf-avril-2025--439881.pdf) [page lue] | Conforme |

### 6. Dates et licence

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Mise en ligne | 15/05/2026 | La page n'a pas de date de mise en ligne ni de publication ; elle affiche « Dernière mise à jour le 06/05/2026 » (lue le 2026-11-02). Le fichier est annoncé comme postérieur (15/05/2026) à la dernière mise à jour de sa propre page : le fichier a peut-être été remplacé sans que la date de la page change. Impossible de trancher sur le web. | [S1](https://www.insee.fr/fr/information/8571524) [page lue] | **Écart non expliqué** (mineur) |
| Géographie | 01/01/2026 | La page liste « Grille de densité au 1er janvier 2026 » (fichier `fichier_diffusion_2026.xlsx`, xlsx 2 Mo), puis 2025, 2024, 2023, 2022, 2021. Le texte d'introduction de la page parle encore de « la géographie communale en vigueur au 1er janvier 2025 » (texte non mis à jour). Les populations 2023 sont dans les limites du 1er janvier 2025, qui comptent les mêmes 34 875 communes. | [S1](https://www.insee.fr/fr/information/8571524) ; [S17](https://www.insee.fr/fr/statistiques/8681011) ; [S19](https://www.collectivites-locales.gouv.fr/files/files/Etudes-et-statistiques/OFGL/2026/Annexes%206%20%C3%A0%208.pdf) [pages lues] | Conforme |
| « Grille de densité 2025 » depuis mai 2025 | oui | Page 2022 (et page 2019) : « Depuis mai 2025, une nouvelle grille de densité a remplacé la grille 2022. » Blog : « La dernière livraison date de mai 2025. » Historique de la page 2025 : « 22/07/2025 : les fichiers 2022 à 2025 ont été remplacés, la part de population à la maille départementale dans le rural qui portait sur l'année 2021 a été corrigée. » Définition c2343 mise à jour le 28/07/2025. | [S8](https://www.insee.fr/fr/information/6439600) ; [S25](https://www.joelmariteau.fr/carnet/2025/07/typologie-des-densites-de-population-en-france/) ; [S1](https://www.insee.fr/fr/information/8571524) ; [S2](https://www.insee.fr/fr/metadonnees/definition/c2343) [pages lues] | Conforme |
| Licence Ouverte 2.0 | oui | La page de la grille n'indique pas de licence. Règle générale du site (mentions légales, mise à jour le 13/04/2026) : « Sauf mention contraire, les informations publiques diffusées sur ce site (données, bases de données, publications, fichiers téléchargeables) sont mises à disposition sous la Licence Ouverte / Open Licence version 2.0 (Etalab) », avec obligation de mentionner « Source : Insee » et la date de dernière mise à jour des données. | [S20](https://www.insee.fr/fr/information/2008466) [page lue] | Conforme (par la règle générale du site) |
| Terme « population municipale 2023 » | PMUN23 | Insee : « populations de référence 2023 » (le terme remplace « populations légales » : information venue d'un résumé de moteur, pas relue sur la page), date de référence 1er janvier 2023, en vigueur au 1er janvier 2026. Population municipale = personnes ayant leur résidence habituelle sur la commune (plus sans-abri, habitations mobiles, détenus) : pas les électeurs. | [S17](https://www.insee.fr/fr/statistiques/8681011) [page lue] | Conforme |

### 7. Versions anglaises

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Page de la grille 2025 | — | **Pas de version anglaise** : `https://www.insee.fr/en/information/8571524` renvoie 404 (testé avec curl et avec l'outil de lecture, le 2026-11-02). Même 404 pour les pages 2022 (`/en/information/6439600`), 2019 (`/en/information/2114627`), le document de travail (`/en/statistiques/6686472`) et l'Insee Références (`/en/statistiques/5039991`). Le sélecteur de langue de la page française renvoie à l'accueil anglais (`https://www.insee.fr/en/accueil`). | [https://www.insee.fr/en/information/8571524](https://www.insee.fr/en/information/8571524) (404) | Non trouvé |
| Définition c2343 | — | **Version anglaise existante** : `https://www.insee.fr/en/metadonnees/definition/c2343`, titre « Municipal degree of urbanisation », mise à jour 28/07/2025 ; texte : « The degree of urbanisation distinguishes three types of municipalities: densely populated municipalities; intermediate density municipalities; rural municipalities. Densely populated municipalities and intermediate density municipalities are called urban municipalities. » | [S3](https://www.insee.fr/en/metadonnees/definition/c2343) [page lue] | Conforme (existe) |
| Mentions légales (licence) | — | Version anglaise : « Legal notice and credits », `https://www.insee.fr/en/information/2409130` (mise à jour 20/04/2026). | [S20b](https://www.insee.fr/en/information/2409130) [page lue] | Conforme (existe) |
| Libellés anglais des 7 niveaux | — | Pas de libellé anglais de l'Insee trouvé pour les 7 niveaux. Terminologie Eurostat (manuel 2021, chapitre 7) : cities ; dense towns ; semi-dense towns ; suburban or peri-urban areas ; villages ; dispersed rural areas ; mostly uninhabited areas (« very dispersed rural area »). Le résumé anglais du document de travail 2022-18 parle de « 7-level grid », « municipalities of intermediate density », « rural municipalities ». | [S21](https://ec.europa.eu/eurostat/statistics-explained/SEPDF/cache/108903.pdf) ; [S5](https://www.insee.fr/fr/statistiques/fichier/6686472/DT2022-18_Document_travail_Grille_de_densite.pdf) [pages lues] | Non trouvé (Insee) ; terminologie Eurostat disponible |

---

### Les quatre notes « À savoir »

#### Note (1) : définition urbain / rural et unité de compte

Texte prévu : « Urbain signifie commune dense ou de densité intermédiaire, rural commune de faible ou très faible densité, selon la grille de densité de l'Insee ; la grille compte les habitants (population municipale 2023), pas les électeurs. »

- **Confirmé** : dense + intermédiaire = « communes urbaines » (page 2025) ; rural = communes « peu denses ou très peu denses » (Insee Références 2021, Sénat) ; population municipale = résidents habituels, pas les inscrits (page Insee des populations de référence).
- **À nuancer 1** : la page 2025 n'emploie plus « peu dense / très peu dense » pour le rural, seulement « communes rurales » (sous-niveaux : bourgs ruraux, habitat dispersé, habitat très dispersé). « Faible densité » est un raccourci qui peut tromper : le classement ne repose pas sur la densité moyenne de la commune (« n'est pas simplement liée à la densité moyenne [...] incluant les surfaces non habitées »), mais sur la part de la population vivant dans des zones denses (carreaux d'un km²).
- **À nuancer 2** : « population municipale 2023 » est le millésime Insee « populations de référence 2023 » ; pour Mayotte, c'est 2017.
- **Proposition** : « Urbain : commune dense ou de densité intermédiaire. Rural : commune rurale de la grille communale de densité de l'Insee (anciennement « peu dense » ou « très peu dense »). La grille classe les communes selon la répartition de leur population sur le territoire, pas selon la seule densité moyenne, et compte les habitants (population municipale, millésime 2023), pas les électeurs. »

#### Note (2) : pas de total national

Texte prévu : « L'Insee ne publie aucun total national par commune : les parts sont sommées à partir de son fichier des 34 875 communes. »

- **Non démontré tel quel** : on n'a pas trouvé de publication nationale pour la grille 2025, mais l'absence ne se prouve pas (et le dossier Pays de la Loire donne « 15 % en France » pour les bourgs ruraux). « Par commune » prête à confusion : le fichier est par commune, les totaux sont par niveau de densité.
- **Chiffres confirmés** : 34 875 communes (DGCL) ; 68 350 798 habitants = 68 094 280 (2023, hors Mayotte) + 256 518 (Mayotte, 2017).
- **Proposition** : « Ces parts sont calculées en additionnant, commune par commune, le fichier de l'Insee sur la grille de densité (34 875 communes, population municipale 2023, 2017 pour Mayotte). Nous n'avons pas trouvé de publication de l'Insee qui donne ces totaux nationaux pour la grille 2025. » Version courte sans affirmation négative : « Parts calculées à partir du fichier de l'Insee, commune par commune (34 875 communes). »

#### Note (3) : définition depuis 2020 et comparabilité

Texte prévu : « Depuis 2020, le rural est défini par la densité ; avant, il s'agissait des communes hors unité urbaine. La grille 2025 ne se compare pas aux précédentes. »

- **Première phrase confirmée** (Insee Références, 29/04/2021, DEPP). Précision possible : décidée en 2020, publiée en avril 2021.
- **Seconde phrase à corriger** : ce que l'Insee écrit, c'est que les évolutions entre la grille 2022 et la grille 2025 viennent surtout du changement de source (RP 2021 au lieu de Fideli 2018). La rupture de série documentée est celle de la définition du rural : sur le recensement 2018, la population rurale passe de 20,8 % (hors unité urbaine) à 32,7 % (densité) selon la DEPP.
- **Proposition** : « Depuis 2020, le rural est défini par la densité ; avant, il s'agissait des communes hors unité urbaine, ce qui donnait une part de population rurale bien plus faible : les deux définitions ne se comparent pas. La grille 2025 (recensement 2021) remplace celle de 2022 (Fideli 2018) : ses écarts avec la précédente viennent surtout du changement de source. »

#### Note (4) : ne pas confondre avec d'autres zonages

Texte prévu : « Ne pas confondre avec les "aires d'attraction des villes" ni les "unités urbaines". »

- **Confirmé** : la grille est une approche « morphologique » (distribution de la population en carreaux), « complémentaire des approches fonctionnelles » (aires d'attraction des villes, zones d'emploi, bassins de vie). L'unité urbaine (bâti continu, au moins 2 000 habitants) était la base de l'ancienne définition du rural. Le zonage en aires d'attraction des villes (2020) a remplacé les aires urbaines ; on le croise avec la grille pour définir le « rural périurbain » (communes rurales dans une aire de plus de 50 000 habitants). Les zonages divergent vraiment : en 2021, 295 communes hors unité urbaine étaient pourtant de densité intermédiaire selon la grille (DEPP).
- **Proposition (même sens, un peu plus précise)** : « Ne pas confondre avec les unités urbaines (zones de bâti continu de 2 000 habitants ou plus, ancienne base du rural) ni avec les aires d'attraction des villes (influence d'un pôle d'emploi) : ce sont d'autres zonages, qui ne donnent pas les mêmes communes urbaines et rurales. »

---

### Conclusion

**Écarts**

1. Niveaux « de 4 (ou 6/7) à 3 et 7 » : attribué à tort à 2025. Passage fait en 2022 ; la grille 2025 garde 3 + 7 niveaux ; aucun « 6 niveaux ».
2. « La grille 2025 ne se compare pas aux précédentes » : formulation plus forte que celle de l'Insee (changement de source). La rupture de série documentée est celle de la définition du rural en 2020.
3. « Mise en ligne le 15/05/2026 » : la page de l'Insee affiche une dernière mise à jour du 06/05/2026 et aucune date de mise en ligne.
4. Écart expliqué : `P_RURAL` départemental (Ain 52,5 %) mesure une part de population par type de carreaux, pas la part des habitants des communes rurales (Ain 48,2 %, cohérent avec 48 % de l'Insee pour 2017).
5. Écart expliqué : population « 2023 » : Mayotte reste à 256 518 (2017) ; le total 68 350 798 est exactement 68 094 280 + 256 518.
6. Vocabulaire « faible / très faible densité » (ancienne grille à 4 niveaux), alors que la page 2025 dit « communes rurales ».

**Non trouvé**

7. Parts nationales exactes de la grille 2025 (87,7 / 32,1 %, 10,3 / 30,8 %, 2,0 / 37,2 %) ; seuls les ordres de grandeur (2022 : 88,0 / 32,7 %, 9,8 / 29,3 %, 2,2 / 38,0 %) et « 15 % en France » pour les bourgs ruraux (2025) sont recoupés.
8. Codes numériques `DENS7` 1 à 7 (seul l'ordre est recoupé) ; Creuse 88,8 % (seul le rang est confirmé) ; Paris 0 % (vrai par construction).
9. Page anglaise de la grille 2025 : elle n'existe pas (404). Seule la définition c2343 a une version anglaise.

**Confirmés** : trois niveaux et libellés des sept niveaux, emboîtement 1 → 3 → 3 ; 34 875 communes au 1er janvier 2026 ; population totale ; remplacement de la grille 2022 en mai 2025 ; recensement 2021 au lieu de Fideli 2018 ; définition du rural hors unité urbaine avant 2020 ; géographie au 1er janvier 2026 ; Licence Ouverte 2.0 (règle générale du site) ; Ain ≈ 48 % ; Creuse en tête devant Lozère et Gers.

### Sources consultées le 2026-11-02

Les pages Insee ont été téléchargées et converties en texte (curl + conversion, `pdftotext` pour les PDF) sauf mention.

| Réf. | URL | Mode |
|---|---|---|
| S1 | https://www.insee.fr/fr/information/8571524 | page lue |
| S2 | https://www.insee.fr/fr/metadonnees/definition/c2343 | page lue |
| S3 | https://www.insee.fr/en/metadonnees/definition/c2343 | page lue |
| S4 | https://www.insee.fr/fr/statistiques/fichier/8571524/note_complementaire.pdf | page lue |
| S5 | https://www.insee.fr/fr/statistiques/6686472 et https://www.insee.fr/fr/statistiques/fichier/6686472/DT2022-18_Document_travail_Grille_de_densite.pdf | page lue |
| S6 | https://www.insee.fr/fr/statistiques/5039991 | page lue |
| S7 | https://www.insee.fr/fr/statistiques/5039883 | page lue |
| S8 | https://www.insee.fr/fr/information/6439600 | page lue |
| S9 | https://www.insee.fr/fr/information/2114627 | page lue |
| S10 | https://www.insee.fr/fr/statistiques/fichier/8887956/pa_ind_16_12.pdf (Insee Dossier Pays de la Loire n° 16) | page lue |
| S11 | https://www.senat.fr/fileadmin/cru-1759398938/Office_et_delegations/Collectivites_territoriales/Controle/2024-2025/Presentation_INSEE.pdf (colloque du 9 octobre 2025) | page lue |
| S12 | https://www.insee.fr/fr/statistiques/fichier/8259620/lm_ind_26_C10.pdf (Insee Dossier Occitanie n° 26) | page lue |
| S13 | https://www.insee.fr/fr/statistiques/8646270 et https://www.insee.fr/fr/statistiques/fichier/8646252/lm_ind_29_1.pdf (Occitanie n° 29, 16/10/2025 ; le PDF du chapitre grille n'a pas de texte extractible) | page lue |
| S14 | https://www.insee.fr/fr/statistiques/5040213 (Insee Analyses Auvergne-Rhône-Alpes n° 113) | page lue |
| S15 | https://www.insee.fr/fr/statistiques/7344780 (Insee Analyses Occitanie n° 133) | extrait |
| S16 | https://www.education.gouv.fr/sites/default/files/2025-04/la-d-finition-de-la-ruralit-par-l-insee-et-les-volutions-de-la-typologie-des-communes-rurales-et-urbaines-de-la-depp-pdf-avril-2025--439881.pdf | page lue |
| S17 | https://www.insee.fr/fr/statistiques/8680659 (départements 2023), https://www.insee.fr/fr/statistiques/8680653 (régions 2023) | extrait ; total recalculé par addition des 100 départements : 68 094 280 |
| S17b | https://www.insee.fr/fr/statistiques/8681011 (populations de référence 2023, communes) | page lue |
| S18 | https://insee.fr/fr/statistiques/3284395 (Mayotte 2017 : 256 518) | page lue |
| S19 | https://www.collectivites-locales.gouv.fr/files/files/Etudes-et-statistiques/OFGL/2026/Annexes%206%20%C3%A0%208.pdf | page lue |
| S20 | https://www.insee.fr/fr/information/2008466 (mentions légales) ; S20b : https://www.insee.fr/en/information/2409130 | page lue |
| S21 | https://ec.europa.eu/eurostat/statistics-explained/SEPDF/cache/108903.pdf (manuel Eurostat, chapitre 7) | page lue |
| S22 | https://www.observatoire-des-territoires.gouv.fr/grille-communale-de-densite-en-7-niveaux | extrait (ni codes, ni chiffres, ni licence) |
| S23 | https://www.data.gouv.fr/datasets/grille-communale-de-densite-7-niveaux-orne-2024 | extrait (libellés dans un autre ordre ; Licence Ouverte 2.0 ; pas de codes) |
| S24 | https://www.senat.fr/questions/base/2025/qSEQ25100755S.html | extrait |
| S25 | https://www.joelmariteau.fr/carnet/2025/07/typologie-des-densites-de-population-en-france/ | page lue |
| S26 | https://www.insee.fr/fr/metadonnees/definition/c2070 (aire urbaine, remplacée par l'aire d'attraction des villes) | extrait |
| S27 | https://www.insee.fr/fr/statistiques/8643805 (Insee Flash Pays de la Loire n° 158) | page lue (aucune part nationale utile) |
| S28 | https://www.maire-info.com/communes-nouvelles/2025-un-bon-cru-pour-les-communes-nouvelles-art26-29256 (estimation AMF « autour de 34 870 » avant le décompte officiel) | page lue |

Sources qui n'ont pas pu être lues (valeurs citées dans aucune conclusion ci-dessus, sauf mention) :

- https://geoconfluences.ens-lyon.fr/glossaire/grille-de-densite, https://geoconfluences.ens-lyon.fr/glossaire/rurale-commune, https://geoconfluences.ens-lyon.fr/actualites/eclairage/grille-densite-zonage-aires-urbaines-definition-rural : erreur 503 ou connexion coupée. **[moteur]** seulement : un extrait donnait « 88 % des communes pour 33 % de la population » en 2021, non utilisé comme preuve.
- https://www.gers.cci.fr/actualites/le-gers-3eme-departement-rural-de-france.html : erreur 503, **[moteur]** seulement (le rang est confirmé par S15).
- Contenu du décret n° 2025-438 du 20 mai 2025 : résumé de moteur seulement ; sa citation par la question du Sénat vient de S24.
- https://data.iledefrance.fr/explore/dataset/grille_densite_7_niveaux_2024/ et https://www.puy-de-dome.gouv.fr/index.php/Publications/Cartes-et-donnees/Demographie-et-zonage-INSEE/Grille-communale-de-densite-INSEE-a-7-niveaux-2024 : pages ouvertes, ni codes ni libellés numérotés.
- Eurostat (pages « glossary », « background »), Statistiques locales (application dynamique) : rien d'exploitable ; aucune part nationale française par DEGURBA trouvée.
- https://www.insee.fr/en/information/8571524, https://www.insee.fr/en/information/6439600, https://www.insee.fr/en/information/2114627, https://www.insee.fr/en/statistiques/6686472, https://www.insee.fr/en/statistiques/5039991 : 404.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
