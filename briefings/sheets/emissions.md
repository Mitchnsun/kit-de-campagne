# `emissions` · Émissions de gaz à effet de serre

**Vérifiée le 02/11/2026** : double vérification sur le web, chiffres conformes (section « Double vérification ») ; une note corrigée (le puits des terres et forêts : affaibli depuis 2005, pas depuis 1990), les trois autres précisées.

| Champ | Valeur |
| --- | --- |
| Indicateur | `emissions`, dossier « Écologie et énergie » (`ecology`), page de type série, ticket #29 de l'app, première page (statut `planned` : les chiffres et la fiche avant la page) |
| Données | `briefings/data/emissions.json`, écrit par `yarn briefings emissions` le 2026-11-02 |
| Sources | Citepa, « Secten, édition 2026 », https://www.citepa.org/donnees-air-climat/donnees-gaz-a-effet-de-serre/secten/ (« Date de mise à jour 16/06/2026 » ; la page anglaise sert le rapport français : `frenchOnly`), fichier `serie_longue_Citepa_Secten_ed_2026-d.xlsx`, feuille `BDD_Secten` ; reproduction autorisée en citant « Citepa/Secten édition juin 2026 », pas de Licence Ouverte (`citation-only`) |
| Séries | `total` : émissions nationales hors UTCATF, en MtCO₂e, 1990 à 2025, somme des lignes « total GES » des six secteurs ; `energyIndustry`, `manufacturing`, `buildings`, `agriculture`, `transport`, `waste` : les six secteurs de niveau 1 ; `landUseSink` : le puits net des terres et forêts (UTCATF), négatif ; 2025 provisoire sur toutes les séries |
| Chiffre clé | 367,0 MtCO₂e en 2024, dernière année inventoriée, en baisse après 378,2 ; l'estimation de 2025 (359,4) vient ensuite sur la page |
| Règles | Le script refuse un secteur inconnu, une autre unité ou un autre périmètre que « France hexagonale + Outre-mer inclus dans l'UE » ; les nombres écrits en notation française (« 7,20771E-05 ») sont lus ; les apostrophes typographiques des libellés sont ramenées à l'apostrophe droite. La dernière année de l'édition est marquée provisoire (#29 ; le Citepa l'appelle « pré-estimation ») ; son puits reprend largement celui de 2024 |
| Contexte | Budgets carbone de la SNBC 3 : 342 / 262 / 194 MtCO₂e par an pour 2024-2028 / 2029-2033 / 2034-2038 (décret n° 2026-636 du 16/07/2026, JORF du 18/07/2026, art. 2) ; les valeurs 261 / 193 sont celles du projet de juin 2026, encore reprises par le rapport Secten, le HCC et la page de suivi du ministère. Pour la page « Objectifs climat » (#29), à venir |
| Première édition | À remplir à la publication |

## « À savoir »

1. Les soutes internationales maritimes, fluviales et aériennes sont exclues, le trafic domestique inclus ; périmètre : Outre-mer inclus dans l'UE (« Lisez-moi » du fichier, rapport Secten).
2. 2025 est une « pré-estimation » remplacée par l'inventaire de juin 2027 ; « chaque nouvelle édition annule et remplace les précédentes » (fichier). 2024 aussi peut bouger (l'estimation de l'édition 2025 prévoyait -1,8 %, l'inventaire a donné -3,0 %).
3. Statistiques d'intérêt général par avis de l'Autorité de la statistique publique du 17/07/2025, pour trois ans ; conditions du Citepa : reproduction « autorisée à la condition de citer le Citepa dans les sources, à chaque utilisation », « Tous droits réservés ». La vérification recommande une confirmation auprès du Citepa (infos@citepa.org) si le kit redistribue les chiffres : à décider par le PO.
4. -39,3 (1990), -68,6 (2005), -69,0 (2006, maximum), -45,8 (2017), -52,0 (2024) ; « fortement dégradé depuis 2015 » (HCC). La note d'abord prévue (« -52 en 2024 contre -39 en 1990 » pour dire un affaiblissement) allait dans le mauvais sens : elle est corrigée.

