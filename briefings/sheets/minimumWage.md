# `minimumWage` · Smic et salaires

**Vérifiée le 02/11/2026** : double vérification sur le web, chiffres conformes (section « Double vérification ») ; deux « À savoir » corrigés avant d'entrer dans le kit (la définition du Smic net, la hausse de juin).

| Champ | Valeur |
| --- | --- |
| Indicateur | `minimumWage`, dossier « Travail et retraites » (`work`), page de type série, ticket #27 de l'app |
| Données | `briefings/data/minimumWage.json`, écrit par `yarn briefings minimumWage` le 2026-11-02 |
| Sources | Insee, « Salaire minimum interprofessionnel de croissance (Smic) », https://www.insee.fr/fr/statistiques/1375188 ; Dares, « Les indices de salaire de base » (enquête Acemo), https://dares.travail-emploi.gouv.fr/donnees/les-indices-de-salaire-de-base (le site refuse les scripts : séries lues dans la BDM de l'Insee) ; Insee, « Les salaires dans le secteur privé en 2024 », Insee Première n° 2079, https://www.insee.fr/fr/statistiques/8657156 ; Licence Ouverte 2.0 |
| Séries | `hourly` : Smic brut horaire, BDM `000822484`, mensuel, 2005-01 à 2026-11 ; `monthlyGross` : Smic mensuel brut pour 35 h, BDM `000879877`, 2005-07 à 2026-11 ; `monthlyNet` : Smic mensuel net (après cotisations salariales, CSG et CRDS), BDM `000879878` ; `mayotteHourly` : Smic brut horaire à Mayotte, BDM `011800491`, 2017-01 à 2026-11 ; `baseWage` : glissement annuel de l'indice des salaires mensuels de base (Dares), BDM `010562675`, 2021-T2 à 2026-T2 ; `meanNetWage` : salaire net annuel moyen en EQTP, secteur privé, BDM `010752333`, 1996 à 2024 |
| Chiffre clé | 12,31 € brut de l'heure depuis juin 2026, en hausse après 12,02 € (1 867,02 € brut et 1 477,93 € net par mois pour 35 h) |
| Règles | Le chiffre clé est le Smic en vigueur, au mois de sa dernière hausse. L'indice des salaires de base n'a pas de valeur au 1er trimestre 2020 ni de glissement au 1er trimestre 2021 (enquête Acemo suspendue au printemps 2020) : le dossier garde les trimestres qui suivent. La page compare salaires et prix en lisant `inflation.json` |
| Première édition | À remplir à la publication |

## « À savoir »

