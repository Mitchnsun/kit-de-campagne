# `teacherPay` · Le salaire des enseignants (partie de la page « PISA, sortants précoces, budget et salaires », saisie à la main)

**Vérifiée le 17/11/2026** : les valeurs saisies sont celles de la figure 1 de la note, relue dans le PDF ; la presse du jour de publication donne les mêmes (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `teacherPay`, quatrième volet de la page `schools`, dossier « Éducation » (`education`), page de type comparaison, recherche du 17/11/2026 (#21) |
| Données | `briefings/manual/teacherPay.json`, saisi le 2026-11-17 depuis le PDF (guide 8 de l'app : le fichier de données de la note n'a pas été trouvé, les pages de la DEPP répondent 403 aux scripts ; les noms de fichier essayés sur le modèle des autres notes répondent 404) |
| Source | DEPP, Note d'Information n° 26.36, août 2026, « L'évolution du salaire des enseignants fonctionnaires ou assimilés entre 2023 et 2024 », https://www.education.gouv.fr/sites/default/files/document/depp-ni-2026-36pdf-519727.pdf (page https://www.education.gouv.fr/depp/l-evolution-du-salaire-des-enseignants-fonctionnaires-ou-assimiles-entre-2023-et-2024-505401), figure 1, page 1 ; publiée le jeudi 20/08/2026 selon la presse (L'Info durable du 20/08/2026 : « publiée jeudi » ; fichier PDF créé le 05/08/2026) ; licence : voir `schools.md` |
| Séries | `meanNetPay` : 3 090 € (2024) ; `fullTimeNetPay` : 3 180 € (2024) ; répartitions de 2024 par corps (`schoolTeachers`, `certified`, `physicalEducation`, `vocational`, `agreges`, `all`) : `byBody` (ensemble), `byBodyFullTime`, `byBodyPartTime` (en euros nets mensuels), `shareOfTeachers` (structure, en %) |
| Chiffre clé | 3 090 € nets par mois en 2024 ; pas de tendance (une seule année : la note avertit que ses niveaux ne se comparent pas à ceux de la publication précédente) |
| Règles | Les colonnes de la figure 1, sans calcul ; la part des enseignants à temps complet par corps (88,9 % à 93,6 %) n'est pas reprise ; la structure ne fait pas 100,0 (99,9) : d'autres corps (PEGC, adjoints d'enseignement) sont dans l'ensemble |
| Première édition | À remplir à la publication |

À actualiser : à la note suivante de la DEPP (août ou septembre) ; chercher alors son fichier « données » pour un script.

## « À savoir »

1. Le champ et les contractuels : encadré « Avertissement », page 1 (« Cette Note d'Information porte uniquement sur les enseignants fonctionnaires [...] ou assimilés », « Les enseignants contractuels [...] qui représentent 8 % du total des enseignants en 2024 en sont exclus », « ils perçoivent en moyenne 2 130 euros nets par mois en 2024 ») ; « Champ : France hors Mayotte, public + privé sous contrat ».
2. L'écart avec l'Insee : page 1 (« Dans l'Insee Première n° 2100 [...] publiée en mai 2026, le salaire moyen des enseignants en 2024 est de 3 190 euros nets mensuels, contre 3 090 euros ici. Les écarts proviennent de différences de champ et de calcul »).
3. L'évolution : résumé, page 1 (+ 6,4 % en euros courants, + 4,3 % en euros constants, inflation de 2,0 %, « principalement par la croissance des primes ») ; avertissement (« pas directement comparables, en niveau, à ceux de la publication réalisée sur le millésime antérieur. Les données de l'année 2023 ont cependant été recalculées »).
4. Les écarts entre corps : résumé (« 1,4 fois plus que les professeurs des écoles ») ; page 1 (primes « en moyenne 16 % du salaire brut d'un enseignant du premier degré et 21 % de celui d'un enseignant du second degré »).

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

**Conclusion.** Conforme.

**Pages consultées** le 17/11/2026 : celles du tableau.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
