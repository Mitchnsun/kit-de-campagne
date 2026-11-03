# `costOfLiving` · Pouvoir d'achat (page composite)

La page « Pouvoir d'achat » (#28) n'a pas de fichier : ses trois parties ont le leur (`rentIndices`, `energyPrices`, `socialBenefits`, PO, 02/11/2026). Cette fiche porte la double vérification commune aux trois. La carte des loyers d'annonce (#28) viendra plus tard.

**Vérifiée le 02/11/2026** : aucun chiffre faux dans les fichiers. Les notes des parties et deux textes de l'app sont corrigés (voir les fiches des parties). Un écart reste ouvert : les personnes couvertes par le RSA (voir `socialBenefits.md`).

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans appeler la BDM de l'Insee ni l'API Cafdata du script. Son rapport, tel quel. Le « +1,38 % » de l'IRL du 2e trimestre venait de la consigne de vérification, pas du fichier, qui porte bien +1,15 % :

Date de la vérification : 2026-11-02.

Méthode : uniquement des sources web. Je n'ai appelé ni l'API BDM de l'Insee ni l'API Cafdata. Je n'ai pas ouvert les pages de série de l'Insee (`/statistiques/serie/…`) ni téléchargé le CSV miroir de data.gouv.fr (qui renvoie vers data.caf.fr) : ces deux sources ne seraient pas indépendantes des scripts. Je n'ai rien lu ni modifié sous `/home/user`.

