# `publicFinances` · Finances publiques

**Vérifiée le 02/11/2026** : double vérification sur le web, chiffres conformes (section « Double vérification ») ; avant d'entrer dans le kit, les tableaux datés par leur page (28/08/2026, et non le 10/08 de leurs fichiers), leurs années marquées provisoire ou semi-définitive, les sources citées pour ce qu'elles sont (les tableaux d'août, pas l'Insee Première de mai), deux « À savoir » précisés.

| Champ | Valeur |
| --- | --- |
| Indicateur | `publicFinances`, dossier « Économie » (`economy`), page de type série, ticket #141 de l'app (statut `planned` : les chiffres et la fiche avant la page) |
| Données | `briefings/data/publicFinances.json`, écrit par `yarn briefings publicFinances` le 2026-11-02 |
| Sources | Insee, « Dette et déficit publics au sens de Maastricht en 2025 », https://www.insee.fr/fr/statistiques/8988843, tableaux 3.101 et 3.106 (XLSX), parue le 28/08/2026 ; Insee, « Dépenses et recettes des administrations publiques en 2025 », https://www.insee.fr/fr/statistiques/8988845, tableaux 3.201 et 3.216, parue le 28/08/2026 (les deux en français seulement) ; Insee, « Dette trimestrielle des administrations publiques au sens de Maastricht », Informations rapides n° 239, https://www.insee.fr/fr/statistiques/9053525 (anglais : https://www.insee.fr/en/statistiques/9057140), séries BDM, 29/09/2026 ; Licence Ouverte 2.0 |
| Séries | `deficitShare` et `deficitBillion` : déficit public au sens de Maastricht, en % du PIB (1949 à 2025) et en milliards d'euros, tableau 3.106, écrit positif comme l'Insee l'écrit dans ses textes (le tableau donne un solde négatif) ; `debtShare` et `debtBillion` : dette au sens de Maastricht, 1978 à 2025, tableau 3.101 ; `spending` et `revenue` : dépenses et recettes des administrations publiques, milliards d'euros, 1959 à 2025, tableau 3.201 ; `compulsoryLevies` : taux de prélèvements obligatoires, % du PIB, 1959 à 2025, tableau 3.216 ; `debtQuarterlyShare` et `debtQuarterlyBillion` : dette trimestrielle, BDM `010777608` et `010777616`, 1995-T4 à 2026-T2 |
| Statuts | 2025 provisoire, 2024 semi-définitif sur toutes les séries annuelles : les tableaux n'en portent pas, le script reprend ceux du PIB annuel de la même campagne (BDM `011779992`) et s'arrête si les tableaux ne finissent pas la même année. La page de l'Insee sur les prélèvements obligatoires, mise à jour le 28/08/2026, marque aussi 2025 « p » et 2024 « sd ». La dette trimestrielle est définitive selon la BDM |
| Chiffre clé | Déficit de 5,1 % du PIB en 2025, en baisse après 5,8 % |
| Règles | Les montants sont ceux du compte semi-définitif avancé du 28/08/2026, que la notification d'Eurostat du 21/10/2026 reprend (151 592 M€ de déficit, 3 460 111 M€ de dette) ; l'Insee Première n° 2106 de mai donnait 152,5 et 3 460,5 Md€, les ratios sont les mêmes. Le tableau 3.216 n'a pas été actualisé en août. Le budget de l'État du PLF 2027 (son solde, ses missions) viendra d'une saisie à la main, dans un autre lot |
| Première édition | À remplir à la publication |

## « À savoir »