Non repris : les incohérences internes au Citepa relevées par la vérification (figure 1 de la synthèse, « CO₂e net » de l'annexe), sans effet sur le fichier ; l'écart de 0,1 point du ministère sur 2025.

À actualiser : l'édition Secten 2027 (juin 2027) ; le baromètre mensuel du Citepa n'entre pas dans le kit (révisé chaque trimestre).

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans resommer le fichier du Citepa. Son rapport, tel quel :

Date du contrôle : 2026-11-02. Aucun fichier sous `/home/user` n'a été lu ni modifié.

### Méthode et limites (à lire d'abord)

- **Aucune valeur ne provient d'un résumé de moteur de recherche.** Le quota de `WebSearch` était épuisé dès les deux premières requêtes (message : « web search budget is used up »). Je n'ai pas contourné la limite. Conséquences : la presse n'a pas été contrôlée, et l'EEA, la CCNUCC et l'édition 2026 des « Chiffres clés du climat » du SDES n'étaient pas accessibles (voir « Non trouvé » plus bas).
- **Lu directement dans le texte source** (HTML ou PDF téléchargé puis converti en texte) : pages Secten FR et EN du Citepa, article d'annonce, mentions légales, synthèse PDF, rapport complet PDF (597 pages), page et note du baromètre d'octobre 2026, pages du ministère, documents SNBC 3 de juillet 2026, rapport annuel 2026 du HCC (chapitre 3).
- **Décret SNBC 3 :** lu dans l'archive open data du Journal officiel (DILA), qui est le texte officiel, pas sur la page Légifrance elle-même (Légifrance ne se charge pas par simple requête HTTP).
- **Résumé produit par l'outil `WebFetch` (petit modèle), donc de moindre fiabilité :** l'avis de l'Autorité de la statistique publique (NOR et numéro de JORF), et la page Wikipédia sur la SNBC (non utilisée comme preuve). Tout le reste a été relu dans le texte brut.
- **Le fichier xlsx n'a pas été re-sommé.** Je n'ai ouvert que sa feuille « Lisez-moi » (textes) et la cellule « date edition ». Pour comparer aux totaux publiés, j'ai lu le tableau « Aperçu des données » de la page Secten du Citepa (lignes par secteur, 1990-2025) : c'est le même jeu de données du Citepa, donc **pas une source indépendante du fichier**. Je ne l'ai utilisé que comme contrôle de cohérence avec les totaux publiés dans le rapport, le décret et le baromètre. Les verdicts s'appuient d'abord sur ces totaux publiés.

Sigles : « Synthèse » = `Synthese-et-messages-cles-Secten-2026.pdf` (19 p.) ; « Rapport » = `Citepa_Secten-2026.pdf`, pagination imprimée (= page PDF − 14).

---

### 1. Total national hors UTCATF

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Total 2024 | 367.0 | « les autres secteurs ont émis 367,0 Mt CO2e » ; « 367 Mt CO2e en 2024 » ; 367 dans le décret et sur la page du ministère | [Synthèse p.17](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf), [Rapport p.516](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf), [décret 2026-636 art. 3](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907), [ministère](https://www.ecologie.gouv.fr/politiques-publiques/strategie-nationale-bas-carbone-snbc) | Conforme |
| Total 2023 | 378.2 | « Hors puits de carbone, les émissions de GES atteignent 378,2 MtCO2e en 2023 » | [Rapport p.106](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf) | Conforme |
| Variation 2024/2023 | -3.0 % | « -11,2 Mt CO2e (-3 %) » ; 367,0 / 378,2 = -2,96 % | [Synthèse p.1](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf), [article d'annonce](https://www.citepa.org/le-rapport-secten-edition-2026-est-en-ligne/) | Conforme |
| Total 2025 | 359.4 (estimation) | « 359 Mt CO2e en 2025 » (-2,1 %, -7,6 Mt) ; **359,4** dans le tableau du baromètre Citepa du 13/10/2026 (« TOTAL national hors UTCATF … 359,4 ») ; HCC : « pré-estimation du Citepa … 359 » | [Synthèse p.3](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf), [note baromètre p.1](https://www.citepa.org/wp-content/uploads/2026/10/Note-barometre-T2-2026vf-d.pdf), [HCC ch.3 p.125 et 131](https://www.hautconseilclimat.fr/wp-content/uploads/2026/07/HCC_RA2026-Chapitre-3_1707.pdf) | Conforme |
| 2025 : « pré-estimation » ou « estimation » dans les mots du Citepa ? | « an estimate » | Les deux, plus « provisoire ». Mots du Citepa : « estimation proxy » (texte), « 2025 : pré-estimation » (légendes des graphiques), « pré-estimations » (chapitres), « estimation provisoire de l'année 2025 » (Synthèse, « Comprendre nos données »). Note de bas de page p.1 : « Les émissions consolidées pour 2025 seront proposées dans l'inventaire prochain – Il s'agit ici de l'estimation réalisée à partir de l'inventaire proxy ». Calendrier p.9 : consolidé 1990-2025 en juin 2027. HCC : « pré-estimation », « chiffre provisoire … à commenter avec prudence » | [Synthèse p.1, 2, 9, 11](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf), [Rapport p.30, 132](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf), [HCC p.125](https://www.hautconseilclimat.fr/wp-content/uploads/2026/07/HCC_RA2026-Chapitre-3_1707.pdf) | Conforme (formuler « estimation provisoire ») |
| 2024 : définitif ou révisable ? | non précisé | « Pour 2024, dernière année consolidée dans l'inventaire national » : valeur consolidée pour cette édition, **mais** « chaque nouvelle édition annule et remplace les précédentes » et met à jour « toute la série historique ». Preuve de révision : le proxy de l'an dernier donnait -1,8 % pour 2024, l'inventaire consolidé donne -3,0 %. Le décret prévoit aussi des budgets « ajustés annuellement » aux évolutions d'inventaire (art. 11) | [Synthèse p.12 et 3](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf), [page Secten](https://www.citepa.org/donnees-air-climat/donnees-gaz-a-effet-de-serre/secten/), [décret art. 11](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907) | Conforme (2024 est consolidé mais reste révisable) |
| Total 1990 | 546.9 | **547** (arrondi à l'entier) dans l'annexe CCNUCC, le décret, la SNBC 3 et le ministère. Le dixième ne se lit que dans le tableau de la page Secten (somme des six lignes = 546,9) | [Rapport p.544](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf), [décret art. 3](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907), [page Secten](https://www.citepa.org/donnees-air-climat/donnees-gaz-a-effet-de-serre/secten/) | Conforme (arrondi) |
| Total 2005 | 555.6 | **556** dans l'annexe, le décret, le ministère. Somme des six lignes arrondies de la page = 555,7 (0,1 d'arrondi) | idem | Conforme (arrondi) |

Remarques de cohérence :
- La somme des six secteurs arrondis à 0,1 donne 367,1 (2024) et 359,5 (2025), contre 367,0 et 359,4 publiés. L'écart de 0,1 vient de l'arrondi. Les totaux du fichier (367.0, 359.4) suivent les totaux publiés.
- Dans la Synthèse (p.2), la **Figure 1** porte les libellés « 2022 : 403 Mt » et « 2023 : 376 Mt », alors que le texte et le tableau de la même édition donnent 406 et 378,2 (courbe tracée à ≈ 406 et ≈ 378). Incohérence interne au Citepa, sans effet sur le fichier ; elle ressemble à un reste de l'édition précédente (hypothèse non confirmée).

### 2. Secteurs 2024 et puits UTCATF

Les valeurs à une décimale viennent du tableau « Aperçu des données » de la page Secten (même jeu de données). Les confirmations indépendantes de ce tableau sont le texte du rapport, le décret (arrondis à l'entier) et le baromètre.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Transports 2024 | 125.4 | « 125,4 MtCO2e » (« 125 Mt » dans la Synthèse) ; décret : 125 | [Rapport p.470](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf), [Synthèse p.6](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf), [décret art. 3](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907) | Conforme |
| Agriculture / sylviculture 2024 | 77.5 | « 77,5 Mt CO2e » ; décret : 78 | [Synthèse p.6](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf), [décret](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907) | Conforme |
| Industrie manufacturière et construction 2024 | 61.6 | Pas de chiffre explicite dans le texte. Tableau de la page : 61,6. Cohérent avec le texte : 2025 « 58 Mt, -3,2 Mt (-5,2 %) » donne 61,5-61,6 ; 2024 « -2,3 Mt (-3,6 %) » sur 63,9 (2023) donne 61,6. Décret : 62 | [page Secten](https://www.citepa.org/donnees-air-climat/donnees-gaz-a-effet-de-serre/secten/), [Synthèse p.6](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf), [décret](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907) | Conforme (valeur déduite, non citée telle quelle) |
| Usage des bâtiments, résidentiel/tertiaire 2024 | 56.1 | « 56,1 Mt CO2e en 2024 » ; décret : 56 | [Synthèse p.5](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf) | Conforme |
| Industrie de l'énergie 2024 | 31.2 | « 31,2 Mt CO2e en 2024 » ; décret : 31 (« Production d'énergie ») | [Synthèse p.4](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf) | Conforme |
| Déchets centralisés 2024 | 15.3 | « 15,3 Mt » ; décret : 15. Libellé du Citepa : « Traitement centralisé des déchets » (page) / « Gestion centralisée des déchets » (sommaire du rapport) | [Rapport p.506](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf) | Conforme |
| Puits net UTCATF 2024 | -52.0 | « En 2024, ce puits net est estimé à -52,0 Mt CO2e », compense « environ 14 % » (52/367 = 14,2 %) ; décret : -52 | [Rapport p.516](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf), [Synthèse p.17](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf), [décret art. 10](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907) | Conforme |
| Puits net UTCATF 2025 | -51.3 | Valeur -51,3 sur la page Secten ; HCC : « pré-estimé à -51 ». **Mais** le Citepa dit que l'évolution 2024-2025 de l'UTCATF « n'est pas encore estimée spécifiquement, faute d'indicateurs fiables » (hors feux de forêt), et sa méthode reporte l'année N-2 (« Tout sauf feux de forêt »). HCC : cette pré-estimation « n'est que partielle, et reprend en grande partie l'estimation pour 2024 : l'évolution 2024-2025 ne peut donc pas être analysée » | [page Secten](https://www.citepa.org/donnees-air-climat/donnees-gaz-a-effet-de-serre/secten/), [Synthèse p.3](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf), [Rapport p.30](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf), [HCC p.131](https://www.hautconseilclimat.fr/wp-content/uploads/2026/07/HCC_RA2026-Chapitre-3_1707.pdf) | Conforme pour la valeur. Écart expliqué pour le statut : ce n'est pas une estimation indépendante de 2025 (reprise de 2024 + feux de forêt) |
| Puits net UTCATF 1990 | -39.3 | Page Secten : -39,3 ; décret art. 10 : -39 | [page Secten](https://www.citepa.org/donnees-air-climat/donnees-gaz-a-effet-de-serre/secten/), [décret art. 10](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907) | Conforme |
| Total « avec UTCATF » 2024 (non demandé, à connaître) | (non fourni) | **Deux valeurs dans le même rapport.** Texte : 315 Mt (367 − 52). Annexe « format CCNUCC – mars 2026 » (p.544) : « CO2e net » 2024 = 326 (1990 : 521 ; 2005 : 495), soit un puits implicite d'environ 41 (1990 : 26). Le Citepa explique que le périmètre Secten 2026 ajoute le puits de la forêt guyanaise (≈ 10 Mt/an) et recalcule à la baisse les défrichements | [Rapport p.106, 544, 524](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf) | Écart expliqué (au sein de la source). Ne pas mélanger les « avec UTCATF » des deux tableaux |

### 3. Définition du total et périmètre

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Définition | « émissions hors UTCATF ; selon définitions de la CCNUCC » | Rapport, note (a) du tableau des transports : « CO2, N2O et autres gaz à effet de serre : selon définitions de la CCNUCC – les émissions répertoriées hors total ne sont pas incluses, à savoir les émissions internationales maritimes, fluviales et aériennes » et (b) « émissions hors UTCATF ». La feuille « Lisez-moi » du fichier reprend la formule, en ajoutant les « sources biotiques de l'agriculture et des forêts » et les « sources non-anthropiques » | [Rapport p.467](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf), [xlsx (Lisez-moi)](https://www.citepa.org/wp-content/uploads/2026/06/serie_longue_Citepa_Secten_ed_2026-d.xlsx) | Conforme |
| Exclusion du transport international maritime et aérien | oui | Annexe p.544, note (*) : « Les émissions du trafic maritime international et du trafic aérien international sont exclues ». Le rapport ajoute le transport **fluvial** international. Le trafic aérien domestique et le maritime domestique sont inclus. Les lancements de fusées du Centre spatial guyanais figurent parmi les « émetteurs non inclus dans le total France » | [Rapport p.544, p.22, p.30](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf) | Conforme (le rapport est plus large : maritime, fluvial, aérien) |
| Périmètre | « France hexagonale + Outre-mer inclus dans l'UE » | Annexe note (d) : « France hexagonale et Outre-mer périmètre UE (Guadeloupe, St-Martin (partie française), Martinique, Guyane, La Réunion, Mayotte) » ; Synthèse p.11 : « La France hexagonale et l'Outre-mer inclus dans l'UE » ; Figure 1 : « France hexagonale et Outre-mer inclus dans l'UE ». Le périmètre des polluants est la France hexagonale seule | [Rapport p.544](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf), [Synthèse p.2, 11](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf) | Conforme |
| PRG | non précisé | PRG du 5e rapport du GIEC (AR5) : CH4 = 28, N2O = 265 | [Rapport p.544](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf), [Synthèse p.11](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf) | Complément utile |

### 4. Dates, édition, citation, licence, statut statistique

| Élément | Valeur du fichier ou annoncée | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| « Date de mise à jour » de la page | 16/06/2026 | « Date de mise à jour 16/06/2026 » (HTML brut, relevé le 2026-11-02) | [page Secten](https://www.citepa.org/donnees-air-climat/donnees-gaz-a-effet-de-serre/secten/) | Conforme |
| Annonce | « Le rapport Secten édition 2026 est en ligne », 16 juin 2026 | Article « Publié le 16 juin 2026 », « Modifié le : 23/06/2026 », Réf. 2026_06_05. Dates HTTP : rapport PDF et xlsx modifiés le 16/06/2026 (07:45 et 07:50 GMT) | [article](https://www.citepa.org/le-rapport-secten-edition-2026-est-en-ligne/) | Conforme |
| « date edition » du fichier | 2026-06-01 | Cellule B2 de BDD_Secten = 46174 (numéro de série Excel) = **2026-06-01**. « Lisez-moi » : « Ces données sont relatives à l'édition juin 2026 » | [xlsx](https://www.citepa.org/wp-content/uploads/2026/06/serie_longue_Citepa_Secten_ed_2026-d.xlsx) | Conforme (le 1er juin sert d'étiquette « édition juin 2026 ») |
| Mention de citation demandée | « Citepa/Secten édition juin 2026 » | « Pour citer les données provenant de ce fichier : Citepa/Secten édition juin 2026 » (feuille « Lisez-moi », **pas** sur la page web). Pour le rapport : « Citepa, 2026. Rapport Secten – Emissions de gaz à effet de serre et de polluants atmosphériques 1990-2025 » | [xlsx](https://www.citepa.org/wp-content/uploads/2026/06/serie_longue_Citepa_Secten_ed_2026-d.xlsx), [Rapport, page de titre et sommaire (p.3 du PDF)](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf) | Conforme |
| Conditions de réutilisation | « citer la source, pas la Licence Ouverte » | Mentions légales : le contenu du site est « la propriété exclusive du Citepa » ; « La reproduction … est autorisée à la condition de citer le Citepa dans les sources, à chaque utilisation » ; « © CITEPA Tous droits réservés ». Le Citepa « n'est pas responsable de l'interprétation des données, ni … de l'utilisation de données obsolètes ou qui auraient été depuis republiées/corrigées ». **Aucune mention de Licence Ouverte, d'Etalab ni d'autre licence ouverte** sur la page Secten, les mentions légales ou le xlsx. Le xlsx ajoute : « le Citepa décline toute responsabilité quant à l'utilisation et l'interprétation de ces données brutes » | [mentions légales](https://www.citepa.org/mentions-legales/), [xlsx (Lisez-moi)](https://www.citepa.org/wp-content/uploads/2026/06/serie_longue_Citepa_Secten_ed_2026-d.xlsx), [page Secten](https://www.citepa.org/donnees-air-climat/donnees-gaz-a-effet-de-serre/secten/) | Conforme (les mentions légales visent le contenu du site ; le xlsx ne porte pas de licence propre) |
| Statistiques d'intérêt général depuis le 17/07/2025 | oui | Page Secten : « reconnues statistiques d'intérêt général par le Comité du label de la statistique publique de l'INSEE depuis le 17 juillet 2025 et ce, pour une durée de trois ans » (idem dans le xlsx). Avis de l'**Autorité de la statistique publique** du 17 juillet 2025 « sur la qualification de reconnaissance d'intérêt général de statistiques produites par le CITEPA », JORF n° 167 du 20 juillet 2025, NOR ECOO2521030V (résumé d'outil) : reconnaissance « pour trois ans » (donc jusqu'à mi-2028, déduit). Les séries sont une référence « à vocation informative » | [page Secten](https://www.citepa.org/donnees-air-climat/donnees-gaz-a-effet-de-serre/secten/), [avis JORF](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000051922154) | Conforme |
| Statut du format Secten | – | « Le format Secten ne correspond pas à un format de rapportage officiel » ; « seule la version … dans le bloc « Rapport » en haut de page fait foi » | [page Secten](https://www.citepa.org/donnees-air-climat/donnees-gaz-a-effet-de-serre/secten/) | Information |
| Version des polluants | – | La ligne « Données de polluants atmosphériques ed. 2026 – version du 16/09/2026 » (`Citepa2025_polluants-v2.zip`) est postérieure à la « mise à jour » affichée (16/06/2026). Sans effet sur les GES | [page Secten](https://www.citepa.org/donnees-air-climat/donnees-gaz-a-effet-de-serre/secten/) | Information |

### 5. Budgets carbone de la SNBC 3

**Le bon jeu est 342 / 262 / 194 MtCO2e par an** (2024-2028 / 2029-2033 / 2034-2038, hors puits de carbone). Il est fixé par le **décret n° 2026-636 du 16 juillet 2026** relatif aux budgets carbone nationaux et à la stratégie nationale bas-carbone, JORF n° 0166 du 18 juillet 2026, NOR TECR2618516D (id Légifrance JORFTEXT000054440907). Article 2 : « Les budgets carbone des périodes 2024-2028, 2029-2033 sont révisés et fixés respectivement à 342 et 262 Mt de CO2e par an et le budget carbone pour la période 2034-2038 est fixé à 194 Mt CO2e par an, hors « puits de carbone » ».

| Élément | Valeur à vérifier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Budget 2024-2028 | 342 | 342 Mt CO2e/an | [décret art. 2](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907), [SNBC 3 juillet 2026 p.66-67](https://www.ecologie.gouv.fr/sites/default/files/documents/SNBC3-Partie1-Juillet2026.pdf), [ministère](https://www.ecologie.gouv.fr/politiques-publiques/strategie-nationale-bas-carbone-snbc) | Conforme |
| Budget 2029-2033 | 262 ou 261 | **262** (décret ; SNBC 3 de juillet 2026 : « fixé à 262 Mt CO2e/an » ; page SNBC du ministère). **261** = valeur du projet de juin 2026, encore citée par le Citepa (Rapport p.90 ; Synthèse parle du « projet »), par le HCC (p.136 : « passe de 265 à 261 Mt ») et par la page « Suivi des émissions » du ministère, mise à jour le 22/10/2026 | idem + [Rapport p.90](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf), [HCC p.136](https://www.hautconseilclimat.fr/wp-content/uploads/2026/07/HCC_RA2026-Chapitre-3_1707.pdf), [ministère, suivi](https://ecologie.gouv.fr/strategie-nationale-bas-carbone/suivi-des-emissions-gaz-effet-serre) | **262 est juste.** 261 est périmé (projet) |
| Budget 2034-2038 | 194 ou 193 | **194** (décret, SNBC 3 juillet 2026). **193** = projet de juin 2026 (Citepa p.90, page « Suivi » du ministère) | idem | **194 est juste.** 193 est périmé |
| Tranches annuelles indicatives | – | 2024 : 367 ; 2025 : 359 ; 2026 : 348 ; 2027 : 328 ; 2028 : 308 (décret art. 6). Le projet citait 369 et 364 pour 2024 et 2025 (Synthèse p.1) ; le décret reprend les valeurs de l'inventaire 2026 (déduit de l'égalité avec Secten 2026) | [décret art. 6](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907), [Synthèse p.1](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf) | Information |
| Années de référence du décret | – | 1990 : 547 ; 2005 : 556 ; 2024 : 367, « issues de l'inventaire … du Citepa au format Secten de 2026 » ; secteurs 2024 : transports 125, bâtiments 56, agriculture 78, industrie 62, énergie 31, déchets 15 | [décret art. 3](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907) | Conforme au fichier (arrondis) |

Points d'attention :
- La page « Suivi des émissions » du ministère est **incohérente avec sa propre page SNBC** (261/193 contre 262/194). Elle n'a manifestement pas été remise à jour après le décret. Ne pas s'y fier pour ces deux budgets.
- Les budgets de puits UTCATF ont aussi changé : décret art. 10, budgets indicatifs -46 / -33 / -31 MtCO2e par an (2024-2028 / 2029-2033 / 2034-2038). Le Citepa (Rapport p.524) cite le projet de juin avec « -33 » pour 2024-2028. Si la page parle du puits, utiliser le décret.
- Avant le décret, les versions antérieures du projet donnaient d'autres valeurs (HCC p.136 : 265 pour 2029-2033 ; Wikipédia, résumé d'outil : 265 et 192, non retenu comme preuve) : la valeur dépend donc de la version citée.
- Non vérifié : le texte consolidé sur la page Légifrance elle-même (lu via l'archive DILA).

### 6. Versions anglaises

| Élément | Valeur attendue | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Page Secten en anglais | existe | Existe : « Secten – Citepa », liée par le sélecteur de langue de la page française. **Mais** son « Updated date » affiche **16/05/2025** (périmé) et un article de 2025 | [page EN](https://www.citepa.org/en/air-climate-data/data-greenhouse-gas/secten/) | Écart expliqué (page non mise à jour) |
| Rapport en anglais | existe | **Pas de rapport anglais.** Le lien « Secten report ed. 2026 » mène à `Citepa_Secten-2026-1.pdf`, **octet pour octet identique au rapport français** (24 656 877 octets, `cmp` identique, texte en français) | [PDF « EN »](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026-1.pdf) | Écart |
| Synthèse en anglais | existe | Non trouvée. Le lien « Key messages and summary » de la page EN pointe vers le **xlsx** (`serie_longue_Citepa_Secten_ed_2026-d-1.xlsx`, même taille que l'original : 2 846 114 octets) | [page EN](https://www.citepa.org/en/air-climate-data/data-greenhouse-gas/secten/) | Écart (lien mal câblé) |
| Données en anglais | – | Les zips et le xlsx sont les mêmes fichiers (suffixe « -1 »). Mentions légales EN : https://www.citepa.org/en/legal-notices/ | [page EN](https://www.citepa.org/en/air-climate-data/data-greenhouse-gas/secten/) | Information |
| Article d'annonce en anglais | – | Non trouvé (aucun lien dans l'article ni sur la page FR) | [article FR](https://www.citepa.org/le-rapport-secten-edition-2026-est-en-ligne/) | Non trouvé |
| Hors Citepa | – | Résumé anglais de la SNBC 3 (ministère) : `SNBC3_Summary_ENG.pdf` | [ministère](https://www.ecologie.gouv.fr/sites/default/files/documents/SNBC3_Summary_ENG.pdf) | Information |

Pour une page anglaise du jeu, ne pas annoncer de rapport ou de synthèse Secten en anglais : il n'y en a pas. Renvoyer à la page EN pour le jeu de données seulement.

### 7. Autres sources demandées

| Source | Résultat | Verdict |
|---|---|---|
| Baromètre mensuel du Citepa | [Page](https://www.citepa.org/barometre-des-emissions-mensuelles/) mise à jour le 12/10/2026, [note du 13/10/2026](https://www.citepa.org/wp-content/uploads/2026/10/Note-barometre-T2-2026vf-d.pdf) : 2025 = **359,4** hors UTCATF (énergie 31,4 ; industrie 58,4 ; déchets 15,3 ; bâtiments 54,9 ; agriculture 76,6 ; transports 122,9) ; prévision 2026 : 349,4 (-2,8 %). Total 2025 identique à celui du fichier (359,4) | Conforme |
| Ministère de la Transition écologique, suivi des émissions | [Page](https://ecologie.gouv.fr/strategie-nationale-bas-carbone/suivi-des-emissions-gaz-effet-serre) (mise à jour le 22/10/2026) : 2024 = 367 (-3,0 %) ; 2025 = 359 « -2,2 % » dans le corps du texte mais « -2,1 % » dans « En bref » (le Citepa dit -2,1 %). Ne qualifie pas 2025 d'estimation. Budgets 261/193 périmés (voir 5) | Écart mineur (-2,2 contre -2,1 ; budgets) |
| HCC, rapport annuel 2026 (09/07/2026) | [Chapitre 3](https://www.hautconseilclimat.fr/wp-content/uploads/2026/07/HCC_RA2026-Chapitre-3_1707.pdf) : 359 « d'après la pré-estimation du Citepa », -2,1 % (-7,6 Mt) depuis 367 ; puits UTCATF 2025 « pré-estimé à -51 », moyenne 2015-2024 de -53 MtCO2e/an ; puits forestier « fortement dégradé depuis 2015 » | Conforme |
| SDES, « Chiffres clés du climat » | L'édition 2026 n'est pas accessible (HTTP 403). La page de l'[édition 2025](https://www.statistiques.developpement-durable.gouv.fr/chiffres-cles-du-climat-france-europe-et-monde-edition-2025?rubrique=26&dossier=1263) (publiée le 04/11/2025) s'appuie sur l'ancienne édition Secten : « -32 % (1990-2024) », UTCATF 2024 = valeur 2023 reportée | Non trouvé (édition 2026) ; édition 2025 périmée |
| CCNUCC, EEA | Pages `unfccc.int` et `eea.europa.eu` non exploitables (contenu vide, HTTP 401). Le rapport Citepa renvoie à un tableau « format CCNUCC – mars 2026 » (p.544) : CO2e hors UTCATF 1990 = 547, 2005 = 556, 2022 = 406, 2023 = 378, 2024 = 367 (-33 %). Aucun contrôle sur le site CCNUCC lui-même | Non trouvé (sites) ; cohérent via le rapport |
| Presse | Non contrôlée (quota de recherche épuisé) | Non trouvé |

---

### Les quatre notes « À savoir »

#### (1) Total hors UTCATF, définition CCNUCC, hors transport international

**Verdict : exacte, à préciser.** Le Citepa exclut les soutes internationales **maritimes, fluviales et aériennes** (pas seulement air et mer) et les sources biotiques ou non anthropiques ; le trafic aérien et maritime **domestique** reste inclus. Le périmètre est l'Outre-mer inclus dans l'UE.

Formulation proposée :
> Ce total ne compte pas le puits de carbone des terres et des forêts (UTCATF), ni les transports internationaux aériens, maritimes et fluviaux, selon les règles de la CCNUCC. Il couvre la France hexagonale et les Outre-mer inclus dans l'Union européenne.

#### (2) 2025 est une estimation, chaque édition révise toute la série

**Verdict : exacte, à préciser.** 2025 est une « estimation proxy » ou « pré-estimation » provisoire ; elle sera remplacée par l'inventaire consolidé de l'édition de juin 2027. 2024 est la dernière année « consolidée » de l'édition 2026, mais elle peut encore bouger (le proxy de 2025 prévoyait -1,8 % pour 2024, l'inventaire a donné -3,0 %). Le fichier et le Citepa disent : « chaque nouvelle édition annule et remplace les précédentes ».

Formulation proposée :
> La dernière année, 2025, est une estimation provisoire du Citepa, à confirmer par l'inventaire de l'édition suivante. À chaque édition, le Citepa recalcule toute la série : les chiffres des années précédentes peuvent changer.

#### (3) Chiffres du Citepa, statistiques d'intérêt général, cités et non sous Licence Ouverte

**Verdict : exacte, avec deux précisions.**
- La reconnaissance d'intérêt général vient d'un **avis de l'Autorité de la statistique publique du 17 juillet 2025**, pour **trois ans**. La page du Citepa l'attribue au « Comité du label de la statistique publique de l'INSEE ». Elle donne à ces séries une valeur de référence « à vocation informative » ; le format Secten reste « pas un format de rapportage officiel ».
- Les conditions publiées sont : reproduction « autorisée à la condition de citer le Citepa dans les sources, à chaque utilisation » ; « Tous droits réservés » ; aucune licence ouverte annoncée. Le fichier demande la mention « Citepa/Secten édition juin 2026 ». Je n'ai trouvé aucune licence propre aux fichiers de données : si le kit redistribue les chiffres, une confirmation auprès du Citepa (infos@citepa.org) reste prudente.

Formulation proposée :
> Ces chiffres sont ceux du Citepa (inventaire Secten, édition juin 2026), reconnus statistiques d'intérêt général en 2025 par l'Autorité de la statistique publique. Ils sont cités avec leur source ; ils ne sont pas publiés sous Licence Ouverte.

#### (4) Le puits des terres et forêts s'est affaibli (« -52 en 2024 contre -39 en 1990 »)

**Verdict : la comparaison proposée va dans le mauvais sens. À corriger.** Un puits de -52 MtCO2e est **plus fort** qu'un puits de -39 : la capacité d'absorption de 2024 dépasse celle de 1990. Ce que dit le Citepa : « Fortement à la hausse entre 1990 et 2005, le puits a drastiquement diminué de 2014 à 2017, passant d'environ -63 Mt CO2e dans les années 2000 à seulement -46 Mt CO2e en 2017 » (Rapport p.516 et 522, Synthèse p.17). La série de la page Secten (même jeu de données) : -39,3 (1990), -68,6 (2005), maximum -69,0 (2006), -67,2 (2013), -45,8 (2017), -59,8 (2018), puis -48,8 à -58,3 entre 2019 et 2023, -52,0 (2024), -51,3 (2025). Le décret reprend -39 / -69 / -52 pour 1990 / 2005 / 2024.

Autres points à respecter :
- Le recul est celui du **puits forestier** depuis 2014-2015 (sécheresses, scolytes, mortalité, prélèvements). Le HCC : « fortement dégradé depuis 2015 ».
- La stabilité récente (≈ -50 à -52) est peut-être trompeuse : le Citepa écrit qu'elle tient « plutôt à l'extrapolation des données en fin de période … qu'à une tendance vérifiée », et que « l'érosion du puits cache en réalité une baisse encore plus importante » tamponnée par le bois mort (Rapport p.522).
- Le niveau dépend de l'édition : l'édition 2026 ajoute un puits en Guyane (≈ 10 Mt/an) et corrige les défrichements (Rapport p.516 et 524). Le tableau « format CCNUCC » de l'annexe donne un autre « net » (voir la partie 2).
- 2025 (-51,3) reprend largement 2024, ne pas en tirer une tendance.

Formulation proposée :
> Les terres et les forêts absorbent plus de carbone qu'elles n'en émettent : environ 52 MtCO2e en 2024, soit près de 14 % des émissions brutes. Ce puits s'est nettement affaibli depuis le milieu des années 2000 (environ 69 MtCO2e en 2005), surtout à cause de la dégradation des forêts, même s'il reste supérieur à son niveau de 1990 (environ 39). Il est recalculé à chaque édition.

---

### Conclusion

#### Écarts et points à corriger (par ordre d'importance)

1. **Note (4), sens de la comparaison.** « -52 en 2024 contre -39 en 1990 » ne montre pas un affaiblissement : le puits est plus fort qu'en 1990. L'affaiblissement se mesure depuis 2005-2006 (≈ -69) ou depuis 2013 (-67). Reformuler comme ci-dessus.
2. **Budgets SNBC 3 : 342 / 262 / 194 est juste** (décret n° 2026-636 du 16/07/2026, JORF du 18/07/2026, art. 2). Les valeurs 261 / 193 sont celles du projet de juin 2026 ; elles figurent encore dans le rapport Secten 2026, le HCC et la page « Suivi des émissions » du ministère (22/10/2026).
3. **Pas de version anglaise du rapport ni de la synthèse.** La page EN existe (avec une date de mise à jour périmée, 16/05/2025), mais son lien « rapport » sert le PDF français (identique octet pour octet) et son lien « synthèse » sert le xlsx.
4. **Puits 2025 (-51,3) : valeur conforme, mais reprise de 2024** (plus feux de forêt). À ne pas présenter comme une estimation indépendante.
5. **Incohérences internes au Citepa, sans effet sur le fichier :** (a) Figure 1 de la Synthèse (libellés 403 et 376 pour 2022 et 2023, contre 406 et 378,2 dans le texte) ; (b) « CO2e net » 2024 = 326 dans l'annexe (p.544) contre 315 dans le texte (périmètre UTCATF différent).
6. **Écart mineur du ministère :** 2025 en « -2,2 % » dans le corps de la page, « -2,1 % » dans « En bref » (le Citepa : -2,1 %).

#### Conformes

Totaux 2024 (367,0), 2023 (378,2), 2025 (359,4, confirmé à la décimale par le baromètre du 13/10/2026), 1990 et 2005 (547 et 556 arrondis ; les dixièmes ne se lisent que dans le tableau du Citepa), les six secteurs 2024, les puits -52,0 / -51,3 / -39,3, la définition du total et le périmètre, les dates (16/06/2026 ; « date edition » 2026-06-01 = « édition juin 2026 »), la mention de citation, le statut d'intérêt général (depuis le 17/07/2025, trois ans), l'absence de Licence Ouverte. Les notes (1), (2) et (3) sont justes, avec les précisions ci-dessus.

#### Non trouvé ou non vérifiable

Valeurs CCNUCC et EEA sur leurs propres sites ; édition 2026 des Chiffres clés du climat du SDES ; presse ; texte Légifrance consolidé du décret sur la page Légifrance (lu dans l'archive DILA, mêmes identifiants).

---

### URL consultées (2026-11-02)

Citepa
- https://www.citepa.org/donnees-air-climat/donnees-gaz-a-effet-de-serre/secten/ (HTML brut et résumé)
- https://www.citepa.org/en/air-climate-data/data-greenhouse-gas/secten/
- https://www.citepa.org/le-rapport-secten-edition-2026-est-en-ligne/
- https://www.citepa.org/mentions-legales/
- https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf
- https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf
- https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026-1.pdf (identique au précédent)
- https://www.citepa.org/wp-content/uploads/2026/06/serie_longue_Citepa_Secten_ed_2026-d.xlsx (feuille « Lisez-moi » et cellule « date edition » seulement ; en-têtes HTTP du fichier « -d-1 »)
- https://www.citepa.org/donnees-air-climat/donnees-gaz-a-effet-de-serre/
- https://www.citepa.org/barometre-des-emissions-mensuelles/
- https://www.citepa.org/wp-content/uploads/2026/10/Note-barometre-T2-2026vf-d.pdf

Journal officiel et Légifrance
- https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907 (décret n° 2026-636 du 16/07/2026 ; texte lu dans https://echanges.dila.gouv.fr/OPENDATA/JORF/JORF_20260718-002549.tar.gz, répertoire https://echanges.dila.gouv.fr/OPENDATA/JORF/)
- https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000051922154 (avis ASP du 17/07/2025, résumé d'outil)
- https://www.legifrance.gouv.fr/jorf/jo/2026/07/17 et pages de codes Légifrance (sans contenu exploitable)

Ministère de la Transition écologique
- https://www.ecologie.gouv.fr/politiques-publiques/strategie-nationale-bas-carbone-snbc
- https://ecologie.gouv.fr/strategie-nationale-bas-carbone/suivi-des-emissions-gaz-effet-serre
- https://www.ecologie.gouv.fr/sites/default/files/documents/SNBC3-Partie1-Juillet2026.pdf
- https://www.ecologie.gouv.fr/sites/default/files/documents/SNBC3-ResumeSNBC-Juillet2026.pdf, SNBC3-Annexes-Juillet2026_0.pdf, SNBC3-Partie2-Juillet2026.pdf, SNBC3_Summary_ENG.pdf, Fiche_SECTEN_2026_V4_mini-site_SNBC_clean.pdf (même répertoire `/sites/default/files/documents/`)

Haut Conseil pour le climat
- https://www.hautconseilclimat.fr/publications/ et https://www.hautconseilclimat.fr/publications/dangers-climatiques-la-france-face-a-ses-responsabilites/
- https://www.hautconseilclimat.fr/wp-content/uploads/2026/07/HCC_RA2026-Chapitre-3_1707.pdf
- https://www.hautconseilclimat.fr/wp-content/uploads/2026/07/HCC_RA2026-Resume-executif-Recommandations_1707.pdf

SDES, CCNUCC, EEA, autres
- https://www.statistiques.developpement-durable.gouv.fr/chiffres-cles-du-climat-france-europe-et-monde-edition-2025?rubrique=26&dossier=1263 (édition 2025) ; la page de l'édition 2026 renvoie HTTP 403
- https://www.statistiques.developpement-durable.gouv.fr/chiffres-cles-du-climat-0?rubrique=26
- https://unfccc.int/ghg-inventories-annex-i-parties/2026 (contenu vide) ; https://www.eea.europa.eu/en/analysis/publications/trends-and-projections-in-europe-2026 (HTTP 401)
- https://fr.wikipedia.org/wiki/Strat%C3%A9gie_nationale_bas-carbone (résumé d'outil, non retenu comme preuve)

## Mises à jour

- **03/11/2026, décision du PO** : citer le Citepa suffit. Ses conditions autorisent la reproduction en citant la source ; le kit reprend des chiffres avec la source et la date, jamais ses fichiers ni ses figures. Pas de demande au Citepa.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
