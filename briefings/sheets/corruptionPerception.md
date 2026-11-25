# `corruptionPerception` · La corruption perçue (saisie à la main)

**Vérifiée le 25/11/2026** : chaque valeur lue dans le classeur de Transparency International ; double vérification ci-dessous.

| Champ | Valeur |
| --- | --- |
| Indicateur | `corruptionPerception`, dossier « Institutions » (`institutions`), page de type série, demande du PO du 25/11/2026 |
| Données | `briefings/manual/corruptionPerception.json`, saisi à la main le 2026-11-25 |
| Sources | Transparency International, Corruption Perceptions Index 2025 (publié le 10/02/2026, « EMBARGOED UNTIL 10.02.2026 »), https://www.transparency.org/fr/cpi/2025, classeur https://images.transparencycdn.org/images/CPI2025_Results.xlsx (feuilles « CPI Timeseries 2012 - 2025 », « CPI 2025 Regional Averages », « Significant Changes since 2012 », « CPI2025 ») et note de méthode (CPI-2025-Methodology.zip). Licence CC BY-ND 4.0 : la FAQ demande de créditer « CONTENT TITLE (YEAR) by Transparency International is licensed under CC-BY-ND 4.0 » avec un lien, sans remanier le contenu ; les notes sont reprises telles quelles |
| Séries | `france` : note de la France sur 100, 2012-2025, 14 points ; `westernEurope` : moyenne de la région « WE/EU » (Europe de l'Ouest et Union européenne, 31 pays en 2025), 2016-2025, au centième, comme le classeur la donne (entière de 2023 à 2025) |
| Chiffre clé | 66 sur 100 en 2025, en baisse (67 en 2024) |
| Règles | Depuis 2012 seulement : la note de méthode et la FAQ disent les notes d'avant 2012 non comparables. La moyenne régionale avant 2016 n'est pas dans le classeur |
| Première édition | La prochaine Release qui suit le merge de la PR de l'app |

## « À savoir »

1. Une perception, pas un décompte : page de l'indice (« perceived levels of public sector corruption ») et note de méthode (enquêtes auprès d'experts et de dirigeants d'entreprise).
2. 27e sur 182, 66 sur 100, plus basse note depuis 2012, « Decliner », −6 depuis 2022 : feuilles « CPI2025 » (rang 27, 182 pays et territoires), « CPI Timeseries » et « Significant Changes since 2012 » (« -6 since 2022 », « Decliner »).
3. Comparables depuis 2012 seulement : FAQ (« Only CPI results from 2012 onwards can be compared ») et note de méthode.

## Double vérification

Faite le 25/11/2026 par un agent Claude (modèle Sonnet) qui a décompressé le classeur (format OOXML strict) et lu sa note de méthode.

| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 66 (2025) | 66, rang 27 sur 182 | « CPI Timeseries », D84 ; « CPI2025 », E31 | Conforme |
| `france` 2012-2025 | 14 valeurs | 14 valeurs identiques | « CPI Timeseries », ligne 84 | Conforme |
| `westernEurope` 2016-2025 | 10 valeurs | identiques au centième ; entières en 2023-2025 dans le classeur | « CPI 2025 Regional Averages », ligne 10 | Conforme |
| −6 depuis 2022, « Decliner » | — | « -6 since 2022 », « Decliner » | « Significant Changes since 2012 », ligne 18 | Conforme |
| Publication | 10/02/2026 | « EMBARGOED UNTIL 10.02.2026 » | classeur | Conforme |
| Licence | CC BY-ND 4.0 | « Creative Commons Attribution-NoDerivs 4.0 » | FAQ | Conforme |

**Conclusion.** Toutes les valeurs conformes ; la moyenne régionale a une précision inégale (entière de 2023 à 2025), reprise telle quelle.

## Mises à jour

Aucune.

## Relecture

- [x] Le chiffre clé et chaque point de la série recoupés par un second agent.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
