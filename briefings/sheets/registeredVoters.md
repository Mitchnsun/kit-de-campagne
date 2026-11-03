# `registeredVoters` · Corps électoral

**Vérifiée le 02/11/2026** : double vérification sur le web, totaux, listes, taux et dates conformes (section « Double vérification ») ; un écart expliqué sur les effectifs par âge (autre champ que la figure 2a de l'Insee Focus n° 378), dit dans la fiche et dans une note ; deux « À savoir » corrigés (la date d'extraction, l'inscription d'office depuis 1997).

| Champ | Valeur |
| --- | --- |
| Indicateur | `registeredVoters`, dossier « Électorat » (`electorate`), page de type comparaison, ticket #144 de l'app, premier volet (statut `planned` : les chiffres et la fiche avant la page) |
| Données | `briefings/data/registeredVoters.json`, écrit par `yarn briefings registeredVoters` le 2026-11-02 |
| Sources | Insee, « Caractéristiques du corps électoral », jeu Melodi `DS_ELECTORAL` (répertoire électoral unique), modifié le 2026-08-01 selon son catalogue, expliqué par l'Insee Focus n° 378 « Corps électoral 2026 » du 11/03/2026, https://www.insee.fr/fr/statistiques/8888278 (anglais, résumé : https://www.insee.fr/en/statistiques/8896480) ; Licence Ouverte 2.0 |
| Série | `voters` : inscrits sur toutes les listes, France hors Nouvelle-Calédonie, à l'extraction de chaque scrutin, par l'année de l'extraction : 2019 (européennes, 14/04) 47 120 498 ; 2020 (municipales, 14/02) 47 664 895 ; 2021 (départementales et régionales, 24/05) 47 947 555 ; 2022 (présidentielle, 09/03) 48 803 175 ; 2024 (européennes, 08/05) 49 339 714 ; 2026 (municipales, 11/02) 50 187 093 |
| Valeurs par catégorie | Au 11/02/2026 : `votersByList` (listes principales 48 154 748, complémentaires 373 681, consulaires 1 658 664, ce que le total laisse) ; `mainListByAge` (Français des listes principales en 6 tranches, champ de Melodi : France hors Nouvelle-Calédonie, collectivités d'outre-mer comprises ; leur somme est le total des listes principales) ; `registrationRateByAge` (taux d'inscription des Français en âge de voter, métropole et DROM, en entiers : 100 / 97 / 92 / 93 / 94 / 93, ensemble 95) |
| Chiffre clé | 50,2 millions d'inscrits en 2026, en hausse (+847 379 depuis 2024) |
| Règles | Une extraction par an au plus, sinon le script s'arrête ; les détails doivent être de la dernière extraction ; les effectifs et les taux n'ont pas le même champ, ils ne se divisent pas |
| Première édition | À remplir à la publication |

## « À savoir »

1. Le 11 février 2026 est une date d'extraction : la date limite d'inscription était le 4 février en ligne et le 6 en mairie, puis cinq jours de traitement par les communes (Insee Focus n° 378). La phrase d'abord prévue (« à la clôture ») est corrigée.
2. Listes principales, complémentaires (sur demande) et consulaires : définitions de l'Insee Focus n° 378.
3. Inscription d'office à 18 ans depuis 1997 (Insee Focus n° 378 et Insee Première n° 1986) ; 2019 est la mise en service du répertoire électoral unique. La phrase d'abord prévue (« depuis 2019 ») était fausse ; « explique » devient « c'est principalement ce qui », comme l'Insee l'écrit.
4. Les effectifs par âge de Melodi ne sont pas ceux de la figure 2a du Focus (47 814 756, métropole et DROM, âge au 1er janvier 2026) : +339 992 inscrits, dont les 255 233 des collectivités d'outre-mer et l'écart d'âge de référence (hypothèse de la vérification : l'âge à la date d'extraction). Le calage de #51 qui reprend la figure 2a garde sa source.

Non repris : « 48,7 millions admis à voter aux municipales », un chiffre de l'Insee qui compte la Nouvelle-Calédonie (48 154 748 + 358 428 + 220 000) ; le ministère de l'Intérieur publie un autre nombre (inscrits du jour du scrutin). La date du 15/03/2026 du jeu Melodi (1er tour des municipales) ne porte pas d'inscrits.

À actualiser : à la prochaine extraction (élection présidentielle de 2027).

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans appeler l'API Melodi. Son rapport, tel quel :

Date de la vérification : 2026-11-02. Méthode : sources web uniquement. L'API Melodi n'a pas été appelée et aucun fichier sous /home/user n'a été lu ni modifié.

### Méthode et limites

