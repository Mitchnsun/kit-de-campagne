# `teacherPay` · Le salaire des enseignants (partie de la page « PISA, sortants précoces, budget et salaires »)

**Vérifiée le 18/11/2026** : le fichier du script concorde avec le PDF de la note (figure 1) et avec une lecture indépendante du fichier de données (Python, openpyxl) ; la presse du jour de publication et le chapitre de l'OCDE recoupent les chiffres clés (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `teacherPay`, quatrième volet de la page `schools`, dossier « Éducation » (`education`), page de type comparaison, recherche du 17/11/2026 (#21) |
| Données | `briefings/data/teacherPay.json`, écrit par `yarn briefings teacherPay` le 2026-11-18 (il était saisi à la main depuis le PDF le 17/11/2026, le fichier de données n'ayant pas été trouvé ; le compte rendu de la page lue pour le PO le 18/11/2026 en donne l'adresse : mêmes valeurs) |
| Source | DEPP, Drégoir M., 2026, « L’évolution du salaire des enseignants fonctionnaires ou assimilés entre 2023 et 2024 », Note d'Information n° 26-36 (« n° 26.36 » dans le PDF et le fichier), publiée le 20/08/2026 (date affichée sur la page, lue pour le PO le 18/11/2026 ; le PDF a été créé le 05/08/2026) ; page https://www.education.gouv.fr/depp/l-evolution-du-salaire-des-enseignants-fonctionnaires-ou-assimiles-entre-2023-et-2024-505401 (en français seulement : `hreflang="fr"`, aucune version anglaise) ; PDF https://www.education.gouv.fr/sites/default/files/document/depp-ni-2026-36pdf-519727.pdf ; fichier de données https://www.education.gouv.fr/sites/default/files/document/depp-ni-2026-26-36-donneesxlsx-519733.xlsx (14 onglets, « Figure 1 » ; certains noms d'onglet finissent par une espace, « Figure 6 - Web », « Figure 8 - Web ») ; DOI https://doi.org/10.48464/ni-26-36 (le registre n'a pas de champ DOI : il est dans son commentaire) ; licence : aucune sur la page ni dans le fichier, seul le pied de page du site, « Sauf mention contraire, tous les contenus de ce site sont sous licence etalab-2.0 » (Licence Ouverte 2.0) |
| Source 2 | OCDE, « Salaires effectifs des enseignants relatif à la rémunération des actifs occupés » (flux `OECD.EDU.IMEP,DSD_EAG_SAL_ACT@DF_TCH_REL`, version 2.1, Regards sur l'éducation 2026, publié le 29/09/2026), https://data-explorer.oecd.org/vis?lc=fr&df[ds]=DisseminateFinal&df[id]=DSD_EAG_SAL_ACT%40DF_TCH_REL&df[ag]=OECD.EDU.IMEP ; requête https://sdmx.oecd.org/public/rest/data/OECD.EDU.IMEP,DSD_EAG_SAL_ACT@DF_TCH_REL,/FRA+OECD+EU25.SAL_ACT_REL_TER..INST_EDU_PUB.ISCED11_1+ISCED11_24+ISCED11_34.Y25T64._T...... (CSV) ; licence CC BY 4.0 aux conditions de l'OCDE (`oecd`, PO, 17/11/2026), https://www.oecd.org/fr/about/terms-conditions.html |
| Séries | `meanNetPay` : 3 090 € (2024) ; `fullTimeNetPay` : 3 180 € (2024) ; répartitions de 2024 par corps (`schoolTeachers`, `certified`, `physicalEducation`, `vocational`, `agreges`, `all`) : `byBody` (ensemble), `byBodyFullTime`, `byBodyPartTime` (en euros nets mensuels), `shareOfTeachers` (structure, en %) ; répartitions de l'OCDE (ratio, deux décimales comme l'attribut `DECIMALS` de l'OCDE) par niveau (`primary` ISCED11_1, `lowerSecondary` ISCED11_24, `upperSecondary` ISCED11_34), mesure `SAL_ACT_REL_TER`, établissements publics, enseignants de 25 à 64 ans, deux sexes : `oecdRatioFrance` (2023 : 0,81, 0,90, 0,98), `oecdRatioOecd` (2025 : 0,87, 0,90, 0,94), `oecdRatioEu` (UE à 25, 2025 : 0,83, 0,86, 0,91). La période est l'attribut `REF_PERIOD` (« Reference period » des salaires) ; les rémunérations des diplômés sont de l'année `BASE_PER` (« Reference year of earnings data » : 2022 pour la France, 2024 pour les moyennes). Le flux n'a pas de dimension de temps |
| Chiffre clé | 3 090 € nets par mois en 2024 ; pas de tendance (une seule année : la note avertit que ses niveaux ne se comparent pas à ceux de la publication précédente) |
| Règles | Le script lit l'onglet « Figure 1 » : il exige le titre « Répartition des salaires nets moyens et des enseignants selon leur corps, en <année> », les intitulés de colonnes sur la dernière ligne d'en-tête (exceljs répète un en-tête fusionné dans chaque cellule qu'il couvre), les cinq corps et « Ensemble1 », le champ « France hors Mayotte », des salaires de 1 000 à 10 000 € et des parts de 0 à 100 ; il arrondit les parts au dixième comme la note (le fichier a les valeurs non arrondies, 47,6047959847569) et garde les salaires tels quels. La part des enseignants à temps complet par corps (88,9 % à 93,6 %) n'est pas reprise ; la structure ne fait pas 100,0 (99,9) : d'autres corps (PEGC, adjoints d'enseignement) sont dans l'ensemble. L'API de l'OCDE : il exige les colonnes et les codes fixes (mesure, unité, public, 25-64 ans, deux sexes, enseignants), un ratio de 0,3 à 2 par zone et par niveau, une seule année par zone, et réessaie une erreur 500 du serveur |
| Première édition | À remplir à la publication |

À actualiser : à la note suivante de la DEPP (août ou septembre) : changer l'adresse du fichier et la date dans `DEPP` du script ; à chaque Regards sur l'éducation (septembre) : la date dans `OECD`.

## « À savoir »

1. Le champ et les contractuels : encadré « Avertissement », page 1 (« Cette Note d'Information porte uniquement sur les enseignants fonctionnaires [...] ou assimilés », « Les enseignants contractuels [...] qui représentent 8 % du total des enseignants en 2024 en sont exclus », « ils perçoivent en moyenne 2 130 euros nets par mois en 2024 ») ; « Champ : France hors Mayotte, public + privé sous contrat ».
2. L'écart avec l'Insee : page 1 (« Dans l'Insee Première n° 2100 [...] publiée en mai 2026, le salaire moyen des enseignants en 2024 est de 3 190 euros nets mensuels, contre 3 090 euros ici. Les écarts proviennent de différences de champ et de calcul »).
3. L'évolution : résumé, page 1 (+ 6,4 % en euros courants, + 4,3 % en euros constants, inflation de 2,0 %, « principalement par la croissance des primes ») ; avertissement (« pas directement comparables, en niveau, à ceux de la publication réalisée sur le millésime antérieur. Les données de l'année 2023 ont cependant été recalculées »).
3 bis. Les écarts entre corps (fusionnés au point 3 le 17/11/2026) : résumé (« 1,4 fois plus que les professeurs des écoles »).
4. L'OCDE : réponse de l'API (voir « Source 2 ») ; les années différentes sont celles de l'attribut `REF_PERIOD`.

## Double vérification

Faite le 17/11/2026 par un agent Claude (modèle Opus) par la recherche web.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Fichier de données, figure 1 | les 24 valeurs de salaire et les 6 parts | Identiques, lues dans le classeur par un script Python (openpyxl) ; identiques au compte rendu de la page lue pour le PO le 18/11/2026 (3 090 € et 3 180 € « confirmé ») et au PDF, figure 1 | https://www.education.gouv.fr/sites/default/files/document/depp-ni-2026-26-36-donneesxlsx-519733.xlsx | Conforme |
| Évolutions sur 2023 | + 6,4 % courants, + 4,3 % constants (notes « À savoir ») | Les mêmes sur la page ; aucune évolution par corps dans la figure 1 | Compte rendu du 18/11/2026 | Conforme |
| Chiffre clé | 3 090 € | « 3.090 euros nets » | https://www.linfodurable.fr/les-enseignants-gagnaient-en-moyenne-3090-euros-en-2024-selon-une-etude-58660 (20/08/2026) | Conforme |
| Temps complet, ensemble | 3 180 € | « 3.180 euros nets » | même article | Conforme |
| Agrégés, temps complet | 4 190 € | 4 190 € | même article | Conforme |
| Certifiés, temps complet | 3 220 € | 3 220 € | même article | Conforme |
| Professeurs des écoles, temps complet | 2 950 € | 2 950 € | même article | Conforme |
| Évolution en euros constants | + 4,3 % (note) | « une hausse de 4,3% » | même article | Conforme |
| Ratios de l'OCDE, moyennes 2025 | 0,87 (primaire), 0,90 (collège), 0,94 (lycée général) | « 87-95% of the average earnings of tertiary-educated workers » au primaire et dans le secondaire général | OCDE, Education at a Glance 2026, « How much are teachers and school heads paid? » (https://www.oecd.org/en/publications/education-at-a-glance-2026_b4968bbc-en/full-report/how-much-are-teachers-and-school-heads-paid_a6233c97), d'après un résumé de moteur (page 403) | Conforme (le haut de la fourchette, 95 %, n'est pas lu ici : 0,9405 arrondi à 0,94) |
| Ratios de la France | 0,81 ; 0,90 ; 0,98 (2023) | Les mêmes valeurs (0,81 au primaire, 0,90 au collège) lues dans l'API par la recherche du 17/11/2026, autre requête ; l'édition 2025 parle d'enseignants du primaire payés « 26 % de moins » que les diplômés du supérieur en 2024, un autre millésime et peut-être une autre mesure | Recherche de l'agent ; résumé de moteur sur l'édition 2025 (https://www.oecd.org/fr/publications/regards-sur-l-education-2025_b26d545c-fr/full-report/how-much-are-teachers-and-school-heads-paid_5daf5678.html) | Écart expliqué (édition et année différentes) ; le chiffre de 2023 reste à lire dans le tableau D3 de l'édition 2026 |

**Conclusion.** Conforme ; les ratios de la France restent à recouper dans le tableau D3 de Regards sur l'éducation 2026.

**Pages consultées** le 17/11/2026 et le 18/11/2026 : celles du tableau.

## Mises à jour

- **18/11/2026** : le compte rendu de la page de la note, lue pour le PO, donne le titre, le numéro (« n° 26-36 »), la référence bibliographique, la date affichée, le DOI, le fichier de données et la licence du site ; l'indicateur passe d'une saisie à la main au script `teacherPay.ts` (fichier de données de la DEPP et API de l'OCDE), mêmes valeurs ; `briefings/manual/teacherPay.json` est supprimé.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
