# `productionTaxes` · Les impôts de production, qui ne sont pas des aides (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart de valeur ; réserves de lecture reprises ci-dessous (périmètres différents de la DGFiP et du rapport du Gouvernement, CVAE nette du dégrèvement). La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `productionTaxes`, dossier « Économie et fiscalité » (`economy`), volet « Impôts de production » de la page composite `businessAid` (voir `businessAid.md`), page de type comparaison, recherche du 09/11/2026. Ces chiffres ne sont pas des aides : le volet sert à situer les mesures du jeu `businessPact` et `productionTax` |
| Données | `briefings/manual/productionTaxes.json`, saisi à la main le 2026-11-09 depuis la DGFiP Statistiques n° 47 (texte, graphique 1 et tableau 1, relus dans le PDF et le classeur) et le rapport annexé au projet de loi de finances pour 2027 (encadré p. 13-14, pour une note) |
| Sources | 1. DGFiP, « Les impôts de production en 2024, DGFiP Statistiques n° 47 », https://www.impots.gouv.fr/dgfip-statistiques-les-impots-de-production-en-2024, PDF https://www.impots.gouv.fr/sites/default/files/media/9_statistiques/0_etudes_et_stats/0_publications/dgfip_statistiques/2026/num47_05/dgfip_stat47_2026.pdf, en français seulement, licence « citation seule ». 2. Assemblée nationale, « Rapport relatif aux aides publiques aux entreprises, annexe au projet de loi de finances pour 2027 » (voir `aidAmounts.md`), licence `etalab-1.0` |
| Dates de publication | 2026-05-19 (DGFiP, « Publié le 19/05/2026 » sur sa page ; le PDF porte « Mai 2026 ») ; 2026-10-12 (rapport du Gouvernement, date du PDF) |
| Séries | `productionTaxes` : impôts de production collectés auprès des entreprises qui ont un numéro Siren, Md€, 2019 à 2024, 6 points (91,2 ; 88,7 ; 83,1 ; 90,1 ; 92,9 ; 96), graphique 1. `valueAddedShare` : leur part de la valeur ajoutée déclarée, %, 2019 à 2024 (5,5 ; 5,7 ; 4,5 ; 4,7 ; 4,5 ; 4,4). `gdpShare` : leur part du PIB, %, 2019 et 2024 (3,7 ; 3,3), du texte |
| Ventilations | `cvaeC3s` : 2024, CVAE nette du dégrèvement de plafonnement 3,0 Md€, contribution sociale de solidarité des sociétés 5,3 Md€ (tableau 1) |
| Chiffre clé | 96,0 Md€ d'impôts de production en 2024 (le classeur écrit 96 dans une colonne au dixième), en hausse (92,9 en 2023) ; à côté, leur part du PIB, 3,3 % |
| Règles | Saisie à la main. Une vue : la série de la DGFiP, puis la CVAE et la C3S de 2024 ; le tableau avec la part de la valeur ajoutée et celle du PIB. Le titre du volet et la note de son premier bloc disent que ce ne sont pas des aides. Les 86,8 Md€ du rapport du Gouvernement (définition d'Eurostat) sont dans une note, jamais dans une série à côté des 96 Md€. Les rapports de 50 Md€ aux impôts de production et aux périmètres d'aides sont dans une note, avec « calculé ». Non saisis : la décomposition du tableau 1 par assiette et par impôt (hors CVAE et C3S), les valeurs de 2023 de la CVAE et de la C3S (4,0 et 4,8), la décomposition des 86,8 Md€ du graphique 1 du rapport (elle fait 86,1 Md€ : non reprise), les prélèvements directs des entreprises (15,8 % du PIB), l'opération D29 d'Eurostat (déjà sur la page « Climat des affaires », ménages propriétaires compris), la phrase de la DGFiP qui écrit 3 % du PIB pour 2023 et 2024 (contradictoire avec les 3,3 % de sa synthèse) |
| Première édition | À remplir à la publication |

## « À savoir »

1. Les impôts de production sont payés par les entreprises : ce ne sont pas des aides. La DGFiP compte ceux des entreprises qui ont un numéro Siren, sans la taxe foncière des ménages. Selon elle, ils font 3,3 % du PIB et 4,4 % de la valeur ajoutée des entreprises en 2024, contre 3,7 % et 5,5 % en 2019. Source : DGFiP Statistiques n° 47 (« En 2024, 96 Md€ d'impôts de production ont été collectés. Ces impôts représentent ainsi en 2024 3,3 % du PIB en valeur et 4,4 % de la valeur ajoutée des entreprises » ; « en 2019, année précédant la réforme des impôts de production, ces derniers représentaient 3,7 % du PIB en valeur et 5,5 % de la valeur ajoutée déclarée » ; champ du classeur : « l'ensemble des entreprises et sociétés disposnt d'un numéro SIREN » ; tableau 1, note 3 : « ll s'agit seulement de la taxe foncière des entreprises »).
2. Le rapport du Gouvernement annexé au projet de loi de finances pour 2027 compte, selon la définition d'Eurostat, 86,8 Md€ d'impôts sur la production payés par les entreprises en 2024, soit 2,9 % du PIB, contre 1,4 % dans la zone euro : un autre périmètre que celui de la DGFiP. Source : rapport du Gouvernement, encadré p. 13-14 et tableau 1 (« Les impôts sur la production payés par les entreprises (86,8 Md€) sont pour plus de la moitié assis sur la masse salariale »).
3. Ordres de grandeur, calculés : 50 Md€ font 52 % des impôts de production de la DGFiP (96 Md€) et 58 % de ceux du rapport du Gouvernement (86,8 Md€) ; côté aides, 84 % du périmètre socle (59,8 Md€) et 30 % de l'élargi (166,1 Md€), en 2024. Le socle compte le CIR, l'élargi aussi les allègements généraux. Source : calcul de la recherche vérifiée (`calculBusinessPact` : 50 / 96 = 0,521 ; 50 / 86,8 = 0,576 ; 50 / 59,8 = 0,836 ; 50 / 166,1 = 0,301), sur les chiffres de la DGFiP et du rapport du Gouvernement ; aucune source officielle ne fait ce rapprochement. Les 50 Md€ sont ceux de la mesure du jeu « Un pacte avec les entreprises », une hypothèse du jeu : la note ne la juge pas.
4. La CVAE de la DGFiP est nette du dégrèvement lié au plafonnement de la contribution économique territoriale : ce n'est pas son rendement pour l'État dans les documents budgétaires. La loi de finances pour 2025 fixe son taux maximal à 0,28 % en 2026 et 2027, puis à 0 % en 2030. Source : DGFiP Statistiques n° 47, tableau 1, note 2 (« Net du dégrèvement résultant du plafonnement de la Contribution économique territoriale (CET) dans la valeur ajoutée ») ; calendrier : DGFiP Statistiques n° 47, encadré 2 (« La loi de finances pour 2025 a prévu la suppression totale de la CVAE pour 2030. » ; taux d'imposition maximal : 0,28 en 2026 et en 2027, 0 en 2030), précaution de la recherche vérifiée.

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Aucune affirmation : voir `businessAid.md`.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-aides.md` : PDF et classeur de la DGFiP retéléchargés, rapport du Gouvernement relu sur la page rendue.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, 2024 | 96 Md€ | texte et classeur : 96 ; 3,3 % du PIB | DGFiP Statistiques n° 47 (URL ci-dessus) | Conforme |
| Série 2019 à 2023 | 91,2 ; 88,7 ; 83,1 ; 90,1 ; 92,9 | graphique 1 du PDF et du classeur | idem | Conforme |
| Part de la valeur ajoutée | 5,5 ; 5,7 ; 4,5 ; 4,7 ; 4,5 ; 4,4 % | graphique 1 du classeur | idem | Conforme |
| CVAE, C3S 2024 | 3,0 ; 5,3 Md€ | « Contribution sur la valeur ajoutée des entreprises2 4,0 3,0 -24,7 -78,7 » ; « Contribution sociale de solidarité sur les sociétés 4,8 5,3 9,0 35,3 » | idem, tableau 1 | Conforme, avec réserve : CVAE nette du dégrèvement |
| 86,8 Md€ du rapport du Gouvernement | note 2 | 86,8 Md€ et 2,9 % du PIB dans le texte ; la décomposition du graphique 1 fait 86,1 : non reprise | rapport du Gouvernement | Conforme, avec réserve |
| Ordres de grandeur pour 50 Md€ | note 3 | calculs refaits | — | Calculé, dit « calculé » |

**Conclusion.** Aucun chiffre du fichier n'est faux ; les impôts de production ne sont jamais présentés comme des aides, ni les deux périmètres mêlés.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus.

## Réserves

- Les 96 Md€ de la DGFiP (entreprises qui ont un numéro Siren), les 86,8 Md€ du rapport du Gouvernement (comptabilité nationale, définition d'Eurostat) et l'opération D29 d'Eurostat (4,4 % du PIB en 2025, ménages propriétaires compris) sont trois périmètres différents.
- La DGFiP écrit aussi que le poids de ces impôts dans le PIB « est resté stable entre 2023 et 2024, à 3 % » : contradictoire avec les 3,3 % de sa synthèse ; seuls 3,3 % (2024) et 3,7 % (2019), dans les chiffres vérifiés, sont saisis.
- La réduction de 50 Md€ et la suppression d'autant d'aides sont la mesure du jeu, pas un chiffre officiel ; les aides supprimables dépendent du périmètre retenu.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert le PDF et le classeur.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
