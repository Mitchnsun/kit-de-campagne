# `unemploymentBenefits` · L'indemnisation du chômage et la durée des droits (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart de valeur ; réserves de lecture reprises dans les notes des blocs, dans « À savoir » et dans le « À savoir » lu en premier (trois montants de trois mesures, une estimation ex ante). La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `unemploymentBenefits`, dossier « Travail et retraites » (`work`), volet « Indemnisation » de la page composite `unemploymentBeyond` (voir `unemploymentBeyond.md`), page de type comparaison, recherche du 09/11/2026 |
| Données | `briefings/manual/unemploymentBenefits.json`, saisi à la main le 2026-11-09 depuis les notes n° 26.015, 26.014 et 26.016 de France Travail, la fiche « Indemnisation du chômage » de l'ECRT 2026 (Insee et Dares) et deux publications de l'Unédic |
| Sources | 1. France Travail, « Demandeurs d'emploi indemnisés au 2e trimestre 2026, Statistiques et indicateurs n° 26.015 », https://statistiques.francetravail.org/indem/indempub/229913 ; 2. France Travail, « Part des demandeurs d'emploi indemnisables : situation au 31 décembre 2025, Statistiques et indicateurs n° 26.014 », https://statistiques.francetravail.org/indem/indempub/229912 ; 3. France Travail, « Montant moyen du droit d'allocation chômage des demandeurs d'emploi indemnisés au 30 septembre 2025, Statistiques et indicateurs n° 26.016 », https://statistiques.francetravail.org/indem/indempub/229984 ; 4. Insee, Dares, « Indemnisation du chômage », fiche de l'ECRT 2026, figures 1 et 3, https://www.insee.fr/fr/statistiques/8733059 ; 5. Unédic, « Réforme 2023 : premiers effets de la réforme de contracyclicité », https://www.unedic.org/publications/reforme-2023-premiers-effets-de-la-reforme-de-contracyclicite (PDF https://s3.eusc-de-east-1.amazonaws.eu/unedic-eks-prod-cms/2025/12/17/reforme-2023-premiers-effets-de-la-reforme-de-contracyclicite_uid_6942b6507b077.pdf) ; 6. Unédic, « Effets de l'adaptation des règles d'assurance chômage à la conjoncture, version actualisée au 17 avril 2023 », https://www.unedic.org/storage/uploads/2023/07/19/Effets-de-ladaptation-des-rgles-dassurance-chmage--la-conjoncture---actualis_0_uid_64b7e3c56dd92.pdf. Licence `etalab-2.0` pour la fiche publiée par l'Insee (4), « citation seule » pour France Travail et l'Unédic (aucune licence lue). Toutes en français seulement. L'Unédic est admise pour ses seuls chiffres d'assurance chômage |
| Dates de publication | 2026-09-25, 2026-09-24 et 2026-09-29 (France Travail : « Publié le » de chaque page, relu le 09/11/2026 ; le document n° 26.016 est daté d'octobre 2026) ; 2026-07-02 (ECRT 2026) ; 2025-12-17 (Unédic, décembre 2025 : date de création du PDF, la date de mise en ligne de la page n'a pas été lue) ; 2023-04-17 (Unédic : version actualisée au 17 avril 2023) |
| Séries | `recipients` : demandeurs d'emploi indemnisés, moyenne trimestrielle CVS, France, 2026-T2, 3 040 400, statut provisoire (note n° 26.015). `eligibleShare` et `paidShare` : part des inscrits en catégories A, B, C indemnisables (67,9 %) et indemnisés (46,9 %), au 31 décembre 2025, période `2025-12` (note n° 26.014). `entitlementAmount` : montant mensuel moyen du droit, 1 337 € brut, et `paidAmount` : montant mensuel réellement versé, 1 090 € brut, septembre 2025, `2025-09`, indemnisés de l'assurance chômage (note n° 26.016). `receivedAmount` : montant mensuel moyen perçu, 1 075 € brut, décembre 2024, `2024-12`, indemnisés de l'assurance chômage (ECRT 2026, figure 3). Une seule valeur par série |
| Ventilations | `reformSavings` : moindres dépenses annuelles attendues de la réforme de 2023 en régime de croisière, période `2027`, statut `projection` (« estimation ex ante » sur la page) : total 4,5 Md€, allocations 4,2 Md€, versements aux caisses de retraite complémentaire 0,3 Md€ (Unédic, avril 2023, repris en décembre 2025) |
| Chiffre clé | 3 040 400 demandeurs d'emploi indemnisés au 2e trimestre 2026 (provisoire), sans tendance (un seul point ; France Travail écrit - 0,3 % sur le trimestre, non saisi) ; à côté, 46,9 % des inscrits en A, B, C indemnisés (décembre 2025) |
| Règles | Saisie à la main. Deux vues. « Indemnisés et montants » : les indemnisés, la part des inscrits indemnisables et indemnisés, puis les montants dans deux blocs : le droit et le versé de France Travail (même document, même mois, même population), le perçu de l'Insee et de la Dares à part, avec une note qui dit qu'il ne se compare pas comme une évolution. Pas de tableau : il mettrait les trois montants côte à côte. « Réforme de 2023 » : les 4,5 Md€ et leur décomposition, le total hachuré. La durée des droits n'est pas en barres (pas d'unité « mois » dans le format) : 18 et 24 mois dans la note du bloc, 16 et 20 mois et le seuil de 9,0 % dans « À savoir ». Le taux de 8,3 % de l'Insee n'est jamais rapproché du seuil de 9,0 % (la note de France Travail ne dit pas quel taux sert de référence). Non saisis : la répartition des indemnisés par régime (État 306 600, autres 107 900 : dans le texte, seuls 2 626 000 et 86,4 % pour l'assurance chômage), les 1 482 € des anciens temps complets, la médiane du perçu (990 €), la durée réellement indemnisée (- 14 %, champ des moins de 53 ans ambigu), les 300 000 indemnisés de moins de l'estimation de 2023 |
| Première édition | À remplir à la publication |

## « À savoir »

1. Depuis la réforme de 2023, les droits à l'assurance chômage durent 18 mois au plus hors filière seniors, contre 24 avant. Pour les droits ouverts en 2024, la durée potentielle moyenne est de 16 mois, contre 20 en 2022, selon l'Unédic. Source : Unédic, décembre 2025 (« La durée potentielle des droits ouverts est désormais limitée à 18 mois maximum hors filière seniors (contre 24 mois auparavant) [...] La durée potentielle de droit s'établit désormais à 16 mois en moyenne, contre 20 mois en 2022 (soit -20 %). »).
2. Selon France Travail, la conjoncture est favorable au sens de la réforme si le taux de chômage est inférieur à 9,0 % ou n'augmente pas de plus de 0,8 point sur un trimestre ; la durée des droits est alors réduite de 25 %. France Travail ne précise pas quel taux sert de référence. Source : note n° 26.015, note 2 (« La conjoncture est considérée comme favorable au sens de la réforme si le taux de chômage est inférieur à 9,0% ou tant qu'il n'augmente pas de plus 0,8 point sur un trimestre. En période de conjoncture favorable, la durée des droits est réduite de 25% ») ; précaution du rapport final (`seuilContracyclicite`).
3. Au 31 décembre 2024, selon l'Insee et la Dares, 48 % des inscrits en catégories A à E sont indemnisés : 42 % des moins de 25 ans, 53 % des 50 ans ou plus. Un autre champ et une autre date que les 46,9 % de France Travail, en catégories A, B, C fin 2025. Source : ECRT 2026, fiche « Indemnisation du chômage », figure 1 (« Au 31 décembre 2024, 3,1 millions de personnes sont indemnisées, soit 48 % des inscrits à France Travail » ; cellules « 48 42 48 53 ») ; note n° 26.014 pour les 46,9 %.

Les trois points en anglais disent la même chose que le français.

**Le « À savoir » lu en premier** (`readFirst` du volet, dans l'app) : un indemnisé n'est pas un chômeur au sens du BIT, c'est un inscrit à France Travail, parfois en formation ou en activité réduite (précaution du rapport final, `indemnises` : « Les indemnisés comprennent des personnes en formation ou en activité réduite ») ; les trois montants mesurent le droit, le versé et le perçu, chacun à sa date et selon son producteur, et ne forment pas une évolution (précautions `montantDroitAllocation` et `montantPercuAllocation`).

**Notes des blocs** (dans l'app) : 2 626 000 indemnisés par l'assurance chômage, 86,4 % (note n° 26.015 : « Assurance chômage 2 622 300 2 638 200 2 626 000 -0,5% 0,1% 86,4% ») ; indemnisable, « qui a un droit ouvert », et 69,0 % des indemnisables indemnisés (note n° 26.014 : « 67,9% des personnes inscrites à France Travail en catégories A, B, C ont un droit ouvert à l'indemnisation. Parmi celles-ci, 69,0% sont indemnisées » ; la baisse sur un an « ne peut être interprétée comme une évolution conjoncturelle ») ; le droit théorique et sa médiane, 1 151 €, et le versé, 1 030 € net (note n° 26.016 : « Le fait que certains jours du mois peuvent ne pas être payés [...] n'est pas pris en compte » ; « Le montant mensuel réellement versé en septembre 2025 est de 1 090€ brut (1 030€ net). ») ; 755 € et 1 215 € selon l'âge, taux de remplacement brut moyen de 64 % (ECRT 2026, figure 3) ; l'estimation ex ante (Unédic, décembre 2025 : « Selon les estimations ex ante de l'Unédic, une fois la mesure pleinement montée en charge – à l'horizon 2027 et sous l'hypothèse d'une conjoncture stable – les moindres dépenses pour le régime seraient de l'ordre de 4,5 Md€ par an » ; avril 2023 : « les moindres dépenses d'allocation atteindraient 4,2 Md€ auxquelles s'ajoutent les moindres versements aux caisses de retraite complémentaire de 0,3 Md€ »). La note dit que ce chiffre ne porte pas sur un passage à 12 mois, la mesure `unemploymentReform` du jeu, sans la juger.

## Ce qu'on entend

Aucune affirmation : voir `unemploymentBeyond.md` (« la plupart des chômeurs sont indemnisés » et « au chômage, on touche autant qu'en travaillant » sont écartées par le rapport final).

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-jeunes.md` : notes de France Travail, fiche de l'ECRT et PDF de l'Unédic retéléchargés et relus.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 3 040 400 (2026-T2) | « 3 040 400 demandeurs d'emploi indemnisés » ; données du 2e trimestre 2026 provisoires ; relu sur la page le 09/11/2026 | note n° 26.015 (URL ci-dessus) | Conforme avec réserve : provisoire |
| Parts des inscrits A, B, C | 67,9 % ; 46,9 % | « 67,9% » ; « 46,9% » ; 67,9 % x 69,0 % = 46,9 % (calculé, cohérent) ; relu sur la page | note n° 26.014 | Conforme ; au 31/12/2025 |
| Droit et versé | 1 337 € ; 1 090 € | « 1 337 euros » ; « 1 090€ brut (1 030€ net) » ; la page arrondit à « environ 1 340 € » | note n° 26.016 | Conforme avec réserve : montant théorique ; le versé, non relevé par la recherche, ajouté par la contre-vérification |
| Perçu | 1 075 € | « ont perçu en moyenne 1 075 euros brut » ; relu sur la page à la saisie | ECRT 2026, figure 3 | Conforme ; autre producteur et autre mois que le droit |
| Durées (note) | 18, 24, 16, 20 mois | phrases de l'Unédic recopiées | Unédic, décembre 2025 | Conforme |
| Seuil (note) | 9,0 % ; 0,8 point ; 25 % | phrase de la note 2 | note n° 26.015 | Conforme |
| Moindres dépenses | 4,5 ; 4,2 ; 0,3 Md€ | « Des moindres dépenses de l'ordre de 4,5 Md€ par an en régime de croisière » ; 4,2 + 0,3 | Unédic, avril 2023, repris en décembre 2025 | Conforme avec réserve : estimation ex ante, sous l'hypothèse d'une conjoncture stable |
| Indemnisés par âge (note) | 48 ; 42 ; 53 % | cellules de la figure 1 ; « 48 % » relu sur la page | ECRT 2026, figure 1 | Conforme ; champ A à E, fin 2024 |

**Conclusion.** Aucun chiffre du fichier n'est faux ; les trois montants restent dans des blocs distincts, et l'estimation de l'Unédic est dite estimation.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus ; à la saisie, les pages des notes n° 26.014, 26.015 et 26.016 de France Travail et la fiche de l'ECRT, relues.

## Réserves

- Les indemnisés du 2e trimestre 2026 sont provisoires (« Les données du 1er trimestre 2026 et du 2e trimestre 2026 sont provisoires »).
- Trois montants, trois mesures : le droit théorique (allocation journalière x 30 jours depuis avril 2025, France Travail, septembre 2025), le versé du même mois (France Travail), le perçu (Insee et Dares d'après MiDAS, décembre 2024). Jamais une évolution.
- Les parts indemnisées n'ont pas le même champ : catégories A, B, C fin 2025 (France Travail), catégories A à E fin 2024 (Insee et Dares).
- Les 4,5 Md€ chiffrent la réforme de 2023 (durée réduite de 25 % en conjoncture favorable) à l'horizon 2027 ; ils ne chiffrent pas un passage de 18 à 12 mois.
- La date de mise en ligne de la publication de l'Unédic de décembre 2025 n'a pas été lue (date de création du PDF retenue).

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a relu les notes, la fiche et les PDF.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Insee : Licence Ouverte 2.0, mention « Source : Insee » et date de dernière mise à jour (https://www.insee.fr/fr/information/2008466) ;
  - citation seule : France Travail, Unédic (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