1. Le déficit au sens de Maastricht est le besoin de financement de l'ensemble des administrations publiques (Insee Première n° 2106 ; définition https://www.insee.fr/fr/metadonnees/definition/c1750) ; le solde d'exécution du budget de l'État 2025 est un troisième chiffre, −124,2 Md€ (conseil des ministres du 22/04/2026), et l'Insee publie un tableau de passage (3.107). La note ne cite pas ces chiffres de mai, qui n'ont pas été relus après la révision d'août.
2. Calendrier de l'Insee (https://www.insee.fr/fr/statistiques/8275612) : en mai N, comptes définitifs N-3, semi-définitifs N-2, provisoires N-1 ; en août, compte semi-définitif avancé des administrations publiques N-1. Révision constatée du déficit 2025 : 152,5 Md€ (mai) puis 151,592 Md€ (août), arrondi à 151,6 dans la note.
3. PIB 2025 : 2 991,1 Md€ (Insee Première n° 2105), 2 991 056 M€ chez Eurostat ; un point vaut 29,9 Md€, « environ 30 ».
4. Définition de l'Insee (https://www.insee.fr/fr/metadonnees/definition/c1571) : impôts et cotisations sociales effectives, sans contrepartie directe, nets des crédits d'impôt, hors cotisations imputées. La première rédaction (« la part des impôts et cotisations sociales dans le PIB ») était trop large : elle est précisée.

Non confirmé hors de l'Insee : la dette trimestrielle de 1995-T4 (701,6 Md€, 57,8 % du PIB), qu'aucune source indépendante ne donne ; la seule autre série lue, un jeu Eurostat extrait en janvier 2026, donne 714,7 Md€ pour 1995, sans doute un ancien rétropolé. Le kit garde la série de l'Insee, en base 2020.

À actualiser : la dette du 3e trimestre 2026 paraît le 18/12/2026 ; les comptes de 2026 en mai 2027 (2025 passera alors semi-définitif, 2024 définitif).

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans lire les tableaux XLSX ni appeler l'API de la BDM qu'utilise le script. Son rapport, tel quel (il relève la date du 10/08 des fichiers, corrigée depuis : les tableaux sont datés par leur page) :

Date de la vérification : 2026-11-02. Méthode : recoupement avec des sources autres que les tableaux détaillés et que l'API BDM (Insee Première n° 2106, Informations rapides n° 78, 158 et 239, notices de mise à jour des pages Insee, notification Eurostat du 21/10/2026, Cour des comptes, Élysée, presse). Les valeurs « trouvées » sont celles lues sur les pages citées ; quand une valeur vient du résumé d'un moteur de recherche et non de la page elle-même, c'est dit.

### Point d'attention n° 1 : le fichier n'est pas dans la version de l'Insee Première, mais dans la version plus récente

L'Insee Première n° 2106 (29/05/2026) donne un déficit 2025 de **152,5 Md€**, une dette de **3 460,5 Md€**, des recettes de **1 561,7 Md€** et des dépenses de **1 714,2 Md€**. Le fichier a **151,592 / 3 460,1 / 1 562,52 / 1 714,112**. Ce n'est pas une erreur de lecture : l'Insee a publié le **28/08/2026** un « compte semi-définitif avancé » des administrations publiques et a actualisé les tableaux 3.101 à 3.106 et 3.108 (page « Dette et déficit publics au sens de Maastricht en 2025 ») ainsi que 3.201 et 3.212 à 3.215 (page « Dépenses et recettes des administrations publiques en 2025 »). La notification Eurostat du **21/10/2026** reprend **exactement** les valeurs du fichier (déficit 151 592 M€, dette 3 460 111 M€). Le fichier est donc la version la plus récente ; l'Insee Première et la Cour des comptes (25/06/2026) citent la version de mai.

Écart sur le solde : 152,5 − 151,592 = 0,908 Md€ = 0,820 (recettes : 1 562,52 − 1 561,7) + 0,088 (dépenses : 1 714,2 − 1 714,112). Les trois écarts sont cohérents entre eux. En points de PIB rien ne bouge : 151,592 / 2 991,056 = 5,07 % et 152,5 / 2 991,1 = 5,10 %, les deux s'arrondissent à 5,1.

### Tableau de vérification

