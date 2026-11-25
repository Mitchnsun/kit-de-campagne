# `mainTaxes` · Les principaux impôts

**Vérifiée le 25/11/2026** : double vérification sur le web, sans écart non expliqué (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `mainTaxes`, dossier « Économie et fiscalité » (`economy`), page de type série, ticket #540 de l'app |
| Données | `briefings/data/mainTaxes.json`, écrit par `yarn briefings mainTaxes` le 2026-11-25 |
| Sources | Insee, « Dépenses et recettes des administrations publiques en 2025 », paru le 28/08/2026, https://www.insee.fr/fr/statistiques/8988845 ; tableau 3.217 « Principaux impôts par catégorie », https://www.insee.fr/fr/statistiques/fichier/8988845/t_3217_fr.xlsx (feuille `T_3217`, comptes nationaux base 2020) ; Licence Ouverte 2.0 (comme les autres tableaux de l'Insee du kit) |
| Séries | En Md€ courants, toutes administrations publiques, 1995 à 2025, 31 points chacune : `vat` (« Taxe sur la valeur ajoutée (TVA) (D211) »), `incomeTax` (« Impôt sur le revenu des personnes physiques (IRPP), avant crédits d'impôt »), `csg` (« Contribution sociale généralisée (CSG) »), `corporateTax` (« Impôt sur les sociétés (IS), avant crédits d'impôt »), `energyExcise` (« Accises sur les produits énergétiques (TICPE) ») ; 2024 semi-définitif, 2025 provisoire, d'après le PIB annuel de la même campagne (BDM `011779992`), comme `publicFinances` |
| Chiffre clé | TVA 2025 : 208,8 Md€ (provisoire), en hausse (207,8 Md€ en 2024) |
| Règles | Toutes les années du tableau ; le script échoue sur un autre tableau, une ligne absente, une valeur hors de 1 à 1 000 Md€, une ligne qui ne finit pas la même année, ou un tableau d'une autre campagne que le PIB |
| Première édition | La prochaine édition du kit |

## « À savoir »

1. 208,8, 89,6, 156,6 et 103,6 Md€ : lus dans `briefings/data/mainTaxes.json` (arrondis au dixième).
2. Le champ et la nature de la TVA : le tableau porte sur les administrations publiques (comptes nationaux, en droits constatés), libellé D211 ; la TVA nette du budget de l'État est une autre grandeur (rapport de la recherche du 25/11/2026, `dossiers2/A-series.md`, « piège principal »).
3. Les lignes « avant crédits d'impôt » et les crédits d'impôt comptés sur des lignes à part : tableau 3.217, lignes 75, 76, 78 et 79. Le statut des années : page « Impôts » de l'Insee du 28/08/2026 (https://www.insee.fr/fr/statistiques/2381408), lue par l'agent de recherche.

## Double vérification

Faite le 25/11/2026 par un agent Claude (modèle Sonnet), sans passer par le tableau du script (rapport `dossiers2/A-series.md` de la session).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| TVA 2024 | 207,753 Md€ | 207 753 M€ | Eurostat `gov_10a_taxag`, `na_item=D211`, `sector=S13`, https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/gov_10a_taxag?format=JSON&lang=fr&geo=FR&sector=S13&na_item=D211&unit=MIO_EUR | Conforme |
| TVA 2025 | 208,821 Md€ | 208 821 M€ | Idem | Conforme |
| TVA 2020 | 162,090 Md€ | 162 090 M€ | Idem | Conforme |
| TVA 1995 | 89,583 Md€ | 90 057 M€ | Idem | Écart expliqué : Eurostat diffère un peu avant 2000 (moins de 1 %), écart non expliqué par le producteur, antérieur à la période qui compte |
| TVA 2024, DGFiP ou Cour des comptes | | Non trouvé | Recherche de l'agent | Non trouvé |

**Conclusion.** Les valeurs du tableau concordent avec Eurostat depuis 2000.

**Pages consultées** le 25/11/2026 : celles du tableau.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande : celle des autres tableaux de l'Insee du kit, non relue pour cette page.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
