# `preCommittedSpending` · Les dépenses pré-engagées (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; réserves de lecture reprises ci-dessous. La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `preCommittedSpending`, dossier « Pouvoir d'achat et logement » (`purchasingPower`), volet « Dépenses contraintes » de la page composite `householdBudget` (voir `householdBudget.md`), page de type série, recherche « Ce qu'on entend » du 09/11/2026 |
| Données | `briefings/manual/preCommittedSpending.json`, saisi le 2026-11-09 depuis le tableau T_DEP_PRE_ENG de l'Insee (onglet « M€cour », lignes `_DEP_REVENU`, `_DEP_LOGT_REVENU`, `_DEP_CONSO`), au millième comme l'Insee les publie, chaque valeur recoupée avec le fichier des chiffres vérifiés (au dixième) |
| Sources | 1. Insee, « Consommation des ménages en 2025 », Insee Résultats, https://www.insee.fr/fr/statistiques/8988813, tableau https://www.insee.fr/fr/statistiques/fichier/8988813/T_DEP_PRE_ENG_fr.xlsx (29/05/2026 ; fichier créé le 26/05/2026), Licence Ouverte 2.0, en français. 2. Insee, « Dépenses pré-engagées », définition c1358, https://www.insee.fr/fr/metadonnees/definition/c1358 (en anglais https://www.insee.fr/en/metadonnees/definition/c1358 ; dernière mise à jour le 07/08/2026), Licence Ouverte 2.0 |
| Séries | `shareOfIncome` : part de la dépense pré-engagée dans le revenu disponible brut (`_DEP_REVENU`), en %, 1959 à 2025, 67 points (1960 : 13,54 ; 2024 : 30,077 ; 2025 : 30,333). `housingShareOfIncome` : part de la dépense liée au logement dans le revenu disponible brut (`_DEP_LOGT_REVENU`), 67 points (2025 : 23,072). `shareOfSpending` : part de la dépense pré-engagée dans la dépense de consommation finale des ménages (`_DEP_CONSO`), 67 points (2025 : 36,826). 2025 provisoire pour les trois |
| Chiffre clé | 30,3 % du revenu disponible brut en 2025 (provisoire), tendance à la hausse (30,1 % en 2024) ; à côté, 36,8 % de la dépense de consommation |
| Règles | Saisie à la main. Des parts publiées par l'Insee, pas calculées. Le logement y comprend les loyers imputés et les services financiers une estimation (SIFIM) : la note sous le graphique le dit, avec la définition de l'Insee recopiée, le saut de 2023 (services financiers) et les 36,8 % de la dépense de consommation. Les dépenses pré-engagées selon le niveau de vie (61 %, 23 %, 32 %) sont écartées : vues seulement dans un résumé de moteur de recherche |
| Première édition | À remplir à la publication |

## « À savoir »

1. La définition de l'Insee, recopiée : « Ensemble des dépenses des ménages réalisées dans le cadre d'un contrat difficilement renégociable à court terme » ; logement, eau, énergie, télécommunications, télévision, cantines, assurances hors assurance-vie, services financiers. Source : définition c1358 (liste relue). En anglais, la définition est traduite (la version anglaise de l'Insee n'est pas reprise telle quelle).
2. Le logement comprend les loyers imputés et les services financiers les services d'intermédiation financière indirectement mesurés, des montants qui ne correspondent pas à des sommes payées ; logement 23,1 % du revenu disponible en 2025. Source : définition c1358 (« y compris, dans le cas de la comptabilité nationale, les loyers imputés » ; « les services d'intermédiation financière indirectement mesurés ») ; T_DEP_PRE_ENG (`_DEP_LOGT_REVENU` 23,072).
3. Le saut de 2023 vient surtout des services financiers (16,2 Md€ en 2022, 47,0 Md€ en 2023) ; en 2025 (provisoire), 569,3 Md€, 30,3 % du revenu disponible brut et 36,8 % de la dépense de consommation. Source : T_DEP_PRE_ENG (« CP122 Services financiers » 16 159,6 puis 46 993,4 ; « CPDPE » 569 300,6 ; `_DEP_REVENU` 30,333 ; `_DEP_CONSO` 36,826).

Les trois points en anglais disent la même chose que le français.

## Ce qu'on entend

Aucune affirmation sur ce volet. L'affirmation « les dépenses contraintes mangent plus de la moitié du revenu » est retirée (décision du PO du 09/11/2026) : elle peut valoir pour les ménages les plus modestes, sans chiffre vérifié ; les 23,1 % du logement dans le revenu disponible servent à l'affirmation sur le logement du volet « Ce qu'ils achètent ».

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-panier.md` (tableur T_DEP_PRE_ENG relu, séries identiques à celles du rapport de recherche ; définition relue).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 30,333 % (2025 p) | « Part de la dépense pré-engagée dans le revenu disponible brut 30.333 » | T_DEP_PRE_ENG | Conforme, avec réserve : provisoire |
| Dans la dépense de consommation | 36,826 % | « dans la dépense de consommation finale 36.826 » | T_DEP_PRE_ENG | Conforme |
| Montant | 569,3 Md€ (note) | « CPDPE 569300.6 » ; revenu disponible « B6G 1876862.7 » | T_DEP_PRE_ENG | Conforme |
| Séries 1959-2025 | 67 points chacune | valeurs relues ; au dixième, identiques au fichier des chiffres vérifiés (2001, logement : 21,25 au millième, 21,2 dans le fichier vérifié, un arrondi) | T_DEP_PRE_ENG | Conforme |
| Saut de 2023 | services financiers 16,2 puis 47,0 Md€ | « CP122 Services financiers » 16 159,6 (2022) ; 46 993,4 (2023) | T_DEP_PRE_ENG | Conforme |
| Définition | recopiée | « Ensemble des dépenses des ménages réalisées dans le cadre d'un contrat difficilement renégociable à court terme. » | https://www.insee.fr/fr/metadonnees/definition/c1358 | Conforme |

**Conclusion.** Aucun chiffre du fichier n'est faux ; la note dit ce que la mesure compte de sommes non payées (loyers imputés, services financiers estimés).

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Pas de script : la double vérification a rouvert le tableau de l'Insee.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
