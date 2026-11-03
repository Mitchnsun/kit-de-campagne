# `energyMix` · Énergie (partie de la page « Mix électrique »)

**Vérifiée le 02/11/2026** : aucun des 23 chiffres contrôlés n'est faux ; ils sont conformes au bilan provisoire de 2025 du SDES (séries longues, avril 2026) et au PDF des Chiffres clés 2026 (1 533 TWh à climat corrigé, parts de 38 % pour le pétrole et 27 % pour l'électricité dans le texte et l'infographie). Corrigé : la rupture de champ de 2011 (les cinq DROM entrent, environ +35 TWh) est marquée dans les séries ; notes précisées (à climat corrigé, secteurs du SDES, exclusions de la consommation finale).

**Écart expliqué** : 2024 dépend du millésime (1 549,3 TWh dans l'édition 2026, 1 552,3 dans le bilan définitif de 2024 de mars 2026, « 1 550 » dans l'édition 2025), sans explication de la source. Le SDES écrit « chaleur commercialisée » ; son tableau, « Chaleur vendue ».

| Champ | Valeur |
| --- | --- |
| Indicateur | `energyMix`, partie de la page composite `electricityMix` (avec `electricityProduction`), dossier « Écologie et énergie », ticket #29 (statut `planned`) |
| Données | `briefings/data/energyMix.json`, écrit par `yarn briefings energyMix` le 2026-11-02 |
| Source | SDES, « Chiffres clés de l'énergie – Édition 2026 », publiée le 30/09/2026, classeur des données associées (onglet P2-38), chiffres arrêtés au bilan provisoire d'avril 2026 ; Licence Ouverte (décret n° 2017-638) ; un résumé anglais de sept phrases sur la page, pas de version anglaise distincte |
| Séries | Consommation finale à usage énergétique, à climat corrigé, en TWh, de 1990 à 2025 : `oil`, `naturalGas`, `coal` (hors hauts-fourneaux), `renewablesAndWaste`, `electricity`, `soldHeat` (depuis 2000) ; 2025 provisoire ; rupture en 2011 |
| Chiffre clé | Pétrole : 583,4 TWh en 2025, en baisse, 38 % de la consommation finale |
| Première édition | À remplir à la publication |

À actualiser : à chaque édition des Chiffres clés (septembre) ; l'adresse du classeur change, le script la lit dans le lien « Données associées » de la page de l'édition.

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans ouvrir le classeur du script. Son rapport, tel quel :

Date de la vérification : 2026-11-02. Vérificateur : agent indépendant, web uniquement.

### 0. Méthode, limites, ce qui n'a pas été fait

- Le classeur « Données associées » des Chiffres clés 2026 (`https://www.statistiques.developpement-durable.gouv.fr/media/9748/download`, onglet P2-38) n'a pas été ouvert, comme demandé.
  - le PDF intégral des Chiffres clés 2026 et l'édition numérique HTML du même chapitre (textes, notes « Champ », tableau 2025 en annexe) ;
  - l'infographie (PDF) et sa version texte sur la page de la publication ;
  - les **séries longues du Bilan énergétique provisoire 2025** (XLSX, avril 2026, `media/9283`) : c'est un autre fichier que celui du script, mais le même bilan SDES et le même millésime (« chiffres arrêtés au 8 avril 2026 »). Il vérifie le fichier, pas la source statistique ;
  - les séries longues du **Bilan 2024 définitif** (XLSX, mars 2026, `media/8958`) et sa méthodologie (PDF, mars 2026) ;
  - l'**édition 2025** des Chiffres clés (PDF et classeur, feuille p38) pour 1990 et 2024 ;
  - **Eurostat** `nrg_bal_c` (API JSON, jeu mis à jour le 2026-08-27).