#### Déficit public (Maastricht)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Déficit 2025, % du PIB | 5,1 (« en baisse » vs 2024) | 5,1 % après 5,8 % ; Eurostat 21/10/2026 : −5,1 (2025), −5,8 (2024) | https://www.insee.fr/fr/statistiques/8997691 ; https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-21102026-ap ; https://www.destatis.de/EN/Themes/Economy/National-Accounts-Domestic-Product/Tables/eu-stability-deficitratio-eu.html | Conforme |
| Déficit 2024, % du PIB | 5,8 | 5,8 (Insee Première n° 2106 et Eurostat 21/10/2026) | idem | Conforme |
| Déficit 2023, % du PIB | 5,4 | 5,4 (Insee Première n° 2106, Eurostat 21/10/2026) ; l'Insee Première de mai 2025 donnait aussi 5,4 | https://www.insee.fr/fr/statistiques/8997691 ; https://www.insee.fr/fr/statistiques/8574492 | Conforme |
| Déficit 2025, Md€ | 151,592 | Insee Première n° 2106 : 152,5 ; Eurostat 21/10/2026 : −151 592 M€ | https://www.insee.fr/fr/statistiques/8997691 ; https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-21102026-ap | Écart expliqué (révision du 28/08/2026, voir point d'attention n° 1) |
| Déficit 2024, Md€ | 169,118 | Insee Première n° 2106 : 169,1 ; Eurostat : −169 118 M€. Pour mémoire, l'Insee Première de mai 2025 donnait 168,6 | https://www.insee.fr/fr/statistiques/8997691 ; https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-21102026-ap ; https://www.insee.fr/fr/statistiques/8574492 | Conforme |
| Déficit 2023, Md€ | 151,92 | Insee Première n° 2106 : 151,9 ; Eurostat : −151 920 M€ (mai 2025 : 151,7) | idem | Conforme |

#### Dette publique (annuelle, Maastricht)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Dette 2025, % du PIB | 115,7 | 115,7 (Insee Première n° 2106, Eurostat 21/10/2026, Cour des comptes 25/06/2026). La première estimation de mars 2026 et Eurostat en avril donnaient 115,6 | https://www.insee.fr/fr/statistiques/8997691 ; https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-21102026-ap ; https://www.ccomptes.fr/fr/publications/la-situation-et-les-perspectives-des-finances-publiques-17 ; https://www.insee.fr/fr/statistiques/8956575 | Conforme (115,6 est la version de mars, remplacée) |
| Dette 2024, % du PIB | 112,6 | 112,6 (Insee Première n° 2106, Eurostat) | idem | Conforme |
| Dette 2023, % du PIB | 109,5 | 109,5 (Insee Première n° 2106, Eurostat) | idem | Conforme |
| Dette 2025, Md€ | 3 460,1 | Insee Première n° 2106 : 3 460,5 ; Cour des comptes : 3 460,5 ; Informations rapides n° 158 (25/06/2026) : 3 460,5 ; Informations rapides n° 239 (29/09/2026), trimestre 2025-T4 : 3 460,1 ; Eurostat 21/10/2026 : 3 460 111 M€ | https://www.insee.fr/fr/statistiques/8997691 ; https://www.insee.fr/fr/statistiques/9010340 ; https://www.insee.fr/fr/statistiques/9053525 ; https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-21102026-ap | Écart expliqué (−0,4 Md€ par la révision d'août 2026, déjà visible dans les Informations rapides n° 239 : sécurité sociale 293,1 → 292,6) |
| Dette 2024, Md€ | 3 306,097 | Insee Première n° 2106 : 3 306,1 ; Eurostat : 3 306 097 M€ | idem | Conforme |

