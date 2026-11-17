# `pensionBalance` · Le solde des retraites (partie de la page « Retraites », saisie à la main)

**Vérifiée le 17/11/2026** : les valeurs saisies sont celles du fichier du COR ; le texte du rapport les recoupe pour 2025, 2030 et 2070 (section « Double vérification »). À confirmer par le PO : l'accord écrit du COR du 03/11/2026 vise la série `contributorsPerRetiree` ; cette page reprend une autre série du même fichier, avec la même mention.

| Champ | Valeur |
| --- | --- |
| Indicateur | `pensionBalance`, cinquième volet de la page « Retraites » (`pensions`), dossier « Travail et retraites » (`work`), page de type série, recherche du 17/11/2026 (#21) |
| Données | `briefings/manual/pensionBalance.json`, saisi le 2026-11-17 (projections) |
| Source | COR, rapport annuel de juin 2026, publié le 11/06/2026, « Données juin 2026 – partie 2 », onglet « Fig 2.14 », « Solde du système de retraite observé et projeté dans le scénario de référence, en % du PIB », convention EPR ; chiffres cités, mention « COR, rapport annuel de juin 2026 » |
| Série | `balance` : solde en % du PIB (la feuille l'écrit en fraction, multipliée par 100 et arrondie au centième), ligne « Obs » de 2002 à 2025, ligne « Sc. Ref » de 2026 à 2070 (`projection`), 69 points |
| Chiffre clé | −0,17 % du PIB en 2025, en baisse après −0,06 % en 2024 |
| Règles | Les valeurs « Obs » et « Sc. Ref » de 2025 sont égales (vérifié) ; 2023 vaut 0,0000000005 dans la feuille, saisi 0,00. Non repris : la convention EEC et les variantes de chômage (« Données complémentaires » de la feuille, dont des cellules `#REF!`), le tableau 2.3 des réserves (cité dans une note) |
| Première édition | À remplir à la publication |

À actualiser : à chaque rapport annuel du COR (juin) ; toute la projection change avec les hypothèses.

## « À savoir »

1. Définition : notes de l'onglet « Fig 2.14 » (« défini par le décret n°2014-654 du 20 juin 2014 », « données hors produits charges financières, hors dotations et reprises sur provisions. Convention conforme à la législation : contributions et subventions d'équilibre évoluant de manière à équilibrer chaque année le solde de ces régimes », « ensemble des régimes de retraite français légalement obligatoires, y compris FSV, hors RAFP »).
2. Le scénario de référence : note de l'onglet (fécondité de 1,45 enfant par femme à partir de 2028, solde migratoire de 150 000 par an, productivité horaire de 0,7 % par an, chômage de 7,0 % à partir de 2040) ; valeurs : −0,20 (2030), −1,22 (2050), −2,39 (2070).
3. Les réserves : onglet « Tab 2.3 », au 31/12/2025, total des réserves 223,92 Md€, Agirc-Arrco 113,61 Md€, FRR 20,7 Md€.

## Double vérification

Faite le 17/11/2026 par un agent Claude (modèle Opus), dans le rapport du COR en PDF (https://www.cor-retraites.fr/sites/default/files/2026-07/RA_2026_def.pdf), hors du fichier de données.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, 2025 | −0,17 % | « déficitaire de 5,1 milliards d'euros (- 0,2 % du PIB), hors charges et produits financiers » | RA_2026_def.pdf, partie 2, chapitre 3 | Conforme |
| 2030 | −0,20 % | « - 0,2 % du PIB en 2030 » | RA_2026_def.pdf, synthèse | Conforme |
| 2070 | −2,39 % | « - 2,4 % du PIB en 2070 » | RA_2026_def.pdf, synthèse | Conforme |
| 2045 | −0,89 % | « - 0,9 % du PIB en 2045 » | RA_2026_def.pdf, synthèse | Conforme (le chapitre 3 donne aussi « - 0,4 % en 2045 » : le solde moyen jusqu’à cet horizon, figure 2.16, un autre indicateur) |
| Presse | — | Article du 28/10/2026 sur le déficit cumulé (92,2 Md€ en 2070), sans part du PIB | https://www.toutsurmesfinances.com/actualites/a/retraite-le-deficit-des-regimes-va-se-creuser-fortement | Non trouvé |

**Conclusion.** Le chiffre clé et les horizons 2030, 2045 et 2070 concordent avec le texte du COR.

**Pages consultées** le 17/11/2026 : celles du tableau.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande : l'accord du COR pour cette série reste à confirmer par le PO.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