1. Deux hausses en 2026 : 12,02 € au 1er janvier (décret n° 2025-1228), 12,31 € au 1er juin (arrêté du 22 mai 2026, JORF du 24 mai), la seconde automatique, l'indice des prix des ménages du premier quintile ayant augmenté de plus de 2 % (+2,5 % depuis novembre 2025).
2. Le Smic net est net des cotisations salariales, de la CSG et de la CRDS (définition de l'Insee ; même montant sur service-public). La phrase d'abord prévue, qui opposait deux « nets », était fausse : elle n'est pas reprise.
3. L'enquête Acemo couvre les entreprises de 10 salariés ou plus, hors agriculture ; elle a été suspendue au printemps 2020 (Dares Indicateurs n° 16).
4. Mayotte a son propre Smic : 9,56 € brut de l'heure en novembre 2026.

Non repris : la rupture de 2024 du salaire moyen, la vérification montrant que seule Mayotte y entre en 2024, pour moins d'un euro net par mois.

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans appeler l'API de la BDM qu'utilise le script.

Date de la vérification : 2026-11-02. Méthode : recherche web et lecture de pages et fichiers publiés (Légifrance, service-public.gouv.fr, Insee hors API, Dares, presse). Aucun appel à api.insee.fr. Aucun fichier du dépôt modifié.

Légende des verdicts : Conforme, Écart expliqué, Écart, Non trouvé. Quand une confirmation n'est qu'indirecte (page inaccessible, résumé d'un moteur de recherche), c'est écrit dans la colonne « Valeur trouvée ».

### 1. Points à retenir en premier

| # | Constat | Gravité |
|---|---|---|
| 1 | « À savoir » n° 2 (le net de la BDM serait « après CSG et CRDS seulement », donc différent du net de service-public) est **réfuté** : le net Smic de l'Insee est net de cotisations sociales salariales, de CSG et de CRDS, et le montant est identique à celui de service-public (1 477,93 €). | Écart (texte à corriger) |
| 2 | « À savoir » n° 4 (« depuis 2024 le salaire moyen inclut apprentis, stagiaires et Mayotte, rupture de série ») est **imprécis** pour la série BDM : les apprentis et stagiaires sont déjà inclus sur toute la série 1996-2023 ; seule Mayotte entre en 2024, avec un effet inférieur à 1 € net par mois. La rupture documentée par l'Insee vise les éditions antérieures de l'Insee Première. | Écart expliqué (texte à reformuler) |
| 3 | Mayotte 2017-01 = 7,37 € : la seule source directe trouvée (Mayotte Hebdo) écrit 7,34 €, mais son propre montant mensuel (1 245,53 € pour 169 h) correspond à 7,37 €, et le décret 2017-1719 (7,46 € en 2018, + 1,23 %) redonne 7,37 €. Aucun texte officiel de 2017 retrouvé. | Écart expliqué (probablement conforme) |
| 4 | Smic mensuel 2005-07 = 1 217,88 € : l'IPP donne 1 217,91 € (base 151,67 h) ; 1 217,88 € correspond à 8,03 × 35 × 52 / 12 (base exacte 151,6667 h). | Écart expliqué (arrondi) |
| 5 | Smic net 2005-07 = 957,74 € : aucune source officielle retrouvée (un seul site commercial, vu par le moteur de recherche seulement) ; cohérent avec le tableau Insee SMIC35. | Non trouvé (source officielle) |

Tout le reste est conforme ou cohérent (détail ci-dessous).

### 2. Smic (BDM 000822484, 000879877, 000879878, 011800491)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Smic horaire brut en vigueur depuis juin 2026 | 12,31 € | 12,31 € à compter du 1er juin 2026 : arrêté du 22 mai 2026, JORF n° 0121 du 24 mai 2026 | https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054126589 ; https://www.service-public.gouv.fr/particuliers/vosdroits/F2300 ; https://www.insee.fr/fr/statistiques/1375188 | Conforme |
| Montant précédent (« hausse » de l'indicateur clé) | 12,02 € | 12,02 € (hausse de 2,41 %, soit + 0,29 €) | https://www.service-public.gouv.fr/particuliers/actualites/A18916?lang=en ; https://www.legisocial.fr/actualites-sociales/7943-smic-revalorisation-automatique-1er-juin-2026.html | Conforme |
| Smic horaire brut au 1er janvier 2026 | 12,02 € | 12,02 € : décret n° 2025-1228 du 17 décembre 2025, JORF du 18 décembre 2025, effet 1er janvier 2026 (+ 1,18 % par rapport à 11,88 €) | https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000053042520 ; https://entreprendre.service-public.gouv.fr/actualites/A16528 | Conforme |
| Smic horaire brut 2005-01 | 7,61 € | 7,61 € en vigueur du 1er juillet 2004 (décret 2004-633) au 30 juin 2005 ; 8,03 € à partir du 1er juillet 2005 (décret 2005-719) | https://baremes.ipp.eu/parameters/marche-du-travail/marche_travail.salaire_minimum.smic/table | Conforme |
| Smic mensuel brut 35 h (151,67 h), novembre 2026 | 1 867,02 € | 1 867,02 € depuis le 1er juin 2026 (arrêté du 22 mai 2026 ; circulaire Cnav 2026-16). Aucune autre revalorisation trouvée entre le 1er juin et le 2 novembre 2026 | https://legislation.lassuranceretraite.fr/Pdf/circulaire_cnav_2026_16_12062026.pdf ; https://www.service-public.gouv.fr/particuliers/vosdroits/F2300 ; https://www.insee.fr/fr/statistiques/1375188 | Conforme |
| Smic mensuel brut 35 h, 2005-07 | 1 217,88 € | 1 217,91 € (8,03 € × 151,67 h) chez l'IPP ; 8,03 × 35 × 52 / 12 = 1 217,88 € (calcul de ma part). Un site (blog-rh.com, vu dans un résumé de moteur de recherche, page inaccessible) donne 1 217,88 € | https://baremes.ipp.eu/parameters/marche-du-travail/marche_travail.salaire_minimum.smic/table | Écart expliqué (3 centimes : durée 151,67 h arrondie contre 151,6667 h exacte ; la BDM utilise l'exacte, comme pour 1 823,03 € et 1 867,02 € en 2026) |
| Smic mensuel net 35 h, novembre 2026 | 1 477,93 € | 1 477,93 € (tableau « Montant net (déduction des cotisations salariales) », « donné à titre indicatif », page vérifiée le 1er juin 2026) | https://www.service-public.gouv.fr/particuliers/vosdroits/F2300 | Conforme |
| Smic mensuel net 35 h, 2005-07 | 957,74 € | Non trouvé en source officielle. Un seul site commercial (blog-rh.com) donne 957,74 € (résumé de moteur de recherche, page non lisible). Cohérence : le tableau Insee SMIC35 donne pour 2005 (moyenne annuelle) 932,70 € net pour 1 186,03 € brut, soit un rapport net/brut de 0,7864, identique à 957,74 / 1 217,88 = 0,7864 (calcul de ma part) | https://www.insee.fr/fr/statistiques/fichier/8668594/SMIC35.xlsx | Non trouvé (source officielle) ; cohérent |
| Smic horaire brut Mayotte, novembre 2026 | 9,56 € | 9,56 € depuis le 1er juin 2026 (arrêté du 22 mai 2026, article 1) ; 9,33 € avant (décret 2025-1228) ; 1 449,93 € brut mensuel | https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054126589 ; https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000053042520 ; https://legislation.lassuranceretraite.fr/Pdf/circulaire_cnav_2026_16_12062026.pdf | Conforme |
| Smic horaire brut Mayotte, 2017-01 | 7,37 € | Pas de texte officiel de 2017 retrouvé. Mayotte Hebdo (3 janvier 2017) annonce « 7,34 € » (contre 7,30 € en 2016) mais « 1 245,53 € brut pour 169 h », or 7,37 × 169 = 1 245,53 et 7,34 × 169 = 1 240,46. Décret n° 2017-1719 du 20 décembre 2017 : 7,46 € au 1er janvier 2018, + 1,23 %, donc 7,46 / 1,0123 = 7,37 € (calcul de ma part). À Mayotte, le Code du travail (donc le Smic) n'est applicable que depuis le 1er janvier 2018 ; avant, le minimum s'appelait SMIG (IEDOM) | https://www.mayottehebdo.com/actualite/en_bref/le-smic-a-augmente-en-2017-de-4-centimes-par-heure/ ; https://www.lemondedudroit.fr/social/306-relations-individuelles-de-travail/55302-relevement-du-smic-au-1er-janvier-2018.html ; https://www.iedom.fr/IMG/rapport_annuel_iedom_mayotte_2020/index-47.html (résumé de moteur de recherche) | Écart expliqué (7,37 très probable ; non confirmé par un texte de 2017 ; la source locale contient une incohérence interne) |

Titres des séries Insee (pages publiques, sans l'API) : 000879877 « Montant mensuel brut du Smic … pour 35 heures de travail par semaine (151,67 heures par mois) » ; 000879878 « Montant mensuel net du Smic … (151,67 heures par mois), après déduction de la CSG et CRDS » ; 011800491 « Montant du Smic … brut horaire à Mayotte ». Sources : https://www.insee.fr/fr/statistiques/serie/000879877, https://www.insee.fr/fr/statistiques/serie/000879878, https://www.insee.fr/fr/statistiques/serie/011800491.

### 3. Indice de salaire mensuel de base, glissement annuel (BDM 010562675)

Les pages Dares (dares.travail-emploi.gouv.fr) renvoient une page de vérification anti-robot : les valeurs Dares ci-dessous sont lues dans la presse qui cite la Dares ou dans les notes de conjoncture de l'Insee.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2026-T2, sur un an | 2,0 % | + 2 % sur un an, + 0,7 % sur le trimestre ; résultats définitifs Dares du 25 septembre 2026 ; inflation hors tabac 1,7 % | https://www.toutsurmesfinances.com/actualites/?p=2130 ; https://bourse.fortuneo.fr/actualites/le-salaire-de-base-dans-le-prive-augmente-plus-vite-que-l-inflation-au-2eme-trimestre-5259463 (AFP, Dares) | Conforme |
| 2026-T1, sur un an | 1,7 % | + 1,7 % sur un an (Dares, via 24matins) ; la note de conjoncture Insee de mars 2026 affichait aussi 1,7 % pour le T1 2026 (colonne de prévision) | https://www.24matins.fr/salaires-prives-ce-que-montre-vraiment-le-regain-face-a-linflation-1421320 ; https://www.insee.fr/fr/statistiques/fichier/8907437/ndc-mars-2026-salaires.pdf | Conforme (source de presse) |
| 2025-T4, sur un an | 1,7 % | + 1,7 % (résultats provisoires Dares du 6 février 2026 ; Insee : « + 1,7 % au quatrième trimestre 2025 ») | https://tpeactu.fr/2026/02/08/salaires-prive-hausse-inflation-2025/ ; https://www.insee.fr/fr/statistiques/fichier/8907437/ndc-mars-2026-salaires.pdf | Conforme |
| 2025-T3, sur un an | 2,0 % | + 2,0 % (Insee : « + 2,0 % au troisième trimestre 2025, après + 2,2 % et + 2,1 % aux deux premiers ») | https://www.insee.fr/fr/statistiques/fichier/8684405/ndc-dec-2025-salaires.pdf ; https://www.insee.fr/fr/statistiques/fichier/8907437/ndc-mars-2026-salaires.pdf | Conforme |
| 2021-T2, sur un an | 1,4 % | + 1,4 % entre juin 2020 et juin 2021, + 0,3 % sur le trimestre (Dares Indicateurs n° 51, 17 septembre 2021) : lu uniquement dans le résumé d'un moteur de recherche, page Dares inaccessible. Recoupement : le tableau 2 de Dares Indicateurs n° 16 (mars 2022) donne + 0,3 % pour le T2 2021 et + 1,5 % sur un an pour le T3 2021 | https://dares.travail-emploi.gouv.fr/publication/evolution-des-salaires-de-base-et-conditions-demploi-dans-le-secteur-prive-T22021 (inaccessible) ; https://presse.tripalio.fr/wp-content/uploads/2022/03/Acemo_2021_T4_definitifs.pdf | Conforme (confirmation indirecte) |
| 2020-T1 « non disponible » et pas de valeur pour la variation du T1 2021 | pourquoi ? | Dares Indicateurs n° 16 (mars 2022) : « pour le salaire mensuel de base, les glissements annuels aux T1 2020 et T1 2021 ne peuvent pas être calculés ». Cause : « l'enquête trimestrielle Acemo de la Dares a été temporairement suspendue au printemps 2020. De ce fait, il n'existe pas de données sur les évolutions du SMB au premier trimestre 2020 » (note Insee, juin 2025, avec des auteurs de la Dares). L'Insee précise que l'enquête trimestrielle a été remplacée au T1 2020 par une enquête flash liée à la crise sanitaire. Sans indice du T1 2020, ni le glissement annuel du T1 2020 ni celui du T1 2021 (qui prend le T1 2020 comme base) ne se calculent. Le questionnaire est allégé depuis l'enquête du T2 2020 | https://presse.tripalio.fr/wp-content/uploads/2022/03/Acemo_2021_T4_definitifs.pdf ; https://www.insee.fr/fr/statistiques/fichier/8594928/ndc-juin-2025-ecl3-SMB.pdf ; https://insee.fr/fr/statistiques/4511787 | Conforme (explication sourcée) |

Remarque : la note de conjoncture Insee de mars 2026 donnait 1,7 % pour le T2 2026 (prévision) ; le chiffre observé par la Dares est 2,0 %, celui du fichier.

### 4. Salaire net annuel moyen en EQTP, secteur privé (BDM 010752333)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2024 | 32 791 € | Insee Première n° 2079 : 2 733 € nets par mois en EQTP en 2024 (3 602 € bruts). 2 733 × 12 = 32 796 € ; 32 791 / 12 = 2 732,6 €, arrondi à 2 733 €. Le montant annuel n'est pas écrit dans la publication. Croissance 2023-2024 : 32 791 / 31 902 = + 2,8 %, comme indiqué (+ 2,8 % en euros courants) | https://www.insee.fr/fr/statistiques/8657156 ; https://www.insee.fr/fr/statistiques/fichier/8657156/ip2079.pdf | Conforme (cohérent, annuel non publié tel quel) |
| 2023 | 31 902 € | 31 902 € dans le tableau EQTP01 de l'Insee Résultats « Séries longues sur les salaires dans le secteur privé » (base Tous salariés 2023, paru le 04/12/2025) | https://www.insee.fr/fr/statistiques/8660332 (fichier https://www.insee.fr/fr/statistiques/fichier/8660332/EQTP01.xlsx) | Conforme |
| 1996 | 18 459 € | 18 459 € dans le même tableau. Les éditions précédentes donnent 18 461 € (base Tous salariés 2022 et 2021, pages 8668519 et 8668548) : révision de 2 € | https://www.insee.fr/fr/statistiques/fichier/8660332/EQTP01.xlsx ; https://www.insee.fr/fr/statistiques/fichier/8668519/EQTP01.xlsx | Conforme |
| Publication de référence | « Les salaires dans le secteur privé en 2024 », Insee Première n° 2079, https://www.insee.fr/fr/statistiques/8657156 | Titre, numéro et lien exacts ; paru le 23/10/2025 (octobre 2025) | https://www.insee.fr/fr/statistiques/8657156 | Conforme |

Note : l'Insee Références (juillet 2026) arrondit à la dizaine : 2 730 € en euros courants pour 2024 (figure 1), 2 733 € en euros constants 2024 (figure 2). Ce n'est pas un désaccord. https://www.insee.fr/fr/statistiques/8733089

### 5. Pages sources et licences

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Page Insee Smic | https://www.insee.fr/fr/statistiques/1375188, « Salaire minimum interprofessionnel de croissance (Smic) » | La page existe ; titre complet « Salaire minimum interprofessionnel de croissance (Smic), Données annuelles de 1980 à 2026 », datée du 09/09/2026 ; elle donne 12,31 € et 1 867,02 € depuis le 01/06/2026, Mayotte 9,56 € et 1 449,93 € ; elle ne donne aucun Smic net. Remarque mineure : la page indique une publication au JO le 22/05/2026, Légifrance indique le 24/05/2026 (l'arrêté est du 22/05) | https://www.insee.fr/fr/statistiques/1375188 ; https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054126589 | Conforme (titre abrégé) |
| Page Dares « Les indices de salaire de base » | https://dares.travail-emploi.gouv.fr/donnees/les-indices-de-salaire-de-base | Page inaccessible (vérification anti-robot). Le titre « Les indices de salaire de base » est attesté par un moteur de recherche (miroir tiers fgeerolf.com, qui recopie le jeu de données Dares) et par Dares Indicateurs n° 16, qui renvoie à une ressource « Les indices de salaire de base » sur le site de la Dares. Je n'ai pas pu ouvrir la page elle-même | https://fgeerolf.com/data/dares/les-indices-de-salaire-de-base.html ; https://presse.tripalio.fr/wp-content/uploads/2022/03/Acemo_2021_T4_definitifs.pdf | Conforme (confirmation indirecte) |
| Licence des données Dares | (à confirmer) | Le jeu de données Dares « Indices de salaires de base par secteur d'activité et catégorie socioprofessionnelle » sur data.gouv.fr (producteur : ministère du Travail) est sous Licence Ouverte (pied de page : version 2.0), dernière mise à jour 29 octobre 2026. Je n'ai pas pu lire les mentions légales du site de la Dares | https://www.data.gouv.fr/datasets/indices-de-salaires-de-base-par-secteur-d-activite-et-categorie-socioprofessionnelle-30378584 | Conforme (via data.gouv.fr, pas via le site de la Dares) |
| Licence des données Insee | Licence Ouverte 2.0 | « Sauf mention contraire, les informations publiques diffusées sur ce site (données, bases de données, publications, fichiers téléchargeables) sont mises à disposition sous la Licence Ouverte / Open Licence version 2.0 (Etalab) » ; mention « Source : Insee » et date de dernière mise à jour à indiquer | https://www.insee.fr/fr/information/2008466 | Conforme |

### 6. Les cinq énoncés « À savoir »

| Énoncé | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| (1) Deux hausses en 2026 : 12,02 € au 1er janvier, 12,31 € au 1er juin, la seconde automatique car l'inflation a dépassé 2 % | Deux hausses ; la seconde automatique, inflation > 2 % | Deux hausses confirmées : décret 2025-1228 (1er janvier, + 1,18 %) et arrêté du 22 mai 2026 (1er juin, + 2,41 %). Hausse de juin = mécanisme légal de l'article L3231-5 du Code du travail : l'indice des prix à la consommation hors tabac des ménages du premier quintile de niveau de vie a progressé de 2,5 % par rapport à novembre 2025 (indice d'avril 2026, définitif le 13 mai 2026), au-delà du seuil de 2 %. Nuance : ce n'est pas l'inflation globale (2,2 % sur un an en avril 2026 selon service-public) mais l'indice des ménages modestes depuis la dernière fixation du Smic | https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000053042520 ; https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054126589 ; https://www.editions-tissot.fr/actualite/droit-du-travail/smic ; https://www.legisocial.fr/actualites-sociales/7943-smic-revalorisation-automatique-1er-juin-2026.html ; https://www.service-public.gouv.fr/entreprendre/actualites/A17008 | Conforme (à préciser : « indice des prix des ménages modestes ≥ 2 % depuis la dernière revalorisation », pas « l'inflation a dépassé 2 % ») |
| (2) Le net de la BDM est après CSG et CRDS seulement, alors que service-public donne un net après toutes les cotisations salariales, donc les deux nets diffèrent | Deux nets différents | **Réfuté.** (a) Insee, tableau SMIC35 : la colonne « Salaire minimum mensuel net de prélèvements » porte la note « Net de cotisations sociales, contribution sociale généralisée (CSG) et contribution au remboursement de la dette sociale (CRDS) » ; (b) définition Insee du salaire net : brut moins cotisations sociales salariales, CSG et CRDS ; (c) service-public affiche 1 477,93 € pour 1 867,02 € brut, soit exactement le montant du fichier ; (d) calcul de ma part : avec la seule CSG-CRDS (9,7 % × 98,25 % ≈ 9,5 %), le net serait d'environ 1 689 €, très loin de 1 477,93 € (taux de prélèvement réel 20,8 %). Le titre de la série (« après déduction de la CSG et CRDS ») est un raccourci de l'Insee. Les deux nets sont avant impôt sur le revenu et indicatifs (dépendent de l'employeur et du secteur selon service-public) | https://www.insee.fr/fr/statistiques/fichier/8668594/SMIC35.xlsx ; https://www.insee.fr/fr/metadonnees/definition/c2166 ; https://www.service-public.gouv.fr/particuliers/vosdroits/F2300 ; https://www.insee.fr/fr/statistiques/serie/000879878 | **Écart** (énoncé à supprimer ou à corriger) |
| (3) L'enquête Acemo couvre les entreprises de 10 salariés ou plus, hors agriculture | Idem | Dares : « L'enquête trimestrielle Acemo porte sur les salariés du privé hors agriculture, particuliers employeurs et activités extraterritoriales des entreprises (au sens d'unités légales) de 10 salariés ou plus » ; champ : France hors Mayotte | https://presse.tripalio.fr/wp-content/uploads/2022/03/Acemo_2021_T4_definitifs.pdf ; https://www.insee.fr/fr/statistiques/fichier/8594928/ndc-juin-2025-ecl3-SMB.pdf ; https://www.insee.fr/fr/metadonnees/definition/c2067 | Conforme |
| (4) Depuis 2024, le salaire moyen inclut apprentis, stagiaires et Mayotte : rupture de série | Idem | Insee Première n° 2079 : « Le champ de cette étude annuelle inclut désormais les salariés de Mayotte, ainsi que les apprentis et les stagiaires rémunérés. Les données de cette étude ne sont pas comparables à celles des publications précédentes. » L'élargissement porte sur 2023 et 2024 pour Mayotte et « sur les années antérieures pour l'inclusion des apprentis et stagiaires ». Pour les séries longues : « les données de 1996 à 2023 correspondent à celles de la France hors Mayotte. À partir de 2024, le champ inclut Mayotte » ; effet de Mayotte : « une baisse de moins de 1 euro » du salaire net mensuel moyen. Les séries longues (Insee Résultats, base Tous salariés 2023) incluaient déjà apprentis et stagiaires sur toute la période, et leurs valeurs 1996 et 2023 sont celles du fichier. Effet de l'inclusion des apprentis et stagiaires sur 2024 : − 81 € nets par mois (− 3 %), 2 733 € contre 2 814 € | https://www.insee.fr/fr/statistiques/fichier/8657156/ip2079.pdf ; https://www.insee.fr/fr/statistiques/8668519 ; https://www.insee.fr/fr/statistiques/fichier/8660332/EQTP01.xlsx | Écart expliqué (pour la série BDM : apprentis et stagiaires inclus sur toute la série, Mayotte seulement à partir de 2024 avec un effet négligeable ; la rupture porte sur les anciennes éditions de l'Insee Première) |
| (5) Mayotte a son propre Smic, plus bas | Idem | Arrêté du 22 mai 2026 : 12,31 € (métropole, DOM, Saint-Barthélemy, Saint-Martin, Saint-Pierre-et-Miquelon) et 9,56 € à Mayotte (soit 77,7 % du taux métropolitain, calcul de ma part) ; décret 2025-1228 : 12,02 € et 9,33 €. Service-public a une section « À Mayotte » avec ses montants | https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054126589 ; https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000053042520 ; https://www.service-public.gouv.fr/particuliers/vosdroits/F2300 | Conforme |

### 7. Conclusion

Les chiffres du fichier sont conformes aux sources indépendantes consultées : Smic horaire (12,31 €, 12,02 €, 7,61 €), Smic mensuel brut 2026 (1 867,02 €), net 2026 (1 477,93 €), Smic de Mayotte 2026 (9,56 €), glissements annuels du salaire mensuel de base (2,0 %, 1,7 %, 1,7 %, 2,0 %, avec 1,4 % pour 2021-T2 en confirmation indirecte) et salaires moyens (31 902 € et 18 459 € exacts dans les tableaux Insee ; 32 791 € cohérent avec 2 733 € par mois). Les licences sont celles annoncées (Licence Ouverte 2.0 pour l'Insee ; Licence Ouverte pour le jeu de données Dares sur data.gouv.fr).

Trois points demandent une action sur les textes, pas sur les chiffres :
1. « À savoir » n° 2 est faux : le net Smic de l'Insee et celui de service-public sont de même nature (après cotisations salariales, CSG et CRDS, avant impôt) et identiques en valeur. À supprimer ou à reformuler (« net avant impôt, indicatif »).
2. « À savoir » n° 4 est à reformuler : pour cette série, les apprentis et stagiaires sont inclus sur toute la période ; Mayotte entre en 2024 avec un effet inférieur à 1 € par mois ; la non-comparabilité vise les éditions antérieures de l'Insee Première.
3. « À savoir » n° 1 est à préciser : la hausse de juin vient de l'indice des prix des ménages du premier quintile (+ 2,5 % depuis novembre 2025), pas de l'inflation globale.

Points non confirmés par un texte officiel : Mayotte 2017-01 (7,37 €, déduit d'un décret de 2017 et d'un montant mensuel local, la dépêche locale écrit 7,34 €), Smic net 2005-07 (957,74 €, un seul site commercial), glissement de 2021-T2 (1,4 %, résumé de moteur de recherche). Les pages de la Dares sont protégées par une vérification anti-robot : leur existence et leur titre sont établis indirectement.

Explication des vides de la BDM : le glissement annuel du T1 2020 et celui du T1 2021 ne se calculent pas parce que l'enquête trimestrielle Acemo a été suspendue au printemps 2020 (remplacée au T1 2020 par une enquête flash liée à la crise sanitaire), donc il n'existe pas d'indice du T1 2020 (sources : Dares Indicateurs n° 16 ; note de conjoncture Insee de juin 2025).

### 8. URLs consultées (2026-11-02)

Textes officiels et services de l'État
- https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054126589 (arrêté du 22 mai 2026)
- https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000053042520 (décret n° 2025-1228)
- https://www.service-public.gouv.fr/particuliers/vosdroits/F2300
- https://www.service-public.gouv.fr/particuliers/actualites/A18916?lang=en
- https://entreprendre.service-public.gouv.fr/actualites/A16528
- https://www.service-public.gouv.fr/entreprendre/actualites/A17008
- https://code.travail.gouv.fr/actualite/le-smic-augmente-au-1er-juin-2026-etes-vous-concerne
- https://legislation.lassuranceretraite.fr/Pdf/circulaire_cnav_2026_16_12062026.pdf
- https://www.unedic.org/la-reglementation/circulaires/circulaire-no-2017-04-du-10-janvier-2017
- https://www.data.gouv.fr/datasets/indices-de-salaires-de-base-par-secteur-d-activite-et-categorie-socioprofessionnelle-30378584

Insee (pages et fichiers publics, pas l'API)
- https://www.insee.fr/fr/statistiques/1375188
- https://www.insee.fr/fr/statistiques/serie/000879877 ; https://www.insee.fr/fr/statistiques/serie/000879878 ; https://www.insee.fr/fr/statistiques/serie/011800491 ; https://www.insee.fr/fr/statistiques/serie/010752333 (titres seulement)
- https://www.insee.fr/fr/metadonnees/definition/c2166 ; https://www.insee.fr/fr/metadonnees/definition/c2067 ; https://www.insee.fr/fr/metadonnees/source/serie/s1189
- https://www.insee.fr/fr/statistiques/8657156 ; https://www.insee.fr/fr/statistiques/fichier/8657156/ip2079.pdf
- https://www.insee.fr/fr/statistiques/8660332 ; https://www.insee.fr/fr/statistiques/fichier/8660332/EQTP01.xlsx
- https://www.insee.fr/fr/statistiques/8668519 ; https://www.insee.fr/fr/statistiques/fichier/8668519/EQTP01.xlsx
- https://www.insee.fr/fr/statistiques/fichier/8668548/EQTP01.xlsx
- https://www.insee.fr/fr/statistiques/8668594 ; https://www.insee.fr/fr/statistiques/fichier/8668594/SMIC35.xlsx
- https://www.insee.fr/fr/statistiques/8660243
- https://www.insee.fr/fr/statistiques/8733089 ; https://www.insee.fr/fr/statistiques/fichier/8733089/ECRT2026_F26.xlsx
- https://www.insee.fr/fr/statistiques/fichier/8684405/ndc-dec-2025-salaires.pdf
- https://www.insee.fr/fr/statistiques/fichier/8907437/ndc-mars-2026-salaires.pdf
- https://www.insee.fr/fr/statistiques/fichier/8594928/ndc-juin-2025-ecl3-SMB.pdf
- https://insee.fr/fr/statistiques/4511787
- https://www.insee.fr/fr/information/2008466
- https://www.insee.fr/fr/statistiques/fichier/1373375/T10F053.pdf (lu : TEF 2010, sans les lignes 2004-2005 utiles)

Dares et presse
- https://presse.tripalio.fr/wp-content/uploads/2022/03/Acemo_2021_T4_definitifs.pdf (copie de Dares Indicateurs n° 16, mars 2022)
- https://www.toutsurmesfinances.com/actualites/?p=2130
- https://bourse.fortuneo.fr/actualites/le-salaire-de-base-dans-le-prive-augmente-plus-vite-que-l-inflation-au-2eme-trimestre-5259463
- https://www.24matins.fr/salaires-prives-ce-que-montre-vraiment-le-regain-face-a-linflation-1421320
- https://tpeactu.fr/2026/02/08/salaires-prive-hausse-inflation-2025/
- https://fgeerolf.com/data/dares/les-indices-de-salaire-de-base.html (miroir tiers, non officiel)
- https://www.editions-tissot.fr/actualite/droit-du-travail/smic ; https://www.editions-tissot.fr/actualite/droit-du-travail/smic-quels-impacts-sur-les-minima-de-votre-convention-collective
- https://www.legisocial.fr/actualites-sociales/7943-smic-revalorisation-automatique-1er-juin-2026.html
- https://baremes.ipp.eu/parameters/marche-du-travail/marche_travail.salaire_minimum.smic/table
- https://www.mayottehebdo.com/actualite/en_bref/le-smic-a-augmente-en-2017-de-4-centimes-par-heure/
- https://www.lemondedudroit.fr/social/306-relations-individuelles-de-travail/55302-relevement-du-smic-au-1er-janvier-2018.html
- https://fiche-paie.fr/blog/histoire-smic-france-1950-2026

Consultées sans succès (page inaccessible ou illisible)
- https://dares.travail-emploi.gouv.fr/donnees/les-indices-de-salaire-de-base (vérification anti-robot)
- https://dares.travail-emploi.gouv.fr/publication/evolution-des-salaires-de-base-et-conditions-demploi-dans-le-secteur-prive-T22021 (idem ; chiffre 1,4 % lu seulement dans un résumé de moteur de recherche)
- https://dares.travail-emploi.gouv.fr/sites/default/files/5774dc90da13881b3daaaed58f13e27d/DI_Acemo_T32025_def.pdf (idem)
- https://www.info.gouv.fr/actualite/le-smic-revalorise-le-1er-juin-2026 (HTTP 403)
- https://www.blog-rh.com/smic/ (vérification anti-robot ; 957,74 € et 1 217,88 € lus seulement dans un résumé de moteur de recherche)
- https://www.mayotte.gouv.fr/ … EDITION_SPECIALE_N°1_JANVIER_2017.pdf (PDF scanné, sans texte)

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
