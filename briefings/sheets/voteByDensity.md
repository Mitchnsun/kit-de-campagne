# `voteByDensity` · Le vote de 2022 selon la densité

**Vérifiée le 15/11/2026** : double vérification sur le web, sans écart non expliqué (section « Double vérification ») ; le calcul est refait au centième par un second agent, à partir des fichiers téléchargés de nouveau. C'est un **calcul du jeu**, pas une publication de l'Insee ni du ministère : la page et le premier « À savoir » le disent.

| Champ | Valeur |
| --- | --- |
| Indicateur | `voteByDensity`, dossier « Électorat » (`electorate`), après « Scrutins passés », page de type scrutin (`chart: 'election'`, chaque niveau un tour, sans carte), nature « scrutin historique » : les candidats sont nommés sous « Donnée réelle · scrutin historique » (décision du PO du 16/11/2026), ticket #446 de l'app |
| Données | `briefings/data/voteByDensity.json`, écrit par `yarn briefings voteByDensity` le 2026-11-16 |
| Sources | (1) Ministère de l'Intérieur, data.gouv.fr, « Données des élections agrégées », https://www.data.gouv.fr/datasets/donnees-des-elections-agregees, les deux fichiers Parquet de la page « Scrutins passés » (`general_results.parquet`, `candidats_results.parquet`, `Last-Modified` 2026-04-05), `id_election` `2022_pres_t1` et `2022_pres_t2`, colonne `code_commune` ; Licence Ouverte 2.0. (2) Insee, « La grille de densité 2025 », https://www.insee.fr/fr/information/8571524 (en français seulement), le fichier diffusé dans la géographie du scrutin : `fichier_diffusion_2022.xlsx`, onglet « Maille communale », en-tête « Grille de densité 2025 / Mise en ligne le 21/07/2025 Géographie au 01/01/2022 », colonnes `CODGEO`, `DENS`, `LIBDENS`, `DENS7`, `LIBDENS7`, `PMUN19` ; 34 955 communes ; Licence Ouverte 2.0 (règle générale du site, voir la fiche `urbanRural`) |
| Séries | La participation au 1er tour (votants / inscrits, en %, deux décimales) dans chacun des trois niveaux, un point 2022 : `turnoutDense` 73,53 ; `turnoutIntermediate` 73,33 ; `turnoutRural` 78,54. Identifiant du producteur : `2022_pres_t1` |
| Scrutins | `elections`, 20 tours, dans l'ordre de la page : les trois niveaux (`DENS`) au 1er puis au 2d tour, puis les sept niveaux (`DENS7`) au 1er puis au 2d tour. Chacun porte sa portée (`scope` : la variable de l'Insee et l'identifiant du niveau dans l'app, `dense`, `rural`, `largeUrbanCentres`…), ses inscrits, votants, blancs, nuls et exprimés, chaque candidat (prénom et nom tels que le ministère les écrit, numéro de panneau, voix, famille du jeu de la table de #246) ; pas de candidat en tête par département (`leaders` absent : Paris n'a ni commune intermédiaire ni rurale) |
| Chiffre clé | 78,54 % de participation au 1er tour de 2022 dans les communes rurales, sans tendance (un seul scrutin) ; à côté, 73,53 % dans les communes urbaines denses |
| Règles | Somme des bureaux par commune, appariement par code commune avec la grille en géographie 2022, somme par niveau des inscrits, votants, blancs, nuls, exprimés et voix ; parts sur les exprimés du niveau, participation = votants / inscrits. Le script s'arrête : si l'en-tête ne dit plus « Grille de densité 2025 » ou « Géographie au 01/01/2022 » ; si une paire de niveaux diffère de `LEVELS` et `LEVELS_7` (`urbanRural.ts`) ou si un niveau à 7 postes n'est pas dans le sien à 3 ; si une commune à résultats sans niveau est d'un des 101 départements, ou si un code sans niveau n'est ni de l'étranger (`ZZ`) ni des collectivités (975, 977, 978, 986, 987, 988) ; si une commune habitée de la grille n'a pas de résultat ; si inscrits des niveaux + hors niveau ≠ inscrits du tour, pour chacune des deux grilles ; si les comptes d'un niveau ne s'additionnent pas ; si les voix d'un niveau ne font pas exactement ses exprimés. Fichier de 2022 et non celui de 2026 avec la table de passage : trois communes de 2022 scindées depuis (`15141`, `60054`, `85084`) resteraient sans niveau |
| Première édition | À remplir à la publication |

## Ce que donne le fichier

Hors niveau (la sortie du script) : au 1er tour, 1 899 082 personnes inscrites sur 48 747 876 (3,90 %) : Français de l'étranger (`ZZ`) 1 435 746, Nouvelle-Calédonie (988) 218 773, Polynésie française (987) 205 576, Saint-Martin (978) 19 147, Wallis-et-Futuna (986) 9 528, Saint-Barthélemy (977) 5 267, Saint-Pierre-et-Miquelon (975) 5 045. Au 2d tour, 1 891 256 sur 48 752 339 (3,88 %). Les communes à résultats des 101 départements ont toutes un niveau ; six communes de la grille sans résultat sont les villages de la Meuse « morts pour la France », sans habitant.

**1er tour, 3 niveaux** (% des exprimés du niveau) :

| | Urbain dense | Urbain intermédiaire | Rural |
| --- | --- | --- | --- |
| Inscrits (part des inscrits dans un niveau) | 15 039 237 (32,10 %) | 14 919 950 (31,85 %) | 16 889 607 (36,05 %) |
| Votants, blancs, nuls | 11 058 852 ; 148 759 ; 58 818 | 10 941 498 ; 167 966 ; 79 379 | 13 265 867 ; 220 200 ; 104 057 |
| Exprimés | 10 851 275 | 10 694 153 | 12 941 610 |
| Participation | 73,53 % | 73,33 % | 78,54 % |
| Macron | 29,03 | 27,25 | 26,55 |
| Le Pen | 15,10 | 25,43 | 28,76 |
| Mélenchon | 29,58 | 20,79 | 16,61 |
| Zemmour | 7,37 | 7,23 | 6,62 |
| Pécresse | 5,02 | 4,48 | 4,82 |
| Jadot | 5,58 | 4,38 | 3,93 |
| Lassalle | 1,82 | 2,88 | 4,54 |
| Roussel | 2,11 | 2,39 | 2,43 |
| Dupont-Aignan | 1,54 | 2,10 | 2,48 |
| Hidalgo | 1,74 | 1,75 | 1,74 |
| Poutou | 0,66 | 0,74 | 0,88 |
| Arthaud | 0,44 | 0,57 | 0,66 |

Par famille (table de #246, calcul sur les voix) : Gauche radicale 31,68 / 23,18 / 19,03 ; Centre 29,03 / 27,25 / 26,55 ; Extrême droite 22,47 / 32,67 / 35,37 ; Écologie 5,58 / 4,38 / 3,93 ; Droite 5,02 / 4,48 / 4,82 ; Sans étiquette 1,82 / 2,88 / 4,54 ; Social-démocratie 1,74 / 1,75 / 1,74 ; Droite souverainiste 1,54 / 2,10 / 2,48 ; Extrême gauche 1,10 / 1,31 / 1,54. (La recherche, qui additionnait les pourcentages arrondis des candidats, donnait 22,47 / 32,66 / 35,38 pour l'extrême droite et 31,69 / 23,18 / 19,04 pour la gauche radicale.)

**2d tour, 3 niveaux** : participation 69,47 % / 72,13 % / 77,83 % ; Macron 69,81 / 55,00 / 51,20 ; Le Pen 30,19 / 45,00 / 48,80 (inscrits 15 045 020 / 14 923 890 / 16 892 173).

**7 niveaux** :

| Niveau `DENS7` | Inscrits | Particip. T1 | Macron · Le Pen · Mélenchon (T1) | Particip. T2 | Le Pen (T2) |
| --- | --- | --- | --- | --- | --- |
| Grands centres urbains | 15 039 237 | 73,53 | 29,03 · 15,10 · 29,58 | 69,47 | 30,19 |
| Centres urbains intermédiaires | 6 510 485 | 70,92 | 26,10 · 24,90 · 23,22 | 69,37 | 44,68 |
| Petites villes | 3 149 983 | 74,22 | 27,26 · 26,52 · 19,05 | 73,35 | 46,32 |
| Ceintures urbaines | 5 259 482 | 75,80 | 28,59 · 25,42 · 18,99 | 74,82 | 44,59 |
| Bourgs ruraux | 7 706 027 | 77,28 | 27,76 · 28,37 · 16,78 | 76,63 | 47,44 |
| Rural à habitat dispersé | 7 800 980 | 79,56 | 25,82 · 29,57 · 16,27 | 78,85 | 50,05 |
| Rural à habitat très dispersé | 1 382 600 | 79,89 | 24,09 · 26,29 · 17,53 | 78,74 | 49,20 |

Les inscrits du 1er tour. Les « grands centres urbains » sont exactement l'urbain dense, et les sept niveaux s'emboîtent dans les trois (contrôle du script).

## Choix

- **Candidats nommés, un `ElectionRound` par niveau** (décision du PO du 16/11/2026) : la page lit chaque niveau comme un tour de la page « Scrutins passés », par candidat ou par famille, sous « Donnée réelle · scrutin historique » ; les noms ne sont que dans ce fichier. Pas de carte : un niveau est réparti sur tout le pays.
- **Le fichier en géographie 2022**, pas celui de 2026 de `urbanRural` : l'Insee diffuse la même grille (recensement de 2021) dans la géographie du scrutin, et 34 855 des 34 863 communes présentes dans les deux fichiers ont les mêmes niveaux ; avec le fichier de 2026 et la table de passage, trois communes scindées depuis resteraient sans niveau. Ne pas confondre avec « La grille de densité 2022 » (Fideli 2018), un autre classement.
- **Parts pondérées par les voix** : sur les exprimés du niveau, où Paris pèse ses exprimés. Une moyenne des communes donne d'autres chiffres pour la même réalité (voir la double vérification).
- **Le bureau des personnes détenues** (`75056_JUS1`, 13 673 inscrits et 10 740 votants au 1er tour) compte à Paris, en urbain dense : moins de 0,1 % des inscrits du niveau. C'est le « bureau de vote unique situé place Vendôme à Paris, au sein du ministère de la justice » où votent par correspondance les personnes détenues de toute la France (vérifié le 16/11/2026, voir plus bas).
- **Jamais les facteurs du moteur** (`TERRITORY_SKEW`, valeur cachée, #145) : la page montre la réalité, pas les ordres de grandeur du jeu, et rien ne les met côte à côte.
- **Dans le jeu** (décision du PO du 16/11/2026) : sur l'écran des actions « Terrain » et « Meeting », une fois « Villes » ou « Campagnes » choisi, une seconde ligne sous la part des habitants (`urbanRural`) donne la participation au 1er tour de 2022 dans les communes du territoire, dite « calcul du jeu à partir des résultats officiels », avec les deux sources de ce fichier, jamais un nom de candidat. « Villes » est l'urbain dense et l'urbain intermédiaire réunis, comme pour la part des habitants : l'app additionne les votants et les inscrits des deux niveaux (11 058 852 + 10 941 498 = 22 000 350 votants pour 15 039 237 + 14 919 950 = 29 959 187 inscrits, 73,43 %, écrit « 73,4 % ») ; « Campagnes » est le niveau rural (78,54 %, écrit « 78,5 % » : le chiffre clé de la page). Ces chiffres viennent des tours de ce fichier, sans nouvelle donnée. Son aperçu montre la participation des trois niveaux au 1er tour, sans candidat, et ouvre la page sur le niveau (urbain dense pour les villes).

## « À savoir »

1. Calcul du jeu : #446 ; la méthode ci-dessus ; « diffusée dans la géographie du scrutin » : en-tête du fichier (« Géographie au 01/01/2022 »). Pondération : la double vérification (Brookes, moyenne des communes).
2. 1 899 082 inscrits hors niveau, 3,9 % : la sortie du script (ci-dessus), identique à la double vérification. Le bureau unique des personnes détenues : Sénat, rapport n° 433 (2024-2025) de M. Louis Vogel sur la proposition de loi relative au droit de vote par correspondance des personnes détenues, enregistré le 12/03/2025 (https://www.senat.fr/rap/l24-433/l24-4331.pdf, page 7 du PDF : « Des modalités spécifiques de vote par correspondance ont été mises en place pour l'élection présidentielle de 2022 avec un bureau de vote unique situé place Vendôme à Paris, au sein du ministère de la justice ») ; ministère de la Justice, « Présidentielle 2022 : large participation des personnes détenues », publié le 29/04/2022 (https://www.justice.gouv.fr/node/1213 : « Plus de 10.000 personnes détenues ont voté au premier et au second tour », « au bureau de vote unique situé au siège du ministère de la Justice, place Vendôme »). Que `75056_JUS1` soit ce bureau se déduit de son identifiant (« JUS », la commune de Paris) et de ses 10 740 votants, cohérents avec les « plus de 10.000 » du ministère.
3. 36 % des inscrits dans un niveau (16 889 607 sur 46 848 794, ci-dessus) ; 32 % des habitants : la page « Urbain et rural » (`urbanRural`, 32,1 % de la population municipale de 2023 dans une commune rurale, grille 2025, géographie 2026). Les deux chiffres n'ont ni la même année ni la même géographie : la note dit « des inscrits, pas des habitants », sans les soustraire.
4. L'emboîtement des sept niveaux dans les trois : définition de l'Insee (c2343), reprise par `LEVELS_7` dans l'app et contrôlée par le script.

## Double vérification

Double vérification sur le web par un agent Claude (modèle Sonnet), 15/11/2026 : téléchargements et calcul refaits sans réutiliser les fichiers ni les scripts de la recherche (somme des bureaux par commune, `2022_pres_t1`, 69 682 bureaux, 35 245 communes, appariement avec `fichier_diffusion_2022.xlsx`, 34 955 communes : 701 / 3 584 / 30 670 aux niveaux 1 / 2 / 3).

| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
| --- | --- | --- | --- | --- |
| Inscrits (dense / intermédiaire / rural) | 15 039 237 / 14 919 950 / 16 889 607 | Identiques | Calcul refait sur les données agrégées et la grille | Conforme |
| Participation, 1er tour | 73,53 / 73,33 / 78,54 | Identiques | Idem | Conforme |
| Exprimés | 10 851 275 / 10 694 153 / 12 941 610 | Identiques | Idem | Conforme |
| Macron, Le Pen, Mélenchon, Zemmour | 29,03 / 27,25 / 26,55 ; 15,10 / 25,43 / 28,76 ; 29,58 / 20,79 / 16,61 ; 7,37 / 7,23 / 6,62 | Identiques | Idem | Conforme |
| Hors niveau | 1 899 082 (3,90 % de 48 747 876) | Identique : `ZZ` 1 435 746 ; 988 218 773 ; 987 205 576 ; 978 19 147 et 977 5 267 ; 975 5 045 ; 986 9 528 | Idem | Conforme |
| Paris, Lyon, Marseille | Communes entières, urbain dense | `75056`, `69123`, `13055` : niveau 1, une commune chacune | Grille | Conforme |
| Bureau `75056_JUS1` | Compté à Paris | 13 673 inscrits, 10 740 votants, compté à Paris (niveau 1) ; sa nature laissée ouverte par la vérification, vérifiée ensuite (ci-dessous) | Données agrégées | Conforme |
| Participation, France entière | 73,69 % (« Scrutins passés ») | 35 923 707 / 48 747 876 = 73,69 % | Données agrégées | Conforme |
| Licence de l'Insee | Licence Ouverte 2.0 | La page de la grille n'en porte pas (ni à la lecture du 15/11, ni à celle du 16/11/2026) ; règle générale des mentions légales du site, voir la fiche `urbanRural` | https://www.insee.fr/fr/information/8571524 ; https://www.insee.fr/fr/information/2008466 | Conforme (règle générale du site) |
| Recoupement hors du calcul : K. Brookes (UGA), « Zones rurales contre zones urbaines : deux France s'opposent-elles vraiment dans les urnes ? », The Conversation | Parts pondérées par les voix : urbain dense 29,03 / 15,10 / 29,58 (Macron, Le Pen, Mélenchon) | Figure 1, moyenne non pondérée des communes, catégories de l'ANCT : urbain dense 29 / 19 / 27 ; urbain intermédiaire 28 / 27 / 18. Refait par la recherche avec la même méthode sur la grille 2025 : 28,5 / 18,6 / 27,4 et 27,7 / 26,9 / 18,5. Texte de l'article (sans chiffres) : « La candidate du RN a obtenu ses meilleurs scores dans les communes rurales » | https://theconversation.com/zones-rurales-contre-zones-urbaines-deux-france-sopposent-elles-vraiment-dans-les-urnes-189609 | Écart expliqué (méthode : moyenne des communes contre somme des voix ; même sens). Date de l'article : 30/08 ou 01/09/2022, non tranchée ; valeurs de la figure non relues par la vérification |

Aucune publication de l'Insee, du CEVIPOF, de la Fondation Jean-Jaurès ou des décodeurs du Monde ne donne ce croisement avec la grille 2025 (recherches du 15/11/2026) : le calcul n'a pas d'équivalent publié à comparer, d'où le « calcul du jeu ».

**Vérification ajoutée le 16/11/2026** (au-delà de la recherche, pour l'« À savoir » 2) : le bureau unique des personnes détenues, place Vendôme : Sénat, rapport n° 433 (2024-2025), https://www.senat.fr/rap/l24-433/l24-4331.pdf, lu (texte extrait du PDF) ; ministère de la Justice, https://www.justice.gouv.fr/node/1213, lu (« Publié le 29 avril 2022 ») ; la page du ministère du 10/03/2022 (https://www.justice.gouv.fr/actualites/actualite/comment-sorganise-droit-vote-personnes-detenues) décrit le vote par correspondance sans parler du dépouillement. À revérifier par la seconde vérification.

**Conclusion.** Le calcul est reproduit au centième ; le seul recoupement publié (une moyenne des communes) diffère par sa méthode et va dans le même sens.

**Pages consultées** le 15/11/2026 : https://www.insee.fr/fr/information/8571524 et le fichier `fichier_diffusion_2022.xlsx` ; les deux fichiers Parquet des données agrégées ; l'article de The Conversation. Le 16/11/2026 : la page de l'Insee (licence), le rapport du Sénat et les deux pages du ministère de la Justice ci-dessus.

## Mises à jour

- **16/11/2026** : la participation de chaque territoire du jeu, lue dans ce fichier par l'app (section « Choix »). Le fichier ne change pas.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script (calcul refait par un second agent ; pas de publication équivalente).
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande : Licence Ouverte 2.0 pour les données agrégées (page du jeu de données) et pour la grille (règle générale du site de l'Insee, « Source : Insee »).
- [x] Aucune donnée interne du jeu (ni `TERRITORY_SKEW`, ni autre facteur du moteur), aucun sondage d'intention de vote pour 2027.