Ce que j'ai lu directement : les Informations rapides de l'Insee (HTML, PDF et fichier de données zip joint à l'IPC), les fiches de service-public.fr, le fichier Excel et la méthodologie du ministère de la Transition écologique, les publications Cnaf « RSA Conjoncture » et « PA Conjoncture », la page data.gouv.fr du jeu de données.

Limites : le site de la DREES a répondu 503 (page ouverte via WebFetch) ou n'a rien renvoyé (curl). Les chiffres DREES viennent donc de reprises (unps.fr, aladom.fr) et de résumés de moteur de recherche. Chaque fois qu'une valeur ne repose que sur un résumé de moteur de recherche, ou sur un site secondaire qui republie l'Insee, c'est écrit dans la colonne Source.

Légende des verdicts : Conforme, Écart expliqué, Écart, Non trouvé.

---

### 1. Loyers

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| IRL 2026-T3, variation annuelle | +1,57 % | +1,57 % (niveau 148,06 contre 145,77 au T3 2025) | https://www.insee.fr/fr/statistiques/9081853 ; version anglaise https://www.insee.fr/en/statistiques/9081855 ; https://www.service-public.gouv.fr/particuliers/vosdroits/F13723 | Conforme |
| IRL 2026-T2, variation annuelle | +1,38 % (avec point d'interrogation dans la demande) | **+1,15 %** (niveau 148,37, publié le 10/07/2026). Aucun trimestre de la série n'affiche +1,38 % | https://www.insee.fr/fr/statistiques/9081853 (tableau, « après +1,15 % au trimestre précédent ») ; https://www.insee.fr/en/statistiques/9022799 ; https://www.service-public.gouv.fr/particuliers/vosdroits/F13723 | **Écart** : +1,38 % est faux, la valeur est +1,15 % |
| IRL 2026-T3, date de publication | 15/10/2026 | 15/10/2026 (Informations rapides n° 246) ; Journal officiel le 16/10/2026 ; prochaine parution le 15/01/2027 | https://www.insee.fr/fr/statistiques/9081853 ; https://www.service-public.gouv.fr/particuliers/vosdroits/F13723 | Conforme |
| Plafonnement à 3,5 % : trimestres | du T3 2022 au T1 2024 | « entre le troisième trimestre 2022 et le premier trimestre 2024 », article 12 de la loi 2022-1158 du 16 août 2022, modifié par l'article 2 de la loi 2023-568 du 7 juillet 2023. Les variations affichées valent 3,49 % ou 3,50 % de 2022-T3 à 2024-T1, puis 3,26 % en 2024-T2 (plus de plafond) | https://www.insee.fr/fr/statistiques/9081853 (« Pour en savoir plus ») ; https://www.anil.org/aj-plafonnement-evolution-indice-reference-loyer/ | Conforme |
| Variantes outre-mer et Corse | non précisé (à vérifier) | Outre-mer 2,5 % ; Corse 2,0 % (arrêté n° R20-2022-10-11-00012 modifié). Depuis 2022-T3, l'Insee publie des IRL distincts : T3 2026 = 145,21 (outre-mer) et 143,80 (Corse), contre 148,06 en métropole. Un site (Bail Facile, via résumé de moteur de recherche) donne 2 % pour l'outre-mer : il contredit l'Insee et l'ANIL, à ignorer | https://www.insee.fr/fr/statistiques/9081853 ; https://www.anil.org/aj-plafonnement-evolution-indice-reference-loyer/ | Conforme (si le fichier ne porte que la métropole) |
| ILH 2026-T2, tous secteurs | 111,1 | 111,1 (hausse de 0,2 % sur trois mois, +1,6 % sur un an) | https://www.insee.fr/fr/statistiques/9050041 ; version anglaise https://www.insee.fr/en/statistiques/9052421 | Conforme |
| ILH 2026-T2, secteur libre (y compris loi de 1948) | 108,8 | 108,8 (+0,9 % sur un an) | idem | Conforme |
| ILH 2026-T2, secteur social | 115,6 | 115,6 (+2,9 % sur un an) | idem | Conforme |
| ILH, date de publication | 15/09/2026 | 15/09/2026 (Informations rapides n° 221) ; prochaine parution le 15/12/2026 | https://www.insee.fr/fr/statistiques/9050041 ; https://www.insee.fr/fr/statistiques/fichier/version-html/9050041/IR221_ILH_juil26.pdf | Conforme |
| ILH, base 100 « janvier 2019 » | janvier 2019 | Le PDF de juillet 2026 indique « base 100 au quatrième trimestre 2018 ». Or le T4 d'une année N est l'indice de janvier N+1 : c'est bien janvier 2019. Le PDF du T3 2019 écrit « base 100 en janvier 2019 » | https://www.insee.fr/fr/statistiques/fichier/version-html/9050041/IR221_ILH_juil26.pdf ; https://www.insee.fr/fr/statistiques/fichier/version-html/4266810/loyers2019T3__.pdf | Conforme |
| ILH : période mesurée par « 2026-T2 » (remarque de #28) | « 2026-Q2 » = indice de juillet | Confirmé. T1 = avril, T2 = juillet, T3 = octobre, T4 = janvier de l'année suivante. Insee : « le point du T2 correspond à l'indice de juillet N » | https://www.insee.fr/fr/statistiques/9050041 (« Lecture ») ; https://www.insee.fr/en/statistiques/9052421 (« How to read ») ; https://www.insee.fr/fr/statistiques/documentation/Note%20m%C3%A9thodologique_IndiceLoyers_oct20.pdf | Conforme |

Remarques sur les loyers :

- Le niveau de l'IRL peut baisser d'un trimestre à l'autre (148,37 au T2 2026, 148,06 au T3) : l'IRL est chaîné en glissement annuel, pas d'un trimestre sur l'autre. Même cas en 2024 (T2 145,17, T3 144,51) et en 2025 (T2 146,68, T3 145,77). Ce n'est pas une erreur ; il ne faut comparer que les variations annuelles. Un résumé de moteur de recherche avait signalé à tort un « conflit ».
- Le « 146,94 » vu dans certains résumés pour le T2 2026 est l'IRL des outre-mer, pas celui de la métropole.
- La page Insee n'emploie pas l'expression « bouclier loyer » ; elle parle de plafond de la variation annuelle.

---

### 2. Énergie

Tous les indices ci-dessous viennent du fichier de données joint à l'Informations rapides n° 247 (`Tableau_Données_Détaillées_2026-09.xls`, lu après conversion), base 100 = année 2025.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| IPC énergie, septembre 2026, variation annuelle | +21,3 % (définitif) | +21,3 % (après +16,7 % en août ; l'estimation provisoire du 30/09 donnait +21,2 %). Indice énergie 120,13, pondération 764/10 000. Publié le 15/10/2026 | https://www.insee.fr/fr/statistiques/9080209 ; https://www.insee.fr/fr/statistiques/fichier/version-html/9080209/IR247_IPCdef_sept26.pdf ; version anglaise https://www.insee.fr/en/statistiques/9080263 | Conforme |
| IPC énergie, octobre 2026, variation annuelle | +24,1 % (provisoire) | +24,1 %, « estimation provisoire » du 30/10/2026 (n° 266). L'Insee précise que ces indices reposent sur un champ restreint de prix et des estimations de tarifs, et ne doivent pas servir aux revalorisations contractuelles. Résultats définitifs le 13/11/2026 | https://www.insee.fr/fr/statistiques/fichier/version-html/9107965/IR266_IPCprov_oct26.pdf ; https://www.insee.fr/fr/statistiques/9107965 ; version anglaise https://www.insee.fr/en/statistiques/9107975 | Conforme |
| Indice électricité, septembre 2026 | 99,89 | 99,89 (poste « Électricité », pondération 265 ; +1,4 % sur un an) | fichier de données de https://www.insee.fr/fr/statistiques/9080209 (zip « Données Complémentaires IR IPC septembre 2026 ») | Conforme |
| Indice gaz, septembre 2026 | 118,57 | 118,57 (poste « Gaz », pondération 127 ; +19,0 % sur un an) | idem | Conforme |
| Indice « carburants », septembre 2026 | 133,52 | 133,52, mais c'est le poste « Carburants et lubrifiants pour véhicules personnels » (pondération 351 ; +34,4 % sur un an). Autres lignes à ne pas confondre : produits pétroliers 135,23 ; gazole 142,88 ; essence 125,21 ; combustibles liquides (fioul) 160,53 | idem | Conforme sur la valeur. Libellé « fuels » à préciser en « carburants » |
| Gazole, moyenne de septembre 2026 | 2,34 €/l | Insee (série citée par eco3min.fr, qui republie l'Insee, mise à jour du 15/10/2026) : 2,34. Ministère de la Transition écologique, moyenne mensuelle des prix de vente du vendredi : **2,3255**. Baromètre tiers prix-carburant.eu : 2,324 | https://eco3min.fr/evolution-prix-carburants/ (secondaire) ; https://www.ecologie.gouv.fr/sites/default/files/documents/Prix%20HTT%20et%20TTC%20depuis%20janvier%202020_0.xlsx (feuille « Carburants routiers ») ; https://prix-carburant.eu/barometre-mensuel-2026-09 (résumé de moteur de recherche) | Écart expliqué : 0,015 €/l (0,6 %) d'écart avec le ministère. Les séries de l'Insee viennent des relevés de l'IPC (résumé de moteur de recherche), pas des déclarations des distributeurs au ministère. Écart non démontré ligne à ligne |
| SP95-E10, moyenne de septembre 2026 | 2,14 €/l | Insee : 2,14 (eco3min.fr ; résumé de moteur de recherche de la page série Insee, qui donne aussi 2,01 en août). Ministère : **2,1224** (moyenne des quatre vendredis : 2,0869 ; 2,1098 ; 2,1506 ; 2,1424). prix-carburant.eu : 2,121 | mêmes sources ; ministère : feuille « Carburants routiers » | Écart expliqué : 0,018 €/l (0,9 %), même cause. En août 2026, Insee 2,01 contre ministère 2,0041 : même ordre de grandeur |
| Fioul domestique, septembre 2026 | 1 833,94 € pour 1 000 l livrés | Insee : 1 833,94 € « pour 1 000 litres livrés à domicile » (eco3min.fr et prixaujourdhui.com, qui citent tous deux l'Insee ; août 2026 : 1 675,26 ; septembre 2025 : 1 126,96). Ministère : fioul domestique **pour des livraisons de 2 000 à 4 999 litres**, septembre 2026 = 1,7447 €/l, soit 1 744,75 € pour 1 000 l | https://prixaujourdhui.com/prix/fioul-domestique/ (secondaire) ; https://eco3min.fr/evolution-prix-carburants/ (secondaire) ; https://www.ecologie.gouv.fr/sites/default/files/documents/M%C3%A9thodologie%20de%20calcul%20des%20prix%20moyens%20des%20produits%20p%C3%A9troliers_0.pdf ; fichier Excel du ministère (feuille « Combustibles ») | Écart expliqué : produit différent. Le ministère ne publie pas de série pour 1 000 litres livrés. L'Insee est 5 à 8,5 % au-dessus (septembre 2025 : 1 127 contre 1 039 ; août 2026 : 1 675 contre 1 554 ; septembre 2026 : 1 834 contre 1 745), cohérent avec une livraison plus petite. Valeur non contrôlable à la source |
| Mois manquants de 2020 : gazole et SP95-E10 | décembre 2020 | Le ministère n'a **aucun trou** en 2020 : une valeur chaque vendredi depuis le 03/01/2020 et douze moyennes mensuelles (décembre 2020 : gazole 1,2570, SP95-E10 1,3349). Le trou est donc propre aux séries de l'Insee. eco3min.fr écrit que l'Insee n'a pas publié décembre 2020 pour les cinq séries | fichier Excel du ministère ; https://eco3min.fr/evolution-prix-carburants/ (secondaire) | Non trouvé : aucune source ne donne la raison propre à décembre 2020 pour les carburants |
| Mois manquants de 2020 : fioul | avril, mai, juin, novembre, décembre 2020 | Même constat : aucun trou côté ministère (avril 2020 0,648 €/l, mai 0,656, juin 0,678, novembre 0,641, décembre 0,678). Côté Insee : la collecte des prix en magasin par les enquêteurs a été suspendue du 16 mars au 15 juin 2020, puis du 30 octobre 2020 au 4 janvier 2021, et l'Insee écrit que la crise a « affecté la qualité de l'IPC de mars, avril, mai, juin, novembre et décembre » 2020. Les mois manquants du fioul (avril à juin, novembre, décembre) tombent dans ces périodes | https://www.insee.fr/fr/statistiques/5012290 ; https://www.insee.fr/fr/statistiques/4993275 et https://www.insee.fr/fr/statistiques/5010784 (résumé de moteur de recherche : 14 % et 15 % de la consommation imputés) | Écart expliqué (le rapprochement est une inférence : aucune page Insee consultée ne cite les séries de prix moyens) |

Remarques sur l'énergie :

- Les prix moyens de vente au détail de l'Insee sont décrits (résumé de moteur de recherche) comme issus de l'indice des prix à la consommation. La méthodologie du ministère est différente : prix moyens pondérés déclarés chaque lundi par les distributeurs (prix pratiqués le vendredi précédent), moyenne mensuelle = moyenne arithmétique des vendredis, France métropolitaine hors Corse. Elle ne publie pas de moyenne à 1 000 litres.
- Les séries de l'Insee ne commencent pas en 2021 : fioul domestique depuis janvier 1992, SP95-E10 mensuel depuis janvier 2019 (résumé de moteur de recherche des pages série). « La série commence en 2021 » décrit donc un choix du kit.
- Le fichier du ministère contient aussi octobre 2026 (gazole 2,3503, SP95-E10 2,1276, fioul 1,8021 €/l pour 2 000 à 4 999 l). Pour les séries de l'Insee, octobre n'est pas encore connu (eco3min.fr indique une mise à jour du 15/10/2026, qui apporte septembre) : à ma connaissance, pas encore publié, non vérifié.

---

### 3. Prestations sociales (Caf seulement)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| RSA, foyers, mars 2026 | 1 847 267 | Cnaf, moyenne du 1er trimestre 2026 : 1 847 milliers (provisoire), confirmée à 1 847 milliers dans la publication de septembre. DREES (édition de mai 2026, chiffres de mars 2026, tous régimes d'après la note de périmètre) : 1,88 million, soit +2,0 % sur un an. Cohérence : 1 847 267 / 0,986 (part des Caf) = 1,874 million | https://www.caf.fr/sites/default/files/medias/cnaf/Nous_connaitre/Recherche_et_statistiques/Rsa%20Conjoncture/RSA%20Conjoncture_2026T1.pdf ; https://caf.fr/sites/default/files/medias/cnaf/Nous_connaitre/Recherche_et_statistiques/Rsa%20Conjoncture/RSA%20Conjoncture_2026T2.pdf ; https://www.unps.fr/suivi-mensuel-des-prestations-de-solidarite-Edition-de-mai-2026-_r_36_a_268.html (reprise de la DREES) | Conforme (« environ 1,85 million de foyers » confirmé par la Cnaf) |
| RSA, personnes couvertes, mars 2026 | 3 720 310 | Cnaf : environ **3,61 millions** au 1er trimestre 2026 (estimation provisoire), 3,64 millions au 2e trimestre, 3,56 millions au 3e trimestre 2025, 3,55 millions au 4e (résumé de moteur de recherche pour ce dernier). Soit 1,95 personne par foyer côté Cnaf contre 2,01 dans le fichier | RSA Conjoncture 2026T1 et 2026T2 (URL ci-dessus) | **Écart** : +110 000 personnes (+3,1 %) non expliqué. Pistes : définition des « personnes couvertes » du jeu de données (tous les membres du foyer Caf plutôt que les seules personnes à charge « au sens du RSA »), ou estimation provisoire de la Cnaf. À trancher en lisant la définition du champ dans le jeu de données |
| Prime d'activité, foyers, mars 2026 | 4 587 327 | Cnaf : 4,62 millions en moyenne au 1er trimestre 2026 (provisoire) ; 4,581 millions au 4e trimestre 2025 (estimation actuelle). DREES : 4,73 millions (-0,2 %). Cohérence : 4,73 × 0,972 (part des Caf) = 4,60 millions | PA Conjoncture 2026T1 : https://www.caf.fr/sites/default/files/medias/cnaf/Nous_connaitre/Recherche_et_statistiques/PPA%20Conjoncture/PA%20Conjoncture_2026T1.pdf ; unps.fr (URL ci-dessus) | Écart expliqué : -0,7 % par rapport à la moyenne provisoire du trimestre (mois définitif contre moyenne estimée) |
| Prime d'activité, personnes couvertes | 8 743 674 | Cnaf : environ 8,89 millions au 1er trimestre 2026 (provisoire) ; 8,7 millions au 3e trimestre 2025 (1,93 personne par foyer ; 1,91 dans le fichier) | PA Conjoncture 2026T1 | Écart expliqué (partiel) : -1,7 %, même nature que la ligne précédente |
| Aides au logement, foyers, mars 2026 | 5 622 098 | DREES, édition de mai 2026 : 5,6 millions, +0,2 % sur un an, première absence de baisse sur un an depuis décembre 2020 ; effectifs « du régime général seulement ». Une reprise l'exprime en « personnes » : probable confusion de libellé | unps.fr et https://www.aladom.fr/actualites/secteur-service/11180/prestations-de-solidarite-ce-que-revelent-les-indicateurs-sociaux-au-printemps-2026/ (reprises de la DREES ; le site de la DREES n'a pas répondu) | Conforme (arrondi à 0,1 million) |
| Aides au logement, personnes couvertes | 10 738 459 | Aucun chiffre Cnaf ou DREES trouvé. Rapport implicite : 1,91 personne par foyer, plausible | recherches sur caf.fr et drees.solidarites-sante.gouv.fr sans résultat | Non trouvé |
| Jeu de données : dernière modification | 09/10/2026 | « Dernière mise à jour : 9 octobre 2026 » ; la page affiche « il y a 24 jours », ce qui est exact au 02/11/2026 | https://www.data.gouv.fr/datasets/toutes-prestations-repartition-des-allocataires-selon-la-prestation-national | Conforme |
| Licence | Licence Ouverte v2.0 | « Licence Ouverte / Open Licence version 2.0 » (la page data.caf.fr n'affiche pas la licence) | idem ; https://data.caf.fr/explore/dataset/s_ben_nat/information/ | Conforme |
| Intitulé et description | « Toutes prestations - Répartition des allocataires selon la prestation [National] » | Intitulé identique. Description : « Bénéficiaires mensuels d'au moins une prestation légale (hors ARS, ADE et AVVC) par type de prestations à l'échelle nationale depuis 2016 », mesures : foyers allocataires, personnes couvertes, montants | idem | Conforme |
| Début de la série | juin 2016 | « depuis 2016 » ; le mois de début n'est écrit nulle part | idem | Non trouvé (mois de début) |
| Fin de la série et retard | mars 2026, environ sept mois | La Cnaf tient ses chiffres pour définitifs six mois après la fin du mois ; mars 2026 + 6 mois = 30/09/2026, jeu mis à jour le 09/10/2026. Retard réel : 6 mois et 9 jours après la fin de mars, 7 mois après son début. En comparaison, la Cnaf publie des estimations provisoires du trimestre en cours de clôture (RSA du 2e trimestre 2026 en septembre) et la DREES donne le RSA de juin 2026 | RSA Conjoncture 2026T1 (« Source et méthode d'estimation ») ; https://www.data.gouv.fr/datasets/toutes-prestations-repartition-des-allocataires-selon-la-prestation-national | Conforme (formulation à ajuster, voir les notes) |
| Périmètre : Caf seulement | Caf, sans la MSA | Les Caf pèsent environ 98,6 % des bénéficiaires du RSA et 97,2 % de ceux de la prime d'activité, tous régimes, en 2025. Pour les aides au logement, la DREES ne compte que le régime général. Le jeu de données exclut aussi l'ARS, l'ADE et l'AVVC | RSA et PA Conjoncture 2026T1 ; unps.fr ; data.gouv.fr | Conforme |

---

### 4. Versions anglaises

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Insee, IRL 2026-T3 | non précisé | Identifiant anglais **9081855** (le français est 9081853). Titre : « In Q3 2026, the Housing Rent Reference Index increased by 1.57% over a year ». Les mêmes chiffres | https://www.insee.fr/en/statistiques/9081855 | Conforme. L'identifiant diffère de celui du français ; `/en/statistiques/9081853` renvoie 404 |
| Insee, ILH juillet 2026 | non précisé | Identifiant anglais **9052421** (le français est 9050041). Titre : « Between April and July 2026, rents increased by 0.2% ». Tableaux identiques, « How to read » traduit | https://www.insee.fr/en/statistiques/9052421 | Conforme. `/en/statistiques/9050041` renvoie 404 |
| Insee, IPC septembre 2026 définitif | non précisé | Identifiant anglais **9080263** (le français est 9080209) | https://www.insee.fr/en/statistiques/9080263 | Conforme |
| Insee, IPC octobre 2026 provisoire | non précisé | Identifiant anglais **9107975** (le français est 9107965) | https://www.insee.fr/en/statistiques/9107975 | Conforme |
| Insee, IPC septembre 2026 provisoire | non précisé | Identifiant anglais **9056972** (le français est 9056956) | https://www.insee.fr/en/statistiques/9056972 | Conforme |
| Insee, IRL 2026-T2 et T1 | non précisé | T2 : 9022799 ; T1 : 8974240 | https://www.insee.fr/en/statistiques/9022799 ; https://www.insee.fr/en/statistiques/8974240 | Conforme |
| Service-public.fr, IRL | non précisé | Version anglaise automatique : `?lang=en` sur la fiche F13723 et sur l'actualité A17342 | https://www.service-public.gouv.fr/particuliers/vosdroits/F13723?lang=en ; https://www.service-public.gouv.fr/particuliers/actualites/A17342?lang=en | Conforme |
| Ministère, prix des produits pétroliers | non précisé | Page, fichier Excel et méthodologie uniquement en français | https://www.ecologie.gouv.fr/politiques-publiques/prix-produits-petroliers | Non trouvé (pas de version anglaise) |
| Cnaf, jeu de données `s_ben_nat` | aucune version attendue | Aucune version anglaise des données ni des métadonnées. data.gouv.fr propose une interface en anglais (`/en/datasets/…` répond 200) mais le titre et la description restent en français. Les PDF « RSA Conjoncture » et « PA Conjoncture » sont en français | https://www.data.gouv.fr/en/datasets/toutes-prestations-repartition-des-allocataires-selon-la-prestation-national/ | Conforme à l'attente (aucune version anglaise) |

---

### 5. Notes « À savoir »

#### Loyers

1. « L'IRL sert à réviser les loyers, ce n'est pas un niveau de loyer » : **exact**. Service-public : l'IRL sert à réviser le loyer des baux vides ou meublés, seulement si le bail le prévoit, une fois par an ; la variation annuelle de l'IRL est la hausse maximale que le bailleur peut appliquer. Source : https://www.service-public.gouv.fr/particuliers/actualites/A17342?lang=en. Précision utile : le niveau d'un trimestre peut être plus bas que celui du trimestre précédent (voir la remarque de la partie 1), donc la note devrait renvoyer à la variation sur un an.
2. « Sa hausse a été plafonnée à 3,5 % de mi-2022 à début 2024 » : **exact, à préciser**. Formulation plus sûre : « pour les indices du 3e trimestre 2022 au 1er trimestre 2024 », avec 3,5 % en métropole (2,5 % outre-mer, 2 % en Corse, qui ont leur propre IRL). Ne pas écrire « bouclier loyer » comme s'il s'agissait d'un terme de l'Insee.
3. « Les ILH mesurent l'évolution des loyers effectivement payés, secteurs libre et social, base 100 en janvier 2019 » : **exact, à compléter**. Insee : loyers hors charges des résidences principales louées vides, France métropolitaine, à qualité constante ; le secteur libre inclut la loi de 1948 ; les loyers du secteur social incluent les surloyers et les réductions de loyer de solidarité. La note de 2020 exclut les locations meublées. L'Insee précise que l'ILH reflète l'évolution constatée des loyers et diffère de l'IRL. Source : https://www.insee.fr/fr/statistiques/9050041.
4. Trimestre affiché de l'ILH : **la remarque de #28 est confirmée**. « 2026-T2 » est l'indice de juillet 2026 (T1 avril, T2 juillet, T3 octobre, T4 janvier de l'année suivante : « 2025-T4 » est janvier 2026). Formulation proposée : « Le trimestre affiché suit l'Insee : 2026-T2 correspond à l'indice de juillet 2026. »

#### Énergie

1. « Évolution sur un an des prix de l'énergie à la consommation ; l'estimation provisoire du dernier mois n'est pas reprise » : **exact**. Appui : l'Insee demande de ne pas utiliser les indices provisoires pour les revalorisations ; octobre 2026 sera définitif le 13/11/2026. Source : https://www.insee.fr/fr/statistiques/fichier/version-html/9107965/IR266_IPCprov_oct26.pdf.
2. « Le tarif réglementé du gaz a disparu en 2023 » : **exact** pour les particuliers (et les copropriétés) : fin au 30 juin 2023, loi Énergie-Climat du 8 novembre 2019. Les clients qui n'avaient pas changé d'offre ont reçu une offre de marché à compter du 1er juillet 2023. Source : https://www.anil.org/parole-expert-logement-fin-tarif-reglemente-gaz-fournisseur/. Pour éviter une lecture trop large, écrire « pour les particuliers ». L'électricité garde un tarif réglementé (connaissance générale, non vérifiée ici).
3. « Prix moyens en métropole, fioul pour 1 000 litres livrés » : **exact pour l'Insee, trompeur si on l'attribue au ministère**. Le ministère publie le fioul pour des livraisons de 2 000 à 4 999 litres, de 5 à 8,5 % moins cher que la série de l'Insee. Les moyennes du kit sont celles de l'Insee ; elles diffèrent légèrement de celles du ministère (0,6 à 0,9 % pour les carburants en septembre 2026). Proposition : citer l'Insee comme source dans le texte et garder « 1 000 litres livrés à domicile », libellé de l'Insee.
4. « Prix moyens manquants certains mois de 2020 : les séries commencent en 2021 » : **à corriger dans la formulation**. Les séries de l'Insee commencent bien avant ; c'est le kit qui commence en 2021 pour éviter les trous. Les trous viennent de la suspension de la collecte des prix pendant la crise sanitaire (documentée pour l'IPC). Proposition : « Certains mois de 2020 manquent (crise sanitaire) : les données du fichier commencent en 2021. » Éviter de lister les mois dans la note : décembre 2020 pour le gazole et le SP95-E10, cinq mois pour le fioul.

#### Prestations

1. « Caf seulement, sans la MSA » : **exact**. Les Caf représentent environ 98,6 % des bénéficiaires du RSA et 97,2 % de ceux de la prime d'activité (tous régimes, 2025). Les chiffres de la DREES sont donc un peu plus hauts (RSA 1,88 million, prime d'activité 4,73 millions) : à dire si la note est rapprochée d'autres sources.
2. « Environ sept mois de retard » : **exact si on compte depuis le début du mois**. La Cnaf considère les données définitives six mois après la fin du mois ; mars 2026 est paru le 09/10/2026 (6 mois et 9 jours après la fin de mars). Formulation plus exacte : « environ six à sept mois de retard : les chiffres ne sont publiés qu'une fois consolidés ».
3. « Foyers allocataires et personnes couvertes sont deux comptes » : **exact**. Cnaf : le foyer couvre le responsable du dossier, son conjoint, les enfants (jusqu'à 25 ans) et les autres personnes à charge ; les « personnes couvertes » comptent tous ces membres. Attention : le chiffre du fichier pour le RSA (3,72 millions) dépasse l'estimation de la Cnaf (3,61 millions) de 3 % ; la note ne doit pas promettre un rapprochement avec les publications de la Cnaf tant que cet écart n'est pas levé.
4. Réforme du RSA depuis janvier 2025 : **effet sur les effectifs non mesuré**. Faits sourcés : depuis le 1er janvier 2025 les bénéficiaires sont inscrits d'office à France Travail (sans effet sur le versement) et signent un contrat d'engagement qui fixe des heures d'activité hebdomadaires (au moins 15 heures, modulables, avec des exemptions) ; un non-respect peut entraîner une suspension ou une réduction du versement. La Cnaf écrit que « le suivi conjoncturel ne permet pas d'évaluer les impacts des réformes ». Les effectifs Caf montent : +1,7 % sur un an au 1er trimestre 2026, +1,5 % au 2e. La Cnaf compte les foyers qui perçoivent la prestation, donc une suspension de versement sort un foyer du compte, sans chiffre publié. Proposition : ne rien affirmer sur l'effet ; écrire seulement « Depuis janvier 2025, les bénéficiaires du RSA sont inscrits à France Travail et signent un contrat d'engagement ; la Cnaf ne mesure pas l'effet de cette réforme sur les effectifs. » Sources : https://www.service-public.gouv.fr/particuliers/actualites/A17997?lang=en ; https://www.service-public.gouv.fr/particuliers/vosdroits/F19778 ; RSA Conjoncture 2026T2.

---

### 6. Conclusion

Écarts d'abord :

1. **IRL 2026-T2 : +1,15 %, pas +1,38 %** (Insee, publié le 10/07/2026). À corriger si le fichier porte +1,38 %.
2. **RSA, personnes couvertes (3 720 310)** : la Cnaf estime 3,61 millions au 1er trimestre 2026 (+3,1 % d'écart, soit environ 110 000 personnes). Non expliqué. Les foyers (1 847 267) sont en revanche identiques à la moyenne Cnaf (1 847 milliers).
3. **Prix moyens (Insee) et ministère** : gazole 2,34 contre 2,3255, SP95-E10 2,14 contre 2,1224, fioul 1 833,94 contre 1 744,75 (autre tranche de livraison). Les valeurs du fichier concordent avec l'Insee tel que republié par eco3min.fr et prixaujourdhui.com, mais je n'ai pas pu les contrôler à la source sans appeler la BDM ni ouvrir les pages de série. Ne pas présenter ces valeurs comme venant du ministère.
4. **Libellé « fuels » 133,52** : c'est l'indice « Carburants et lubrifiants pour véhicules personnels », pas les produits pétroliers (135,23) ni le fioul (160,53).
5. **Prestations, écarts mineurs** : prime d'activité -0,7 % (foyers) et -1,7 % (personnes) par rapport aux moyennes provisoires du 1er trimestre de la Cnaf, compatibles avec mois définitif contre moyenne estimée.
6. **Non trouvé** : raison de l'absence de décembre 2020 pour le gazole et le SP95-E10 ; personnes couvertes pour les aides au logement (10 738 459) ; mois de début de la série (juin 2016).
7. **Note Énergie (4)** : la phrase « les séries commencent en 2021 » est inexacte pour les séries de l'Insee. Notes Énergie (3), Loyers (2), Loyers (3), Prestations (2) et (4) : à préciser comme proposé en partie 5.

Conforme :

- IRL 2026-T3 (+1,57 %, 148,06, publié le 15/10/2026) ; plafond à 3,5 % du T3 2022 au T1 2024, 2,5 % outre-mer, 2,0 % en Corse.
- ILH 2026-T2 : 111,1 ; 108,8 ; 115,6 ; publié le 15/09/2026 ; base 100 en janvier 2019 ; remarque de #28 confirmée (T2 = indice de juillet).
- IPC énergie : +21,3 % en septembre 2026 (définitif), +24,1 % en octobre 2026 (provisoire). Indices base 2025 de septembre : électricité 99,89, gaz 118,57, carburants 133,52.
- Prestations : RSA foyers (environ 1,85 million), aides au logement foyers (5,6 millions), jeu de données mis à jour le 09/10/2026, Licence Ouverte v2.0, périmètre Caf.
- Versions anglaises : identifiants trouvés pour l'IRL (9081855), l'ILH (9052421) et l'IPC (9080263, 9107975) ; aucune version anglaise du jeu Cnaf ni du ministère.

Valeurs qui reposent seulement sur un résumé de moteur de recherche ou sur un site secondaire :

- SP95-E10 2,14 (septembre) et 2,01 (août), début des séries (fioul 1992, SP95-E10 janvier 2019), source « IPC » des prix moyens : résumé de moteur de recherche des pages série de l'Insee, non ouvertes.
- Gazole 2,34, SP95-E10 2,14, fioul 1 833,94 et mois manquants de 2020 : eco3min.fr et prixaujourdhui.com, qui republient l'Insee.
- RSA du 4e trimestre 2025 (3,55 millions) et DREES : résumés de moteur de recherche et reprises (unps.fr, aladom.fr), le site de la DREES étant injoignable.
- Part des Caf de 98,6 % (RSA) et 97,2 % (PA) : texte des publications Cnaf, tous régimes, 2025. L'hypothèse que les chiffres DREES du RSA et de la prime d'activité sont « tous régimes » vient de la note de périmètre (seuls l'AAH et les aides au logement sont limités au régime général).

---

### 7. URL consultées (2026-11-02)

Insee, loyers :
- https://www.insee.fr/fr/statistiques/9081853
- https://www.insee.fr/en/statistiques/9081855
- https://www.insee.fr/en/statistiques/9022799
- https://www.insee.fr/en/statistiques/8974240
- https://www.insee.fr/en/statistiques/8608934 (IRL T2 2025, titre seulement)
- https://www.insee.fr/en/statistiques/7344859 (IRL T1 2023, titre seulement)
- https://www.insee.fr/fr/statistiques/9050041
- https://www.insee.fr/en/statistiques/9052421
- https://www.insee.fr/en/statistiques/9008997 et https://www.insee.fr/en/statistiques/8902524 (ILH d'avril et de janvier 2026, titres seulement)
- https://www.insee.fr/fr/statistiques/fichier/version-html/9050041/IR221_ILH_juil26.pdf
- https://www.insee.fr/fr/statistiques/fichier/version-html/4266810/loyers2019T3__.pdf
- https://www.insee.fr/fr/statistiques/documentation/Note%20m%C3%A9thodologique_IndiceLoyers_oct20.pdf

Insee, prix à la consommation :
- https://www.insee.fr/fr/statistiques/9080209 (et son fichier zip « Données Complémentaires IR IPC septembre 2026 »)
- https://www.insee.fr/fr/statistiques/fichier/version-html/9080209/IR247_IPCdef_sept26.pdf
- https://www.insee.fr/fr/statistiques/9107965
- https://www.insee.fr/fr/statistiques/fichier/version-html/9107965/IR266_IPCprov_oct26.pdf
- https://www.insee.fr/fr/statistiques/9056956
- https://www.insee.fr/fr/statistiques/9051406 (août 2026)
- https://www.insee.fr/en/statistiques/9080263 ; https://www.insee.fr/en/statistiques/9107975 ; https://www.insee.fr/en/statistiques/9056972
- https://www.insee.fr/fr/statistiques/5012290 (bilan 2020)
- https://www.insee.fr/fr/plan-du-site/famille-bdm/103157792 (liste des séries de prix moyens, sans valeurs)
- Apparues dans des résultats de recherche, non ouvertes : https://www.insee.fr/fr/statistiques/4993275 ; https://www.insee.fr/fr/statistiques/5010784 ; https://www.insee.fr/fr/statistiques/serie/000442588 ; https://www.insee.fr/fr/statistiques/serie/010596132 ; https://www.insee.fr/fr/statistiques/serie/000442573

Service-public, ANIL, ministère :
- https://www.service-public.gouv.fr/particuliers/vosdroits/F13723 ; https://www.service-public.gouv.fr/particuliers/vosdroits/F13723?lang=en
- https://www.service-public.gouv.fr/particuliers/actualites/A17342?lang=en
- https://www.service-public.gouv.fr/particuliers/vosdroits/F19778 ; https://www.service-public.gouv.fr/particuliers/actualites/A17997?lang=en
- https://www.service-public.gouv.fr/particuliers/vosdroits/F20820 (ouverte : sans rapport avec le gaz réglementé)
- https://www.anil.org/aj-plafonnement-evolution-indice-reference-loyer/
- https://www.anil.org/parole-expert-logement-fin-tarif-reglemente-gaz-fournisseur/
- https://www.vie-publique.fr/loi/289644-prolongation-plafonnement-hausse-des-loyers-proposition-de-loi (page vide à la lecture)
- https://www.ecologie.gouv.fr/politiques-publiques/prix-produits-petroliers
- https://www.ecologie.gouv.fr/sites/default/files/documents/Prix%20HTT%20et%20TTC%20depuis%20janvier%202020_0.xlsx
- https://www.ecologie.gouv.fr/sites/default/files/documents/M%C3%A9thodologie%20de%20calcul%20des%20prix%20moyens%20des%20produits%20p%C3%A9troliers_0.pdf
- https://www.ecologie.gouv.fr/sites/default/files/documents/Tuto%20-%20Donn%C3%A9es%20prix%20des%20produits%20p%C3%A9troliers.pdf

Cnaf, data.gouv.fr, DREES :
- https://www.caf.fr/sites/default/files/medias/cnaf/Nous_connaitre/Recherche_et_statistiques/Rsa%20Conjoncture/RSA%20Conjoncture_2026T1.pdf
- https://caf.fr/sites/default/files/medias/cnaf/Nous_connaitre/Recherche_et_statistiques/Rsa%20Conjoncture/RSA%20Conjoncture_2026T2.pdf
- https://www.caf.fr/sites/default/files/medias/cnaf/Nous_connaitre/Recherche_et_statistiques/PPA%20Conjoncture/PA%20Conjoncture_2026T1.pdf
- https://data.caf.fr/explore/dataset/s_ben_nat/information/ (page de métadonnées ; modèles de métadonnées non rendus)
- https://www.data.gouv.fr/datasets/toutes-prestations-repartition-des-allocataires-selon-la-prestation-national ; version `/en/` (statut 200)
- https://www.unps.fr/suivi-mensuel-des-prestations-de-solidarite-Edition-de-mai-2026-_r_36_a_268.html
- https://www.aladom.fr/actualites/secteur-service/11180/prestations-de-solidarite-ce-que-revelent-les-indicateurs-sociaux-au-printemps-2026/
- https://drees.solidarites-sante.gouv.fr/communique-de-presse-jeux-de-donnees/jeux-de-donnees/260605-suivi-mensuel-des-prestations-de-solidarite-mai-2026 et …/260831-suivi-mensuel-des-prestations-de-solidarite-aout-2026 (injoignables : 503 / réponse vide)

Presse et sites secondaires :
- https://eco3min.fr/evolution-prix-carburants/
- https://prixaujourdhui.com/prix/fioul-domestique/
- https://www.jechange.fr/energie/gaz/news/prix-fioul-plein-automne-2026-hausse-un-an
- https://selectra.info/energie/fioul/prix/evolution
- https://prix-carburant.eu/barometre-mensuel-2026-09 (résumé de moteur de recherche seulement)

## Mises à jour

- **03/11/2026** : l'écart des personnes couvertes par le RSA est expliqué par deux définitions (foyer Caf contre personnes à charge au sens du RSA, mois contre moyenne trimestrielle) : voir `socialBenefits.md`.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
