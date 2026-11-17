# `teacherPay` · Le salaire des enseignants (partie de la page « PISA, sortants précoces, budget et salaires », saisie à la main)

**Vérifiée le 17/11/2026** : les valeurs saisies sont celles de la figure 1 de la note, relue dans le PDF, et celles de l'API de l'OCDE, relue par un script Python ; la presse du jour de publication et le chapitre de l'OCDE les recoupent (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `teacherPay`, quatrième volet de la page `schools`, dossier « Éducation » (`education`), page de type comparaison, recherche du 17/11/2026 (#21) |
| Données | `briefings/manual/teacherPay.json`, saisi le 2026-11-17 depuis le PDF (guide 8 de l'app : le fichier de données de la note n'a pas été trouvé, les pages de la DEPP répondent 403 aux scripts ; les noms de fichier essayés sur le modèle des autres notes répondent 404) ; les ratios de l'OCDE, saisis le même jour depuis la réponse de son API SDMX (un indicateur est soit écrit par un script, soit saisi à la main : ceux de la DEPP n'ayant pas de script, ceux de l'OCDE sont saisis avec eux) |
| Source | DEPP, Note d'Information n° 26.36, août 2026, « L'évolution du salaire des enseignants fonctionnaires ou assimilés entre 2023 et 2024 », https://www.education.gouv.fr/sites/default/files/document/depp-ni-2026-36pdf-519727.pdf (page https://www.education.gouv.fr/depp/l-evolution-du-salaire-des-enseignants-fonctionnaires-ou-assimiles-entre-2023-et-2024-505401), figure 1, page 1 ; publiée le jeudi 20/08/2026 selon la presse (L'Info durable du 20/08/2026 : « publiée jeudi » ; fichier PDF créé le 05/08/2026) ; licence : voir `schools.md` |
| Source 2 | OCDE, « Salaires effectifs des enseignants relatif à la rémunération des actifs occupés » (flux `OECD.EDU.IMEP,DSD_EAG_SAL_ACT@DF_TCH_REL`, version 2.1, Regards sur l'éducation 2026, publié le 29/09/2026), https://data-explorer.oecd.org/vis?lc=fr&df[ds]=DisseminateFinal&df[id]=DSD_EAG_SAL_ACT%40DF_TCH_REL&df[ag]=OECD.EDU.IMEP ; requête https://sdmx.oecd.org/public/rest/data/OECD.EDU.IMEP,DSD_EAG_SAL_ACT@DF_TCH_REL,/FRA+OECD+EU25.SAL_ACT_REL_TER..INST_EDU_PUB.ISCED11_1+ISCED11_24+ISCED11_34.Y25T64._T...... (CSV) ; licence CC BY 4.0 aux conditions de l'OCDE (`oecd`, PO, 17/11/2026), https://www.oecd.org/fr/about/terms-conditions.html |
| Séries | `meanNetPay` : 3 090 € (2024) ; `fullTimeNetPay` : 3 180 € (2024) ; répartitions de 2024 par corps (`schoolTeachers`, `certified`, `physicalEducation`, `vocational`, `agreges`, `all`) : `byBody` (ensemble), `byBodyFullTime`, `byBodyPartTime` (en euros nets mensuels), `shareOfTeachers` (structure, en %) ; répartitions de l'OCDE (ratio, deux décimales comme l'attribut `DECIMALS` de l'OCDE) par niveau (`primary` ISCED11_1, `lowerSecondary` ISCED11_24, `upperSecondary` ISCED11_34), mesure `SAL_ACT_REL_TER`, établissements publics, enseignants de 25 à 64 ans, deux sexes : `oecdRatioFrance` (2023 : 0,81, 0,90, 0,98), `oecdRatioOecd` (2025 : 0,87, 0,90, 0,94), `oecdRatioEu` (UE à 25, 2025 : 0,83, 0,86, 0,91). La période est l'attribut `REF_PERIOD` (« Reference period » des salaires) ; les rémunérations des diplômés sont de l'année `BASE_PER` (« Reference year of earnings data » : 2022 pour la France, 2024 pour les moyennes). Le flux n'a pas de dimension de temps |
| Chiffre clé | 3 090 € nets par mois en 2024 ; pas de tendance (une seule année : la note avertit que ses niveaux ne se comparent pas à ceux de la publication précédente) |
| Règles | Les colonnes de la figure 1, sans calcul ; la part des enseignants à temps complet par corps (88,9 % à 93,6 %) n'est pas reprise ; la structure ne fait pas 100,0 (99,9) : d'autres corps (PEGC, adjoints d'enseignement) sont dans l'ensemble |
| Première édition | À remplir à la publication |

À actualiser : à la note suivante de la DEPP (août ou septembre) ; chercher alors son fichier « données » pour un script.

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
| Chiffre clé | 3 090 € | « 3.090 euros nets » | https://www.linfodurable.fr/les-enseignants-gagnaient-en-moyenne-3090-euros-en-2024-selon-une-etude-58660 (20/08/2026) | Conforme |
| Temps complet, ensemble | 3 180 € | « 3.180 euros nets » | même article | Conforme |
| Agrégés, temps complet | 4 190 € | 4 190 € | même article | Conforme |
| Certifiés, temps complet | 3 220 € | 3 220 € | même article | Conforme |
| Professeurs des écoles, temps complet | 2 950 € | 2 950 € | même article | Conforme |
| Évolution en euros constants | + 4,3 % (note) | « une hausse de 4,3% » | même article | Conforme |
| Ratios de l'OCDE, moyennes 2025 | 0,87 (primaire), 0,90 (collège), 0,94 (lycée général) | « 87-95% of the average earnings of tertiary-educated workers » au primaire et dans le secondaire général | OCDE, Education at a Glance 2026, « How much are teachers and school heads paid? » (https://www.oecd.org/en/publications/education-at-a-glance-2026_b4968bbc-en/full-report/how-much-are-teachers-and-school-heads-paid_a6233c97), d'après un résumé de moteur (page 403) | Conforme (le haut de la fourchette, 95 %, n'est pas lu ici : 0,9405 arrondi à 0,94) |
| Ratios de la France | 0,81 ; 0,90 ; 0,98 (2023) | Les mêmes valeurs (0,81 au primaire, 0,90 au collège) lues dans l'API par la recherche du 17/11/2026, autre requête ; l'édition 2025 parle d'enseignants du primaire payés « 26 % de moins » que les diplômés du supérieur en 2024, un autre millésime et peut-être une autre mesure | Recherche de l'agent ; résumé de moteur sur l'édition 2025 (https://www.oecd.org/fr/publications/regards-sur-l-education-2025_b26d545c-fr/full-report/how-much-are-teachers-and-school-heads-paid_5daf5678.html) | Écart expliqué (édition et année différentes) ; le chiffre de 2023 reste à lire dans le tableau D3 de l'édition 2026 |

**Conclusion.** Conforme ; les ratios de la France restent à recouper dans le tableau D3 de Regards sur l'éducation 2026.

**Pages consultées** le 17/11/2026 : celles du tableau.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