- Aucune valeur n'a été retenue sur la seule foi d'un résumé de moteur de recherche. Les résumés de WebSearch m'ont servi à trouver les pages ; chaque chiffre cité ci-dessous a été relu dans le document source. Aucun site secondaire (miroirs de type fgeerolf.com vus dans les résultats) n'a été utilisé.
- Seul le texte du décret n° 2017-638 sur Légifrance repose sur un résumé automatique (WebFetch), signalé comme tel dans la section 4. Tout le reste a été relu directement : PDF via `pdftotext`, HTML brut via `curl`, XLSX via `openpyxl`, JSON Eurostat via Python. Les premiers survols par WebFetch (pages d'accueil, bilan provisoire) ont été refaits sur le HTML brut avant d'être cités.
- Limite : l'édition numérique HTML est une application qui renvoie la même page d'accueil pour toute adresse inconnue. Seul le chapitre 7 a pu être lu en HTML, à l'adresse `.../chiffres-cles-energie/7-consommation-finale-denergie-par-secteur.php`. Les valeurs en TWh par énergie ne sont pas imprimées dans le PDF (graphique sans étiquettes). Elles viennent donc des séries longues XLSX du bilan (D) et du classeur de l'édition 2025 (F).

#### Sources principales (codes utilisés dans les tableaux)

| Code | Document | URL |
|---|---|---|
| A | Chiffres clés de l'énergie, édition 2026, PDF intégral (p. 32 à 41, 72, 88, 91, 95) | https://www.statistiques.developpement-durable.gouv.fr/edition-numerique/chiffres-cles-energie/pdf/Chiffres-cles-energie-2026.pdf |
| B | Édition numérique 2026, chapitre 7 (même texte que A p. 38 à 41) | https://www.statistiques.developpement-durable.gouv.fr/edition-numerique/chiffres-cles-energie/7-consommation-finale-denergie-par-secteur.php |
| C | Page de la publication (« Publié le 30/09/2026 », texte de l'infographie, résumé anglais) | https://www.statistiques.developpement-durable.gouv.fr/chiffres-cles-de-lenergie-edition-2026 |
| C2 | Infographie PDF (« Consommation finale à usage énergétique en 2025 ») | https://www.statistiques.developpement-durable.gouv.fr/media/9771/download |
| D | Bilan énergétique de la France en 2025, données provisoires (22/04/2026) : page, publication PDF, séries longues XLSX | https://www.statistiques.developpement-durable.gouv.fr/bilan-energetique-de-la-france-en-2025-donnees-provisoires ; https://www.statistiques.developpement-durable.gouv.fr/media/9287/download?inline ; https://www.statistiques.developpement-durable.gouv.fr/media/9283/download?inline |
| E | Bilan énergétique de la France pour 2024 (définitif, mars 2026) : page, séries longues XLSX, méthodologie PDF | https://www.statistiques.developpement-durable.gouv.fr/bilan-energetique-de-la-france-pour-2024 ; https://www.statistiques.developpement-durable.gouv.fr/media/8958/download?inline ; https://www.statistiques.developpement-durable.gouv.fr/media/9074/download?inline |
| F | Chiffres clés de l'énergie, édition 2025 (09/10/2025) : page, PDF, classeur (feuille p38) | https://www.statistiques.developpement-durable.gouv.fr/chiffres-cles-de-lenergie-edition-2025 ; https://www.statistiques.developpement-durable.gouv.fr/media/9755/download?inline ; https://www.statistiques.developpement-durable.gouv.fr/media/8710/download?inline |
| G | Eurostat nrg_bal_c, FC_E, France (API JSON) | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/nrg_bal_c?format=JSON&lang=EN&geo=FR&nrg_bal=FC_E&siec=TOTAL&unit=GWH&sinceTimePeriod=2022 (et la même requête avec `time=1990` et les produits `E7000`, `G3000`, `O4000XBIO`, `RA000`, `H8000`, `W6100_6220`) |
| H | Mentions légales du SDES | https://www.statistiques.developpement-durable.gouv.fr/mentions-legales |
| I | Décret n° 2017-638 (Légifrance) | https://www.legifrance.gouv.fr/eli/decret/2017/4/27/2017-638/jo/texte |

Dans le fichier XLSX D, la colonne `TYPDONNEE` distingue `CVC` (corrigées des variations climatiques) et `Réelles`, et `NIVGEO` distingue `Métropole` et `France`. Les valeurs du fichier à vérifier correspondent à `CVC` : `Métropole` pour 1990 et 2000, `France` pour 2024 et 2025.

---

### 1. Tableaux de vérification

#### 1.1 Valeurs par énergie (TWh)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Pétrole 1990 | 748,2 | 748,17 (Métropole, CVC). Édition 2025 : 748,174 ; Bilan 2024 déf. : 748,17 | [D xlsx](https://www.statistiques.developpement-durable.gouv.fr/media/9283/download?inline), [E xlsx](https://www.statistiques.developpement-durable.gouv.fr/media/8958/download?inline), [F xlsx](https://www.statistiques.developpement-durable.gouv.fr/media/8710/download?inline) | Conforme |
| Pétrole 2024 | 588,9 | 588,92 (millésime avril 2026). Autres millésimes : 588,99 (Bilan 2024 déf.), 589,64 (éd. 2025, provisoire) | D xlsx (lien ci-dessus), E xlsx, F xlsx | Conforme au millésime 2026 ; écart expliqué (révision) vs autres millésimes, voir 1.3 |
| Pétrole 2025 | 583,4 | 583,37 (France, CVC). Réel : 581,25 | D xlsx ; [A p. 88](https://www.statistiques.developpement-durable.gouv.fr/edition-numerique/chiffres-cles-energie/pdf/Chiffres-cles-energie-2026.pdf) (tableau « Bilan énergétique physique 2025 », données réelles) | Conforme |
| Chiffre clé « 583,4 TWh en 2025, en baisse » | baisse | « les produits pétroliers (- 0,9 %) reculent » ; calcul 583,37 / 588,92 = - 0,94 % | A p. 38 ; B (`.../7-consommation-finale-denergie-par-secteur.php`) | Conforme |
| Gaz naturel 1990 | 260,4 | 260,36 | D xlsx ; E xlsx ; F xlsx | Conforme |
| Gaz naturel 2024 | 286,6 | 286,64 (millésime avril 2026). Autres : 288,53 (Bilan 2024 déf.), 287,21 (éd. 2025) | D xlsx ; E xlsx ; F xlsx | Conforme au millésime 2026 ; écart expliqué (révision) vs autres millésimes |
| Gaz naturel 2025 | 272,0 | 272,01 (CVC). Réel : 254,03. Variation « - 5,1 % » (A p. 38) : 272,01 / 286,64 = - 5,10 % | D xlsx ; A p. 38 et p. 88 | Conforme |
| Charbon (hors hauts-fourneaux) 1990 | 58,9 | 58,91 (CVC) ; 58,38 en réel | D xlsx ; E xlsx ; F xlsx | Conforme |
| Charbon 2025 | 5,3 | 5,30 (réel = CVC : le charbon n'est pas corrigé du climat, les deux séries sont identiques) | D xlsx ; A p. 88 | Conforme |
| EnR et déchets 1990 | 116,6 | 116,62 | D xlsx ; E xlsx ; F xlsx | Conforme |
| EnR et déchets 2025 | 216,0 | 215,97 (CVC). Réel : 206,88 | D xlsx ; A p. 88 | Conforme |
| Électricité 1990 | 304,1 | 304,11 | D xlsx ; E xlsx ; F xlsx | Conforme |
| Électricité 2024 | 407,9 | 407,89 (millésime avril 2026). Autres : 409,31 (Bilan 2024 déf.), 409,53 (éd. 2025) | D xlsx ; E xlsx ; F xlsx | Conforme au millésime 2026 ; écart expliqué (révision) vs autres millésimes |
| Électricité 2025 | 410,5 | 410,54 (CVC). Réel : 403,73. Variation « + 0,7 % » (A p. 38) : le calcul sur valeurs arrondies donne + 0,65 % | D xlsx ; A p. 38 et p. 88 | Conforme (différence d'arrondi sur la variation) |
| Chaleur vendue depuis 2000 (32,1) | 32,1 | 32,09 en 2000 (Métropole, CVC). Aucune valeur pour 1990-1999. Le SDES écrit « chaleur commercialisée » | D xlsx ; F xlsx (1990-1999 vides) | Conforme |
| Chaleur 2025 | 45,4 | 45,37 (CVC, identique à 2024 : « la chaleur restant stable », A p. 38). Réel : 43,55 | D xlsx ; A p. 38 et p. 88 | Conforme |

#### 1.2 Totaux et parts

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Total 2025 | 1 532,6 | 1 532,57 (CVC). Publication : « TOTAL : 1 533 TWh en 2025 (donnée corrigée des variations climatiques) » ; « 1 495 TWh en donnée réelle » (1 494,73 en détail) | D xlsx ; [A p. 38](https://www.statistiques.developpement-durable.gouv.fr/edition-numerique/chiffres-cles-energie/pdf/Chiffres-cles-energie-2026.pdf) ; B | Conforme (la somme des six valeurs arrondies fait bien 1 532,6) |
| Total 2024 | 1 549,3 | 1 549,31 (millésime avril 2026). Bilan 2024 déf. : 1 552,32. Éd. 2025 : « 1 550 TWh » (1 549,9 dans le classeur) | D xlsx ; E xlsx ; [F, PDF p. 38](https://www.statistiques.developpement-durable.gouv.fr/media/9755/download?inline) ; F xlsx | Conforme au millésime 2026 ; écart expliqué (révision) vs autres millésimes |
| Variation 2024-2025 | (implicite) | « - 1,1 % » (A p. 38 et p. 40) ; 1 532,57 / 1 549,31 = - 1,08 %. Avec le total 2024 définitif (1 552,32) on aurait - 1,27 % : la publication 2026 utilise donc bien le millésime 2026 de 2024 | A p. 38 | Conforme |
| Part pétrole 2025 | 38,1 % | 38,07 % (calcul). Publié : « 38 % » (A p. 38 ; infographie C/C2) | A p. 38 ; [C](https://www.statistiques.developpement-durable.gouv.fr/chiffres-cles-de-lenergie-edition-2026) ; [C2](https://www.statistiques.developpement-durable.gouv.fr/media/9771/download) | Conforme (la décimale n'est pas publiée, elle se calcule) |
| Part électricité 2025 | 26,8 % | 26,79 %. Publié : « 27 % » | A p. 38 ; C ; C2 | Conforme |
| Part gaz 2025 | 17,7 % | 17,75 % (arrondi 17,7 sur 272,0 / 1 532,6). Publié : « 18 % » (infographie seulement) | C ; C2 | Conforme |
| Part EnR et déchets 2025 | 14,1 % | 14,09 %. Publié : « 14 % » | A p. 38 ; C ; C2 | Conforme |
| Part chaleur 2025 | 3,0 % | 2,96 %. Publié : « 3 % » | C ; C2 | Conforme |
| Part charbon 2025 | 0,3 % | 0,35 %. Publié : « moins de 1 % » | C ; C2 | Conforme |
| Total 1990 (utile aux parts de 1990) | non fourni | 1 488,17 TWh, sans chaleur (série à partir de 2000) : pétrole 50,3 %, EnR 7,8 %, électricité 20,4 %. Publié : « de 50 % à 38 % », « de 8 % à 14 % », « de 20 % à 27 % » | D xlsx ; A p. 38 | Conforme |

Les 23 valeurs de l'instantané (15 valeurs par énergie, 2 totaux, 6 parts) sont conformes au millésime d'avril 2026. Aucune n'est fausse.

#### 1.3 Les valeurs 2024 dépendent du millésime (TWh, climat corrigé, France)

| Énergie | Éd. 2025 (09/10/2025, 2024 provisoire) | Bilan 2024 définitif (mars 2026) | Millésime avril 2026 (= éd. 2026 = fichier) |
|---|---|---|---|
| Pétrole | 589,64 | 588,99 | 588,92 |
| Gaz naturel | 287,21 | 288,53 | 286,64 |
| Charbon | 6,64 | 5,48 | 5,48 |
| EnR et déchets | 213,43 | 214,68 | 215,01 |
| Électricité | 409,53 | 409,31 | 407,89 |
| Chaleur commercialisée | 43,45 | 45,33 | 45,37 |
| **Total** | **1 549,9** (publié « 1 550 ») | **1 552,3** | **1 549,3** |

Sources : F xlsx (feuille p38), E xlsx, D xlsx (liens du tableau 1.1). Verdict : **Écart expliqué**. Le fichier suit le millésime de l'édition 2026, cohérent avec sa variation de - 1,1 %. Les autres millésimes diffèrent de 3 TWh au plus sur le total, jusqu'à 1,9 TWh sur une énergie. Je n'ai pas lu d'explication de la révision. La méthodologie du bilan est datée de mars 2026.

#### 1.4 Réel contre corrigé, 2025 (preuve que le fichier est corrigé du climat)

| Énergie | Réel (A p. 88) | Corrigé (D xlsx) | Part corrigée | Part réelle |
|---|---|---|---|---|
| Produits pétroliers | 581,25 | 583,37 | 38,1 % | 38,9 % (soit 39 %) |
| Électricité | 403,73 | 410,54 | 26,8 % | 27,0 % |
| Gaz naturel | 254,03 | 272,01 | 17,7 % | 17,0 % (soit 17 %) |
| EnR thermiques et déchets | 206,88 | 215,97 | 14,1 % | 13,8 % |
| Chaleur commercialisée | 43,55 | 45,37 | 3,0 % | 2,9 % |
| Charbon | 5,30 | 5,30 | 0,3 % | 0,4 % |
| **Total** | **1 494,73** | **1 532,57** | | |

Les valeurs du fichier sont celles de la colonne « Corrigé ». Les parts publiées (38 / 27 / 18 / 14 / 3 / moins de 1) sont aussi celles de la colonne corrigée : sur les données réelles, on aurait 39 / 27 / 17 / 14 / 3.

#### 1.5 Eurostat (ordre de grandeur, données réelles, non corrigées du climat)

| Élément (TWh) | Valeur du fichier (CVC) | Eurostat FC_E France | SDES réel, même année | Source (URL) | Verdict |
|---|---|---|---|---|---|
| Total 2024 | 1 549,3 | 1 503,4 | 1 499,5 | [G](https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/nrg_bal_c?format=JSON&lang=EN&geo=FR&nrg_bal=FC_E&siec=TOTAL&unit=GWH&sinceTimePeriod=2022) ; D xlsx | Écart expliqué : le fichier est corrigé du climat (+ 49,8 TWh sur 2024), Eurostat est en réel. Eurostat dépasse le SDES réel de 3,9 TWh (+ 0,3 %), presque tout sur le pétrole (589,99 contre 586,17) ; je n'ai pas trouvé pourquoi |
| Total 2023 | (non fourni) | 1 500,4 | 1 500,3 | G ; D xlsx | Conforme |
| Total 2022 | (non fourni) | 1 560,0 | (non lu) | G | Non comparé |
| Total 1990 | 1 488,2 | 1 487,6 (France, dont 5,5 de chaleur) | 1 475,0 (Métropole, réel) | [G, requête 1990](https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/nrg_bal_c?format=JSON&lang=EN&geo=FR&nrg_bal=FC_E&unit=GWH&time=1990&time=2023&time=2024&siec=TOTAL&siec=O4000XBIO&siec=G3000&siec=E7000&siec=RA000&siec=H8000&siec=W6100_6220) ; D xlsx | Ordre de grandeur cohérent (± 1 %) |
| Électricité 2024 | 407,9 | 398,26 | 398,26 | G ; D xlsx | Écart expliqué (corrigé contre réel) ; Eurostat identique au SDES réel |
| Gaz 2024 | 286,6 | 263,33 | 263,33 | G ; D xlsx | Écart expliqué (idem) ; identique au SDES réel |
| Chaleur 2024 | 45,4 | 43,00 | 43,00 | G ; D xlsx | Écart expliqué (idem) |
| Pétrole 2024 | 588,9 | 589,99 | 586,17 | G ; D xlsx | Ordre de grandeur cohérent (Eurostat au niveau du fichier corrigé, + 3,8 TWh sur le réel SDES) |
| Total 2025 | 1 532,6 | non publié | 1 494,7 | G (le jeu s'arrête à 2024, mis à jour le 2026-08-27) | Non trouvé |

Eurostat n'a pas encore de valeur 2025 pour la France dans `nrg_bal_c`. Eurostat ne publie pas de série corrigée du climat dans ce jeu, donc la comparaison porte sur les séries « Réelles » du SDES, avec lesquelles l'électricité, le gaz et la chaleur concordent à la décimale.

#### 1.6 Rupture de champ 2010/2011 (utile à la lecture de 1990 contre 2025)

| Élément (TWh, CVC) | Métropole | France (métropole + 5 DROM) | Écart | Source |
|---|---|---|---|---|
| Total 2011 | 1 665,8 | 1 700,6 | + 34,8 (+ 2,1 %) | D xlsx |
| Total 2025 | 1 494,1 | 1 532,6 | + 38,5 | D xlsx |
| Pétrole 2025 | 553,75 | 583,37 | + 29,6 | D xlsx |
| Électricité 2025 | 403,54 | 410,54 | + 7,0 | D xlsx |

Le fichier compare donc 1990 (métropole) à 2024 et 2025 (France entière), comme le fait la publication. À périmètre constant (métropole), pétrole 1990 à 2025 : - 26,0 % (et non - 22,0 %) ; total : + 0,4 % (et non + 3,0 %) ; électricité : + 32,7 % (et non + 35,0 %). Le gaz et le charbon sont identiques sur les deux champs.

---

### 2. Réponses aux quatre points précis

#### Point 1. Corrigé des variations climatiques ou non ?

**Oui, les valeurs du fichier sont corrigées des variations climatiques.** Un seul des éléments de preuve suffirait, ils concordent :

- Le chapitre (A p. 38 ; B) : « CONSOMMATION FINALE À USAGE ÉNERGÉTIQUE PAR ÉNERGIE. TOTAL : 1 533 TWh en 2025 (donnée corrigée des variations climatiques) », puis l'axe « En TWh (données corrigées des variations climatiques) » (sous-titre que vous avez vu). Le texte ajoute : « En 2025, la consommation finale à usage énergétique corrigée du climat atteint 1 533 TWh (1 495 TWh en donnée réelle), en baisse de 1,1 % par rapport à 2024 ».
- Le tableau physique 2025 en annexe (A p. 88, « données réelles ») donne 1 494,73 TWh. Détail dans le tableau 1.4 : aucune valeur du fichier n'y figure, toutes sont dans la série CVC.
- Les séries longues D et E étiquettent les mêmes valeurs `CVC`. Le classeur de l'édition 2025 a la même disposition que celle que vous décrivez (« En TWh » au-dessus du tableau, « En TWh (données corrigées des variations climatiques) » comme titre de graphique) ; ses valeurs de 2024 sont les CVC.
- Le charbon est l'exception : réel et corrigé sont identiques (5,30).
- L'**infographie** (C2) intitulée « Consommation finale à usage énergétique en 2025 – par énergie » **ne mentionne pas la correction**. Ses parts (38 / 27 / 18 / 14 / 3 / moins de 1) sont pourtant celles de la série corrigée (réel : 39 / 27 / 17 / 14 / 3).
- Pour le secteur, la publication donne les deux chiffres : 1 495 TWh en réel, 1 533 en corrigé (A p. 40).
- Définition (A p. 91) : « Consommation corrigée des variations climatiques : consommation qui aurait été observée si les températures hivernales […] avaient été égales à la moyenne de celles constatées sur une période de référence (soit 1991-2000). La consommation non corrigée est qualifiée de réelle. » **Anomalie dans la source** : la méthodologie du bilan (mars 2026, E, chapitre 09, p. 135) dit « période de référence, couvrant les années 1991 à 2020 » avec une moyenne de 1 523 degrés-jours unifiés. « 1991-2000 » est très probablement une coquille du glossaire. À ne pas reprendre dans le jeu.
- À ne pas confondre : la même famille de documents donne aussi « 1 609 TWh » (consommation finale **y compris non énergétique**, A p. 36), « - 0,9 % en réel et - 1,6 % corrigé » (cette consommation finale totale, D PDF p. 3) et « 1 499 TWh » (consommation à usage énergétique **2024**, réel, page du Bilan 2024 synthèse, https://www.statistiques.developpement-durable.gouv.fr/bilan-et-chiffres-cles-de-lenergie-0). La consommation à usage énergétique 2025 fait 1 495 TWh réel (- 0,3 %) et 1 533 TWh corrigé (- 1,1 %) (D PDF p. 3 ; A p. 38).

#### Point 2. Les parts 2025 (pétrole environ 38 %, électricité environ 27 %) figurent-elles dans le texte ?

**Oui, dans les deux.**

- Texte de la publication (A p. 38 ; B) : « Depuis 1990, la part du pétrole de 50 % à 38 % en 2025, alors que celle des énergies renouvelables augmente de 8 % à 14 % et celle de l'électricité de 20 % à 27 %. » (La phrase est incomplète dans la source, il manque le verbe « passe ».)
- Infographie, version texte de la page de la publication (C) et PDF (C2) : « Pétrole : 38 % ; Électricité : 27 % ; Gaz naturel : 18 % ; Énergies renouvelables thermiques et déchets : 14 % ; Chaleur commercialisée : 3 % ; Charbon : moins de 1 % », et par secteur « Transports 33 %, Résidentiel 30 %, Industrie 18 %, Tertiaire 15 %, Agriculture 4 % ».
- Le gaz à 18 % n'est que dans l'infographie, pas dans le texte du chapitre. Les décimales du fichier (38,1 ; 26,8 ; 17,7 ; 14,1 ; 3,0 ; 0,3) ne sont publiées nulle part, elles se calculent à partir des TWh.
- Pour mémoire, l'édition 2025 donnait pour 2024 « de 20 % à 26 % » pour l'électricité (26,3 % ici) et 38 % pour le pétrole (A 2025 p. 38).

#### Point 3. Champ géographique et exclusions

**Champ** (A p. 38 ; B ; repris sous chaque graphique de la section) : « Champ : jusqu'à l'année 2010 incluse, le périmètre géographique est la France métropolitaine. À partir de 2011, il inclut en outre les cinq DROM. » La méthodologie (E, https://www.statistiques.developpement-durable.gouv.fr/media/9074/download?inline) précise : « Le champ géographique du bilan de l'énergie comprend, depuis le millésime 2011, la France métropolitaine et les cinq départements d'outre-mer (DROM). Pour les années antérieures, il est limité à la France métropolitaine. » La formulation de l'instantané est donc conforme. Les séries du fichier XLSX D le confirment (`NIVGEO` : `Métropole` jusqu'en 2010 inclus, `France` à partir de 2011, avec une rupture d'environ 35 TWh au total, voir 1.6).

**Ce que « consommation finale à usage énergétique » exclut** (A p. 91, définitions ; A p. 35, 36, 39, 41) :

- Définition : « consommation d'énergie, par combustion ou sous forme d'électricité, de toutes les branches de l'économie, à l'exception des quantités consommées par les producteurs et transformateurs d'énergie (par exemple : consommation propre d'une raffinerie) et des quantités de produits énergétiques transformés en d'autres produits. Elle est nette des pertes de distribution (par exemple : pertes en lignes électriques). »
- **Usages non énergétiques exclus** : « usages de l'énergie […] ne donnant pas lieu à une combustion. Il s'agit principalement d'utilisations de l'énergie en tant que matière première : produits pétroliers dans la pétrochimie, gaz naturel pour la fabrication d'engrais… ». Ils pèsent 114,30 TWh en 2025 (A p. 88 ; « 114 TWh », 7,5 % de moins qu'en 2024, A p. 35).
- **Branche énergie exclue** : usages internes de la branche énergie (74,75 TWh en 2025), pertes de transport et de distribution (45,91 TWh) et pertes de transformation (centrales, nucléaire comptabilisé en chaleur) (A p. 88). Les **hauts-fourneaux** sont rangés dans la branche énergie : « Charbon (hors hauts-fourneaux) » (A p. 38) explique pourquoi le charbon final n'est que de 5,3 TWh, alors que la consommation nette de charbon de la filière fonte est de 31 TWh (D PDF p. 2).
- **Hors du périmètre aussi** : exportations nettes d'électricité (94 TWh) et soutes aériennes et maritimes internationales (85 TWh) (A p. 36).
- Secteurs inclus : transports, résidentiel, industrie (construction incluse, hors hauts-fourneaux), tertiaire, agriculture-pêche (A p. 40 et 41).
- Étiquettes : « Pétrole » désigne les produits pétroliers raffinés. Les biocarburants incorporés, par exemple 7,1 % de l'énergie des transports, sont comptés avec les « énergies renouvelables thermiques et déchets » (A p. 42 : pour les transports, « 89,2 % » de produits pétroliers et « 7,1 % de biocarburants incorporés »). L'électricité d'origine renouvelable est dans « Électricité », pas dans « EnR et déchets » (14 %) (A p. 88 : colonnes « EnR électriques » et « EnR thermiques et déchets » distinctes).

#### Point 4. Licence et version anglaise

Voir la section 4 plus bas.

---

### 3. Les quatre notes « À savoir » : verdict et rédaction proposée

Les chiffres cités en parenthèses viennent des tableaux ci-dessus. Les longueurs sont comptées en caractères, espaces comprises ; la limite est 320.

#### Note 1

Texte prévu : « Le mix énergétique compte toutes les énergies consommées, pas seulement l'électricité : en 2025, le pétrole fait 38 % de la consommation finale à usage énergétique, l'électricité 27 %. »

**Verdict : confirmée, à nuancer.**

- 38 % et 27 % sont publiés (A p. 38, C, C2). Mais ces parts sont calculées sur les valeurs **corrigées du climat**. Sur les données réelles de 2025, le pétrole ferait 38,9 % (39 %) et le gaz 17,0 % (voir 1.4). La note doit donc dire « à climat corrigé », comme la note 2 le dit pour l'ensemble des chiffres.
- « Pétrole » = produits pétroliers raffinés ; les biocarburants sont ailleurs (point 3).
- Les chiffres sont provisoires (note 3).

Rédaction proposée (216 caractères) : « Le mix énergétique compte toutes les énergies consommées, pas seulement l'électricité. En 2025, à climat corrigé, le pétrole fait 38 % de la consommation finale à usage énergétique, l'électricité 27 % et le gaz 18 %. »

Sources : A p. 38 ; C ; C2 ; D xlsx ; A p. 88.

#### Note 2

Texte prévu : « La consommation finale est celle des utilisateurs (ménages, entreprises, transports, agriculture), hors usages non énergétiques ; les chiffres sont corrigés des variations climatiques. »

**Verdict : confirmée sur le fond, à corriger sur la liste des secteurs et à compléter.**

- « Corrigés des variations climatiques » : confirmé (point 1).
- « Hors usages non énergétiques » : confirmé (A p. 91 pour la définition, p. 88 pour les 114 TWh de 2025). Il faut aussi exclure **la consommation propre de la branche énergie** (raffineries, centrales, hauts-fourneaux) et les pertes ; l'instantané ne le dit pas.
- Les secteurs du SDES sont : résidentiel, tertiaire, transports, industrie, agriculture-pêche (A p. 40, 41, 45). « Ménages » n'est pas un secteur du SDES : les ménages sont dans le résidentiel et aussi dans les transports (voitures). « Entreprises » recouvre industrie et tertiaire, mais le tertiaire inclut des services non marchands que je n'ai pas vérifiés. Je propose donc les noms SDES. « Agriculture » doit être « agriculture et pêche ».

Rédaction proposée (282 caractères) : « La consommation finale est celle des utilisateurs : ménages, industrie, services, transports, agriculture et pêche. Elle exclut les usages non énergétiques (pétrochimie, engrais) et la consommation propre de la branche énergie. Les chiffres sont corrigés des variations climatiques. »

Si « ménages, industrie, services » est jugé trop libre par rapport au vocabulaire du SDES (résidentiel, industrie, tertiaire), écrire « résidentiel, tertiaire, industrie, transports, agriculture-pêche ».

Sources : A p. 91, p. 88, p. 38, p. 40 et p. 41 ; B.

#### Note 3

Texte prévu : « 2025 est provisoire. Jusqu'en 2010, le champ est la France métropolitaine ; les cinq départements d'outre-mer s'y ajoutent depuis 2011. »

**Verdict : confirmée, une précision utile.**

- Provisoire : « Les données portant sur l'année 2025 sont provisoires et susceptibles d'être révisées. » et « Chiffres arrêtés au 8 avril 2026. » (A p. 2 ; page d'accueil de l'édition numérique). La version provisoire du bilan est datée du 22/04/2026 (D) et le Bilan 2025 définitif n'est pas paru à la date de cette vérification : la page « Bilan et chiffres clés de l'énergie » (publiée le 30/09/2026) ne liste que le Bilan 2025 provisoire et le Bilan 2024 définitif. Le SDES écrit qu'il y a « une version provisoire dès le mois d'avril suivant l'année étudiée, une version courte définitive en fin d'année et une version longue au début de l'année suivante » (https://www.statistiques.developpement-durable.gouv.fr/bilan-et-chiffres-cles-de-lenergie-0). Une révision de 2025 est donc probable d'ici fin 2026 ; le fichier donne un ordre de grandeur de ce que ça change : 3 TWh sur le total de 2024 entre deux millésimes.
- Champ : repris mot pour mot (point 3). Les noms des cinq DROM ne figurent pas dans la définition du champ ; la carte des centrales électriques (A p. 70) montre Guadeloupe, Martinique, Guyane, La Réunion et Mayotte.
- Ajout utile : la rupture de champ crée un saut d'environ 2 % dans la série (+ 35 TWh en 2011) ; la comparaison 1990 / 2025 est donc légèrement biaisée (1.6).

Rédaction proposée (196 caractères) : « 2025 est provisoire et pourra être révisé. Jusqu'en 2010, le champ est la France métropolitaine ; les cinq départements d'outre-mer s'y ajoutent depuis 2011, ce qui crée une rupture dans la série. »

Sources : A p. 2 et p. 38 ; B ; C ; E (méthodologie) ; page Bilan et chiffres clés.

#### Note 4

Texte prévu : « La consommation primaire compte autrement le nucléaire (la chaleur dégagée, environ trois fois l'électricité produite) : ses parts ne sont pas celles de la consommation finale. »

**Verdict : confirmée.**

- A p. 32 : « la production nucléaire correspond à la chaleur dégagée par la réaction nucléaire évaluée par convention à environ le triple de la production d'électricité obtenue au final ». A p. 36 : « chaleur dont les deux tiers sont perdus lors de la conversion en énergie électrique ».
- Les chiffres 2025 : chaleur nucléaire 1 182 TWh (A p. 33) pour 373 TWh d'électricité nucléaire (A p. 72), soit un rapport de 3,2.
- Mix primaire réel 2025 (A p. 33) : « 43 % de chaleur nucléaire, 26 % de pétrole, 17 % d'énergies renouvelables et déchets (dont 1 % de déchets non renouvelables), 12 % de gaz naturel et 2 % de charbon », sur 2 558 TWh en réel (2 601 TWh en corrigé, A p. 35). C'est du **réel**, alors que le mix final est **corrigé** ; il ne faut pas les rapprocher à la décimale.
- Le nucléaire n'apparaît pas comme énergie dans la consommation finale : son électricité est comptée dans « Électricité » (27 %).

Rédaction proposée (250 caractères) : « La consommation primaire compte le nucléaire pour la chaleur du réacteur, environ trois fois l'électricité produite : 43 % de la consommation primaire en 2025, contre 26 % pour le pétrole. Ses parts diffèrent donc de celles de la consommation finale. »

Sources : A p. 32, 33, 35, 36 et 72.

#### Remarque hors des quatre notes

Libellé : le SDES écrit « chaleur commercialisée » (« chaleur vendue par les réseaux et chaleur cogénérée vendue », A p. 36) ; le fichier et les séries longues disent « chaleur vendue ». Pour rester proche de la source, préférer « chaleur commercialisée ».
La série de chaleur commence en 2000. Le total 1990 de 1 488,2 TWh **n'a donc pas de chaleur** et les parts de 1990 publiées (50 % / 8 % / 20 %) sont calculées sans elle.

---

### 4. Licence du site du SDES et version anglaise

#### Licence

- Mentions légales du site (H), rubrique « Propriété intellectuelle » : « Les publications et données mises à disposition sur le site du service des données et études statistiques (SDES) sont consultables et téléchargeables gratuitement sous licence ouverte telle que décrite dans le décret n°2017-638 ; sauf spécification contraire, elles peuvent être réutilisées à des fins commerciales et sans versement de redevances. La réutilisation des informations suppose que celles-ci ne soient pas altérées, que leur sens ne soit pas dénaturé et que leurs sources et la date de leur dernière mise à jour soient mentionnées : Service des données et études statistiques (ou SDES), enquête XXX. » Le lien du mot « décret n°2017-638 » pointe vers Légifrance : https://www.legifrance.gouv.fr/eli/decret/2017/4/27/2017-638/jo/texte.
- **Confirmé** : la licence ouverte du décret n° 2017-638 s'applique aux publications et données du site, « sauf spécification contraire ».
- Décret (I, lecture par résumé automatique, à relire sur Légifrance) : « Décret n° 2017-638 du 27 avril 2017 relatif aux licences de réutilisation à titre gratuit des informations publiques et aux modalités de leur homologation ». Il introduit un article D. 323-2-1 (le résumé ne nomme pas le code ; à ma connaissance, le code des relations entre le public et l'administration) qui cite « La licence ouverte de réutilisation d'informations publiques », avec l'Open Database License. Le décret **cite** la licence ; son texte intégral est publié par ailleurs (Licence Ouverte / Open Licence d'Etalab), que je n'ai pas consultée.
- Mention propre au PDF des Chiffres clés 2026 (A p. 95) : « © SDES – Reproduction partielle autorisée sous réserve de la mention de la source et de l'auteur. » Les deux textes sont compatibles (attribuer la source), mais ne sont pas identiques ; le premier est le plus large.
- Le PDF indique aussi « Infographie : Bertrand Gaillet » et l'infographie porte le crédit « CGDD/SDES, 2026 - Bertrand Gaillet ». Le jeu n'utilise que les chiffres ; reprendre l'image demanderait de citer ce crédit.
- Conditions à respecter pour le jeu : ne pas altérer ni dénaturer (indiquer que les parts à 0,1 près, les variations et les rapprochements 1990-2025 sont des calculs du jeu à partir des TWh), citer la source et la date de mise à jour.
- Attribution proposée : « SDES, Chiffres clés de l'énergie, édition 2026 (30/09/2026), d'après le Bilan énergétique de la France ; données provisoires arrêtées au 8 avril 2026. Licence ouverte (décret n° 2017-638). »
- La page de la publication elle-même (C) n'affiche aucune licence, elle renvoie seulement vers « Mentions légales ». Une licence propre au classeur « Données associées » n'est pas indiquée ; c'est donc la règle générale du site qui s'applique.

#### Version anglaise « Key Energy Figures – 2026 Edition »

- **Il existe un résumé en anglais, pas de page ni de PDF distinct.** Sur la page de la publication (C), sous le résumé français, figure un bloc intitulé « Key Energy Figures – 2026 Edition – September 2026 » : un paragraphe de sept phrases (par exemple « Renewable energies account for a growing share of the national energy mix, representing 24 % of primary energy production in France in 2025. »). Aucune des valeurs de l'instantané n'y figure.
- Cherché sans succès :
  - la page « English contents » du SDES (https://www.statistiques.developpement-durable.gouv.fr/english-contents), qui à la date du 2026-11-02 liste comme dernières publications en anglais : un PDF sur la désinformation climatique (09/07/2026), « Key Figures on Climate – 2025 Edition » (04/11/2025), « International climate change indicators » (29/08/2025) et « State of the environment in France » (04/07/2025) ;
  - la recherche du site avec le filtre « publication en anglais » et le mot « energy » : seulement « Renewable Energies and Energy Intensity » et « Energy-related CO2 emissions in the World » ;
  - la recherche « Key Energy Figures » : seule la page française « Chiffres clés de l'énergie – Édition 2026 » ressort ;
  - l'édition numérique (A/B) : la page est en français (`<html lang="fr">`), sans sélecteur de langue ; les adresses `.../en/...` testées renvoient la même page française ;
  - un PDF anglais à l'adresse `.../pdf/Key-Energy-Figures-2026.pdf` : n'existe pas (renvoie la page d'accueil de l'édition).
- Conclusion : si le jeu veut une source en anglais, il peut citer le résumé anglais de la page C, mais pour les chiffres il faut citer l'édition française (A ou B). Une traduction anglaise intégrale paraîtra peut-être plus tard ; elle n'existait pas le 2026-11-02.

---

### 5. Conclusion

#### Écarts et points d'attention (d'abord)

1. **Aucun chiffre de l'instantané n'est faux.** Les 23 valeurs (15 par énergie, 2 totaux, 6 parts) sont celles du millésime d'avril 2026 (Bilan provisoire 2025, Chiffres clés 2026), à l'arrondi près.
2. **Écart expliqué, 2024 selon le millésime** : le fichier suit l'édition 2026 (total 1 549,3). Le Bilan 2024 définitif (mars 2026) donne 1 552,3 (gaz 288,5 contre 286,6 ; électricité 409,3 contre 407,9), l'édition 2025 « 1 550 ». À citer avec « édition 2026 » et non avec les anciens bilans.
3. **Note 1 à corriger** : 38 % et 27 % valent à climat corrigé. En réel : 38,9 % (soit 39 %) pour le pétrole, 17,0 % pour le gaz. Ajouter « à climat corrigé ».
4. **Note 2 à corriger** : le SDES n'a pas de secteur « ménages » (résidentiel), « entreprises » ni « agriculture » seule (agriculture-pêche). Il faut ajouter l'exclusion de la branche énergie (hauts-fourneaux compris) et des pertes.
5. **Champ** : la comparaison 1990 / 2025 mélange métropole et France entière (rupture d'environ + 35 TWh en 2011). À périmètre constant : pétrole - 26,0 % (au lieu de - 22,0 %), total + 0,4 % (au lieu de + 3,0 %). Le total de 1990 ne comprend pas de chaleur (série à partir de 2000).
6. **Données provisoires** : le Bilan 2025 définitif n'est pas paru au 2026-11-02. Les chiffres sont arrêtés au 8 avril 2026 alors que la page est datée du 30/09/2026.
7. **Anomalies dans la source** (sans effet sur les valeurs) :
   - le glossaire des Chiffres clés 2026 (p. 91) donne la période de référence climatique « 1991-2000 », la méthodologie du bilan dit 1991 à 2020 (DJU0 = 1 523) ;
   - la page du bilan provisoire dit que la consommation à climat corrigé baisse de 9,6 % « par rapport à 2021 », le PDF dit « par rapport à 2012 » (la page indique par ailleurs une correction du 21 mai 2026, sur la production d'électricité, sans lien avec la consommation) ;
   - la phrase p. 38 « Depuis 1990, la part du pétrole de 50 % à 38 % » n'a pas de verbe.
8. **Eurostat** : pas de valeur 2025 (`nrg_bal_c` s'arrête à 2024). Eurostat est en données réelles : 2024 = 1 503,4 TWh contre 1 499,5 pour le SDES réel (+ 0,3 %, presque tout sur le pétrole, non expliqué par les documents lus) et 1 549,3 pour le fichier corrigé. L'ordre de grandeur est cohérent.
9. **Licence** : confirmée (licence ouverte du décret n° 2017-638, avec obligation de citer la source et la date de mise à jour, et de ne pas altérer le sens). Le PDF a en plus la mention « Reproduction partielle autorisée sous réserve de la mention de la source et de l'auteur ».
10. **Version anglaise** : un résumé en anglais sur la page de la publication, pas de page ni de PDF « Key Energy Figures – 2026 Edition » distinct.

#### Ce qui est confirmé sans réserve

- Corrigé du climat : oui (point 1).
- Parts 38 % et 27 % dans le texte du chapitre et dans l'infographie (point 2).
- Champ géographique conforme à la note 3 (point 3).
- Note 4 : nucléaire compté à environ trois fois l'électricité produite (A p. 32 ; 1 182 TWh de chaleur pour 373 TWh d'électricité en 2025).

#### URL consultées

SDES, documents lus en entier ou en partie :
- https://www.statistiques.developpement-durable.gouv.fr/chiffres-cles-de-lenergie-edition-2026
- https://www.statistiques.developpement-durable.gouv.fr/edition-numerique/chiffres-cles-energie/
- https://www.statistiques.developpement-durable.gouv.fr/edition-numerique/chiffres-cles-energie/7-consommation-finale-denergie-par-secteur.php
- https://www.statistiques.developpement-durable.gouv.fr/edition-numerique/chiffres-cles-energie/pdf/Chiffres-cles-energie-2026.pdf
- https://www.statistiques.developpement-durable.gouv.fr/media/9771/download (infographie 2026)
- https://www.statistiques.developpement-durable.gouv.fr/bilan-energetique-de-la-france-en-2025-donnees-provisoires
- https://www.statistiques.developpement-durable.gouv.fr/media/9287/download?inline (publication, avril 2026)
- https://www.statistiques.developpement-durable.gouv.fr/media/9283/download?inline (séries longues provisoires 2025)
- https://www.statistiques.developpement-durable.gouv.fr/media/9282/download?inline et https://www.statistiques.developpement-durable.gouv.fr/media/9281/download?inline (tableaux de synthèse et figures du bilan provisoire : téléchargés, seules les feuilles et en-têtes ont été listées)
- https://www.statistiques.developpement-durable.gouv.fr/bilan-et-chiffres-cles-de-lenergie-0
- https://www.statistiques.developpement-durable.gouv.fr/bilan-energetique-de-la-france-pour-2024
- https://www.statistiques.developpement-durable.gouv.fr/bilan-energetique-de-la-france-en-2024-synthese
- https://www.statistiques.developpement-durable.gouv.fr/media/8958/download?inline (séries longues 2024 définitives)
- https://www.statistiques.developpement-durable.gouv.fr/media/9074/download?inline (méthodologie du bilan, mars 2026)
- https://www.statistiques.developpement-durable.gouv.fr/media/9087/download?inline (publication Bilan 2024, téléchargée, non exploitée)
- https://www.statistiques.developpement-durable.gouv.fr/chiffres-cles-de-lenergie-edition-2025
- https://www.statistiques.developpement-durable.gouv.fr/media/9755/download?inline (PDF édition 2025)
- https://www.statistiques.developpement-durable.gouv.fr/media/8710/download?inline (classeur édition 2025)
- https://www.statistiques.developpement-durable.gouv.fr/mentions-legales
- https://www.statistiques.developpement-durable.gouv.fr/english-contents
- https://www.statistiques.developpement-durable.gouv.fr/recherche?publications%5Bpublication_anglais%5D=publication_anglais&text=energy
- https://www.statistiques.developpement-durable.gouv.fr/recherche?text=Key%20Energy%20Figures et https://www.statistiques.developpement-durable.gouv.fr/recherche?text=key%20energy

Autres :
- https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/nrg_bal_c?format=JSON&lang=EN&geo=FR&nrg_bal=FC_E&nrg_bal=FC_OTH_HH_E&unit=GWH&time=1990&time=2023&time=2024&time=2025&siec=TOTAL&siec=O4000XBIO&siec=G3000&siec=E7000&siec=C0000&siec=RA000&siec=H8000&siec=W6100_6220&siec=R5110-5150_W6000RI&siec=N900H (2025 demandé, non renvoyé ; `C0000` non renvoyé)
- https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/nrg_bal_c?format=JSON&lang=EN&geo=FR&nrg_bal=FC_E&siec=TOTAL&unit=GWH&sinceTimePeriod=2022
- https://www.legifrance.gouv.fr/eli/decret/2017/4/27/2017-638/jo/texte (lecture par résumé automatique)

Adresses de l'édition numérique `.../fr/livre?page=38`, `.../fr/donnees-cles`, `.../en/...` : renvoient l'application sans contenu exploitable ; seule l'adresse `.../7-consommation-finale-denergie-par-secteur.php` a donné le texte du chapitre.

Résumés de moteur de recherche (WebSearch), utilisés seulement pour trouver des pages, jamais comme valeur : requêtes sur « Chiffres clés de l'énergie édition 2026… », « Consommation finale énergétique par énergie… », « Key Energy Figures 2026 Edition… » et « Bilan énergétique de la France 2025 données définitives ». Un site miroir (fgeerolf.com) apparaît dans les résultats ; non consulté.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