#### Dépenses, recettes, prélèvements obligatoires

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Dépenses 2025, Md€ | 1 714,112 | Insee Première n° 2106 : 1 714,2 (+2,5 %) ; Informations rapides n° 78 (mars) : 1 714,1. Non trouvé en valeur absolue dans Eurostat | https://www.insee.fr/fr/statistiques/8997691 ; https://www.insee.fr/fr/statistiques/8956575 | Écart expliqué (−0,088 Md€, révision d'août) |
| Dépenses 2025, % du PIB (contrôle demandé) | 1 714,112 / 2 991,056 = 57,31 % | 57,3 % (Insee Première n° 2106, Eurostat 21/10/2026). PIB 2025 = 2 991,1 Md€ (Insee Première n° 2105) ; 2 991 056 M€ (Eurostat). 1 714,1 / 2 991,1 = 57,30 % | https://www.insee.fr/fr/statistiques/8997691 ; https://www.insee.fr/fr/statistiques/8996855 ; https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-21102026-ap | Conforme |
| Dépenses 2024, Md€ | 1 672,589 | Non trouvé en valeur absolue hors tableaux. Contrôles indirects : 1 672,589 / 2 935,236 (PIB Eurostat) = 56,98 % pour 57,0 % publié ; 1 714,112 / 1 672,589 = +2,48 % pour +2,5 % publié | https://www.insee.fr/fr/statistiques/8997691 ; https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-21102026-ap | Non trouvé (cohérent) |
| Recettes 2025, Md€ | 1 562,52 | Insee Première n° 2106 : 1 561,7 (+3,9 %) ; Informations rapides n° 78 : 1 561,6. Eurostat : 52,2 % du PIB (1 562,52 / 2 991,056 = 52,24 %) | https://www.insee.fr/fr/statistiques/8997691 ; https://www.insee.fr/fr/statistiques/8956575 ; https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-21102026-ap | Écart expliqué (+0,82 Md€, révision d'août). 1 714,112 − 1 562,52 = 151,592 = déficit Eurostat |
| Recettes 2024, Md€ | 1 503,471 | Non trouvé en valeur absolue hors tableaux. 1 503,471 / 2 935,236 = 51,22 % pour 51,2 % publié ; 1 672,589 − 1 503,471 = 169,118 = déficit 2024 Eurostat ; croissance 2025 : +3,93 % pour +3,9 % publié | idem | Non trouvé (cohérent) |
| Prélèvements obligatoires 2025, % du PIB | 43,632 | 43,6 % (Insee Première n° 2106 ; page Insee « Taux de prélèvements obligatoires… 1959 à 2025 », mise à jour du 28/08/2026, statut « p »). Décimales non trouvées hors tableau 3.216 | https://www.insee.fr/fr/statistiques/8997691 ; https://www.insee.fr/fr/statistiques/2381412 | Conforme (au dixième) |
| Prélèvements obligatoires 2024, % du PIB | 42,723 | 42,7 % (Insee Première n° 2106 ; page 2381412, statut « sd »). La première estimation de mars 2026 donnait 42,8 | idem ; https://www.insee.fr/fr/statistiques/8956575 | Conforme (au dixième) |

