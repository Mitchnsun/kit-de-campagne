# `taxFraud` · Fraude fiscale (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; réserves de lecture reprises ci-dessous. La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `taxFraud`, dossier « Économie et fiscalité » (`economy`), volet de la page composite `fraud` (voir `fraud.md`), page de type comparaison |
| Données | `briefings/manual/taxFraud.json`, saisi à la main depuis « VAT gap in Europe – report 2025 » de la Commission européenne (11/12/2025) et le rapport « La lutte contre la fraude fiscale » de la Cour des comptes (16/12/2025) le 2026-11-09 |
| Sources | Commission européenne, « VAT gap in Europe – report 2025 », page `vat-gap_en` ; Cour des comptes, « La lutte contre la fraude fiscale » (rapport et synthèse, 16/12/2025) ; Cour des comptes, présentation à la presse du Premier président (16/12/2025) ; licence « citation seule » pour les trois, la Commission en anglais aussi, la Cour en français seulement |
| Séries | `vatGap` : écart de TVA de la France, Md€, 2023 seulement, 1 point (12,121) ; `vatGapShare` : le même écart en % de la TVA théoriquement due, 2019 à 2023, 5 points ; `auditClaimed` : droits rappelés et crédits d'impôt non remboursés, Md€, 2015 et 2024, 2 points ; `auditCollected` : recettes encaissées grâce au contrôle fiscal, Md€, 2015 et 2024, 2 points |
| Chiffre clé | 12,121 Md€ d'écart de TVA en 2023 (5,6 % de la TVA théoriquement due), sans tendance saisie (5,1 % en 2022) |
| Règles | Saisie à la main. Aucune estimation officielle de la fraude fiscale totale : la page ne donne aucun total. L'écart de TVA mêle fraude, erreurs et faillites. Le montant en euros n'est saisi que pour 2023 ; les parts vont de 2019 à 2023. La colonne 2024 du fichier de la Commission (France : 16 451 M€, 7,4 %) est volontairement écartée tant que le rapport ne l'a pas commentée. « Rappelé » n'est pas « encaissé ». Euros courants. La fourchette de la DGFiP (6 à 10 Md€, 2019) est citée dans « À savoir », pas saisie en série |
| Première édition | À remplir à la publication |

## « À savoir »

1. L'écart de TVA de la Commission va, selon elle, de l'exploitation légale des failles à la fraude organisée à grande échelle, et compte aussi les erreurs et les faillites. La Cour des comptes cite une fourchette de la DGFiP, entre 6 et 10 Md€, soit 4 à 5 % de la TVA collectée. Source : Commission européenne, https://taxation-customs.ec.europa.eu/taxation/vat/fight-against-vat-fraud/vat-gap_en (« from the legal exploitation of loopholes in tax systems to evasion or organized large-scale tax fraud. Non-compliance can also be unintentional, resulting from administrative errors, omissions, non-fraudulent bankruptcies, and other factors. » ; relu sur la page le 09/11/2026 par le coordinateur) ; fourchette : Cour des comptes, synthèse du 16/12/2025, https://www.ccomptes.fr/sites/default/files/2025-12/20251216-synthese-Lutte-contre-la-fraude-fiscale.pdf (« entre 6 et 10 Md€, soit entre 4 et 5 % du montant de TVA effectivement collectée »), et DGFiP Analyses n° 7, https://www.impots.gouv.fr/sites/default/files/media/9_statistiques/0_etudes_et_stats/0_publications/dgfip_analyses/2024/num07_09/dgfip_analyses_07_2024.pdf (« une fourchette de 6 à 10 », « un minorant », 2019, entreprises déclarantes seulement).
2. Les résultats annoncés du contrôle fiscal sont des sommes rappelées, pas encaissées, et se rapportent à plusieurs exercices antérieurs. Les recettes encaissées une année comprennent les recouvrements de cette année-là, quel que soit leur millésime. Source : Cour des comptes, rapport du 16/12/2025, https://www.ccomptes.fr/sites/default/files/2025-12/20251216-Lutte-contre-la-fraude-fiscale.pdf (« Ces résultats se rapportent à plusieurs exercices antérieurs, et non aux impôts de l'année N […] Le montant des recettes encaissées au titre du contrôle fiscal en année N (qui ne comprend pas les crédits d'impôt non remboursés) intègre à l'inverse les recouvrements cette année-là sur les droits rappelés et les pénalités, quel que soit leur millésime. » ; relu le 09/11/2026 par le coordinateur ; 11,4 Md€ en 2024 et 12,2 Md€ en 2015).
3. Le chiffre de 80 à 100 Md€ de fraude fiscale, d'origine syndicale, repose sur des données de 2012 ou 2013. Selon la Cour des comptes, son périmètre se rapproche davantage de l'écart fiscal que de la fraude. Source : Cour des comptes, présentation à la presse, https://www.ccomptes.fr/sites/default/files/2025-12/20251216-discours-PPdt-lutte-contre-la-fraude-fiscale.pdf, et rapport (tableau n° 3 : estimation de Solidaires Finances publiques, 80 à 100 Md€). La double vérification précise que la Cour écrit « se rapproche davantage de l'écart fiscal que de la fraude fiscale » (et non « mesure en réalité l'écart fiscal ») et « de 2012 ou de 2013 » (et non « antérieures à 2013 ») : le texte des notes suit la source.