- **Source de référence** : Insee Focus n° 378 « Corps électoral 2026 ». J'ai téléchargé le HTML de la page et son classeur `if378.xlsx` (feuilles « Figure 1a » à « Figure 4 » et « Tableau complémentaire »). Les valeurs Insee citées ci-dessous sont lues dans le HTML ou le classeur eux-mêmes, pas dans un résumé.
- **Résumés automatiques** : pour data.gouv.fr, service-public.gouv.fr, Wikipédia, le Conseil constitutionnel et la Banque des Territoires, je n'ai eu que le résumé produit par l'outil de lecture de pages (WebFetch), pas le HTML brut. Je l'indique « (résumé de page) » dans les tableaux.
- **Moteur de recherche** : quatre informations ne venaient d'abord que d'un résumé de moteur de recherche : l'identifiant anglais 8896480, la phrase « 50,2 millions » de la page annuelle de l'Insee, la couverture temporelle du jeu (14/04/2019 au 15/03/2026) et une mise à jour du jeu au 26 juin 2026. Les trois premières ont été revérifiées sur les pages elles-mêmes. La quatrième est contredite par la page de data.gouv.fr (3 août 2026) : je retiens la page.
- **Ministère de l'Intérieur** : les archives des résultats (`archives-resultats-elections.interieur.gouv.fr`, `elections.interieur.gouv.fr`) répondent HTTP 403 depuis l'environnement. Le site actuel (`resultats-elections.interieur.gouv.fr/municipales2026/`) n'offre qu'une recherche par commune, sans total national. **Je n'ai donc aucun chiffre du ministère lu à la source**, sauf le second tour de la présidentielle 2022 (décision du Conseil constitutionnel). Les autres chiffres « ministère » viennent des encadrés Wikipédia, qui renvoient vers le ministère sans note précise : à traiter comme secondaires.
- **Recherches** : le quota de recherches web a été atteint en cours de session. Je n'ai pas pu chercher les Focus Insee de 2021 et 2022 ni de presse supplémentaire. Les points concernés sont marqués « Non trouvé ».
- **Catalogue Melodi** : la page `catalogue-donnees.insee.fr/.../DS_ELECTORAL` est une application JavaScript, illisible sans appeler l'API. Je me suis appuyé sur la copie du jeu sur data.gouv.fr.

### 1. Nombre d'inscrits (France hors Nouvelle-Calédonie, toutes listes)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2019, européenne, extraction du 14/04/2019 | 47 120 498 | 47 120 498, « données au 14 avril 2019 » | Insee Focus n° 154 : https://www.insee.fr/fr/statistiques/4134308 ; Figure 1b du Focus 378 (https://www.insee.fr/fr/statistiques/8888278) | Conforme |
| 2020, municipale, 14/02/2020 | 47 664 895 | 47 664 895, « données au 14 février 2020 » | Insee Focus n° 186 (26/02/2020) : https://www.insee.fr/fr/statistiques/4317766 ; Figure 1b du Focus 378 | Conforme |
| 2021, départementales et régionales, 24/05/2021 | 47 947 555 | 47 947 555 (Figure 1b du Focus 378 et du Focus 328). **Date d'extraction du 24/05/2021 : absente des pages consultées** | https://www.insee.fr/fr/statistiques/8888278 ; https://www.insee.fr/fr/statistiques/fichier/8192479/if328.xlsx | Valeur : Conforme. Date : Non trouvé |
| 2022, présidentielle, 09/03/2022 | 48 803 175 | 48 803 175, « Nombre d'électeurs au 9 mars 2022 » (Figure 3 du Focus 328) | https://www.insee.fr/fr/statistiques/fichier/8192479/if328.xlsx ; https://www.insee.fr/fr/statistiques/8192479 | Conforme |
| 2024, européenne, 08/05/2024 | 49 339 714 | 49 339 714, « données du 8 mai 2024 » | Insee Focus n° 328 (30/05/2024) : https://www.insee.fr/fr/statistiques/8192479 | Conforme |
| 2026, municipale, 11/02/2026 | 50 187 093 | 50 187 093, « données du 11 février 2026 » (Figure 1a, 1b, 3) | https://www.insee.fr/fr/statistiques/8888278 ; https://www.insee.fr/fr/statistiques/fichier/8888278/if378.xlsx | Conforme |
| Chiffre clé « 50,2 millions », en hausse | 50,2 M, hausse | « 50,2 millions d'électeurs » hors Nouvelle-Calédonie ; +847 379 (+1,7 %) depuis le 8 mai 2024 ; +3 066 595 (+6,5 %) depuis 2019 (calcul à partir des Figures 1b et 3) | https://www.insee.fr/fr/statistiques/8888278 ; https://www.insee.fr/fr/statistiques/2389209 (« 50,2 millions », Lecture de la Figure 1) | Conforme |

Les six valeurs se retrouvent aussi ligne à ligne par sexe (Figure 1b : par exemple 24 644 779 femmes et 22 475 719 hommes en 2019), et la somme femmes + hommes redonne chaque total.

**Dates d'extraction.** Les dates 14/04/2019, 14/02/2020, 09/03/2022, 08/05/2024 et 11/02/2026 sont des dates d'extraction du répertoire électoral unique (REU), pas des dates limites d'inscription. L'Insee écrit pour 2026 : « Les dates limites pour les élections municipales étaient le 4 février pour la démarche en ligne et le 6 février en mairie. Ensuite, les communes disposent de 5 jours pour traiter les demandes. » Le 11 février est donc cinq jours après la clôture. Par calcul (date limite en mairie = sixième vendredi avant le premier tour, règle décrite par service-public.gouv.fr), l'extraction suit la date limite de 5 jours en 2022 et 2024, de 7 jours en 2020 et de 10 jours en 2021 (date limite du 14 mai 2021, extraction du 24 mai : plausible, mais non confirmée). Pour 2019, première utilisation du REU, je n'ai pas vérifié la date limite.

