# `unemployment` · Chômage

**Vérifiée le 02/11/2026** : double vérification sur le web, chiffres conformes (section « Double vérification ») ; deux « À savoir » reformulés avant d'entrer dans le kit (le champ du taux national, le statut des taux par département).

| Champ | Valeur |
| --- | --- |
| Indicateur | `unemployment`, dossier « Travail et retraites » (`work`), page de type série avec une carte des départements, ticket #140 de l'app (statut `planned` : les chiffres et la fiche avant la page) |
| Données | `briefings/data/unemployment.json`, écrit par `yarn briefings unemployment` le 2026-11-02, puis le 2026-11-12 (« Mises à jour ») |
| Sources | Insee, « Enquête emploi en continu », https://www.insee.fr/fr/metadonnees/source/serie/s1223 (anglais : https://www.insee.fr/en/metadonnees/source/serie/s1223), Informations rapides n° 192 du 7 août 2026 ; Insee, « Taux de chômage localisés », https://www.insee.fr/fr/statistiques/2012804 (en français seulement), Informations rapides n° 223 du 18 septembre 2026 ; France Travail et Dares, « Statistiques trimestrielles France Travail » (STMT, CVS-CJO), https://statistiques.francetravail.org/stmt/publication, publiées le 28 octobre 2026, séries lues dans la BDM de l'Insee ; Licence Ouverte 2.0 (pour France Travail : licence indiquée sur la fiche data.gouv.fr du jeu, non sur ses pages) |
| Séries | `rate` : taux de chômage au sens du BIT, France (Mayotte comprise), BDM `011818543`, trimestriel, 2003-T1 à 2026-T3, 95 points ; `youthRate` : taux des 15-24 ans, BDM `011818548`, mêmes périodes ; `employmentRate` : taux d'emploi des 15-64 ans, BDM `011818676`, mêmes périodes ; `rateSince1975` : taux de chômage France hors Mayotte, BDM `001688527`, 1975-T1 à 2026-T3, 207 points ; `jobseekersA` : demandeurs d'emploi inscrits en catégorie A, France hors Mayotte, BDM `010597456`, 1996-T1 à 2026-T3, 123 points ; `jobseekersAbc` : catégories A, B, C, BDM `010597571`, mêmes périodes |
| Carte | `localRate` : taux de chômage localisé de 100 départements (sans Mayotte), jeu BDM `TAUX-CHOMAGE`, 2026-T2, statut semi-définitif selon la BDM (« provisoire » sur la page de l'Insee) ; du Cantal (4,8 %) à la Guyane (20,4 %) |
| Chiffre clé | 8,2 % au 3e trimestre 2026, en baisse après 8,3 % |
| Règles | Le chiffre clé est le taux BIT de la France entière. L'ensemble et les 15-24 ans « France entière » partent de 2003-T1 : l'Insee les publie depuis 1975 depuis le 10/11/2026, et le script n'en garde que 2003-T1 et après, comme la page ; la série longue reste `rateSince1975`, hors Mayotte (PO, 12/11/2026). Les inscrits à France Travail restent une série à part, jamais additionnée ni comparée au taux BIT. Le statut des départements est le moins définitif de leurs valeurs du trimestre (`leastDefinitive`) |
| Première édition | À remplir à la publication |

## « À savoir »

1. Chômeurs BIT et inscrits à France Travail : « deux concepts différents », les populations « ne se recouvrent qu'en partie » (Insee, L'essentiel sur le chômage, https://www.insee.fr/fr/statistiques/4805248).
2. Depuis l'IR n° 192 du 7 août 2026, le champ principal est la France, Mayotte comprise ; la série hors Mayotte reste publiée (tableau 5) ; les taux localisés gardent le champ « France hors Mayotte » (IR n° 223). La phrase d'abord prévue, « la série France métropolitaine s'est arrêtée », n'est pas soutenue : elle n'est pas reprise. « Rétropolé jusqu'en 2003 » n'est pas repris non plus : l'Insee publie le taux de chômage « France » depuis 1975 dans son fichier, la série BDM du script commençant en 2003.
3. Inscription automatique depuis janvier 2025 des bénéficiaires du RSA, des jeunes suivis par les missions locales et des personnes handicapées suivies par Cap emploi ; l'Insee parle d'une hausse « mécanique » des inscrits. Le mot « rupture » n'est pas celui des sources : la note dit « mécaniquement ».
4. « Les données sont provisoires pour le dernier trimestre et révisées pour les trimestres précédents » (IR n° 223) ; la BDM marque le trimestre « semi-définitif ». La note dit « pas définitifs », vrai pour les deux. Réserve de l'Insee sur les départements d'outre-mer : moyennes annuelles conseillées.

Non repris : la marge d'incertitude de ±0,3 point (utile à la page, qui dira la hausse sans la grossir) ; la catégorie A hors publics de la loi pour le plein emploi (+0,3 % sur le trimestre), une série que le script ne lit pas.

À actualiser : le 3e trimestre 2026, publié par l'Insee le 10/11/2026, est entré le 12/11/2026 (« Mises à jour ») ; les taux localisés le 6 janvier 2027 ; France Travail le 28 janvier 2027.

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans appeler l'API de la BDM qu'utilise le script. Son rapport, tel quel :


Date de la vérification : 2026-11-02. Méthode : sources autres que l'API `api.insee.fr` (pages et fichiers publiés sur insee.fr, Informations rapides, fichiers `sl_chomage.xlsx` / `sl_indicateurs.xlsx` joints à l'IR n° 192, pages France Travail / data.gouv.fr, Eurostat, presse). Aucun fichier du projet n'a été modifié.