Les trois points en anglais (relus le 09/11/2026) disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/taxFraud.json` (clé `claims`, français et anglais). Source de chaque chiffre de la réponse :

1. « On entend que la fraude fiscale représente 80 à 100 milliards par an. » « Nul ne peut aujourd'hui se hasarder à affirmer que ce montant est proche de 30 ou de 130 Md€ » : Cour des comptes, rapport du 16/12/2025. « Au minimum une approximation, voire une affirmation gratuite » : Premier président, présentation à la presse du 16/12/2025. Réserve : « ce montant » est flou (écart fiscal et fraude), et la DGFiP a bien une estimation pour la TVA ; « aucune estimation fiable » traduit « absence d'estimation fiable, quasiment sans exception ».
2. « On entend que la fraude à la TVA représente des dizaines de milliards. » 12,1 Md€ en 2023 et 5,6 % : Commission européenne, page `vat-gap_en`. « Fraude, erreurs et faillites » : même page.

**Retirée le 09/11/2026** : « On entend que le fisc a récupéré un record de 17 milliards. » (17,4 Md€ de droits rappelés et de crédits d'impôt non remboursés en 2024, pour 11,4 Md€ encaissés, Cour des comptes). Elle recoupait l'affirmation du volet `taxPenalties` (« le fisc a récupéré 17 milliards d'euros de fraude en 2025 »), qui répond avec le bilan de 2025 de la DGFiP, plus récent et plus complet (droits et pénalités, sommes encaissées, crédits non remboursés) : celle-là est gardée, voir `taxPenalties.md`. Les sommes rappelées et encaissées de 2015 et de 2024 restent dans la vue « Contrôle fiscal » de ce volet ; elles ne se raccordent pas aux montants de `taxPenalties` (définitions différentes, ce que dit une note de ce volet-là).

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web : chaque URL du rapport de recherche rouverte (PDF passés à `pdftotext`, fichier XLSX de la Commission ouvert). Producteurs officiels seulement. Aucun écart numérique. Le contrôle de 16,1 et 17,4 Md€ vient de la double vérification du thème « finances » (09/11/2026, même méthode).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, écart de TVA | 12,121 Md€ (2023) | 12 121 M€, soit 5,6 % de la TVA théoriquement due (UE : 9,5 %), TVA collectée 206 049 M€ | https://taxation-customs.ec.europa.eu/taxation/vat/fight-against-vat-fraud/vat-gap_en | Conforme |
| Parts 2019 à 2023 | 6,8 ; 7,5 ; 4,2 ; 5,1 ; 5,6 % | Même série dans le fichier XLSX de la Commission (tableau 205) ; 2022 : 10 670 M€, 5,1 % | fichier XLSX joint à la page `vat-gap_en` (URL ci-dessus) | Conforme |
| Écart de TVA, composition | fraude, erreurs et faillites | « from the legal exploitation of loopholes in tax systems to evasion or organized large-scale tax fraud. Non-compliance can also be unintentional, resulting from administrative errors, omissions, non-fraudulent bankruptcies, and other factors. » | page `vat-gap_en` (relue le 09/11/2026 par le coordinateur) | Conforme |
| Colonne 2024, France (écartée) | non saisie | 16 451 M€, 7,4 % dans le XLSX ; la page HTML ne commente pas cette année | fichier XLSX (URL ci-dessus) | Non saisie : estimation rapide ou non, non établi |
| Droits rappelés | 16,1 (2015), 17,4 (2024) Md€ | « de 16,1 Md€ à 17,4 Md€, soit une progression de 8 % en euros courants » | https://www.ccomptes.fr/sites/default/files/2025-12/20251216-synthese-Lutte-contre-la-fraude-fiscale.pdf | Conforme |
| Recettes encaissées | 12,2 (2015), 11,4 (2024) Md€ | « passées de 12,2 Md€ en 2015 à 11,4 Md€ en 2024 en euros courants, avec deux points bas en 2018 et 2020 » ; « résultats » du contrôle : 20,1 (2024) contre 21,2 Md€ | https://www.ccomptes.fr/sites/default/files/2025-12/20251216-Lutte-contre-la-fraude-fiscale.pdf | Conforme |
| Fraude fiscale non estimée | « 30 ou 130 Md€ » | « Nul ne peut aujourd'hui se hasarder à affirmer que ce montant est proche de 30 ou de 130 Md€ » ; absence d'estimation fiable « quasiment sans exception » | même rapport | Conforme, avec réserve : « ce montant » est flou ; la DGFiP a une estimation pour la TVA |
| « 80 à 100 Md€ » | « affirmation gratuite », données de 2012 ou 2013, périmètre proche de l'écart fiscal | « … au minimum une approximation, voire une affirmation gratuite tant on part de loin en matière statistique » ; Solidaires, 80 à 100 Md€, au tableau 3 du rapport | https://www.ccomptes.fr/sites/default/files/2025-12/20251216-discours-PPdt-lutte-contre-la-fraude-fiscale.pdf | Conforme, avec réserve : « se rapproche davantage de l'écart fiscal que de la fraude fiscale », données « de 2012 ou de 2013 » |
| Fourchette DGFiP | 6 à 10 Md€, 4 à 5 % | « fourchette de 6 à 10 …, soit 4-5% du montant de TVA effectivement collecté » ; « est un minorant » ; 2019, stable sur dix ans ; le symbole Md€ est perdu à l'extraction, mais le HCFiPS écrit « entre 6 et 10 Md€ pour l'année 2019 » | DGFiP Analyses n° 7 (URL ci-dessus, « À savoir », 1) | Conforme, avec réserve : entreprises déclarantes seulement ; la DGFiP juge que la méthode de la Commission ne prend pas en compte « toutes les spécificités de la réglementation de la TVA » |
| Dates de publication | 2025-12-11 (Commission), 2025-12-16 (Cour, deux documents) | « Report 11 December 2025 » sur la page de la Commission ; 16/12/2025 pour la Cour (nom des fichiers et texte) | URL des trois documents | Conforme (la page de la Commission porte « Report 11 December 2025 », relu le 09/11/2026 par le coordinateur) |

**Conclusion.** Aucun chiffre du fichier n'est faux. Il n'existe aucune estimation officielle de la fraude fiscale totale ; l'écart de TVA et les sommes du contrôle fiscal ne sont pas des montants de fraude.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus. Le bilan du contrôle fiscal 2025 (economie.gouv.fr, 403) n'a pas pu être ouvert ; la DGFiP annonce des droits et pénalités notifiés en hausse de 2,8 % pour 2025 (https://www.impots.gouv.fr/actualite/publication-du-rapport-dactivite-2025-de-la-dgfip), chiffre non saisi.

## Mises à jour

- 09/11/2026 : l'affirmation « le fisc a récupéré un record de 17 milliards » est retirée de `notes/taxFraud.json` (doublon de celle du volet `taxPenalties`, gardée) ; aucun chiffre du fichier n'a changé. Le bilan du contrôle fiscal de 2025 que la page du ministère bloquait est désormais lu dans le document de politique transversale annexé au PLF 2027, par le volet `taxPenalties` ; ses montants ne sont pas saisis dans ce volet.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert les documents eux-mêmes ; l'écart de TVA de 2023 a été relu dans la page et dans le fichier XLSX de la Commission.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais. Les trois points le sont (points 1 et 2 relus dans les documents d'origine le 09/11/2026) ; les versions anglaises des notes et des affirmations ont été relues et concordent avec le français.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - citation seule : Commission européenne, Cour des comptes (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
