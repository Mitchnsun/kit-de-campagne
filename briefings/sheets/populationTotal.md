# `populationTotal` · Population totale (partie de la page « Population »)

**Vérifiée le 16/11/2026** : les chiffres sont ceux de la série `population` de la pyramide des âges, doublement vérifiée le 02/11/2026 (fiche `populationPyramid.md`, section « Double vérification », point 1 et point 7) ; chaque année de 1991 à 2026 recoupée le 16/11/2026 avec le fichier de la pyramide interactive de l'Insee (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `populationTotal`, premier onglet (« Population totale ») de la page composite `population` (« Population »), dossier « Électorat » (`electorate`), page de type série, ticket #453 de l'app (décision du PO du 16/11/2026) ; l'autre onglet est la pyramide des âges, `populationPyramid` (« Pyramide ») |
| Données | `briefings/data/populationTotal.json`, écrit par `yarn briefings populationTotal` le 2026-11-16 |
| Sources | Insee, « Bilan démographique 2025 - Tableaux rétrospectifs », https://www.insee.fr/fr/statistiques/8721185 (en français seulement), parue le 13/01/2026 : POP5 `5_Pop1janv_grands_grages.xlsx`, onglet FR-Ensemble, colonne « Total » ; Licence Ouverte 2.0 |
| Séries | `population` : population au 1er janvier, France, POP5, annuel, 1991 à 2026, 36 points ; 2024 à 2026 provisoires (« (p) » de POP5) ; rupture de série en 2014 (`breaks`), l'entrée de Mayotte dans le champ |
| Chiffre clé | 69 081 996 habitants au 1er janvier 2026, provisoire (« 69,1 millions »), en hausse après 68 851 996 en 2025 (« 68,9 millions ») |
| Règles | Toutes les années de POP5, sans en écarter : les années provisoires gardent leur statut, que la page dit (« 2026 (provisoire) »). La rupture de 2014 est lue dans la note de POP5 (« Champ : France hors Mayotte jusqu'en 2013, France à partir de 2014 ») : le script échoue si la note change. La page l'appelle « entrée de Mayotte » dans le tableau (« 2014 (entrée de Mayotte) »), la marque sur la courbe avec la phrase de la rupture et écrit le champ sous la courbe ; la courbe s'ouvre sur toute la série, de 1991 à 2026, pour que la rupture se voie |
| Première édition | À remplir à la publication |

Quelques points : 1991 : 58 280 135 ; 1996 : 59 487 413 ; 2001 : 60 941 410 ; 2006 : 63 186 117 ; 2011 : 64 933 400 ; 2013 : 65 564 756 (France hors Mayotte) ; 2014 : 66 130 873 (France, Mayotte comprise) ; 2016 : 66 602 645 ; 2021 : 67 697 091 ; 2023 : 68 404 843 ; 2024 (p) : 68 638 377 ; 2025 (p) : 68 851 996 ; 2026 (p) : 69 081 996.

## « À savoir »

1. Les personnes qui résident en France au 1er janvier, toutes nationalités ; l'électorat est un autre ensemble (Insee Première n° 2087, https://www.insee.fr/fr/statistiques/8719824 ; Insee Focus n° 378 et n° 328 ; voir la fiche `populationPyramid.md`, note 1).
2. « Champ : France hors Mayotte jusqu'en 2013, France à partir de 2014 » (note de POP5 ; page 8331297 : « Mayotte, devenu un département d'outre-mer, est intégré au champ France à partir de l'année 2014 ») ; la hausse de 2014 (+566 117) compte aussi l'entrée de Mayotte, sans que la page en donne la part.
3. Le bilan démographique paraît chaque année en janvier (« Comme chaque année en janvier, l'Insee a publié le 13 janvier 2026 le bilan démographique », https://blog.insee.fr/france-2025-plus-de-deces-que-de-naissances/) ; « Données provisoires arrêtées à fin 2025 » pour 2024 à 2026 (page 5225246) ; révision constatée : le 1er janvier 2025 valait 68 605 616 en novembre 2025 et vaut 68 851 996 dans le bilan 2025.

## Double vérification

Les chiffres de ce fichier sont ceux de la série `population` du fichier `populationPyramid` du 02/11/2026, à l'identique : sa double vérification (agent Claude, modèle Sonnet, 02/11/2026, sur le web, sans relire POP5) a trouvé conformes les totaux de 1991, 2006, 2024, 2025 et 2026 (Melodi, Insee Première n° 2087, `demo-pop-france.xlsx`) et la rupture de 2014 (65 564 756 en 2013, 66 130 873 en 2014). Le 16/11/2026, chaque année de 1991 à 2026 a en plus été recoupée par une session Claude avec la somme des âges du fichier de la pyramide interactive de l'Insee (`https://www.insee.fr/fr/outil-interactif/5014911/data/FR/donnees_pyramide_act.csv`) :

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, 2026 | 69 081 996 | 69 081 996 ; 69 082 milliers « p » | CSV de l'outil ; Insee Première n° 2087 (double vérification du 02/11/2026) | Conforme |
| 34 années de 1991 à 2026, hors 1994 et 2022 | (le fichier) | identiques à l'unité | CSV de l'outil | Conforme |
| 1994 | 59 070 077 | 59 109 616 dans le CSV de l'outil (+39 539) | CSV de l'outil | Écart expliqué : une ligne du CSV de l'outil, les femmes de 99 ans ou plus de 2022 (39 539), porte l'année 1994 (voir `populationPyramid.md`, « Mises à jour ») |
| 2022 | 68 060 207 | 68 020 668 dans le CSV de l'outil (-39 539) | CSV de l'outil | Écart expliqué : la même ligne, absente de 2022 ; 68 060 207 = 68 020 668 + 39 539 |
| Rupture de 2014 | 2013 : 65 564 756 ; 2014 : 66 130 873 | les mêmes | CSV de l'outil ; Melodi (double vérification du 02/11/2026) | Conforme |

**Conclusion.** Aucun écart non expliqué ; une seconde vérification sur le web de la série entière reste à faire pour l'édition.

**Pages consultées** le 16/11/2026 : le fichier de l'outil ci-dessus ; la page de l'outil, https://www.insee.fr/fr/outil-interactif/5014911/pyramide.htm.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
