# `poverty` · Pauvreté

**Vérifiée le 02/11/2026** : double vérification sur le web, chiffres conformes (section « Double vérification ») ; l'unité du seuil corrigée avant d'entrer dans le kit (euros constants de 2024, `base: 2024`), et deux « À savoir » précisés (les ruptures de série, la comparaison des départements).

| Champ | Valeur |
| --- | --- |
| Indicateur | `poverty`, dossier « Économie » (`economy`), page de type carte, ticket #26 de l'app (statut `planned` : les chiffres et la fiche avant la page, qui vient avec la zone) |
| Données | `briefings/data/poverty.json`, écrit par `yarn briefings poverty` le 2026-11-02 |
| Sources | Insee, « Niveau de vie et pauvreté en 2024 », Insee Première n° 2117 du 9 juillet 2026, https://www.insee.fr/fr/statistiques/9019316 (anglais, autre identifiant : https://www.insee.fr/en/statistiques/9025469), jeu Melodi `DS_ERFS_RETROPOLE` (modifié le 2026-07-30 selon son catalogue) ; Insee, « Indicateurs sur les revenus et la pauvreté au niveau local en 2023 », https://www.insee.fr/fr/statistiques/8984752 (en français seulement), jeu Melodi `DS_FILOSOFI_CC` (2026-08-06) ; Licence Ouverte 2.0 |
| Séries | `rate` : taux de pauvreté au seuil de 60 % du niveau de vie médian, France métropolitaine, `PR_MD60`, annuel, 1996 à 2024, 29 points ; `poorPeople` : nombre de personnes pauvres, `NUM_PER_MD60` (publié en milliers, écrit en personnes), mêmes années ; `threshold` : seuil mensuel pour une personne seule, `PT_MD60`, en euros constants de 2024 (`base: 2024`), de 1 050 € en 1996 à 1 337 € en 2024 |
| Carte | `localRate` : taux de pauvreté de 97 départements (les 96 de la métropole et La Réunion), Filosofi 2023, `DS_FILOSOFI_CC`, de la Vendée (9,2 %) à La Réunion (36,4 %) ; seuil de 60 % du niveau de vie médian métropolitain |
| Chiffre clé | 15,4 % en 2024, stable après 15,4 % en 2023 |
| Règles | La série nationale est la série rétropolée sans rupture (ERFS) : ses valeurs avant 2020 diffèrent de la série longue des tableaux de l'Insee (1996 : 14,3 % contre 15,3 %). Le seuil est en euros de la dernière année : Melodi dit « en euros constants » sans l'année, le script lit ce libellé et prend la dernière année de la série, comme l'IP 2117 (« en euros constants de 2024 ») ; il s'arrête si le libellé ne dit plus « euros constants ». Les taux départementaux ne se lisent jamais à côté du taux national |
| Dates | Le jeu national porte la date de sa dernière modification dans le catalogue Melodi (30/07/2026), que la Licence Ouverte demande de citer ; l'IP 2117 est parue le 09/07/2026, avec les mêmes chiffres. Filosofi 2023 est paru le 05/05/2026, sa page de données le 06/08/2026 après une diffusion complémentaire |
| Première édition | À remplir à la publication |

## « À savoir »

