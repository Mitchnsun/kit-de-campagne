# `socialSpending` · Où va l'argent social (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; réserves de lecture (données semi-définitives ou provisoires, prévisions, périmètres), reprises dans « À savoir » et « Ce qu'on entend ». La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `socialSpending`, dossier « Économie et fiscalité » (`economy`), aussi dans « Travail » (`alsoIn: ['work']`), page de type comparaison |
| Données | `briefings/manual/socialSpending.json`, saisi à la main le 2026-11-09 depuis le classeur des comptes de la protection sociale de la DREES (23/10/2026), deux tableaux d'Eurostat (mis à jour le 26/10/2026) et le rapport d'octobre 2026 de la Commission des comptes de la sécurité sociale |
| Sources | DREES, « La protection sociale en France de 1959 à 2024 » : page du jeu de données https://data.drees.solidarites-sante.gouv.fr/explore/dataset/305_les-comptes-de-la-protection-sociale/ (adresse de la plateforme, non ouverte ici : DREES inaccessible le 09/11/2026), fichier https://data.drees.solidarites-sante.gouv.fr/api/v2/catalog/datasets/305_les-comptes-de-la-protection-sociale/attachments/la_protection_sociale_en_france_de_1959_a_2024xlsx (feuille `prestations_1959_2024`, colonne 2024SD), licence non vérifiée, « citation seule » ; Eurostat, « Dépenses de protection sociale en pourcentage du PIB » (tps00098), https://ec.europa.eu/eurostat/databrowser/view/tps00098/default/table?lang=fr, licence Eurostat ; Eurostat, « Dépenses de prestations sociales par fonction » (spr_exp_func), https://ec.europa.eu/eurostat/databrowser/view/spr_exp_func/default/table?lang=fr, licence Eurostat ; Commission des comptes de la sécurité sociale, « Les comptes de la Sécurité sociale, octobre 2026 » (rapport « Résultats 2025, prévisions 2026 et 2027 »), https://www.securite-sociale.fr/files/live/sites/SSFR/files/medias/CCSS/2026/CCSS-octobre-2026_assemble_VDEF.pdf, « citation seule », en français seulement |
| Séries | `benefits` : prestations de protection sociale, Md€ courants, 2024 (semi-définitif), 1 point (933,1605) ; `franceGdpShare` et `euGdpShare` : dépenses de protection sociale en % du PIB, France et UE à 27, tps00098, 2024 (provisoire), 1 point chacune (34,19 et 28,42) ; `basicSchemesDeficit` : déficit des régimes de base et du FSV, Md€, 2025 à 2027, 3 points (21,6 ; 21,0 et 22,6, ces deux derniers au statut `projection`, dit « prévision » par la page), saisi en positif comme un déficit (le rapport écrit − 21,6 Md€) |
| Valeurs par catégorie | `byRisk` (2024, semi-définitif, Md€) : vieillesse-survie 426,6988 ; santé 339,4386 ; famille 65,4767 ; emploi 51,3013 ; logement 16,0586 ; pauvreté et exclusion sociale 34,1864. `targeted` (2024, semi-définitif, Md€) : pensions de droit direct 359,3579 ; RSA socle 11,9836 ; prime d'activité 10,5572 ; toutes prestations 933,1605 (la référence hachurée). `franceByFunction` et `euByFunction` (2024, provisoire, % du PIB, spr_exp_func) : vieillesse et survie 14,54 / 12,81 ; maladie et soins de santé 9,48 / 8,11 ; famille 2,23 / 2,40 ; chômage 1,75 / 1,08 ; logement 0,55 / 0,37 ; exclusion sociale 1,16 / 0,60 |
| Chiffre clé | 933,2 Md€ de prestations de protection sociale en 2024 (semi-définitif), sans tendance (un seul point saisi) |
| Règles | Saisie à la main, rien n'est lu par script. Les montants de la DREES sont en millions d'euros dans le classeur, saisis en milliards sans arrondi (933 160,5 M€ → 933,1605). Les parts par risque (45,7 %, 36,4 %…) et le poids du RSA (1,3 %, 2,8 %) sont calculés : aucun n'est saisi en série, les notes et les affirmations disent « calculé ». La fonction « invalidité » d'Eurostat n'est pas dans la recherche : les six fonctions saisies ne font pas le total des prestations (31,79 % du PIB en France). Les estimations 2025 d'Eurostat ne sont pas retenues. Le tableau COFOG d'Eurostat (dépenses publiques par fonction), vérifié, n'est pas saisi : son champ (administrations publiques) diffère du SESPROS |
| Première édition | À remplir à la publication |