#### 1b. Comparaison avec les inscrits comptés par le ministère de l'Intérieur

Les deux comptes ne mesurent pas la même chose. Le fichier donne **toutes les listes du REU hors Nouvelle-Calédonie** à la clôture des inscriptions. Le ministère compte **les inscrits du scrutin** : pour les municipales, les régionales et les départementales, ni les listes consulaires (1,3 à 1,7 million de Français de l'étranger qui n'y votent pas), ni la liste complémentaire européenne seule ; pour la présidentielle, ni les listes complémentaires (les citoyens de l'UE n'y votent pas) ; Nouvelle-Calédonie incluse ou non selon le scrutin ; liste du jour du scrutin et non de l'extraction. L'Insee prévient d'ailleurs en 2019 que le REU « ne peut être comparé ni aux données publiées jusqu'à présent par l'Insee à partir du Fichier général des électeurs ni au nombre d'électeurs annoncé à l'occasion de chaque élection » (Focus 154).

Les chiffres « ministère » ci-dessous sont des chiffres d'encadrés Wikipédia (résumé de page), sauf mention contraire.

| Scrutin | Fichier (REU, toutes listes, hors Nouvelle-Calédonie) | Corps électoral du scrutin selon l'Insee | Inscrits du ministère (source) | Explication de l'écart | Verdict |
|---|---|---|---|---|---|
| Européenne 2019 | 47 120 498 | 47,3 M, Nouvelle-Calédonie comprise (Focus 328) | 47 345 328 (https://fr.wikipedia.org/wiki/Élections_européennes_de_2019_en_France) | Fichier − ministère = −224 830. La Nouvelle-Calédonie comptait 211 000 électeurs au 28/02/2019 (Focus 154) : 47 120 498 + 211 000 = 47 331 498, à 14 000 près du ministère | Écart expliqué |
| Municipales 2020 | 47 664 895 | 46,6 M admis à voter (Focus 378, Nouvelle-Calédonie comprise) | 46 437 411 (https://fr.wikipedia.org/wiki/Élections_municipales_de_2020_en_France) | Fichier − ministère = +1 227 484. Les listes consulaires (1 308 642 en 2020, Figure 1 du Focus 186) ne votent pas aux municipales. Hors consulaires : 46 356 253, dont environ 318 000 de listes complémentaires municipales (estimation : 358 000 en 2026, soit « 40 000 de plus qu'en 2020 »). Le ministère est 93 000 au-dessus de ce total hors Nouvelle-Calédonie et environ 160 000 au-dessous des « 46,6 M » arrondis de l'Insee (Nouvelle-Calédonie comprise) : écart résiduel non élucidé | Écart expliqué (au niveau du périmètre, pas au chiffre près) |
| Départementales et régionales 2021 | 47 947 555 | non publié | Régionales 45 924 359 ; départementales 43 248 887 (1er tour, Wikipédia, notes non lisibles) | Hors consulaires (environ 1,3 à 1,5 M) et hors complémentaires (environ 0,3 M), il reste environ 46,1 à 46,3 M, puis environ −0,25 M pour les collectivités d'outre-mer, sans élection régionale, soit 45,9 à 46,0 M : ordre de grandeur cohérent avec 45,9 M (calcul approximatif de ma part, chiffres consulaires de 2021 non trouvés). Les départementales ne couvrent que les cantons renouvelés | Écart expliqué (ordre de grandeur) |
| Présidentielle 2022 | 48 803 175 | non publié | 1er tour 48 747 876 (Wikipédia) ; 2d tour 48 752 339 (décision n° 2022-197 PDR du Conseil constitutionnel, résumé de page : https://www.conseil-constitutionnel.fr/decision/2022/2022197PDR.htm) | Fichier − ministère = +55 299 (1er tour). Le fichier contient les listes complémentaires (citoyens de l'UE, qui ne votent pas à la présidentielle) mais pas la Nouvelle-Calédonie (qui vote) : les deux effets se compensent presque (environ 0,3 M de listes complémentaires contre environ 0,22 M en Nouvelle-Calédonie, ordres de grandeur) | Écart expliqué |
| Européenne 2024 | 49 339 714 | 49,5 M, Nouvelle-Calédonie comprise (Focus 328) | 49 462 981 (https://fr.wikipedia.org/wiki/Élections_européennes_de_2024_en_France) | Fichier − ministère = −123 267. Corps électoral recalculé : 47 445 283 + 1 565 655 + 253 854 + 15 273 = 49 280 065 (listes complémentaires municipale seule exclues) ; avec 222 000 électeurs de Nouvelle-Calédonie (Focus 328) : 49 502 065, soit 39 084 de plus que le ministère. Résidu non élucidé (hypothèse : liste du jour du scrutin et non de l'extraction) | Écart expliqué (résidu de 39 000) |
| Municipales 2026 | 50 187 093 | 48,7 M admis à voter, dont Nouvelle-Calédonie (Focus 378) | 1er tour 48 474 213 ; 2d tour 16 879 356 pour les communes concernées (Wikipédia : https://fr.wikipedia.org/wiki/Élections_municipales_de_2026_en_France) | Fichier − ministère = +1 712 880 = consulaires 1 658 664 + complémentaire européenne seule 15 253 + 38 963. Liste principale + complémentaires municipales hors Nouvelle-Calédonie : 48 154 748 + 358 428 = 48 513 176, soit 38 963 de plus que le ministère. Le même résidu de 39 000 qu'en 2024, ce qui suggère un effet systématique de date de liste. **Avec 220 000 électeurs de Nouvelle-Calédonie on obtient 48 733 176, soit les « 48,7 M » de l'Insee** | Écart expliqué (voir ci-dessous) |

**Point d'attention : le « 48,7 millions » n'est pas un chiffre du ministère.** C'est le chiffre de l'Insee (sous-titre du Focus 378 : « 48,7 millions d'électeurs inscrits pour les élections municipales 2026 »), Nouvelle-Calédonie comprise (220 000 électeurs au 23 janvier 2026). La Banque des Territoires l'attribue aussi à l'Insee (https://www.banquedesterritoires.fr/municipales-combien-de-personnes-susceptibles-daller-voter-ce-dimanche, résumé de page). Le seul chiffre du ministère que j'ai vu, 48 474 213 au premier tour, est secondaire (Wikipédia) et suit la logique hors Nouvelle-Calédonie. Verdict sur l'attribution au ministère : **Écart**. Le chiffre du ministère n'a pas été confirmé à la source (403).

### 2. Inscrits par type de liste au 11/02/2026

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Listes communales principales | 48 154 748 | 48 154 748 (femmes 25 125 014, hommes 23 029 734) | Figure 1a : https://www.insee.fr/fr/statistiques/8888278 ; if378.xlsx | Conforme |
| Listes complémentaires, ensemble (citoyens de l'UE) | 373 681 | 373 681 (Figure 4 : « 373 681 électeurs inscrits sur au moins une des deux listes complémentaires »). Insee : « 374 000 » | Figure 4 du Focus 378 | Conforme |
| dont municipale et européenne | 278 856 | 278 856 | Figure 1a | Conforme |
| dont municipale seule | 79 572 | 79 572 | Figure 1a | Conforme |
| dont européenne seule | 15 253 | 15 253 | Figure 1a | Conforme |
| Listes consulaires | 1 658 664 | 1 658 664 (Insee : « 1,7 million », 214 listes consulaires, Genève 140 000) | Figure 1a | Conforme |
| Total | 50 187 093 | 48 154 748 + 373 681 + 1 658 664 = 50 187 093 ; 278 856 + 79 572 + 15 253 = 373 681 | Calcul sur la Figure 1a | Conforme |
| Électeurs inscrits pour les municipales (listes complémentaires) | non mentionné | 358 428 = 278 856 + 79 572 (« 358 000 ») | Figure 4 | Conforme |
| Nouvelle-Calédonie | 220 000 | « 220 000 électeurs étaient inscrits sur les listes de Nouvelle-Calédonie au 23 janvier 2026 » (rubrique Méthodes) | https://www.insee.fr/fr/statistiques/8888278 | Conforme |
| Corps électoral total | 50,4 millions | 50,4 millions (50 187 093 + 220 000 = 50 407 093) | Chapeau et texte du Focus 378 | Conforme |
| Admis à voter aux municipales | 48,7 millions | 48,7 millions (48 154 748 + 358 428 + 220 000 = 48 733 176) ; 46,6 millions en 2020 | Texte du Focus 378 | Conforme |

Détail utile : la liste principale se répartit en 46,3 M en métropole, 1,6 M dans les DROM et 255 000 dans les COM hors Nouvelle-Calédonie. Le « Tableau complémentaire » du classeur donne 1 566 505 pour les cinq DROM et 255 233 pour les cinq COM.

### 3. Français sur les listes principales, par âge

**Cette série ne correspond pas au tableau publié par l'Insee (Figure 2a).** Les six valeurs du fichier somment exactement à 48 154 748, le total des listes principales (Figure 1a). Le tableau publié par l'Insee somme à 47 814 756 et couvre un autre périmètre.

| Élément | Valeur du fichier | Valeur trouvée (Insee, Figure 2a) | Écart | Source (URL) | Verdict |
|---|---|---|---|---|---|
| 18-24 ans | 5 546 036 | 5 427 080 | +118 956 | https://www.insee.fr/fr/statistiques/8888278 ; if378.xlsx, feuille « Figure 2a » | Écart expliqué |
| 25-39 ans | 10 560 844 | 10 489 900 | +70 944 | idem | Écart expliqué |
| 40-54 ans | 10 758 876 | 10 690 167 | +68 709 | idem | Écart expliqué |
| 55-64 ans | 7 610 505 | 7 569 269 | +41 236 | idem | Écart expliqué |
| 65-79 ans | 9 837 366 | 9 805 067 | +32 299 | idem | Écart expliqué |
| 80 ans ou plus | 3 841 121 | 3 833 273 | +7 848 | idem | Écart expliqué |
| Ensemble | 48 154 748 (somme calculée) | 47 814 756 | +339 992 (+0,7 %) | idem | Écart expliqué |

**Pourquoi les deux séries diffèrent** (notes de la Figure 2a : « âge révolu au 1er janvier 2026 », « inscrits ayant 18 ans ou plus à cette date », champ « France métropolitaine et DROM »).

1. **Périmètre** : la Figure 2a exclut les COM. Les 255 233 inscrits des COM (Polynésie française 215 471, Saint-Martin 20 220, Wallis-et-Futuna 9 227, Saint-Barthélemy 5 256, Saint-Pierre-et-Miquelon 5 059 ; « Tableau complémentaire ») sont dans le total de la liste principale du fichier.
2. **Date de référence de l'âge** : la Figure 2a prend l'âge au 1er janvier 2026 et laisse de côté ceux qui ont eu 18 ans entre le 1er janvier et le 11 février. Le fichier semble prendre l'âge à la date de l'extraction, puisque son total est le total complet.
3. **Arithmétique de contrôle (mon calcul)** : 48 154 748 − 255 233 (COM) − 47 814 756 = 84 759. Ce solde correspond à l'ordre de grandeur des jeunes devenus majeurs en 41 jours (l'Insee compte 1 476 369 jeunes atteignant l'âge électoral du 8 mai 2024 au 11 février 2026, soit environ 2 300 par jour, donc environ 94 000 sur 41 jours). Cela explique que la tranche 18-24 ans porte l'écart le plus fort (+118 956, soit +2,2 %).

Je ne peux pas confirmer les six valeurs du fichier une à une : l'Insee ne publie pas cette ventilation avec ce périmètre (liste principale complète, âge à la date de l'extraction). Elles sont cohérentes avec le total publié, c'est la seule vérification indépendante possible.

**Conséquences pour le kit.**
- L'intitulé doit préciser le périmètre : « Français inscrits sur une liste communale principale, collectivités d'outre-mer comprises, âge révolu à la date de l'extraction ». Ce n'est pas la Figure 2a.
- Ne pas mélanger ces effectifs avec les taux de la partie 4 : les taux Insee sont calculés sur un autre périmètre (métropole et DROM, âge au 1er janvier). Un effectif du fichier divisé par un taux Insee donnerait un faux dénominateur.
- Si l'on préfère un chiffre directement publié, la Figure 2a (47 814 756) est la référence citable ; elle figure aussi dans https://www.insee.fr/fr/statistiques/2389209 et son classeur https://www.insee.fr/fr/statistiques/fichier/2389209/cond-vie-soc-liste-elec.xlsx.

### 4. Taux d'inscription par âge (liste communale principale, France métropolitaine et DROM)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Ensemble | 95 % | 95 % (femmes 95, hommes 96) | Figure 2b : https://www.insee.fr/fr/statistiques/8888278 ; if378.xlsx | Conforme |
| 18-24 ans | 100 % | 100 % (femmes 100, hommes 100) | idem | Conforme |
| 25-39 ans | 97 % | 97 % (femmes 97, hommes 98) | idem | Conforme |
| 40-54 ans | 92 % | 92 % (femmes 92, hommes 91) | idem | Conforme |
| 55-64 ans | 93 % | 93 % (femmes 94, hommes 93) | idem | Conforme |
| 65-79 ans | 94 % | 94 % (femmes 94, hommes 95) | idem | Conforme |
| 80 ans ou plus | 93 % | 93 % (femmes 93, hommes 94) | idem | Conforme |

Les mêmes valeurs figurent dans https://www.insee.fr/fr/statistiques/2389209 (Figure 2, avec effectifs 5 427 080 … 47 814 756).

**Décimales.** Aucune. Les deux classeurs (`if378.xlsx` et `cond-vie-soc-liste-elec.xlsx`) et le HTML ne donnent que des pourcentages entiers, comme le Focus 328 de 2024. Il n'est pas possible de récupérer des décimales à partir de ces sources.

**Définition (Focus 378, rubrique Définitions).** Le taux est « le rapport entre le nombre d'électeurs de nationalité française inscrits sur les listes électorales principales des communes et l'estimation de la population de plus de 18 ans de nationalité française résidant en France, hors collectivités d'outre-mer ». Le dénominateur vient des estimations de population de l'Insee, « données provisoires et arrêtées fin décembre 2025 ».

**Comment le taux des 18-24 ans atteint 100 %.**
- Ce que dit l'Insee : « Tous les jeunes adultes (entre 18 et 24 ans) sont inscrits sur une liste électorale, principalement du fait de la procédure d'inscription d'office à 18 ans. » Les générations plus âgées « n'ont pas bénéficié de l'inscription d'office à 18 ans qui s'est progressivement mise en place à partir de 1997 » et ne se réinscrivent pas toujours après un déménagement, d'où le minimum de 92 % chez les 40-54 ans.
- Ce que l'Insee ne dit pas : le taux brut. C'est un pourcentage arrondi à l'entier : « 100 % » signifie entre 99,5 % et 100,5 %. Le numérateur (inscrits du REU) et le dénominateur (estimation provisoire de population) viennent de deux sources différentes. Un petit écart de mesure entre elles suffit à approcher ou dépasser 100 %. **C'est mon interprétation**, pas une affirmation de l'Insee.
- Pour mémoire : 97 % des moins de 30 ans en 2019 (Focus 154), 99 % en 2020 (Focus 186), 100 % pour les 18-24 ans en 2024 et 2026.

### 5. Dates et licence

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Parution de l'Insee Focus n° 378 | 11/03/2026 | « Paru le : 11/03/2026 » ; « Mars 2026 · n° 378 » ; auteure Manuella Baraton. Même date sur la page annuelle et sur « Les électeurs en 2026 » | https://www.insee.fr/fr/statistiques/8888278 ; https://www.insee.fr/fr/statistiques/2389209 ; https://www.insee.fr/fr/statistiques/8276873?geo=DEP-37 | Conforme |
| Dernière modification du jeu Melodi | 2026-08-01 | data.gouv.fr (copie du catalogue Insee) : « Dernière mise à jour 3 août 2026 », création 8 octobre 2024, fréquence irrégulière (résumé de page) | https://www.data.gouv.fr/datasets/caracteristiques-du-corps-electoral et /informations | Écart expliqué (2 jours : moisson de la copie data.gouv.fr, hypothèse) |
| Trace d'une mise à jour après mars 2026 | non précisé | Oui : le jeu a été modifié début août 2026. Couverture temporelle annoncée : 14 avril 2019 au 15 mars 2026 | idem | Voir ci-dessous |
| Date d'extraction 2026 | 11/02/2026 | 11/02/2026 pour les inscrits (Insee) ; 15/03/2026 = jour du 1er tour des municipales | https://www.insee.fr/fr/statistiques/8888278 | Conforme |
| Licence | Licence Ouverte 2.0 | « Licence Ouverte / Open Licence version 2.0 » (jeu sur data.gouv.fr ; mentions légales de l'Insee) | https://www.data.gouv.fr/datasets/caracteristiques-du-corps-electoral ; https://www.insee.fr/fr/information/2008466 | Conforme |

**Mise à jour après mars 2026.**
- Rien dans les pages Insee consultées n'indique une révision du Focus 378 (aucune mention « mis à jour » ; mêmes chiffres dans le HTML, les deux classeurs et la page annuelle).
- La couverture temporelle de la copie data.gouv.fr court jusqu'au 15 mars 2026. Cette date est le jour du premier tour des municipales, pas un jour de clôture des inscriptions. La description du jeu indique : « les données sur les électeurs sont extraites à la clôture des inscriptions de l'élection mentionnée » (aussi dans la note de https://www.insee.fr/fr/statistiques/8276873), et le nombre de procurations est celui « valides le jour du scrutin ». **Hypothèse (non vérifiée, car Melodi n'est pas appelé)** : les lignes datées du 15/03/2026 sont des lignes de procurations, et la mise à jour d'août 2026 les a ajoutées ou complétées. Les inscrits 2026 restent alors ceux du 11/02/2026.
- À vérifier côté Melodi pour lever le doute : que les lignes « type de liste » et « âge » de 2026 portent bien la période 2026-02-11, et non 2026-03-15.
- Un résumé de moteur de recherche avait annoncé « dernière mise à jour 26 juin 2026 ». La page elle-même indique le 3 août 2026 : je retiens la page.

**Licence.** Les mentions légales de l'Insee précisent que les données publiques sont sous Licence Ouverte 2.0 (Etalab), « sous réserve de mentionner la source sous la forme "Source : Insee", de mentionner la date de dernière mise à jour des données lorsque celle-ci est connue et de ne pas altérer le sens des informations ». La page du Focus 378 ne porte pas de licence propre, elle renvoie à ces mentions. À reprendre dans la mention de source du kit : « Source : Insee, Répertoire électoral unique, données du 11 février 2026 ».

### 6. Versions anglaises

| Élément | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|
| Insee Focus n° 378 en anglais | Autre identifiant : **8896480**. Titre : « 2026 electoral body — 48.7 million registered voters for the 2026 municipal elections ». « Paru le : 11/03/2026 ». Page de résumé uniquement : pas de tableaux ni de lien vers le classeur | https://www.insee.fr/en/statistiques/8896480 | Conforme (autre id) |
| Version française | 8888278 ; lien de langue « English » vers `/langue/en` | https://www.insee.fr/fr/statistiques/8888278 | Conforme |
| Croisement d'identifiants | `/en/statistiques/8888278` et `/fr/statistiques/8896480` renvoient 404 ; `/en/statistiques/fichier/8896480/if378.xlsx` renvoie 500 | testés par requête directe | Information |
| Classeur de données | `if378.xlsx` (207 Ko) n'existe qu'en français | https://www.insee.fr/fr/statistiques/fichier/8888278/if378.xlsx | Information |

Le jeu data.gouv.fr porte un titre anglais : « Electoral body characteristics ». Je n'ai pas trouvé de PDF anglais du Focus 378. Le Focus 328 (2024) n'a pas de page à `/en/statistiques/8192479` (404) ; son éventuel identifiant anglais n'a pas été cherché.

### 7. Les quatre notes « À savoir »

#### Note 1 : « Le décompte est fait à la clôture des inscriptions avant chaque scrutin (11 février 2026 pour les municipales de mars 2026) ; la Nouvelle-Calédonie n'est pas dans le répertoire unique. »

- **Fondé** : « À la clôture des inscriptions pour les élections municipales, début février 2026 » (Focus 378) ; « Les données sur les électeurs sont extraites à la clôture des inscriptions de l'élection mentionnée » (https://www.insee.fr/fr/statistiques/8276873). Le REU ne contient pas la Nouvelle-Calédonie car la loi du 1er août 2016 ne s'y applique pas (Focus 378, rubrique Méthodes).
- **Imprécis** : le 11 février n'est pas la date de clôture. La date limite était le 4 février en ligne et le 6 février en mairie, puis cinq jours de traitement par les communes. Même chose pour les autres scrutins : ce sont des dates d'extraction (partie 1).
- **Formulation proposée** : « Le décompte est arrêté quelques jours après la clôture des inscriptions de chaque scrutin, une fois les demandes traitées par les mairies : le 11 février 2026 pour les municipales de mars 2026. Le répertoire électoral unique ne contient pas la Nouvelle-Calédonie (environ 220 000 électeurs, qui ont leurs propres listes). »

#### Note 2 : « Les listes principales : les Français qui votent dans leur commune ; les complémentaires : les citoyens d'un autre pays de l'UE, pour les municipales ou les européennes ; les consulaires : les Français de l'étranger, qui ne votent pas aux municipales. »

- **Fondé** : définitions du Focus 378 (listes principales, complémentaires, consulaires). Le Focus précise que les inscrits consulaires « ne seront pas admis à voter pour les élections municipales » mais votent aux élections présidentielles, législatives et européennes, aux référendums, et aux élections des conseillers des Français de l'étranger de fin mai 2026.
- **À nuancer** : l'inscription sur une liste complémentaire n'est pas automatique, elle se demande (service-public.gouv.fr, résumé de page : https://www.service-public.gouv.fr/particuliers/vosdroits/F1937). Les citoyens de l'UE inscrits ne votent qu'au scrutin choisi (municipal, européen ou les deux). Seuls 374 000 sur 1,3 million de citoyens de l'UE majeurs établis en France sont inscrits (Focus 378).
- **Formulation proposée** : « Les listes principales rassemblent les Français qui votent dans leur commune. Les listes complémentaires rassemblent les citoyens d'un autre pays de l'Union européenne qui ont demandé à voter en France, aux municipales, aux européennes ou aux deux. Les listes consulaires rassemblent les Français établis hors de France, qui ne votent pas aux municipales. »

#### Note 3 : « Depuis 2019, les jeunes sont inscrits d'office à 18 ans, ce qui explique le taux de 100 % chez les 18-24 ans. »

- **Date fausse.** L'inscription d'office à 18 ans date de **1997** et non de 2019. Sources : Focus 378 (« l'inscription d'office à 18 ans qui s'est progressivement mise en place à partir de 1997 ») ; Insee Première n° 1986 (« L'inscription n'est systématique que depuis 1997 pour les jeunes atteignant l'âge de 18 ans. Avant cette date, la première inscription […] était un acte volontaire », https://www.insee.fr/fr/statistiques/7766966) ; le Focus 154 de 2019 la cite déjà (« Grâce à la procédure de l'inscription d'office »). 2019 est l'année de mise en service du REU (1er janvier 2019), pas du dispositif. Je n'ai pas vérifié le texte de loi de 1997 sur le web.
- **« Explique » trop fort** : l'Insee écrit « principalement du fait de la procédure d'inscription d'office ». Il s'y ajoute l'arrondi à l'entier et l'estimation de population (partie 4). Sur service-public.gouv.fr, l'inscription automatique suppose que le jeune se soit fait recenser à 16 ans (résumé de page : https://www.service-public.gouv.fr/particuliers/vosdroits/F1367).
- **Formulation proposée** : « Les jeunes sont inscrits d'office sur les listes à 18 ans (une règle appliquée depuis 1997, que le répertoire électoral unique gère depuis 2019) : c'est pourquoi presque tous les 18-24 ans sont inscrits (100 % une fois arrondi). Les générations plus âgées ne l'ont pas connue et se réinscrivent moins souvent après un déménagement. »

#### Note 4 : « Les inscrits ne sont ni les habitants (pyramide des âges) ni les votants (participation par âge). »

- **Exacte.** Compléments sourcés : le taux d'inscription de 95 % montre que 5 % des Français adultes résidents ne sont pas inscrits (5,8 % en 2022, soit 2,9 millions, Insee Première 1986) ; les étrangers hors UE n'ont pas de liste ; 16,5 % des inscrits de 2022 ne l'étaient pas dans la commune de leur résidence principale (titre de l'Insee Première 1986) ; les listes consulaires comptent 1,7 million de personnes qui ne résident pas en France.
- **Participation** : la participation par âge relève d'autres études de l'Insee (Insee Première n° 1929, « Vingt ans de participation électorale », cité dans le Focus 378), sur l'enquête participation électorale, pas du REU.
- **Formulation proposée** : « Les inscrits ne sont pas les habitants : les étrangers hors Union européenne n'y figurent pas, les Français de l'étranger y figurent, et environ 5 % des Français adultes résidant en France ne sont pas inscrits. Ils ne sont pas non plus les votants : la participation par âge est un autre indicateur. »

### 8. Conclusion

#### Écarts à traiter (par ordre d'importance)

1. **Effectifs par âge (partie 3)** : les six valeurs du fichier ne sont pas celles du tableau publié (Figure 2a). Écart total +339 992 (+0,7 %), +118 956 pour les 18-24 ans. Il s'explique par le périmètre (COM incluses : 255 233) et la date de référence de l'âge (extraction du 11/02 au lieu du 1er janvier : environ 85 000 jeunes de 18 ans de plus), et non par une erreur de lecture : la somme redonne exactement 48 154 748. Le libellé du kit doit dire ce périmètre. Je n'ai pas pu confirmer chaque valeur à la source.
2. **Note 3** : « depuis 2019 » est faux, l'inscription d'office date de 1997. Corriger et nuancer « explique ».
3. **« 48,7 millions » attribué au ministère de l'Intérieur** : c'est le chiffre de l'Insee, Nouvelle-Calédonie comprise. Le chiffre du ministère (Wikipédia, non confirmé à la source) est de 48 474 213 au premier tour. À corriger si le texte du jeu cite le ministère.
4. **Note 1** : le 11 février est une date d'extraction postérieure de cinq jours à la clôture du 6 février. Reformuler.
5. **Extraction du 24/05/2021** : non trouvée dans les pages Insee consultées. La valeur 47 947 555 est correcte, seule la date n'est pas confirmée.
6. **Écart résiduel avec le ministère** : environ 39 000 inscrits en 2024 et en 2026, 93 000 à 120 000 en 2020. Il vient de la liste du jour du scrutin, à confirmer avec les sources primaires du ministère (inaccessibles).

#### Conforme

- Les six totaux 2019 à 2026, les dates d'extraction 2019, 2020, 2022, 2024 et 2026, la hausse de +847 379 depuis 2024.
- Les trois types de liste du 11/02/2026 et leurs sous-totaux, la Nouvelle-Calédonie (220 000), le total de 50,4 M et les 48,7 M admis à voter (calculs vérifiés).
- Les sept taux d'inscription (entiers, sans décimale publiée), la parution du 11/03/2026, la Licence Ouverte 2.0.
- Notes 2 et 4 : exactes, avec des précisions proposées.

#### Points ouverts

- La mise à jour d'août 2026 du jeu (3 août sur data.gouv.fr) n'est pas expliquée par une source Insee. La période 15/03/2026 est très probablement le jour du scrutin, associé aux procurations. À vérifier dans les données Melodi.
- Aucun chiffre du ministère de l'Intérieur n'a pu être lu à la source (sauf le second tour de 2022).

### 9. URLs consultées (2026-11-02)

**Insee (HTML brut ou classeur lu directement)**
- https://www.insee.fr/fr/statistiques/8888278 (Focus 378, version française)
- https://www.insee.fr/fr/statistiques/fichier/8888278/if378.xlsx
- https://www.insee.fr/en/statistiques/8896480 (Focus 378, version anglaise)
- https://www.insee.fr/fr/statistiques/2389209 (« Inscrits sur les listes électorales, données annuelles 2026 »)
- https://www.insee.fr/fr/statistiques/fichier/2389209/cond-vie-soc-liste-elec.xlsx
- https://www.insee.fr/fr/statistiques/8276873?geo=DEP-37 (« Les électeurs en 2026 », note sur l'extraction)
- https://www.insee.fr/fr/statistiques/8192479 (Focus 328, mai 2024)
- https://www.insee.fr/fr/statistiques/fichier/8192479/if328.xlsx
- https://www.insee.fr/fr/statistiques/4317766 (Focus 186, février 2020)
- https://www.insee.fr/fr/statistiques/4134308 (Focus 154, mai 2019)
- https://www.insee.fr/fr/statistiques/7766966 (Insee Première 1986, mars 2024)
- https://www.insee.fr/fr/statistiques/6480276 (Focus 273, août 2022 : consulté, non utilisé dans les tableaux)
- https://www.insee.fr/fr/metadonnees/source/serie/s1046 (REU)
- https://www.insee.fr/fr/information/2008466 (mentions légales, licence)
- https://catalogue-donnees.insee.fr/fr/catalogue/recherche/DS_ELECTORAL (illisible : application JavaScript)

**Autres sources (résumés de page)**
- https://www.data.gouv.fr/datasets/caracteristiques-du-corps-electoral et /informations
- https://www.service-public.gouv.fr/particuliers/vosdroits/F1367 et /F1937
- https://www.conseil-constitutionnel.fr/decision/2022/2022197PDR.htm
- https://fr.wikipedia.org/wiki/Élections_européennes_de_2019_en_France
- https://fr.wikipedia.org/wiki/Élections_municipales_de_2020_en_France
- https://fr.wikipedia.org/wiki/Élection_présidentielle_française_de_2022
- https://fr.wikipedia.org/wiki/Élections_régionales_françaises_de_2021
- https://fr.wikipedia.org/wiki/Élections_départementales_françaises_de_2021
- https://fr.wikipedia.org/wiki/Élections_européennes_de_2024_en_France
- https://fr.wikipedia.org/wiki/Élections_municipales_de_2026_en_France
- https://www.banquedesterritoires.fr/municipales-combien-de-personnes-susceptibles-daller-voter-ce-dimanche

**Ministère de l'Intérieur**
- https://www.resultats-elections.interieur.gouv.fr/municipales2026/index.html : lu, recherche par commune seulement
- https://www.archives-resultats-elections.interieur.gouv.fr/ , https://www.elections.interieur.gouv.fr/ , https://www.interieur.gouv.fr/Elections : HTTP 403

**Non aboutis** : l'API data.gouv.fr (connexion coupée par le proxy), les pages Insee 6324351, 6324198 et 6324616 (404).

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