#### Dette trimestrielle (Maastricht)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2026-T2, % du PIB | 119,0 | Informations rapides n° 239 : 119,0 % ; Eurostat 21/10/2026 : 119,1 | https://www.insee.fr/fr/statistiques/9053525 ; https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-21102026-bp | Conforme (l'écart de 0,1 point avec Eurostat vient très probablement d'un PIB de référence différent, non vérifié) |
| 2026-T2, Md€ | 3 595,5 | 3 595,5 (+59,6) ; Eurostat : 3 595 525 M€ | idem | Conforme |
| 2026-T1, % du PIB | 117,5 | 117,5 % (Informations rapides n° 158 et n° 239) ; Eurostat : 117,7 | https://www.insee.fr/fr/statistiques/9010340 ; https://www.insee.fr/fr/statistiques/9053525 ; https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-21102026-bp | Conforme (même remarque pour Eurostat, 0,2 point) |
| 2026-T1, Md€ | 3 535,9 | Informations rapides n° 239 : 3 535,9 ; Eurostat : 3 535 929 M€. Informations rapides n° 158 (25/06/2026) : 3 536,1 | idem | Conforme à la version du 29/09/2026 (révisée de −0,2 depuis juin) |
| 1995-T4, % du PIB | 57,8 | 57,8 sur DBnomics (miroir de la série Insee, donc non indépendant) ; site historysaid.com : 57,80 (source d'origine non indiquée) | https://db.nomics.world/INSEE/DETTE-TRIM-APU-2020/T.DETTE_MAASTRICHT.S13.F.PROPORTION.FE.POURCENT.BRUT.2020.FALSE ; https://historysaid.com/france/government-debt-to-gdp/1995 | Non trouvé (source indépendante) ; valeur retrouvée sur un miroir seulement |
| 1995-T4, Md€ | 701,6 | Aucune source indépendante ne donne 701,6. La seule autre série lue, Eurostat (gov_10dd_edpt1 via DBnomics, extraction du 22/01/2026), donne **714 688,8 M€** pour 1995, soit 13,1 Md€ de plus. Raison probable : ancien jeu de données rétrospectif non recalculé en base 2020 (non vérifié) | https://db.nomics.world/Eurostat/gov_10dd_edpt1/A.MIO_EUR.S13.GD.FR | Non trouvé ; écart non expliqué avec la seule série tierce (à traiter comme non confirmé) |
| Publication | 2026-09-29, Informations rapides n° 239 | « Paru le 29/09/2026 », prochaine parution 18/12/2026 | https://www.insee.fr/fr/statistiques/9053525 | Conforme |

#### Dates et révision

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Date de dernière modification des tableaux | 2026-08-10 | Pas de date « dernière modification » lisible sur les pages. Les pages Insee portent une notice : « 28 août 2026 : les tableaux 3.101 à 3.106 et 3.108 ont été actualisés à l'occasion de la publication du compte semi-définitif avancé des administrations publiques » ; idem pour 3.201 et 3.212 à 3.215. Les deux pages sont datées « Paru le 28/08/2026 ». Le tableau 3.216 n'est pas dans la liste actualisée | https://www.insee.fr/fr/statistiques/8988843 ; https://www.insee.fr/fr/statistiques/8988845 | Écart expliqué (il existe bien une révision de l'été 2026, publiée le 28/08). La date du 10/08 est antérieure à cette publication ; le contenu du fichier est pourtant celui de la version du 28/08 (identique à Eurostat), donc le 10/08 est probablement une date de préparation du fichier. Non vérifié |
| Page d'agrégats « Finances publiques en 2025 » | Hors fichier | Reste datée 29/05/2026 et en version de mai (5,1 ; 115,7 ; 57,3 ; 52,2 ; 43,6), non actualisée | https://www.insee.fr/fr/statistiques/8988841 | Information |
| Révision France entre notifications Eurostat d'avril et d'octobre 2026 | Hors fichier | Note Eurostat : révision 2025 de la France à 0,0 point pour le déficit et +0,1 point pour la dette (due au PIB), chiffres arrondis | https://ec.europa.eu/eurostat/documents/d/government-finance-statistics/edp-notif-2026-oct-main-revisions | Information |

#### Versions anglaises

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| « Le compte des administrations publiques en 2025 » (Insee Première n° 2106) | Hors fichier | Existe : « General Government Accounts in 2025 » (« Deficit Declined as Revenue rose and Expenditure Slowed »), paru le 29/05/2026. La page lue ne contient que le résumé (152,5 Md€, 5,1 %, 169,1 Md€, 5,8 %, dette 115,7 % / 112,6 %), pas le corps ni les figures | https://www.insee.fr/en/statistiques/9008766 | Conforme (adresse différente de la version française) |
| Informations rapides n° 239 | Hors fichier | Existe : « At the end of Q2 2026, the Maastricht debt accounted for 119.0% of GDP », 29 September 2026, texte complet en anglais | https://www.insee.fr/en/statistiques/9057140 | Conforme (adresse différente de la version française) |
| Pour mémoire : Informations rapides n° 78 | Hors fichier | « In 2025, the public deficit stands at 5.1% of GDP, the public debt at 115.6% of GDP », 27/03/2026 | https://www.insee.fr/en/statistiques/8961174 | Information |
| Tableaux 2025 en anglais | Hors fichier | Les adresses /en/statistiques/8988843, 8988845, 8997691 et 9053525 renvoient 404 ; pas de version anglaise des tableaux 2025 trouvée | https://www.insee.fr/en/statistiques/8988843 | Non trouvé |

### Les quatre énoncés « À savoir »

| Énoncé | Verdict | Source (URL) et justification |
|---|---|---|
| (1) Le déficit public (administrations publiques, sens de Maastricht) n'est pas le solde budgétaire de l'État de la loi de finances | **Confirmé** | Insee Première n° 2106 : solde de l'État en comptabilité nationale −128,1 Md€, contre −152,5 Md€ pour l'ensemble des administrations publiques (État, organismes divers d'administration centrale, collectivités, sécurité sociale) ; le « déficit public au sens de Maastricht » est défini comme le besoin de financement de l'ensemble des APU (https://www.insee.fr/fr/statistiques/8997691). Le solde budgétaire de l'État d'exécution 2025 est un troisième chiffre, −124,2 Md€ (projet de loi d'approbation des comptes 2025, conseil des ministres du 22/04/2026 : https://www.elysee.fr/emmanuel-macron/2026/04/22/compte-rendu-du-conseil-des-ministres-du-22-avril-2026). L'Insee publie un tableau de passage « du résultat d'exécution des lois de finances au déficit de l'État au sens de Maastricht » (tableau 3.107, https://www.insee.fr/fr/statistiques/8988843). Définition générale : https://www.insee.fr/fr/metadonnees/definition/c1750 |
| (2) Les comptes annuels des deux dernières années sont révisés (provisoire, semi-définitif) | **Confirmé, avec une précision** | Calendrier Insee : mai N, comptes « définitifs N-3, semi-définitifs N-2, provisoires N-1 » ; août, « comptes semi-définitifs avancés des APU N-1 » (https://www.insee.fr/fr/statistiques/8275612). La page Insee sur les prélèvements obligatoires marque 2023 « définitif », 2024 « sd », 2025 « p » (https://www.insee.fr/fr/statistiques/2381412). Note de l'Insee sur le déroulement d'une campagne de comptes : https://www.insee.fr/fr/statistiques/fichier/8988934/Note_revisions_2023a2025.pdf. Révisions constatées : déficit 2024 = 168,6 (mai 2025) → 169,1 (mai 2026) → 169,118 (août/octobre 2026) ; dette 2024 = 113,2 % (mai 2025) → 112,6 % ; dette 2025 = 115,6 % (mars 2026) → 115,7 % (mai), 3 460,5 → 3 460,1 Md€ (août). Précision : il y a trois millésimes en cours de vie ; seules les deux dernières années du snapshot (2024 et 2025) ne sont pas définitives, 2023 l'est |
| (3) 1 point de PIB vaut environ 30 Md€ en 2025 | **Confirmé** | PIB 2025 = 2 991,1 Md€ (Insee Première n° 2105 : https://www.insee.fr/fr/statistiques/8996855) ; 2 991 056 M€ (Eurostat). 1 point = 29,9 Md€. La Cour des comptes ne donne pas l'équivalence dans la page lue (https://www.ccomptes.fr/fr/publications/la-situation-et-les-perspectives-des-finances-publiques-17) ; un avis du HCFP d'avril 2024 écrit « 30 Md€, soit un point de PIB » pour 2025 (lu dans un résumé de recherche, non rouvert) |
| (4) Le taux de prélèvements obligatoires 2025 est la part des impôts et cotisations sociales dans le PIB | **Confirmé, avec des nuances à écrire** | L'Insee définit les prélèvements obligatoires comme « les impôts et cotisations sociales effectives reçues par les administrations publiques et les institutions européennes sans aucune contrepartie directe et immédiate », nets des montants non recouvrables et des crédits d'impôt (https://www.insee.fr/fr/metadonnees/definition/c1571). Le tableau de l'Insee Première précise que le taux est « calculé net des crédits d'impôt » et la page 2381412 qu'il est « hors cotisations sociales imputées et crédit d'impôts » ; 43,6 % en 2025, dont 0,1 point au profit de l'Union européenne (https://www.insee.fr/fr/statistiques/8988841). Il ne s'agit donc pas de tous les impôts et cotisations de la comptabilité nationale (1 374,1 Md€ d'impôts et cotisations sociales dans le tableau 4 de l'Insee Première, cotisations imputées comprises). La définition d'Eurostat est plus large (45,2 % du PIB en 2024 contre 42,8 % selon l'Insee, d'après le blog de l'Insee, lu dans un résumé de recherche : https://blog.insee.fr/depenses-et-recettes-des-comptes-publics/) |

### Conclusion

1. **Aucun écart réel non expliqué sur les chiffres clés.** Les pourcentages du fichier (5,1 ; 5,8 ; 5,4 ; 115,7 ; 112,6 ; 109,5 ; 57,3 ; 52,2 ; 43,6 ; 42,7) sont tous confirmés par l'Insee Première n° 2106 et par Eurostat (21/10/2026).
2. **Les montants 2025 du fichier (151,592 ; 3 460,1 ; 1 562,52 ; 1 714,112) diffèrent de l'Insee Première (152,5 ; 3 460,5 ; 1 561,7 ; 1 714,2) parce que le fichier est dans la version plus récente** du compte semi-définitif avancé du 28/08/2026. Eurostat (21/10/2026) donne 151 592 M€ et 3 460 111 M€, soit les valeurs du fichier au millier d'euros près. Les contrôles internes (dépenses − recettes = déficit, pour 2024 et 2025 ; ratios au PIB) sont cohérents. À écrire dans le jeu si l'Insee Première est cité à côté : « 152,5 Md€ (mai 2026), révisé à 151,6 Md€ (août 2026) ».
3. **À signaler** : la date de modification du 10/08/2026 précède la publication du 28/08/2026 dont le fichier contient pourtant les valeurs ; préférer, dans la documentation du jeu, la date de la notice Insee (28/08/2026) à celle du fichier. Les pages de l'Insee Première et de la page d'agrégats (8988841) restent en version de mai.
4. **Non confirmés** : la dette trimestrielle de 1995-T4 en milliards (701,6) n'a pas de source indépendante, et la seule autre série lue (Eurostat, extraction de janvier 2026) donne 714,7 Md€ ; le 57,8 % n'est retrouvé que sur un miroir de la série Insee. Les valeurs absolues des dépenses et recettes 2024 et les décimales des prélèvements obligatoires (43,632 ; 42,723) ne sont pas lisibles hors tableaux ; elles sont cohérentes avec les ratios publiés. Les ratios trimestriels d'Eurostat (117,7 ; 119,1) diffèrent de ceux de l'Insee (117,5 ; 119,0) de 0,1 à 0,2 point, très probablement à cause du PIB de référence (non vérifié). Avis du HCFP sur les chiffres 2025 : non trouvé.
5. **Énoncés « À savoir »** : les quatre sont confirmés ; (2) mérite la précision « 2023 est définitif, 2024 semi-définitif, 2025 provisoire puis semi-définitif avancé », et (4) la précision « effectives, nettes des crédits d'impôt, hors cotisations imputées ».
6. **Versions anglaises** : Insee Première n° 2106 en anglais à https://www.insee.fr/en/statistiques/9008766 (résumé seulement) ; Informations rapides n° 239 en anglais à https://www.insee.fr/en/statistiques/9057140.

### URL consultées (toutes le 2026-11-02)

- https://www.insee.fr/fr/statistiques/8997691 (Insee Première n° 2106, 29/05/2026, texte complet téléchargé et lu)
- https://www.insee.fr/en/statistiques/9008766 (version anglaise de l'Insee Première n° 2106)
- https://www.insee.fr/fr/statistiques/8996855 (Insee Première n° 2105, PIB 2025)
- https://www.insee.fr/fr/statistiques/8988841 (page « Finances publiques en 2025 », 29/05/2026)
- https://www.insee.fr/fr/statistiques/8988843 (page « Dette et déficit publics au sens de Maastricht en 2025 », notice du 28/08/2026)
- https://www.insee.fr/fr/statistiques/8988845 (page « Dépenses et recettes des administrations publiques en 2025 », notice du 28/08/2026)
- https://www.insee.fr/fr/statistiques/2381412 (taux de prélèvements obligatoires, 1959 à 2025, mise à jour du 28/08/2026)
- https://www.insee.fr/fr/statistiques/8956575 et https://www.insee.fr/en/statistiques/8961174 (Informations rapides n° 78, 27/03/2026)
- https://www.insee.fr/fr/statistiques/9010340 (Informations rapides n° 158, 25/06/2026)
- https://www.insee.fr/fr/statistiques/9053525 et https://www.insee.fr/en/statistiques/9057140 (Informations rapides n° 239, 29/09/2026)
- https://www.insee.fr/fr/statistiques/8574492 (Insee Première n° 2054, 28/05/2025)
- https://www.insee.fr/fr/statistiques/8275612 (calendrier de diffusion des comptes)
- https://www.insee.fr/fr/statistiques/fichier/8988934/Note_revisions_2023a2025.pdf (note sur les révisions, mai 2026)
- https://www.insee.fr/fr/metadonnees/definition/c1571 (définition des prélèvements obligatoires) ; https://www.insee.fr/fr/metadonnees/definition/c1750 (déficit public, via résultat de recherche)
- https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-21102026-ap (Eurostat, 21/10/2026, déficit et dette 2022-2025)
- https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-21102026-bp (Eurostat, 21/10/2026, dette trimestrielle)
- https://ec.europa.eu/eurostat/documents/d/government-finance-statistics/edp-notif-2026-oct-main-revisions (note Eurostat sur les révisions)
- https://www.hellenicshippingnews.com/euro-area-government-deficit-at-2-9-and-eu-at-3-1-of-gdp/ (reprise du communiqué Eurostat d'avril 2026 : France −5,1 % et 115,6 %)
- https://www.destatis.de/EN/Themes/Economy/National-Accounts-Domestic-Product/Tables/eu-stability-deficitratio-eu.html (Destatis, notification d'octobre 2026)
- https://www.ccomptes.fr/fr/publications/la-situation-et-les-perspectives-des-finances-publiques-17 (Cour des comptes, 25/06/2026) ; la synthèse PDF https://www.ccomptes.fr/sites/default/files/2026-06/20260625-synthese-RSPFP-2026.pdf a renvoyé une erreur 503
- https://www.elysee.fr/emmanuel-macron/2026/04/22/compte-rendu-du-conseil-des-ministres-du-22-avril-2026 (solde budgétaire de l'État 2025)
- https://db.nomics.world/INSEE/DETTE-TRIM-APU-2020 et la série en % (miroir de la BDM, non indépendant) ; https://db.nomics.world/Eurostat/gov_10dd_edpt1/A.MIO_EUR.S13.GD.FR (Eurostat, extraction du 22/01/2026)
- https://historysaid.com/france/government-debt-to-gdp/1995 (résultat de recherche seulement)
- https://blog.insee.fr/depenses-et-recettes-des-comptes-publics/ et l'avis HCFP d'avril 2024 (résultats de recherche seulement, non rouverts)
- Cherchés sans succès : avis du HCFP sur le déficit 2025 (HCFP-2026-2), valeur absolue des dépenses et recettes 2024 et 2025 chez Eurostat, valeur 701,6 Md€ de 1995-T4, version anglaise des tableaux 2025 (404 aux adresses /en/ des identifiants français).

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
