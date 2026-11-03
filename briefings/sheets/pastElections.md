# `pastElections` · Scrutins passés

**Non vérifiée** : double vérification sur le web à faire (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `pastElections`, dossier « Électorat » (`electorate`), repris dans « Institutions », page de type scrutin, ticket #33 de l'app (statut `planned` : les chiffres et la fiche avant la page). Vrais noms des candidats et des listes : sur cette page seulement, sous « Donnée réelle · scrutin historique » |
| Données | `briefings/data/pastElections.json`, écrit par `yarn briefings pastElections` le 2026-11-03 |
| Sources | Ministère de l'Intérieur, data.gouv.fr, « Données des élections agrégées », https://www.data.gouv.fr/datasets/donnees-des-elections-agregees : les résultats définitifs du ministère par bureau de vote, toutes les élections depuis 1999, en deux fichiers Parquet, `general_results.parquet` (inscrits, votants, abstentions, blancs, nuls, exprimés) et `candidats_results.parquet` (voix de chaque candidat ou liste, nuance, nom, titre de liste), servis par https://object.files.data.gouv.fr/data-pipeline-open/elections/ ; mis à jour le 2026-04-05 (`Last-Modified` des deux fichiers) ; Licence Ouverte 2.0 ; en français seulement |
| Séries | La participation (votants / inscrits, en %, deux décimales) de chaque tour, un point chacune : `presidentialRound1` (2022) 73,69 ; `presidentialRound2` (2022) 71,99 ; `legislativeRound1` (2024) 66,71 ; `european` (2024) 51,49. Identifiant du producteur : l'`id_election` des données agrégées (`2022_pres_t1`, `2022_pres_t2`, `2024_legi_t1`, `2024_euro_t1`) |
| Scrutins | `elections`, dans l'ordre du sélecteur de la page : pour chaque tour, la France entière (outre-mer et Français de l'étranger compris), ses inscrits, votants, blancs, nuls et exprimés ; chaque candidat (prénom et nom, numéro de panneau), liste (titre, numéro de panneau, nuance) ou, aux législatives, nuance, avec ses voix et sa famille du jeu (table du PO du 25/10/2026, `briefings/families.ts` dans l'app) ; le candidat, la liste ou la nuance en tête dans chacun des 101 départements |
| Chiffre clé | 73,69 % de participation au 1er tour de la présidentielle de 2022, sans tendance (un seul point) |
| Règles | Quatre tours, ceux du sélecteur de #33 (le 2d tour des législatives de 2024 est écarté : il n'a eu lieu que dans une partie des circonscriptions, voir « Choix ») ; une famille pour chaque candidat, nuance ou liste, sinon le script s'arrête ; ZA, ZB, ZC, ZD et ZM deviennent 971 à 974 et 976 ; les autres codes Z (collectivités d'outre-mer, Français de l'étranger) et les codes 975, 977, 978, 986 à 988 restent dans les totaux, hors de la carte ; un département sans résultat ou à égalité en tête arrête le script ; les comptes de chaque tour doivent s'additionner (inscrits − votants = abstentions ; blancs + nuls + exprimés = votants), et les voix des candidats donner les exprimés à 1 pour 100 000 près (`CAST_GAP`) |
| Première édition | À remplir à la publication |

## Ce que donne le fichier

| Tour | Inscrits | Votants | Blancs | Nuls | Exprimés | Participation |
| --- | --- | --- | --- | --- | --- | --- |
| Présidentielle 2022, 1er tour (10/04) | 48 747 876 | 35 923 707 | 543 609 | 247 151 | 35 132 947 | 73,69 % |
| Présidentielle 2022, 2d tour (24/04) | 48 752 339 | 35 096 478 | 2 233 904 | 805 249 | 32 057 325 | 71,99 % |
| Législatives 2024, 1er tour (30/06) | 49 332 709 | 32 908 657 | 582 908 | 267 803 | 32 057 946 | 66,71 % |
| Européennes 2024 (09/06) | 49 462 981 | 25 470 472 | 346 240 | 370 459 | 24 753 773 | 51,49 % |

- **Présidentielle 2022, 1er tour** (% des exprimés) : Macron 9 783 058 (27,85) ; Le Pen 8 133 828 (23,15) ; Mélenchon 7 712 520 (21,95) ; Zemmour 2 485 226 (7,07) ; Pécresse 1 679 001 (4,78) ; Jadot 1 627 853 (4,63) ; Lassalle 1 101 387 (3,13) ; Roussel 802 422 (2,28) ; Dupont-Aignan 725 176 (2,06) ; Hidalgo 616 478 (1,75) ; Poutou 268 904 (0,77) ; Arthaud 197 094 (0,56). Par famille : Gauche sociale 25,56 ; Écologie 4,63 ; Social-démocratie 1,75 ; Centre 27,85 ; Droite 4,78 ; Droite nationale 32,29 ; Sans étiquette 3,13. En tête : Macron dans 49 départements, Le Pen dans 42, Mélenchon dans 10.
- **Présidentielle 2022, 2d tour** : Macron 18 768 639 (58,55) ; Le Pen 13 288 686 (41,45). En tête : Macron dans 73 départements, Le Pen dans 28.
- **Législatives 2024, 1er tour**, par nuance (22 des 24 nuances de la grille ; REN et MDM n'apparaissent pas dans les résultats) : RN 9 379 092 (29,26) ; UG 8 971 581 (27,99) ; ENS 6 425 707 (20,04) ; LR 2 106 166 (6,57) ; UXD 1 251 125 (3,90) ; DVD 1 172 482 (3,66) ; DVG 490 898 (1,53) ; DVC 391 423 (1,22) ; EXG 366 594 (1,14) ; REG 334 372 (1,04) ; REC 238 934 (0,75) ; HOR 231 667 (0,72) ; ECO 182 478 (0,57) ; UDI 163 072 (0,51) ; DIV 142 871 (0,45) ; DSV 90 110 (0,28) ; EXD 59 679 (0,19) ; SOC 29 242 (0,09) ; RDG 12 434 (0,04) ; FI 12 224 (0,04) ; COM 3 125 (0,01) ; VEC 2 668 (0,01). Par famille : Gauche sociale 29,18 ; Écologie 0,58 ; Social-démocratie 1,66 ; Centre 21,99 ; Droite 10,74 ; Droite nationale 34,37 ; Sans étiquette 1,49. En tête : RN dans 55 départements, UG 29, ENS 8, REG 3, DVD 2, UXD 2, LR 1, DVG 1.
- **Européennes 2024**, 38 listes : n° 5 « La France revient ! » (LRN) 7 765 936 (31,37) ; n° 11 « Besoin d'Europe » (LENS) 3 614 646 (14,60) ; n° 27 « Réveiller l'Europe » (LUG) 3 424 216 (13,83) ; n° 4 « La France insoumise - Union populaire » (LFI) 2 448 703 (9,89) ; n° 18 (LLR) 1 794 171 (7,25) ; n° 6 « Europe Écologie » (LVEC) 1 361 883 (5,50) ; n° 3 « La France fière » (LREC) 1 353 127 (5,47) ; n° 33 (LCOM) 584 067 (2,36) ; n° 29 « Alliance rurale » (LDVD) 582 901 (2,35) ; les 29 autres listes sous 2,1 %. Par famille : Gauche sociale 12,93 ; Écologie 7,77 ; Social-démocratie 13,89 ; Centre 14,60 ; Droite 7,25 ; Droite nationale 37,79 ; Sans étiquette 5,78 (les totaux du PO dans #33, à la décimale près). En tête : la liste n° 5 dans 96 départements, la n° 4 dans 3 (Seine-Saint-Denis, Val-de-Marne, Martinique), la n° 27 à Paris, la n° 11 dans les Hauts-de-Seine.

## Choix

- **La source.** #33 conseille les Parquet des données agrégées pour un instantané hors ligne. Les fichiers « France entière » et « département » du ministère sur data.gouv.fr n'ont pas pu être lus le 03/11/2026 : `www.data.gouv.fr` et `static.data.gouv.fr` coupaient les connexions depuis l'environnement du script, alors que `object.files.data.gouv.fr`, qui sert les données agrégées, répondait. Les sites du ministère refusent les scripts (403). Le script lit les fichiers par plages HTTP : seulement les colonnes utiles, dans les groupes de lignes dont les statistiques contiennent l'un des quatre tours (une quarantaine sur 250).
- **Les noms.** Tels que le producteur les écrit : prénom et nom des candidats de 2022 (« Emmanuel MACRON »), titre complet de chaque liste de 2024 (`libelle_etendu_liste` : « LA FRANCE REVIENT ! AVEC JORDAN BARDELLA ET MARINE LE PEN »), code de chaque nuance aux législatives (« UG ») ; la page nommera les nuances. Les données agrégées n'ont ni le nom des têtes de liste (colonne vide en 2024), ni le parti des candidats à la présidentielle, ni le libellé des nuances.
- **Le 2d tour des législatives de 2024** n'est pas repris : #33 ne le met pas dans le sélecteur, et il n'a eu lieu que dans une partie des circonscriptions (61 615 bureaux sur 70 102 dans les données agrégées) ; ses totaux ne se comparent pas à ceux d'un tour national.
- **Les anomalies de la source, gardées telles quelles.** Un bureau des européennes (`78311_0013`) compte −1 bulletin nul (895 votants, 2 blancs, 894 exprimés) : les totaux restent la somme des bureaux, et le script le signale. Aux législatives, dans cinq bureaux (`16029_0001`, `27322_0001`, `34316_0001`, `75056_0521`, `75056_0522`), les voix des candidats ne font pas les exprimés : au total, 32 057 944 voix pour 32 057 946 exprimés, d'où la tolérance de 1 pour 100 000 du lecteur de l'app. Aux législatives, les résultats par candidat codent l'outre-mer en codes de l'Insee (971 à 976, 986 à 988), les résultats généraux en codes Z : le script lit les deux.

## « À savoir »

1. Résultats définitifs du ministère, additionnés par bureau de vote ; à la présidentielle, les résultats proclamés par le Conseil constitutionnel font foi (point d'attention de #33). La décision n° 2022-195 PDR (1er tour) donne 35 132 947 suffrages exprimés et 73,69 % de participation, comme le fichier (copie de la préfecture du Territoire de Belfort citée dans #33 : https://www.territoire-de-belfort.gouv.fr/contenu/telechargement/28593/204221/file/D%C3%A9cision%20du%20conseil%20constitutionnel.pdf). Les Français de l'étranger et les collectivités d'outre-mer sont dans les totaux, pas sur la carte (#33). Source : #33.
2. Participation et suffrages exprimés : définitions du ministère (colonnes `votants`, `inscrits`, `exprimes`, `blancs`, `nuls` des données agrégées). Le regroupement par famille est un choix éditorial : #33, « Familles politiques : ce que disent les sources », et `briefings/families.ts` dans l'app.
3. Les 24 nuances des législatives de 2024 et les trois nuances d'alliance (UG, ENS, UXD) : instruction du 11/06/2024 (NOR IOMA2415630C), grille reprise par la préfecture du Calvados (https://calvados.gouv.fr/contenu/telechargement/24610/181062/file/Annexe%201-Grille%20nuance%20-l%C3%A9gislatives%202024.pdf) ; la composition de l'UG et le rangement en Gauche sociale : décision du PO du 25/10/2026 (#33).
4. Les quatre listes qui ne suivent pas leur nuance (n° 16, 27, 29, 31) : décision du PO du 25/10/2026 (#33), `EUROPEAN_2024_LISTS` dans l'app.

## Double vérification

À faire : recouper sur le web, sans passer par les données agrégées, les comptes des quatre tours, les voix des candidats et des listes principales (Conseil constitutionnel pour la présidentielle, résultats du ministère pour les législatives et les européennes) et quelques départements en tête ; vérifier la licence et les sources des « À savoir ».

## Mises à jour

Aucune.

## Relecture

- [ ] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [ ] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [ ] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