1. Seuil à 60 % du niveau de vie médian ; champ : « France métropolitaine, personnes vivant dans un logement ordinaire, dans un ménage dont le revenu déclaré est positif ou nul et dont la personne de référence n'est pas étudiante » (IP 2117 ; tableau 2408345).
2. Environ 18 mois de décalage (2022 paru le 11/07/2024, 2023 le 07/07/2025, 2024 le 09/07/2026). Les ruptures de 2010, 2012 et 2020 sont neutralisées « en chaînant leurs évolutions à méthodologie constante » ; le point 2020 « présente des fragilités ». La note dit « neutralisant », pas « supprimant ».
3. Seuil en euros constants de 2024 (intitulé du tableau complémentaire 3 de l'IP 2117) : le millésime précédent donnait 1 288 € pour 2023, en euros de 2023, contre 1 314 € ici.
4. Filosofi 2023 ne se compare pas au taux national de l'ERFS (15,4 %) mais à son propre taux pour la France métropolitaine (15,9 %) ; « pour la Guadeloupe, la Guyane, la Martinique et Mayotte, aucune statistique n'est diffusée » (note d'accompagnement de Filosofi 2023).

Non repris : l'interdiction de comparer Filosofi 2023 aux millésimes 2012 à 2021 (le kit n'a que 2023) ; le taux Eurostat (EU-SILC, 15,9 % en 2024), une autre enquête.

À actualiser : l'Insee publie les chiffres de 2025 vers juillet 2027 ; tous les seuils changeront alors d'année de référence.

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans appeler l'API Melodi qu'utilise le script. Son rapport, tel quel (les numéros d'« À savoir » qu'il cite sont ceux du premier jet, cinq points) :

Date de la vérification : 2026-11-02. Je n'ai pas appelé l'API Melodi (`api.insee.fr/melodi`).

Méthode et limites :

- Les valeurs ont été relues dans les fichiers publiés sur insee.fr (xlsx de l'Insee Première n° 2117, xlsx des tableaux « Taux de pauvreté », « Personnes pauvres » et « Intensité de la pauvreté », CSV `FILOSOFI_CC_csv.zip` de la page 8984752), téléchargés par HTTP puis lus directement (pas de résumé par un modèle). Ce circuit est indépendant de l'API Melodi mais reste de l'Insee : ce n'est pas une confirmation par un producteur tiers.
- Confirmation tierce : Eurostat (API de diffusion, contexte), franceinfo (chiffres nationaux et date). Pour les taux départementaux 2023, je n'ai trouvé aucun relais de presse fiable ; les seules confirmations sont des publications de l'Insee (Insee Résultats n° « Niveau de vie et pauvreté des territoires en 2023 », Insee Flash La Réunion n° 317).
- Les pages résumées par WebFetch (franceinfo, IP 2004, page des seuils) sont citées pour ce qu'elles disent et signalées comme telles quand le résumé n'était pas décisif.
- La page `catalogue-donnees.insee.fr` (catalogue Melodi) est une application JavaScript sans contenu lisible sans navigateur : les dates « dernière modification » 2026-07-30 et 2026-08-06 n'ont donc pas pu être relues sur le catalogue lui-même.

### 1. Chiffres nationaux, série rétropolée sans rupture (ERFS, France métropolitaine)

Source principale pour toutes les lignes de cette section : fichier de données de l'Insee Première n° 2117, feuille « Tableau complémentaire 3 – Indicateurs de pauvreté de 1996 à 2024 » (`ip2117.xlsx`, https://www.insee.fr/fr/statistiques/fichier/9019316/ip2117.xlsx), recoupée avec le texte de la publication (https://www.insee.fr/fr/statistiques/9019316) et, pour 2020 à 2024, avec les tableaux https://www.insee.fr/fr/statistiques/2408282 et https://www.insee.fr/fr/statistiques/2408345.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Taux de pauvreté 60 %, 2024 (PR_MD60) | 15,4 % | 15,4 % (« Le taux de pauvreté est stable par rapport à 2023 à 15,4 % et reste ainsi à son plus haut niveau depuis 1996 ») | https://www.insee.fr/fr/statistiques/9019316 ; https://www.insee.fr/fr/statistiques/fichier/9019316/ip2117.xlsx ; franceinfo https://www.franceinfo.fr/societe/pauvrete/le-taux-de-pauvrete-se-stabilise-a-15-4-en-2024-en-france-son-plus-haut-niveau-selon-l-insee_8101586.html | Conforme |
| Taux 2023, « stable » | 15,4 % | 15,4 % (même valeur dans l'IP 2063 de 2025, qui disait déjà « 15,4 % après 14,4 % en 2022 ») | https://www.insee.fr/fr/statistiques/9019316 ; https://www.insee.fr/fr/statistiques/8600989 | Conforme |
| Taux 2022 | 14,4 % | 14,4 % | ip2117.xlsx ; https://www.insee.fr/fr/statistiques/2408282 | Conforme |
| Taux 2021 | 14,5 % | 14,5 % | ip2117.xlsx ; https://www.insee.fr/fr/statistiques/2408282 | Conforme |
| Taux 1996 | 14,3 % | 14,3 % en série rétropolée (tableau complémentaire 3). La série longue non rétropolée donne autre chose : 15,3 % (colonne « 1996 ») et 14,5 % (colonne « 1996¹ », dont la note 1 indique des données hors revenus financiers) | ip2117.xlsx ; https://www.insee.fr/fr/statistiques/fichier/2408282/reve-pauv-taux-seuil.xlsx | Conforme (série rétropolée). Écart expliqué si on le compare à la série longue |
| Taux 1997 | 14,0 % | 14,0 % en série rétropolée ; 14,2 % en série longue | mêmes fichiers | Conforme (série rétropolée). Écart expliqué si on le compare à la série longue |
| Personnes pauvres 2024 (NUM_PER_MD60) | 9 817 000 | 9 817 milliers (« Lecture : en 2024, au seuil de 60 % du niveau de vie médian, le nombre de personnes pauvres est de 9 817 000 ») | https://www.insee.fr/fr/statistiques/2408345 ; ip2117.xlsx | Conforme |
| Personnes pauvres 2023 | 9 792 000 | 9 792 milliers | ip2117.xlsx ; https://www.insee.fr/fr/statistiques/2408345 | Conforme |
| Personnes pauvres 1996 | 8 003 000 | 8 003 milliers en série rétropolée. Série longue non rétropolée : 8 616 milliers (colonne « 1996 ») et 8 179 milliers (« 1996¹ ») | ip2117.xlsx ; https://www.insee.fr/fr/statistiques/fichier/2408345/reve-pauv-nbre-personne-seuil.xlsx | Conforme (série rétropolée). Écart expliqué si on le compare à la série longue |
| Seuil mensuel 60 %, 2024 (PT_MD60) | 1 337 € | 1 337 € par mois et par unité de consommation (« 1 337 euros pour une personne seule, 2 005 euros pour un couple, + 401 euros par enfant de moins de 14 ans et 669 euros par enfant plus âgé ») | https://www.insee.fr/fr/statistiques/9019316 ; https://www.insee.fr/fr/statistiques/3564980 | Conforme |
| Seuil mensuel 2023 | 1 314 € | 1 314 € mais en euros constants de 2024. L'IP 2063 (juillet 2025) donnait 1 288 € pour 2023, en euros constants de 2023 | ip2117.xlsx (Figure 3) ; https://www.insee.fr/fr/statistiques/8600989 | Conforme à l'IP 2117. Écart expliqué avec l'IP 2063 (changement d'année de référence des prix) |
| Seuil mensuel 1996 | 1 050 € | 1 050 € en euros constants de 2024 (intitulé de la ligne : « Seuil de pauvreté (en euros constants de 2024 par mois) ») | ip2117.xlsx, tableau complémentaire 3 | Conforme. Le soupçon est fondé : ce n'est pas un montant courant de 1996 |
| Montant courant (nominal) du seuil 1996 | non fourni | Non trouvé : aucune série en euros courants depuis 1996 sur les pages consultées (tableaux 2408282, 2408345, 3564980, « Pauvreté monétaire en France depuis 1970 » 5371219 non lu en détail) | recherches sur insee.fr | Non trouvé |

### Question clé : le seuil rétropolé est-il en euros courants ou constants ?

Réponse : en euros constants de 2024 pour toute la série 1996-2024, selon l'intitulé explicite de la ligne dans le fichier de l'IP 2117 (« Seuil de pauvreté (en euros constants de 2024 par mois) », feuilles « Figure 3 » et « Tableau complémentaire 3 ») et dans la page https://www.insee.fr/fr/statistiques/3564980 (« Intensité de la pauvreté en euros 2024 constants », 2021 : 1 304, 2022 : 1 302, 2023 : 1 314, 2024 : 1 337).

Preuve par comparaison de deux millésimes de la même publication (mêmes années, base de prix différente) :

| Année | IP 2063, juillet 2025 (euros constants de 2023) | IP 2117, juillet 2026 (euros constants de 2024) | Rapport |
|---|---|---|---|
| 2017 | 1 224 | 1 249 | 1,0204 |
| 2019 | 1 258 | 1 284 | 1,0207 |
| 2022 | 1 276 | 1 302 | 1,0204 |
| 2023 | 1 288 | 1 314 | 1,0202 |

Le rapport est constant (environ 1,02) : c'est l'inflation 2024, +2,0 % en moyenne annuelle selon l'Insee (Informations rapides n° 6, 15/01/2025, https://www.insee.fr/fr/statistiques/8330913). Donc :

- 2024 : courant = constant (année de base), 1 337 €.
- 2023 : 1 288 € en euros de 2023 (valeur de l'IP 2063), 1 314 € en euros de 2024 (valeur du fichier). Le jeu ne doit pas présenter 1 314 € comme un montant « courant de 2023 ».
- 1996 : 1 050 € en euros de 2024. Les montants de la série changent à chaque millésime (le prochain sera exprimé en euros de 2025) : il faut étiqueter la série « euros constants de 2024 » et le millésime.

Autres sources notées : l'IP 2004 (11/07/2024, https://www.insee.fr/fr/statistiques/8216285) donnait 1 216 € pour 2022 ; la page ne dit pas explicitement la base de prix (le rapport 1 302 / 1 216 = 1,071, soit 1,049 x 1,020, est cohérent avec des euros de 2022, c'est une inférence).

### 2. Taux de pauvreté par département, Filosofi 2023 (DS_FILOSOFI_CC, PR_MD60)

Source du recoupement : `FILOSOFI_CC_csv.zip` de la page https://www.insee.fr/fr/statistiques/8984752 (fichier `DS_FILOSOFI_CC_2023_data.csv`, 97 lignes `GEO_OBJECT = DEP` pour `PR_MD60`, toutes renseignées ; statut d'observation `A` vérifié pour les cinq départements cités) et texte de l'Insee Résultats https://www.insee.fr/fr/statistiques/8984748 (tableau « Figure 2a – Taux de pauvreté par département en 2023 »).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Nombre de départements | 97 (96 métropolitains + La Réunion) | 97 codes : 01 à 95 sans le 20 (94), 2A, 2B, plus 974. Aucun code 971, 972, 973, 976 | CSV de https://www.insee.fr/fr/statistiques/8984752 | Conforme |
| Vendée (85) | 9,2 % | 9,2 % (« la Vendée (9,2 %) et la Haute-Savoie (10,2 %) sont les deux départements avec les plus faibles taux de pauvreté ») | https://www.insee.fr/fr/statistiques/8984748 ; CSV | Conforme |
| Haute-Savoie (74) | 10,2 % | 10,2 % | idem | Conforme |
| La Réunion (974) | 36,4 % | 36,4 % (« une part 2,3 fois plus élevée que dans l'Hexagone (15,9 %) ») | https://www.insee.fr/fr/statistiques/8984748 ; https://www.insee.fr/fr/statistiques/9061484 (Insee Flash La Réunion n° 317) ; CSV | Conforme |
| Seine-Saint-Denis (93) | 29,5 % | 29,5 % (plus élevé des départements métropolitains) | idem | Conforme |
| Pyrénées-Orientales (66) | 22,4 % | 22,4 % (deuxième taux le plus haut des 96 départements métropolitains après la Seine-Saint-Denis, dans le CSV) | tableau de https://www.insee.fr/fr/statistiques/8984748 ; CSV | Conforme |
| Rang « le plus haut / le plus bas » | La Réunion plus haut, Vendée plus bas | Confirmé par le CSV (tri des 97 valeurs) et par le texte de l'Insee | CSV ; https://www.insee.fr/fr/statistiques/8984748 | Conforme |
| Taux Filosofi 2023 France métropolitaine (pour comparer) | non fourni | 15,9 % (ligne `FRANCE`/`FM` du CSV ; « Hexagone (15,9 %) » dans le Flash La Réunion). France métropolitaine + La Réunion : 16,2 % | CSV ; https://www.insee.fr/fr/statistiques/9061484 ; https://www.insee.fr/fr/statistiques/8984748 | Information (utile pour l'affirmation 4) |

Remarque : dans Filosofi le seuil est « fixé à 60 % du niveau de vie médian métropolitain » (encadré de https://www.insee.fr/fr/statistiques/8984748, et libellé de `PR_MD60` sur https://www.insee.fr/fr/statistiques/8984752). Le taux de La Réunion est donc mesuré avec le seuil de la métropole, pas avec une médiane réunionnaise.

### 3. Dates et versions anglaises

| Élément | Valeur du fichier / du ticket | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Parution de l'IP 2117 « Niveau de vie et pauvreté en 2024 » | 09/07/2026 | « Paru le 09/07/2026 » (jeudi 9 juillet 2026 ; franceinfo : « Publié le 09/07/2026 18:40 », « annonce l'Insee jeudi 9 juillet ») ; auteurs Christelle Rieg et Arnaud Rousset | https://www.insee.fr/fr/statistiques/9019316 ; franceinfo (URL ci-dessus) | Conforme |
| Parution des tableaux nationaux (2408282, 2408345, 3564980) | non fourni | « Paru le 09/07/2026 », « Juillet 2026 » | https://www.insee.fr/fr/statistiques/2408282 ; https://www.insee.fr/fr/statistiques/2408345 ; https://www.insee.fr/fr/statistiques/3564980 | Conforme au ticket |
| Jeu national Melodi « dernière modification » | 2026-07-30 | Aucune mention du 30/07/2026 sur les pages insee.fr consultées (IP 2117, trois tableaux, page départementale). Dates de modification internes des xlsx : 2026-07-06 (`ip2117.xlsx`) et 2026-06-22 (`reve-pauv-nbre-personne-seuil.xlsx`). Les valeurs sont identiques à celles du snapshot | pages et fichiers ci-dessus | Non trouvé (la date du 30/07 n'est ni confirmée ni contredite ; hypothèse : rechargement ou mise à jour de métadonnées postérieurs à la parution, sans effet sur les chiffres) |
| Parution de la page départementale « Indicateurs sur les revenus et la pauvreté au niveau local en 2023 » | 2026-08-06 (Melodi) | « Paru le 06/08/2026 », « Insee Résultats – Août 2026 », avec l'avis daté du 06/08/2026 « Diffusion complémentaire des taux de pauvreté et géographie de diffusion » (erreur technique : taux de pauvreté non diffusé pour un nombre important de territoires, corrigée). Les fichiers du zip portent la date interne 2026-07-17 | https://www.insee.fr/fr/statistiques/8984752 | Conforme à la date Melodi du 06/08/2026 |
| Première diffusion de Filosofi 2023 | non fourni | L'étude Insee Résultats « Niveau de vie et pauvreté des territoires en 2023 » est « Paru le 05/05/2026 » (avec un avertissement du 20/07/2026 : niveaux de vie médians de La Réunion et de la Seine-Saint-Denis inversés dans le texte, corrigés). La date du 06/08/2026 de la page de données est donc au moins la date d'une diffusion complémentaire. Je n'ai pas pu consulter une archive de la page de données (Wayback Machine : erreur 429) | https://www.insee.fr/fr/statistiques/8984748 | Écart expliqué (à signaler si le jeu écrit « publié en août 2026 ») |
| Version anglaise de l'IP 2117 | « à une autre adresse ? » | Oui : « Standards of Living and Poverty in 2024 », Insee Première n° 2117, juillet 2026, « Paru le 09/07/2026 ». `https://www.insee.fr/en/statistiques/9019316` renvoie 404 | https://www.insee.fr/en/statistiques/9025469 | Conforme (existe, autre identifiant 9025469) |
| Version anglaise de la page départementale 8984752 | « à une autre adresse ? » | Pas de page anglaise à la même référence (`/en/statistiques/8984752` : 404 ; `?lang=en` renvoie le texte français). Contrepartie anglaise la plus proche : « Household income and poverty in 2023 – Localised disposable income system (Filosofi) », « Paru le 06/08/2026 », outil de résultats par zone géographique (équivalent de la page française 8986545 « Revenus et pauvreté des ménages en 2023 »), pas une traduction de la page 8984752. L'Insee Résultats 8984748 n'a pas non plus de version `/en/` (404) | https://www.insee.fr/en/statistiques/8988612 ; https://www.insee.fr/fr/statistiques/8986545 | Écart expliqué (pas de traduction de la page ; une page anglaise voisine, autre identifiant) |
| Lien « English » des pages françaises | n/a | Le lien pointe vers `/langue/en`, un sélecteur de langue du site, pas vers une traduction de la page | https://www.insee.fr/fr/statistiques/9019316 | Information |

Rythme de publication des données nationales : IP 2004 (données 2022) paru le 11/07/2024 (https://www.insee.fr/fr/statistiques/8216285), IP 2063 (données 2023) paru le 07/07/2025 (https://www.insee.fr/fr/statistiques/8600989), IP 2117 (données 2024) paru le 09/07/2026.

### 4. Les cinq affirmations « À savoir »

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| (1) Seuil à 60 % du niveau de vie médian ; taux national sur la France métropolitaine, personnes en logement ordinaire | Affirmation du texte « À savoir » | Confirmé : « le seuil de pauvreté monétaire est défini en France et en Europe à 60 % du niveau de vie médian de l'ensemble de la population » ; champ : « France métropolitaine, personnes vivant dans un logement ordinaire, dans un ménage dont le revenu déclaré est positif ou nul et dont la personne de référence n'est pas étudiante » (63,8 millions de personnes fin 2024 ; institutions et sans-domicile exclus) | https://www.insee.fr/fr/statistiques/9019316 ; https://www.insee.fr/fr/statistiques/2408345 | Conforme |
| (2) Données publiées environ un an et demi après (2024 en juillet 2026) | idem | Confirmé : 2022 paru le 11/07/2024, 2023 le 07/07/2025, 2024 le 09/07/2026, soit environ 18 mois après la fin de l'année. Nuance : Filosofi 2023 (départements) est paru le 05/05/2026 (compléments le 06/08/2026), soit plus de 2 ans après la fin de 2023, et Filosofi 2022 n'a pas pu être produit (note d'accompagnement) | https://www.insee.fr/fr/statistiques/9019316 ; https://www.insee.fr/fr/statistiques/8600989 ; https://www.insee.fr/fr/statistiques/8216285 ; https://www.insee.fr/fr/statistiques/8984748 ; note https://www.insee.fr/fr/statistiques/fichier/8984752/Note_accompagnement_Filosofi_2023.pdf | Conforme pour le national. À nuancer pour les départements |
| (3) Série longue avec ruptures (2010, 2012, 2020) ; la série rétropolée les supprime | idem | Confirmé : « la mesure des revenus dans les ERFS a fait l'objet d'améliorations qui génèrent trois ruptures de séries, en 2010, 2012 et 2020, avec deux enquêtes disponibles pour chaque millésime. [...] les indicateurs ont été rétropolés jusqu'en 1996 en chaînant leurs évolutions à méthodologie constante ». Précisions : la rétropolation couvre 1996 à 2020 et peut différer des séries longues publiées ailleurs sur insee.fr ; le point 2020 « présente des fragilités liées aux difficultés de production en 2020 » ; exemples d'écart entre séries : taux 1996 = 15,3 % (série longue) contre 14,3 % (rétropolée) | https://www.insee.fr/fr/statistiques/9019316 ; https://www.insee.fr/fr/statistiques/2408282 ; ip2117.xlsx | Conforme (formule « supprime les ruptures » : plutôt « les neutralise en chaînant les évolutions » ; la fragilité de 2020 subsiste) |
| (4) Les taux départementaux (Filosofi 2023) ne se comparent ni au taux national ni aux années Filosofi 2012-2021 | idem | Confirmé pour 2012-2021 : « les indicateurs 2023 issus du dispositif Filosofi 2 ne sont pas directement comparables avec les indicateurs issus de Filosofi (millésimes 2012 à 2021) » ; la note d'accompagnement va plus loin : « toute analyse [...] comparant les données de Filosofi et celles de Filosofi 2 est à proscrire ». Confirmé pour le national : « Au niveau national, l'ERFS reste la source de référence » ; Filosofi donne 15,9 % pour la métropole en 2023, contre 15,4 % pour l'ERFS (champs et traitements différents, étudiants notamment). Nuance : on peut comparer un département à 15,9 % (France métropolitaine, même source et même seuil), pas à 15,4 % | https://www.insee.fr/fr/statistiques/8984752 ; https://www.insee.fr/fr/statistiques/fichier/8984752/Note_accompagnement_Filosofi_2023.pdf ; https://www.insee.fr/fr/statistiques/8984748 (encadré) | Conforme, avec la nuance sur le 15,9 % |
| (5) Filosofi ne couvre pas Guadeloupe, Martinique, Guyane et Mayotte en 2023 (ou dire quels DROM sont couverts) | idem | Confirmé : « Pour la Guadeloupe, la Guyane, la Martinique et Mayotte, aucune statistique n'est diffusée » (cause : une part importante de la population n'est pas rattachée à un logement). « Ces résultats portent sur la France métropolitaine et La Réunion » ; « La Réunion est le seul département et région d'outre-mer (Drom) couvert ». Formulation : l'Insee parle de non-diffusion, pas d'absence de couverture de l'ensemble du dispositif | https://www.insee.fr/fr/statistiques/fichier/8984752/Note_accompagnement_Filosofi_2023.pdf ; https://www.insee.fr/fr/statistiques/8984752 ; https://www.insee.fr/fr/statistiques/9061484 | Conforme |

### 5. Contexte Eurostat (autre source, autre concept)

Données Eurostat `ilc_li02` (EU-SILC, taux de risque de pauvreté au seuil de 60 % de la médiane, population totale), interrogées par l'API de diffusion Eurostat le 2026-11-02 (jeu mis à jour le 2026-10-20) : https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/ilc_li02 (paramètres `geo=FR&geo=EU27_2020&age=TOTAL&sex=T&rskpovth=B_60&sinceTimePeriod=2021`, unité PC, statinfo MED_EI).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| France, taux de risque de pauvreté 60 %, 2023 | 15,4 % (ERFS) | 15,4 % (SILC) | Eurostat ilc_li02 | Conforme (hasard de concordance possible entre deux sources) |
| France, 2024 | 15,4 % (ERFS) | 15,9 % (SILC) | Eurostat ilc_li02 | Écart expliqué (autre enquête, autre champ : EU-SILC contre ERFS métropole en logement ordinaire ; à ne pas mélanger) |
| France, 2025 (hors fichier) | non fourni | 16,3 % (SILC) ; 2022 : 15,6 % (rupture de série signalée `b`) | Eurostat ilc_li02 | Information |
| UE27, 2024 | non fourni | 16,2 % (2025 : 16,3 %) | Eurostat ilc_li02 | Information |

### Conclusion

Aucun écart réel sur les valeurs. Les 12 valeurs nationales (6 taux, 3 nombres de personnes pauvres, 3 seuils) et les 5 taux départementaux du fichier sont identiques aux publications de l'Insee consultées en dehors de l'API Melodi. Les deux points à traiter sont des libellés, pas des chiffres :

1. Unité du seuil mensuel : toute la série `PT_MD60` (1 050 € en 1996, 1 314 € en 2023, 1 337 € en 2024) est en euros constants de 2024. Il faut l'écrire dans le jeu (« euros de 2024 ») et ne pas la comparer à des montants nominaux. En particulier, 1 314 € n'est pas le seuil « courant » de 2023 (l'IP 2063 donnait 1 288 € en euros de 2023, soit 1 314 € divisé par 1,0202). Le montant courant de 1996 n'a pas été trouvé.
2. Série : les valeurs 1996 et 1997 (14,3 % et 14,0 %) viennent de la série rétropolée. La série longue des tableaux insee.fr 2408282 et 2408345 donne d'autres valeurs avant 2020 (1996 : 15,3 %, 8 616 milliers ; 1997 : 14,2 %). Les deux séries coïncident à partir de 2020.

Points de vigilance sur les dates et les formulations :

- Date de l'IP 2117 : 09/07/2026, confirmée par l'Insee et par franceinfo.
- Date Melodi du jeu national (2026-07-30) : non retrouvée sur insee.fr (rien de contradictoire, les valeurs sont identiques à celles du 09/07). Date du jeu départemental (2026-08-06) : cohérente avec la page 8984752.
- Filosofi 2023 est sorti le 05/05/2026 (Insee Résultats 8984748) ; le 06/08/2026 est la date de la page de données, après une diffusion complémentaire. « Publié en août 2026 » serait donc imprécis.
- Affirmation 2 : vraie pour le national (environ 18 mois), plus longue pour Filosofi (plus de 2 ans, et 2022 manquant).
- Affirmation 4 : la formulation « ne se compare pas au taux national » devrait préciser « 15,4 % de l'ERFS » ; le taux de référence pour comparer un département est le 15,9 % de Filosofi 2023 pour la France métropolitaine (16,2 % avec La Réunion).
- Affirmation 3 : « la série rétropolée supprime les ruptures » est une simplification (chaînage des évolutions à méthodologie constante) ; le point 2020 reste signalé comme fragile.
- Versions anglaises : l'IP 2117 existe en anglais à l'adresse `/en/statistiques/9025469`. La page 8984752 n'a pas de traduction ; la page anglaise la plus proche est `/en/statistiques/8988612` (autre contenu, outil par zone géographique).

### URLs consultées (2026-11-02)

Insee, publications et tableaux nationaux :
- https://www.insee.fr/fr/statistiques/9019316 (IP 2117, page HTML lue)
- https://www.insee.fr/fr/statistiques/fichier/9019316/ip2117.xlsx (données de l'IP 2117, lues)
- https://www.insee.fr/fr/statistiques/fichier/9019316/ip2117.pdf (le PDF renvoyé par l'outil de lecture est une figure isolée, inexploitable ; la page HTML et le xlsx ont servi à la place)
- https://www.insee.fr/en/statistiques/9025469 (IP 2117 en anglais)
- https://www.insee.fr/fr/statistiques/2408282 et https://www.insee.fr/fr/statistiques/fichier/2408282/reve-pauv-taux-seuil.xlsx (taux, série longue)
- https://www.insee.fr/fr/statistiques/2408345 et https://www.insee.fr/fr/statistiques/fichier/2408345/reve-pauv-nbre-personne-seuil.xlsx (nombre de personnes pauvres, série longue)
- https://www.insee.fr/fr/statistiques/3564980 (intensité de la pauvreté et seuils, euros 2024 constants)
- https://www.insee.fr/fr/statistiques/8600989 (IP 2063, données 2023, euros constants de 2023)
- https://www.insee.fr/fr/statistiques/8216285 (IP 2004, données 2022)
- https://www.insee.fr/fr/statistiques/8330913 (Informations rapides n° 6, inflation 2024 : +2,0 %)

Insee, Filosofi 2023 :
- https://www.insee.fr/fr/statistiques/8984752 (page départementale ; lue en HTML)
- https://www.insee.fr/fr/statistiques/fichier/8984752/FILOSOFI_CC_csv.zip (CSV `DS_FILOSOFI_CC_2023_data.csv`, lu)
- https://www.insee.fr/fr/statistiques/fichier/8984752/Note_accompagnement_Filosofi_2023.pdf (note « Refonte du dispositif Filosofi », lue)
- https://www.insee.fr/fr/statistiques/8984748 (Insee Résultats « Niveau de vie et pauvreté des territoires en 2023 », 05/05/2026)
- https://www.insee.fr/fr/statistiques/9061484 (Insee Flash La Réunion n° 317, 06/10/2026)
- https://www.insee.fr/fr/statistiques/8986545 et https://www.insee.fr/en/statistiques/8988612 (outil par zone géographique, FR et EN, 06/08/2026)
- Tests d'adresses anglaises : https://www.insee.fr/en/statistiques/9019316, /8984752, /8984748, /8986545, /2408282, /2408345 (tous 404) ; https://www.insee.fr/fr/statistiques/9019316?lang=en et https://www.insee.fr/fr/statistiques/8984752?lang=en (renvoient le texte français)
- https://catalogue-donnees.insee.fr/fr/catalogue/recherche/DS_FILOSOFI_CC et https://catalogue-donnees.insee.fr/fr/catalogue/recherche/DS_ERFS_RETROPOLE (coquille JavaScript, sans contenu lisible)

Autres sources :
- https://www.franceinfo.fr/societe/pauvrete/le-taux-de-pauvrete-se-stabilise-a-15-4-en-2024-en-france-son-plus-haut-niveau-selon-l-insee_8101586.html (presse, chiffres nationaux et date du 09/07/2026)
- https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/ilc_li02 (Eurostat, API de diffusion, contexte)
- Tentative de consultation de la Wayback Machine (`archive.org/wayback/available`) pour l'historique de la page 8984752 : erreur 429, sans résultat

Les fichiers téléchargés et les scripts de lecture sont restés dans l'espace de travail de la session de vérification. Aucun fichier du dépôt n'a été modifié.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