Légende : Conforme / Écart expliqué (le chiffre est bon, la formulation ou le périmètre demande une précision) / Écart (le texte du snapshot n'est pas soutenu par la source) / Non trouvé.

### 1. Taux de chômage BIT, France y compris Mayotte (BDM 011818543)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Taux de chômage 2026-T2 (clé) | 8,3 % | 8,3 % de la population active, « +0,2 point » sur le trimestre, +0,7 point sur un an, 2,7 millions de chômeurs (2 677 000), plus haut depuis le T3 2020 | https://www.insee.fr/fr/statistiques/9032359 (IR n° 192, PDF https://www.insee.fr/fr/statistiques/fichier/version-html/9032359/IR192_Chomage_2T2026.pdf) ; version anglaise https://www.insee.fr/en/statistiques/9033057 | Conforme |
| Sens de la variation (« up ») | hausse vs 2026-T1 | +0,2 point (8,1 % -> 8,3 %) | idem ; tableau `Tab1` de `sl_chomage.xlsx` (https://www.insee.fr/fr/statistiques/fichier/9032359/Chomage2026T2.zip) | Conforme |
| 2026-T1 | 8,1 % | 8,1 % (aussi 8,1 % hors Mayotte à la publication du 13 mai 2026) | IR 192 ; https://www.insee.fr/fr/statistiques/2532173 ; https://www.lafinancepourtous.com/2026/05/13/le-chomage-atteint-81-en-france-debut-2026/ | Conforme |
| 2025-T4 | 8,0 % | 8,0 % (série « France », Mayotte incluse ; la série d'origine hors Mayotte donnait 7,9 %) | `sl_chomage.xlsx` onglets `Tab1` (8,0) et `Tab4` (publication T4 2025 : 7,9 hors Mayotte) ; page https://www.insee.fr/fr/statistiques/2532173 (suite 2025-T1 à 2026-T2 : 7,5 / 7,6 / 7,8 / 8,0 / 8,1 / 8,3) | Conforme |
| 2003-T1 | 8,4 % | 8,4 % (`Tab1`, ligne T1.2003 ; identique dans `Tab5` hors Mayotte) | `sl_chomage.xlsx` (zip ci-dessus) | Conforme |
| Début de la série « France » | trimestriel depuis 2003 (BDM) | Le tableau 1 de l'Insee « Taux de chômage BIT en France » commence au T1 1975 (3,2 % ; la note Insee parle d'une rétropolation annuelle 1982-2023 puis d'une conversion trimestrielle « avec la même profondeur temporelle qu'auparavant », soit 1975 pour le taux de chômage et 2003 pour les autres indicateurs). La date de début propre à l'idbank 011818543 n'est pas vérifiable hors API | `sl_chomage.xlsx` (Index : « Tableau 1. Taux de chômage au sens du BIT en France depuis 1975 ») ; IR 192 ; note https://www.insee.fr/fr/statistiques/documentation/Note_methodologique_2026T2.pdf | Écart expliqué (à vérifier : « depuis 2003 » vaut pour le taux d'emploi et la plupart des indicateurs, pas pour le taux de chômage publié depuis 1975) |
| Identifiant 011818543 | BDM | Aucune page publique trouvée citant cet idbank (les pages de séries `statistiques/series/...` sont rendues en JavaScript et illisibles hors navigateur) | recherche web, https://www.insee.fr/fr/statistiques/series/103167923 | Non trouvé (valeurs confirmées par les fichiers Insee, pas l'identifiant) |

### 2. Autres indicateurs BIT

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Taux de chômage des 15-24 ans (BDM 011818548), 2026-T2 | 21,6 % | 21,6 % (+0,4 point) | IR 192 (tableau « Taux de chômage BIT », ligne 15-24 ans) ; https://www.insee.fr/fr/statistiques/2532173 | Conforme |
| idem, 2026-T1 | 21,2 % | 21,2 % | IR 192 ; `Tab1` | Conforme |
| Taux d'emploi 15-64 ans (BDM 011818676), 2026-T2 | 69,0 % | 69,0 % (-0,3 point, -0,5 point sur un an) | IR 192 (« Taux d'emploi BIT dans la population des 15-64 ans ») ; `sl_indicateurs.xlsx` onglet `Tab1` | Conforme |
| idem, 2026-T1 | 69,3 % | 69,3 % (2025-T4 aussi 69,3 %) | idem | Conforme |
| Marge d'incertitude (pour mémoire) | non indiquée | ±0,3 point sur le niveau du taux de chômage et sur son évolution trimestrielle ; ±0,4 point sur le taux d'emploi | IR 192 ; note méthodologique 2T2026 | Information utile (non contradictoire) |

### 3. Taux de chômage BIT hors Mayotte (BDM 001688527)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 1975-T1 | 3,2 % | 3,2 % (`Tab5`, T1.1975) | `sl_chomage.xlsx` (https://www.insee.fr/fr/statistiques/fichier/9032359/Chomage2026T2.zip) | Conforme |
| 2025-T4 | 7,9 % | 7,9 % (`Tab5` ; `Tab4` : publication T4 2025 et T1 2026 à 7,9) | idem | Conforme |
| 2026-T2 | 8,3 % | 8,3 % (`Tab5`) ; la page localisée donne aussi « France hors Mayotte : 8,3 » | idem ; https://www.insee.fr/fr/statistiques/2012804 | Conforme |
| La série hors Mayotte est toujours publiée | implicite | Oui : « Pour le taux de chômage, une série sur le champ France hors Mayotte continue d'être publiée dans le fichier de données complémentaires » (tableau 5 « depuis 1975 »). Effet de Mayotte au T2 2026 : +0,06 point sur le taux de chômage, -0,17 point sur le taux d'emploi | note méthodologique 2T2026 ; IR 192 | Conforme |

### 4. Demandeurs d'emploi inscrits à France Travail (STMT, CVS-CJO, France hors Mayotte)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Catégorie A, 2026-T3 | 3 353 400 | 3 353 400 (+0,9 %, +30 400 sur le trimestre ; +2,1 % sur un an) | https://statistiques.francetravail.org/stmt/publication ; https://www.francetravail.org/statistiques-analyses/breve-chiffres-stmt/inscrits-a-france-travail-au-3e-trimestre-2026.html?type=article ; presse : https://www.economiematin.fr/?p=235933 | Conforme |
| Catégorie A, 2026-T2 | 3 323 000 | 3 323 000 (publié le 28 juillet 2026, +0,8 %, +27 900) ; 3 353 400 - 30 400 = 3 323 000 : même millésime à la publication d'octobre | https://www.optionfinance.fr/info-financiere-en-continu/d/2026-07-28-france-legere-augmentation-des-demandeurs-demploi-au-2e-trimestre.html (via recherche) ; DREETS Occitanie https://occitanie.dreets.gouv.fr/sites/occitanie.dreets.gouv.fr/IMG/pdf/les_inscrits_a_ft_occitanie_t2_2026.pdf (même chiffre, vu dans les extraits de recherche) | Conforme |
| Catégories A, B, C, 2026-T3 | 5 847 500 | 5 847 500 (+0,8 %, +46 000 ; +2,4 % sur un an) ; dont 2 494 000 en activité réduite (B, C) | STMT et francetravail.org ci-dessus | Conforme |
| Catégories A, B, C, 2026-T2 | 5 801 500 | 5 801 500 (juillet : +1,3 %, +73 500) ; 5 847 500 - 46 000 = 5 801 500 | idem + optionfinance (T2) | Conforme |
| Champ et corrections | CVS-CJO, hors Mayotte | « France hors Mayotte » ; source imprimée : « Source : France Travail-Dares, STMT, données CVS-CJO » | https://statistiques.francetravail.org/stmt/publication | Conforme |
| Date de publication | 2026-10-28 | « Publié le 28/10/2026 » (francetravail.org) ; 28 octobre 2026 aussi chez ABC Bourse et la DREETS Normandie ; prochaine publication : jeudi 28 janvier 2027 à 12 h. Une réponse de recherche évoquait « 26 octobre » (Dares Indicateurs n° 47) : non confirmé, quatre sources concordent sur le 28 | https://www.francetravail.org/statistiques-analyses/breve-chiffres-stmt/inscrits-a-france-travail-au-3e-trimestre-2026.html?type=article ; https://www.abcbourse.com/marches/le-chomage-repart-a-la-hausse-de-0-9-en-france-les-moins-de-25-ans-particulie_705066 ; https://normandie.dreets.gouv.fr/Les-inscrits-a-France-travail-au-3e-trimestre-2026 | Conforme |
| Autre point utile | non indiqué | Hors bénéficiaires du RSA et jeunes en parcours (Pacea, CEJ, AIJ), la catégorie A ne progresse que de +0,3 % sur le trimestre et +0,9 % sur un an ; catégories F (597 000) et G (386 100) créées en janvier 2025, publiées en données brutes | STMT (page ci-dessus) | Information utile (à ne pas confondre avec A, B, C) |

### 5. Taux de chômage localisés (Insee, 2026-T2, hors Mayotte)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Cantal (15), plus bas | 4,8 % | 4,8 % ; plus bas des 100 départements (suivent Lozère 5,0 %, Manche 5,7 %) | https://www.insee.fr/fr/statistiques/2012804 (tableau parsé : 100 départements + 2 agrégats) ; IR 223 anglais https://www.insee.fr/en/statistiques/9053040 (« Lozère, the department with the second-lowest unemployment rate (5.0%) ») | Conforme |
| Guyane (973), plus haut | 20,4 % | 20,4 % (19,3 % au T1) ; plus haut de tous les départements (La Réunion 18,8 %, Guadeloupe 16,4 %) | idem | Conforme |
| Seine-Saint-Denis (93) | 11,5 % | 11,5 % (11,1 % au T1) | idem | Conforme |
| Paris (75) | 6,6 % | 6,6 % (6,4 % au T1) | idem | Conforme |
| La Réunion (974) | 18,8 % | 18,8 % (19,0 % au T1) ; la presse arrondit à 19 % (https://outremers360.com/bassin-indien-appli/la-reunion-le-taux-de-chomage-augmente-et-atteint-19-de-la-population-active-au-deuxieme-trimestre-2026-selon-linsee) | idem | Conforme |
| Nombre de départements | 100, sans Mayotte | 100 lignes (96 métropolitains avec Corse-du-Sud et Haute-Corse, plus 4 DOM) ; Mayotte absente, champ « France hors Mayotte » | https://www.insee.fr/fr/statistiques/2012804 | Conforme |
| Date de publication | 2026-09-18 | « Paru le 18/09/2026 » ; prochaine publication 6 janvier 2027 à 12 h | https://www.insee.fr/fr/statistiques/2012804 ; https://www.insee.fr/fr/statistiques/9053037 (IR 223) | Conforme |
| Statut « semi-définitif » (BDM) | semi-définitif | La page Insee écrit : « (p) Les données du dernier trimestre sont provisoires » et l'IR 223 « Les données sont provisoires pour le dernier trimestre et révisées pour les trimestres précédents ». Le mot « semi-définitif » du BDM n'est vérifiable que dans l'API | https://www.insee.fr/fr/statistiques/2012804 ; https://www.insee.fr/fr/statistiques/9053037 | Écart expliqué (dire « provisoire » côté lecteur ; « semi-définitif » : non trouvé hors API) |
| Réserve de l'Insee sur les DOM | non indiquée | Les taux localisés des DOM (hors Mayotte) ont « un aléa statistique » sur les variations de court terme ; l'Insee recommande les moyennes annuelles pour ces territoires. Concerne Guyane, La Réunion, Guadeloupe, Martinique | IR 223 (« Pour en savoir plus ») | Information utile |

### 6. Dates et pages sources

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Dernière mise à jour des séries BIT | 2026-08-07, IR n° 192 | IR n° 192, « 7 août 2026 » ; prochaine parution (T3 2026) le 10 novembre 2026 à 7 h 30, soit dans 8 jours : le snapshot sera alors périmé | https://www.insee.fr/fr/statistiques/9032359 | Conforme (à actualiser le 10/11/2026 ; Eurostat donne déjà 8,5 % pour septembre) |
| Fiche source `s1223` (français) | « Enquête emploi en continu » | Existe, titre « Enquête emploi en continu \| Insee », « Paru le 02/11/2026 » (date de mise à jour de la fiche, pas des données) ; « depuis 2024, Mayotte intègre le processus de l'enquête Emploi en continu. Le champ de l'enquête à partir de 2024 est la France » ; ne parle ni de révisions ni de licence ni des inscrits à France Travail | https://www.insee.fr/fr/metadonnees/source/serie/s1223 | Conforme |
| Fiche source `s1223` (anglais) | page anglaise | Existe à l'adresse annoncée, titre « Labour force survey \| Insee » (et non « Continuous labour force survey »), « Paru le 02/11/2026 » | https://www.insee.fr/en/metadonnees/source/serie/s1223 | Conforme |
| `statistiques/2012804`, version anglaise | « existe-t-elle à une autre adresse ? » | Pas de page anglaise à la même adresse : `https://www.insee.fr/en/statistiques/2012804` renvoie 404. Le lien « English » de la page française mène seulement à l'accueil anglais (`/langue/en`). Équivalents anglais trouvés : (a) l'Informations rapides n° 223 en anglais, « Localized employment and unemployment rates (by region and department) - second quarter 2026 », qui reprend les taux T2 2026 par région et département (Cantal 4,8, Guyane 20,4, Seine-Saint-Denis 11,5, Paris 6,6, La Réunion 18,8) et la note sur Mayotte ; (b) la fiche source anglaise « Localised unemployment rates » ; (c) la fiche indicateur p1660 anglaise. La version française de l'IR 223 est à https://www.insee.fr/fr/statistiques/9053037 | https://www.insee.fr/en/statistiques/9053040 ; https://www.insee.fr/en/metadonnees/source/serie/s2107 ; https://www.insee.fr/en/metadonnees/source/indicateur/p1660/presentation | Écart expliqué (pas de traduction à la même adresse ; adresse anglaise de remplacement : 9053040) |
| Licence de réutilisation France Travail | à confirmer | Les pages STMT, `francetravail.org` (brève, page open data, « Informations légales ») n'énoncent aucune licence : seulement « © FRANCE TRAVAIL 2026 » et la ligne de source du graphique. La licence est indiquée sur data.gouv.fr : le jeu « Demandeurs d'emploi inscrits à France Travail » (producteur France Travail, co-produit Dares) porte la licence `fr-lo`, « Licence Ouverte / Open Licence » (Etalab), séries CVS-CJO mises à jour le 28/07/2026 dans la méta-donnée. Version de la licence non précisée sur la fiche du jeu de données | https://www.data.gouv.fr/datasets/demandeurs-demploi-inscrits-a-france-travail ; https://statistiques.francetravail.org/stmt/publication ; https://francetravail.org/accueil/informations-legales.html ; https://francetravail.org/opendata/ | Écart expliqué (licence trouvée côté data.gouv.fr seulement) |
| Mention de source demandée par France Travail | « Source : France Travail-Dares, STMT » ? | La formule imprimée sous le graphique est « Source : France Travail-Dares, STMT, données CVS-CJO. » ; aucune obligation spécifique de mention n'est énoncée par France Travail. La Licence Ouverte 2.0 impose de nommer le producteur et la date de dernière mise à jour (lien hypertexte accepté), sans suggérer une caution officielle ni induire en erreur sur le contenu, la source ou la date | https://statistiques.francetravail.org/stmt/publication ; https://www.data.gouv.fr/pages/legal/licences/etalab-2.0 | Conforme sur la formule (recommandation : « Source : France Travail-Dares, STMT, données CVS-CJO, publiées le 28 octobre 2026 ») |
| Licence de l'Insee (pour mémoire) | non demandée | Licence Ouverte / Open Licence 2.0 ; mention « Source : Insee » et date de dernière mise à jour ; ne pas altérer le sens | https://www.insee.fr/fr/information/2008466 | Information utile |

### 7. Énoncés « À savoir »

| Énoncé | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|
| (1) Un chômeur au sens du BIT n'est pas un demandeur d'emploi inscrit à France Travail : ne pas comparer directement | Confirmé. L'Insee : « deux concepts différents » ; « Un demandeur d'emploi en catégorie A peut ne pas être chômeur au sens du BIT » et inversement ; « les deux populations ne se recouvrent qu'en partie » ; les changements de règles d'inscription « peuvent avoir un effet sur le nombre d'inscrits à France Travail sans affecter le chômage BIT ». Champs différents (France hors Mayotte contre France logement ordinaire). Même propos dans l'étude Insee/Dares de juin 2023 (2,2 millions de chômeurs BIT contre 3,1 millions en catégorie A au T4 2022). Eurostat/presse : séries non comparables | https://www.insee.fr/fr/statistiques/4805248 ; https://www.insee.fr/fr/statistiques/7456935 ; https://www.economiematin.fr/?p=236988 | Conforme |
| (2a) Depuis le 7 août 2026 le taux national BIT inclut Mayotte, rétropolé jusqu'en 2003 | Mayotte incluse à partir de l'IR 192 (champ « France » au lieu de « France hors Mayotte », toutes les séries rétropolées). Précision : la rétropolation annuelle porte sur 1982-2023, puis conversion trimestrielle « avec la même profondeur temporelle qu'auparavant » ; le taux de chômage « France » est publié depuis 1975, les autres indicateurs depuis 2003 | IR 192 ; note méthodologique 2T2026 https://www.insee.fr/fr/statistiques/documentation/Note_methodologique_2026T2.pdf ; `sl_chomage.xlsx` | Écart expliqué (« rétropolé jusqu'en 2003 » est exact pour le taux d'emploi, pas pour le taux de chômage publié depuis 1975) |
| (2b) « La série France métropolitaine s'est arrêtée » (depuis le 7 août 2026) | Non soutenu tel quel. Ce qui change le 7 août 2026 : le champ principal passe de « France hors Mayotte » à « France » ; la série « France hors Mayotte » continue d'être publiée (tableau 5). Dans l'historique des publications de l'Insee (`Tab4`), la série « France métropolitaine (ancienne enquête) » ne figure que jusqu'à la publication 2019-T3 (note de rétropolation du 14/11/2019 : à partir de l'IR du T3 2019 tout est diffusé sur « France hors Mayotte »). La publication des taux localisés du 18/09/2026 affiche toujours un agrégat « France métropolitaine » (8,1 % au T2 2026). Aucune annonce d'arrêt datée du 7 août 2026 trouvée | `sl_chomage.xlsx` (`Tab4`) ; https://www.insee.fr/fr/statistiques/documentation/Retro_m_14112019.pdf ; https://www.insee.fr/fr/statistiques/2012804 | Écart (à reformuler : « depuis le 7 août 2026 le taux national porte sur la France entière, Mayotte comprise ; la série hors Mayotte reste publiée à part ») |
| (2c) Les taux localisés excluent toujours Mayotte | Confirmé : « à ce stade, les taux de chômage localisés de cette présente publication n'intègrent pas cette extension de champ : le champ couvert ici reste le total « France hors Mayotte » ». Les séries propres à Mayotte ne sont pas publiées : du recul est nécessaire pour estimer un taux localisé | IR 223 https://www.insee.fr/fr/statistiques/9053037 (EN https://www.insee.fr/en/statistiques/9053040) ; page https://www.insee.fr/fr/statistiques/2012804 (« Champ : France hors Mayotte ») ; note méthodologique 2T2026 | Conforme |
| (3) Depuis janvier 2025, la loi plein emploi (inscription automatique des bénéficiaires du RSA et des jeunes suivis en mission locale) affecte le nombre d'inscrits, rupture de série | Confirmé pour le fond. France Travail/Dares : les demandeurs et bénéficiaires du RSA, les jeunes suivis par les missions locales et les personnes handicapées suivies par Cap emploi sont systématiquement inscrits depuis janvier 2025 ; création des catégories F et G ; séries complémentaires hors publics concernés. L'Insee : « hausse importante du nombre d'inscrits à France Travail au premier trimestre 2025 » de façon « mécanique ». Catégorie A +8,7 % au T1 2025 (3 408 100). L'Autorité de la statistique publique a suspendu la labellisation des séries en 2025-2026. Nuances : le mot « rupture de série » n'est pas employé par les sources officielles trouvées ; la liste omet Cap emploi (personnes handicapées) | https://statistiques.francetravail.org/stmt/publication ; IR 192 https://www.insee.fr/fr/statistiques/9032359 ; https://www.data.gouv.fr/datasets/demandeurs-demploi-inscrits-a-france-travail | Conforme (avec nuance de vocabulaire : « effet mécanique » plutôt que « rupture ») |
| (4) Le dernier trimestre est provisoire, les précédents sont révisés | Taux localisés : confirmé mot pour mot (« Les données sont provisoires pour le dernier trimestre et révisées pour les trimestres précédents » ; politique de révision de la fiche s2107). Taux BIT national : l'Insee ne qualifie pas le dernier trimestre de « provisoire » ; chaque trimestre l'actualisation des coefficients saisonniers révise légèrement toute la série, une révision annuelle au T1 intègre les données démographiques du recensement, et l'IR 192 indique que les taux ne sont pas révisés par rapport au T1 hors cet effet ; incertitude ±0,3 point. France Travail : coefficients CVS-CJO révisés chaque année en février ; le millésime du T2 2026 est resté identique entre juillet et octobre | IR 223 ; https://www.insee.fr/fr/metadonnees/source/serie/s2107/revision-donnees ; note méthodologique 2T2026 (« Publication et révision des séries ») ; https://www.data.gouv.fr/datasets/demandeurs-demploi-inscrits-a-france-travail | Conforme pour les taux localisés ; Écart expliqué pour le taux BIT national (révisions réelles mais faibles, non étiquetées « provisoire ») |

### 8. Recoupements complémentaires (hors Insee)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Eurostat, France (BIT, mensuel, CVS) | non présent | Août 2026 : 8,3 % ; septembre 2026 : 8,5 % (2 732 000 chômeurs) ; moins de 25 ans : 20,8 % puis 21,9 %. Estimation mensuelle Eurostat, non comparable terme à terme avec le trimestre Insee, mais cohérente avec 8,3 % au T2 et annonciatrice d'une hausse au T3 | https://ec.europa.eu/eurostat/en/web/products-euro-indicators/w/3-30102026-bp ; https://www.economiematin.fr/?p=236988 | Information utile (cohérent) |
| La Réunion 19 % (presse) | 18,8 % | « 19 % de la population active » au T2 2026, note de conjoncture Insee du 30/09/2026 | URL Outremers 360 ci-dessus | Conforme (arrondi) |

### Conclusion

Tous les chiffres du snapshot sont confirmés par au moins une source publiée autre que l'API : taux BIT (8,3 / 8,1 / 8,0 / 8,4), moins de 25 ans (21,6 / 21,2), taux d'emploi (69,0 / 69,3), série hors Mayotte (3,2 / 7,9 / 8,3), inscrits France Travail (3 353 400, 3 323 000, 5 847 500, 5 801 500) et les cinq taux départementaux (Cantal 4,8 et Guyane 20,4 sont bien les extrêmes des 100 départements). Les dates sont exactes (7 août, 18 septembre, 28 octobre 2026).

Aucun chiffre n'est en écart. Les points à corriger sont des formulations :

1. Écart réel (énoncé 2) : « la série France métropolitaine s'est arrêtée le 7 août 2026 » n'est pas soutenu. Le 7 août, le champ principal est passé de « France hors Mayotte » à « France » ; la série hors Mayotte reste publiée ; la série « France métropolitaine » du taux BIT ne figure dans l'historique de l'Insee que jusqu'en 2019-T3, et un agrégat « France métropolitaine » existe toujours dans les taux localisés (8,1 % au T2 2026). À reformuler.
2. « Rétropolé jusqu'en 2003 » : exact pour le taux d'emploi, mais l'Insee publie le taux de chômage « France » depuis 1975 (tableau 1). La date de début de l'idbank 011818543 n'a pas pu être vérifiée hors API.
3. « Semi-définitif » : l'Insee écrit « provisoire » pour le dernier trimestre des taux localisés. Préférer « provisoire » dans les textes lus par le joueur.
4. Page anglaise de `statistiques/2012804` : n'existe pas (404). Adresse anglaise la plus proche : Informations rapides n° 223, https://www.insee.fr/en/statistiques/9053040 (français : https://www.insee.fr/fr/statistiques/9053037).
5. France Travail : aucune licence ni obligation de mention sur les pages STMT ; la licence (Licence Ouverte, Etalab) figure sur la fiche data.gouv.fr du jeu de données. Formule d'attribution à utiliser : « Source : France Travail-Dares, STMT, données CVS-CJO » (celle de la page), avec la date de publication et un lien, comme le demande la Licence Ouverte 2.0.
6. Péremption : l'Insee publie le T3 2026 le 10 novembre 2026 à 7 h 30 ; Eurostat donne déjà 8,5 % pour septembre. Le snapshot du 2 novembre sera donc dépassé 8 jours plus tard (localisés : 6 janvier 2027 ; France Travail : 28 janvier 2027).

Limites : les pages de séries BDM (`statistiques/series/...`) sont rendues en JavaScript et illisibles hors navigateur ; les identifiants 011818543, 011818548, 011818676, 001688527 et le libellé « semi-définitif » du BDM sont donc « non trouvés » hors API. Le site de la Dares (`dares.travail-emploi.gouv.fr`) a répondu par une page de vérification anti-robot : la publication Dares elle-même n'a pas été lue, les chiffres viennent de France Travail (même série STMT « France Travail-Dares »), de la presse et des DREETS. Certains chiffres de juillet (T2) ont été lus dans des extraits de recherche (optionfinance, DREETS Occitanie), pas dans les documents complets.

### URLs consultées (toutes le 2026-11-02)

- https://www.insee.fr/fr/statistiques/9032359 (IR n° 192, 7 août 2026) et https://www.insee.fr/fr/statistiques/fichier/version-html/9032359/IR192_Chomage_2T2026.pdf
- https://www.insee.fr/fr/statistiques/fichier/9032359/Chomage2026T2.zip (fichiers `2026T2_sl_chomage.xlsx` et `2026T2_sl_indicateurs.xlsx`)
- https://www.insee.fr/fr/statistiques/documentation/Note_methodologique_2026T2.pdf
- https://www.insee.fr/fr/statistiques/documentation/Retro_m_14112019.pdf
- https://www.insee.fr/en/statistiques/9033057 (IR 192 en anglais)
- https://www.insee.fr/fr/statistiques/2532173 (taux de chômage selon le sexe et l'âge, 1975-T1 à 2026-T2)
- https://www.insee.fr/fr/statistiques/4805248 (L'essentiel sur le chômage)
- https://www.insee.fr/fr/statistiques/7456935 (chômeurs BIT et catégorie A, juin 2023)
- https://www.insee.fr/fr/statistiques/2012804 (taux de chômage localisés T2 2026)
- https://www.insee.fr/en/statistiques/2012804 (404)
- https://www.insee.fr/fr/statistiques/9053037 et https://www.insee.fr/en/statistiques/9053040 (IR n° 223, 18 septembre 2026)
- https://www.insee.fr/fr/metadonnees/source/serie/s1223 et https://www.insee.fr/en/metadonnees/source/serie/s1223
- https://www.insee.fr/fr/metadonnees/source/serie/s2107 (+ `/revision-donnees`, `/documentation-methodologique`) et https://www.insee.fr/en/metadonnees/source/serie/s2107
- https://www.insee.fr/en/metadonnees/source/indicateur/p1660/presentation
- https://www.insee.fr/fr/information/2008466 (réutilisation des données Insee)
- https://www.insee.fr/fr/statistiques/series/103167923 et https://www.insee.fr/fr/statistiques/series/102412458 (JavaScript, illisibles)
- https://statistiques.francetravail.org/stmt/publication
- https://statistiques.francetravail.org/stmt/static/methode_2018
- https://www.francetravail.org/statistiques-analyses/breve-chiffres-stmt/inscrits-a-france-travail-au-3e-trimestre-2026.html?type=article
- https://www.francetravail.org/opendata/statistiques-du-marche-du-travai.html?type=article
- https://francetravail.org/accueil/informations-legales.html
- https://francetravail.org/opendata/
- https://www.data.gouv.fr/datasets/demandeurs-demploi-inscrits-a-france-travail (et son API JSON publique) ; https://www.data.gouv.fr/datasets/inscrits-a-france-travail-entrees-et-sorties-des-listes-france-et-regions-trimestrielles-brutes
- https://www.data.gouv.fr/pages/legal/licences/etalab-2.0
- https://dares.travail-emploi.gouv.fr/dossier/les-inscrits-france-travail (page anti-robot, non lue)
- https://ec.europa.eu/eurostat/en/web/products-euro-indicators/w/3-30102026-bp
- https://www.economiematin.fr/?p=235933 et https://www.economiematin.fr/?p=236988
- https://www.lafinancepourtous.com/2026/05/13/le-chomage-atteint-81-en-france-debut-2026/
- https://outremers360.com/bassin-indien-appli/la-reunion-le-taux-de-chomage-augmente-et-atteint-19-de-la-population-active-au-deuxieme-trimestre-2026-selon-linsee
- https://www.abcbourse.com/marches/le-chomage-repart-a-la-hausse-de-0-9-en-france-les-moins-de-25-ans-particulie_705066, https://normandie.dreets.gouv.fr/Les-inscrits-a-France-travail-au-3e-trimestre-2026, https://www.optionfinance.fr/info-financiere-en-continu/d/2026-07-28-france-legere-augmentation-des-demandeurs-demploi-au-2e-trimestre.html et https://occitanie.dreets.gouv.fr/sites/occitanie.dreets.gouv.fr/IMG/pdf/les_inscrits_a_ft_occitanie_t2_2026.pdf (extraits de résultats de recherche seulement)
- https://db.nomics.world/INSEE/TAUX-CHOMAGE (miroir : dernière mise à jour du jeu localisé le 18/09/2026)

## Mises à jour

**12/11/2026**, `yarn briefings unemployment`, pour l'édition 0003 (Mitchnsun/moi-president#357) :
- **Nouvelle période** : le 3e trimestre 2026, publié le 10/11/2026 (Informations rapides n° 270). Taux de chômage 8,2 % (8,3 % au 2e trimestre), 15-24 ans 21,0 %, taux d'emploi des 15-64 ans 69,1 %. Les inscrits à France Travail (déjà au 3e trimestre) et les taux par département (encore au 2e trimestre, prochaine publication le 6 janvier 2027) ne changent pas.
- **Révisions de l'Insee**, 0,1 point chacune : le taux d'ensemble en 2016-T1 (10,3 → 10,2) et 2026-T1 (8,1 → 8,2) ; onze trimestres des 15-24 ans, dont 2026-T2 (21,6 → 21,5) ; six du taux d'emploi, dont 2025-T1 (69,4 → 69,3) ; 2019-T1 de la série depuis 1975 (8,8 → 8,7).
- **Changement de la source** : l'Insee publie désormais l'ensemble et les 15-24 ans « France entière » depuis 1975. Le script ne garde que 2003-T1 et après (règle ci-dessus).
- **Vérification refaite** le 12/11/2026 par une session Claude, sur la publication de l'Insee et non sur l'API :

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Taux de chômage 2026-T3 (clé) | 8,2 % | « s'établit à 8,2 % de la population active », « quasi stable sur le trimestre (-0,1 point) », « supérieur de 0,4 point à son niveau du troisième trimestre 2025 » (7,8 % dans le fichier) | https://www.insee.fr/fr/statistiques/9118603 (IR n° 270, 10/11/2026) | Conforme |
| Taux des 15-24 ans 2026-T3 | 21,0 % | « diminue pour les 15-24 ans (-0,5 point, à 21,0 %) », « +1,6 point » sur un an (21,5 % puis 19,4 % dans le fichier) | idem | Conforme |
| Taux d'emploi des 15-64 ans 2026-T3 | 69,1 % | « quasi stable (+0,1 point), à 69,1 % », « Sur un an, il baisse de 0,2 point » (69,0 % et 69,3 % dans le fichier) | idem | Conforme |

Les chiffres de la page d'accueil de l'Insee le 12/11/2026 (« 8,2 % Chômage au 3e trimestre 2026 ») concordent.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