## « À savoir »

1. Les prestations de 2024 sont des données semi-définitives de la DREES, en euros courants et tous régimes ; la santé comprend l'invalidité et les accidents du travail. La vieillesse-survie en représente 45,7 % et la santé 36,4 % (calculé). Source : DREES, classeur des comptes de la protection sociale (URL ci-dessus ; « 2024SD », prochaine mise à jour annoncée en décembre 2026) ; parts refaites à la double vérification (426 698,8 / 933 160,5 = 45,7 % ; 339 438,6 / 933 160,5 = 36,4 %).
2. Le RSA socle pèse 1,3 % des prestations (calculé : 11,98 Md€ sur 933,2 Md€), sur le périmètre des comptes de la protection sociale. Les données de la DREES sur les minima sociaux, qui comptent la prime de Noël et les indus, donnent au RSA un montant plus élevé. Source : DREES, même classeur (lignes « RSA socle » 11 983,57 et « Prestations de protection sociale » 933 160,53) ; le montant plus élevé est celui du fichier des dépenses de minima sociaux de la DREES (12 358 M€, voir `minimumIncomes.md`), cité sans son chiffre parce qu'il n'est pas une source de cette page.
3. Les chiffres d'Eurostat de 2024 sont provisoires, pour la France comme pour l'UE. Le total en % du PIB compte les prestations et les frais de fonctionnement : il dépasse les seules prestations (31,79 % du PIB en France). Les fonctions montrées ne comprennent pas l'invalidité. Source : Eurostat, tps00098 (« 34.19 p », « 28.42 p ») et spr_exp_func (total des prestations, France, 2024 : « 31.79 p »), https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/spr_exp_func?format=JSON&lang=en&geo=FR&geo=EU27_2020&unit=PC_GDP&sinceTimePeriod=2022. La fonction « Disability / Invalidité » est listée par le même tableau (relu le 09/11/2026 par l'agent qui a écrit la page, sans en saisir la valeur).
4. Le déficit des régimes de base de la sécurité sociale et du Fonds de solidarité vieillesse (FSV) atteint 0,7 point de PIB en 2025. Les montants de 2026 et 2027 sont des prévisions de la Commission des comptes, faites avant les mesures de la loi de financement pour 2027. Source : rapport de la CCSS d'octobre 2026 (« En 2025, le déficit des régimes de base et du FSV a crû de plus de 40 % pour atteindre - 21,6 Md€, soit - 0,7 point de PIB » ; 2026 : « avant prise en compte des mesures de la loi de financement, se réduirait à la marge pour s'élever à 21,0 Md€ » ; 2027 : « avant les mesures de la loi de financement, le déficit augmenterait de nouveau pour atteindre 22,6 Md€ »).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/socialSpending.json` (clé `claims`, français et anglais), reprise des affirmations relues du rapport de recherche du 09/11/2026. Source de chaque chiffre de la réponse :

1. « On entend que le RSA coûte une fortune et que l'assistanat plombe les comptes. » 11,98 Md€ (RSA socle), 933,2 Md€ (prestations) et 426,7 Md€ (vieillesse-survie), 2024 : DREES, classeur des comptes de la protection sociale. 1,3 % : calculé (11 983,6 / 933 160,5 = 1,28 %). La phrase de la recherche sur l'ensemble des minima sociaux (33,3 Md€, fichier des dépenses de minima de la DREES) est retirée de la réponse : ce fichier n'est pas une source de cette page, et son périmètre diffère.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web (rapport `verify-social.md`) : chaque URL rouverte, le classeur de la DREES lu cellule par cellule (Python), l'API d'Eurostat relue et reclassée, le PDF de la CCSS passé à `pdftotext`. Producteurs officiels seulement. Aucun écart de valeur, aucun chiffre non retrouvé. Verdicts : Conforme, ou Conforme avec la réserve dite dans la colonne.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, prestations 2024 | 933,1605 Md€ | 933160,53 M€ (2024SD) ; parution 23/10/2026 ; mise à jour annoncée en décembre 2026 | classeur de la DREES (URL ci-dessus) | Conforme (semi-définitif) |
| Prestations par risque | 426,6988 / 339,4386 / 65,4767 / 51,3013 / 16,0586 / 34,1864 Md€ | 426698,85 / 339438,64 / 65476,73 / 51301,31 / 16058,55 / 34186,45 M€ ; parts 45,7 / 36,4 / 7,0 / 5,5 / 1,7 / 3,7 % refaites | classeur de la DREES | Conforme (arrondi au dixième de million de la recherche) |
| RSA socle, prime d'activité, pensions de droit direct | 11,9836 / 10,5572 / 359,3579 Md€ | 11983,57 / 10557,19 / 359357,86 M€ | classeur de la DREES | Conforme |
| Poids du RSA | 1,3 % (note, affirmation) | 1,28 % et 2,81 % refaits | calcul | Conforme avec réserve : totaux de natures différentes, gardé « calculé » |
| Protection sociale en % du PIB | 34,19 (FR) ; 28,42 (UE) | « 34.19 p » ; « 28.42 p » ; mis à jour le 26/10/2026 ; classement refait : FR 34,19, FI 32,91, AT 32,31, DE 30,87, BE 30,18 | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/tps00098?format=JSON&lang=en | Conforme avec réserve : provisoire pour la France et l'UE |
| Prestations par fonction | 14,54/12,81 ; 9,48/8,11 ; 2,23/2,40 ; 1,75/1,08 ; 0,55/0,37 ; 1,16/0,60 | tous retrouvés, provisoires ; total des prestations 31,79 % (France) | API spr_exp_func (URL ci-dessus) | Conforme avec réserve : provisoire |
| Déficit des régimes de base et du FSV | 21,6 (2025) ; 21,0 et 22,6 (2026, 2027, prévision) | − 21,6 Md€ ; − 21,0 ; − 22,6 Md€ | https://www.securite-sociale.fr/files/live/sites/SSFR/files/medias/CCSS/2026/CCSS-octobre-2026_assemble_VDEF.pdf | Conforme avec réserve : prévisions avant la loi de financement pour 2027 |
| IJ du régime général (affirmation 3) | 11,1 Md€ ; 5,7 % ; 0,7 % ; 12,6 % | 11 122 M€ ; 5,7 % ; 0,7 % ; 12,6 % (tableau 1 des soins de ville, colonne « taux de croissance annuel moyen 2019/2025 ») | rapport de la CCSS (URL ci-dessus) | Conforme avec réserve : données corrigées des jours ouvrables ; 2026 prévu |
| Plafond des IJ (affirmation 3) | 1,4 Smic, avril 2025 | « à 1,4 fois le Smic depuis le 1er avril 2025 » | rapport de la CCSS | Conforme |
| Dates de publication | 2026-10-23 (DREES), 2026-10-26 (Eurostat, deux tableaux), 2026-10-05 (CCSS) | DREES : date de parution lue dans le classeur ; Eurostat : « updated 2026-10-26 » ; CCSS : date de création du PDF (rapport d'octobre 2026) | URL ci-dessus | Conforme avec réserve : la date de la CCSS vient du PDF |

**Conclusion.** Aucun chiffre du fichier n'est faux ; trois lectures sont à garder : 2024 est semi-définitif (DREES) ou provisoire (Eurostat), 2026 et 2027 sont des prévisions, et le RSA n'a pas le même montant selon le périmètre.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus (la DREES par son fichier, son site étant intermittent). Les titres français des deux tableaux d'Eurostat et le statut provisoire de la France ont été relus dans l'API (`lang=fr`) le 09/11/2026 par l'agent qui a écrit la page.

## Mises à jour

**09/11/2026** : le bloc « Ce qu'on entend » ne garde que les fausses vérités que les chiffres de la page démentent (décision du PO) : affirmations retirées : « On entend que la France est championne d'Europe des dépenses sociales. » ; « On entend que les arrêts maladie explosent. ».

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert le classeur, l'API et le rapport eux-mêmes.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Eurostat : réutilisation permise, commerciale comprise, mention « Source : Eurostat » et modifications signalées (https://ec.europa.eu/eurostat/help/copyright-notice) ;
  - citation seule : DREES, Commission des comptes de la sécurité sociale (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
