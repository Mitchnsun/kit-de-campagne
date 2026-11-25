# `births` · Naissances et fécondité

**Vérifiée le 25/11/2026** : double vérification sur le web, sans écart non expliqué (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `births`, troisième volet de « Population » (`population`), dossier « Électorat » (`electorate`), page de type série, ticket #540 de l'app |
| Données | `briefings/data/births.json`, écrit par `yarn briefings births` le 2026-11-25 |
| Sources | Insee, « Bilan démographique 2025 » (Insee Première n° 2087, paru le 13/01/2026), https://www.insee.fr/fr/statistiques/8719824 ; séries de la BDM https://www.insee.fr/fr/statistiques/serie/001641590 et https://www.insee.fr/fr/statistiques/serie/001686832 ; Licence Ouverte 2.0 (comme les autres séries de l'Insee du kit) |
| Séries | `births` : naissances vivantes, France (Mayotte comprise à partir de 2014), BDM `001641590`, annuel, 1957 à 2025, 69 points, mise à jour du 29/10/2026 ; `fertilityRate` : indicateur conjoncturel de fécondité, France (Mayotte comprise à partir de 2014), BDM `001686832`, annuel, 1994 à 2025, 32 points, mise à jour du 19/01/2026, 2023 à 2025 provisoires. La BDM écrit l'ICF en enfants pour 100 femmes (156) : le script le divise par 100 (1,56), comme l'écrivent les publications de l'Insee. Les deux séries marquent une rupture en 2014 (entrée de Mayotte) |
| Chiffre clé | 643 905 naissances en 2025, en baisse (660 787 en 2024) ; l'ICF de 2025 à côté, 1,56 (provisoire) |
| Règles | Toutes les années de la BDM ; le script échoue sur un titre changé, une année manquante, une valeur hors bornes (400 000 à 1 200 000 naissances, 100 à 300 enfants pour 100 femmes), une année 2014 absente, ou deux séries qui ne finissent pas la même année |
| Première édition | La prochaine édition du kit |

## « À savoir »

1. 643 905 naissances en 2025 (BDM, mise à jour du 29/10/2026) ; le bilan démographique du 13/01/2026 en estimait 645 000 (« données définitives jusqu'en 2024 et estimées pour 2025 », page https://www.insee.fr/fr/statistiques/8721209). Le plus bas et le plus haut de la série (1971 : 916 370) sont lus dans `briefings/data/births.json`. Note : la recherche du 25/11/2026 avait annoncé le pic en 1964 (916 087) ; la série du fichier donne 1971, chiffre retenu.
2. La définition de l'ICF : note du fichier `3_ICF_age_moyen_femmes.xlsx` du bilan (tableaux https://www.insee.fr/fr/statistiques/8721207) ; la descendance finale d'une génération est un autre indicateur (fichier `4_Descendance_femmes.xlsx`, non repris).
3. 2,03 en 2010, le plus haut de la série, et 1,56 en 2025, le plus bas : lus dans `briefings/data/births.json` (BDM `001686832`).
4. Le champ : titres des deux séries (« France (inclus Mayotte à partir de 2014) ») ; les séries de la métropole commencent en 1901 (BDM `000067677` et `001686825`, fichiers du bilan).

## Double vérification

Faite le 25/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans passer par la BDM (rapport `dossiers2/A-series.md` de la session).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Naissances 2025 | 643 905 | 645 000 (estimation arrondie du 13/01/2026) | https://www.insee.fr/fr/statistiques/fichier/8721207/1_Naissances_tnat.xlsx | Écart expliqué : la BDM a été mise à jour le 29/10/2026 |
| Naissances 2025 | 643 905 | 644 343 | Eurostat `demo_gind`, `LBIRTH`, https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/demo_gind?format=JSON&lang=fr&geo=FR&indic_de=LBIRTH | Écart expliqué : 0,1 % ; l'Insee prévient que ses chiffres et ceux d'Eurostat peuvent différer |
| Naissances 2024 | 660 787 | 660 787 | Fichier du bilan, ci-dessus | Conforme |
| ICF 2024 | 1,61 | 1,61 | Eurostat `demo_find`, `TOTFERRT`, https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/demo_find?format=JSON&lang=fr&geo=FR&indic_de=TOTFERRT | Conforme |
| ICF 2025 | 1,56 (provisoire) | 1,56 (p) | Fichier `3_ICF_age_moyen_femmes.xlsx` du bilan | Conforme ; Eurostat n'a pas 2025 |
| ICF 2023 | 1,65 | 1,66 | Eurostat `demo_find` | Écart expliqué : 0,01, chiffres provisoires des deux côtés |

**Conclusion.** Les chiffres de la BDM concordent avec le bilan démographique et avec Eurostat, aux mises à jour près.

**Pages consultées** le 25/11/2026 : celles du tableau.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande : celle des autres séries de l'Insee du kit, non relue pour cette page.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
