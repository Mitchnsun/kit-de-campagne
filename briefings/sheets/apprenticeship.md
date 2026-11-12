# `apprenticeship` · L'apprentissage (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart de valeur ; une série du rapport de recherche retirée (entrées 2018-2025, non homogène) et une autre non reprise (dépense d'aide 2019-2025, deux périmètres) ; réserves reprises ci-dessous. La licence des sources n'a pas été vérifiée (voir « Relecture »).

**Le 2e trimestre 2026.** Ce volet n'a aucune valeur du 2e trimestre 2026 : la publication de l'Insee du 10/11/2026 ne le change pas. La prochaine édition du kit remplacera les valeurs trimestrielles des volets `youthUnemployment` et `youthActivity`.

| Champ | Valeur |
| --- | --- |
| Indicateur | `apprenticeship`, dossier « Travail et retraites » (`work`), volet « Apprentissage » de la page composite `youthEmployment` (voir `youthEmployment.md`), page de type comparaison, recherche du 09/11/2026 |
| Données | `briefings/manual/apprenticeship.json`, saisi à la main le 2026-11-09 depuis les documents ci-dessous ; les apprentis de 2011 à 2023 et la part dans l'emploi des moins de 26 ans recopiés des fichiers SDMX de la BDM téléchargés par la contre-vérification |
| Sources | 1. Dares, « Emplois aidés », Emploi, chômage, revenus du travail, édition 2026 (publication de l'Insee), https://www.insee.fr/fr/statistiques/8733047, « citation seule » (chiffres de la Dares publiés par l'Insee). 2. DEPP, « L'apprentissage au 31 décembre 2025 : une baisse des effectifs de 2,8 % par rapport à 2024 », Note d'information n° 26.35, https://www.education.gouv.fr/sites/default/files/document/deppni-2026-35sifapdf-519078.pdf, « citation seule ». 3. Insee, « Apprentis au 31 décembre 2023 », https://www.insee.fr/fr/statistiques/2134441, série BDM 001775672 « Nombre total d'apprentis - France » (enquête SIFA de la DEPP), `etalab-2.0`. 4. Cour des comptes, « Les mesures d'aide exceptionnelles : une sortie de crise à achever pour le budget de l'État » (note thématique), https://www.ccomptes.fr/sites/default/files/2025-01/20250109-Les-mesures-daide-exceptionnelles-une-sortie-de-crise-a-achever-pour-le-budget-de-lEtat.pdf, « citation seule ». 5. Insee, « Part des emplois aidés dans l'emploi des jeunes de moins de 26 ans - Apprentissage » (BDM 010596076, indicateur 8.i8 des objectifs de développement durable), https://www.insee.fr/fr/statistiques/serie/010596076, page anglaise, `etalab-2.0`. 6. Cour des comptes, « Note de l'exécution budgétaire 2025, mission Travail, emploi et administration des ministères sociaux », https://www.ccomptes.fr/sites/default/files/2026-04/NEB-2026-Travail-emploi.pdf, « citation seule ». 7. DILA, entreprendre.service-public.fr, « Aides à l'embauche en contrat d'apprentissage », https://entreprendre.service-public.fr/vosdroits/F23556, « citation seule ». 8. Cour des comptes, « Rapport public annuel 2025 : les politiques publiques en faveur des jeunes », synthèses, https://www.ccomptes.fr/sites/default/files/2025-03/20250319-RPA2025-syntheses_1.pdf, « citation seule ». Huit sources, le plafond d'un fichier |
| Dates de publication | 2026-07-02 (fiche « Emplois aidés ») ; 2026-07-15 pour la DEPP (« Juillet 2026 » sur la note ; la page de la DEPP répond 403, le jour n'a pas été lu : date de la dernière modification du PDF, créé le 10/07/2026) ; 2025-10-13 (« Apprentis au 31 décembre 2023 ») ; 2025-01-09 (note de la Cour) ; 2026-05-27 (mise à jour de la série 010596076) ; 2026-04-27 pour la note d'exécution budgétaire (« Avril 2026 » sur la couverture : date du PDF) ; 2026-07-22 (« Vérifié le 22 juillet 2026 ») ; 2025-03-19 (rapport public annuel) |
| Séries | `entries` : entrées en contrat d'apprentissage (nouveaux contrats et reconductions), 2023 à 2025, figure 1a de la fiche « Emplois aidés » de l'édition 2026 seule (851 800 ; 890 300 ; 846 900, les « 851,8 ; 890,3 ; 846,9 milliers » de la fiche). `apprentices` : apprentis inscrits en CFA au 31 décembre, 2011 à 2025, 15 points (2011 à 2023 : BDM 001775672 ; 2024 et 2025 : note DEPP 26.35, figure 2 ; 436 334 en 2011, 1 049 965 en 2024, 1 020 373 en 2025). `higherShareOfNewContracts` : part du supérieur dans les nouveaux contrats du secteur privé, 2015, 2020, 2022, 2023 (33,9 ; 56,1 ; 61,2 ; 61,4), Cour des comptes d'après la Dares (seconde main). `shareOfYouthEmployment` : part de l'apprentissage dans l'emploi des moins de 26 ans, BDM 010596076, 2010 à 2024, 15 points (15,8 puis 29,5), rupture en 2020 (champ). `hiringAidSpending` : dépense d'aide à l'embauche d'apprentis, crédits de paiement du programme 103, 2024 et 2025 (3,973 et 3,435 Md€) |
| Ventilations | `levels` (31/12/2025) : enseignement supérieur 61,6 %, CAP 17,3 % (figure 2 de la note DEPP). `smallFirms` et `largeFirms` (période « 2026 », barème des contrats conclus depuis le 8 mars 2026) : moins de 250 salariés 5 000, 4 500, 2 000 € ; 250 salariés ou plus 2 000, 1 500, 750 €, selon que le diplôme préparé est de niveau 4 ou moins, de niveau 5, ou au-delà jusqu'au niveau 7 |
| Chiffre clé | 846 900 entrées en contrat d'apprentissage en 2025, en baisse (890 300 en 2024) |
| Règles | Saisie à la main. Cinq vues : « Entrées », « Apprentis », « Diplômes préparés » (supérieur et CAP parmi les apprentis, puis la part du supérieur dans les nouveaux contrats), « Part dans l'emploi », « Aide à l'embauche » (dépense, puis barème). Les entrées ne viennent que de l'édition 2026 : la série 2018-2025 du rapport, assemblée à partir de cinq éditions qui se révisent, n'est pas saisie. La dépense n'est saisie que pour 2024 et 2025, périmètre du programme 103 : les valeurs 2019-2023 viennent d'un autre document de la Cour au découpage différent. Les phrases de la Cour sur l'effet sont dans « À savoir », mot pour mot. Non saisis : les bénéficiaires de contrats de la Dares (1 015 200 fin 2025, dans une note), la part des apprentis parmi les 16-29 ans (8,5 %), le coût public total (16,5 Md€ en 2023), la contribution de l'apprentissage aux créations d'emplois, l'aide de 6 000 € pour un apprenti en situation de handicap (dans une note) |
| Première édition | À remplir à la publication |

## « À savoir »

1. La Cour des comptes, sur l'effet de l'alternance : « a augmenté de six points entre 2017 et 2023. L'essor de l'alternance explique, à lui seul, plus de la moitié de cette hausse. » ; sa note de janvier 2025 : « environ la moitié » ; elle parle d'emploi, pas de chômage. Source : rapport public annuel 2025, synthèses, page 59 du PDF (« Depuis 2017, la situation des jeunes sur le marché de l'emploi s'améliore : leur taux d'emploi a augmenté de six points entre 2017 et 2023. L'essor de l'alternance explique, à lui seul, plus de la moitié de cette hausse. ») ; note de janvier 2025, page 15 du PDF (« Le développement de l'alternance explique environ la moitié de cette hausse, l'autre moitié étant liée à l'amélioration de la conjoncture. »).
2. La Cour des comptes sur le lien de causalité, mot pour mot. Source : rapport public annuel 2025, synthèses (« Or le lien de causalité entre l'effort financier de l'État et l'amélioration de l'emploi des jeunes est incertain. D'une part, la conjoncture économique reste le principal déterminant de l'accès des jeunes à l'emploi. »).
3. Une seule édition pour les entrées (2024 : 881,0 milliers dans l'édition 2025, 890,3 dans l'édition 2026) ; inscrits en CFA (DEPP) et contrats (Dares, 1 015 200 fin 2025) à ne pas mêler. Source : fiche « Emplois aidés » de l'édition 2026, figures 1a et 1b (« Apprentissage 851,8 890,3 4,5 846,9 -4,9 » ; « Apprentissage 1 015,6 1 049,4 3,3 1 015,2 -3,3 ») ; édition 2025 (« Apprentissage 834,4 850,4 1,9 881,0 3,6 »), relue par la contre-vérification.
4. Dépense du programme 103 ; avec la ligne du programme 364 (78 M€ en 2024), 4 052 M€ (calculé) ; barème en montants maximums, proratisés ; 6 000 € au plus pour un apprenti en situation de handicap. Source : note d'exécution budgétaire, page 5 du PDF (« (3 435 M€ en 2025 contre 3 973 M€ en 2024) ») et tableau 7 (2025 : -15,6 + 3 450,9 ; 2024 : 139 + 3 835, et 78 au programme 364) ; service-public (« L'aide est octroyée uniquement pour la 1re année du contrat. Ce montant est proratisé en fonction de la durée réelle de l'apprentissage. »).

Les quatre points en anglais disent la même chose que le français ; les phrases de la Cour y sont traduites entre guillemets.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/apprenticeship.json` (clé `claims`). Source de chaque chiffre de la réponse :

1. « On entend que l'apprentissage, c'est surtout pour les CAP. » 61,6 %, 628 436 sur 1 020 373 et 17,3 % au 31 décembre 2025 : note DEPP 26.35, figure 2 (« Supérieur 657 930 628 436 - 4,5 61,6 48,3 » ; « CAP 182 804 176 204 - 3,6 17,3 28,8 » ; « Total 1 049 965 1 020 373 - 2,8 »). 33,9 % en 2015 et 61,4 % en 2023 parmi les nouveaux contrats du secteur privé : note de la Cour des comptes de janvier 2025, d'après la Dares (seconde main, dit dans la réponse : « Cour des comptes, d'après la Dares »). Le stock d'apprentis (DEPP) et les nouveaux contrats (Dares via la Cour) sont deux mesures, nommées chacune.

L'affirmation « l'apprentissage a fait baisser le chômage des jeunes » est écartée : ni démentie ni confirmée (la Cour parle du taux d'emploi et juge le lien causal « incertain »).

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-jeunes.md` : PDF retéléchargés et lus avec `pdftotext`, séries de la BDM rouvertes par l'API, éditions 2021, 2022, 2023, 2025 et 2026 de la fiche « Emplois aidés » relues.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, entrées 2025 | 846 900 | « Apprentissage 851,8 890,3 4,5 846,9 -4,9 » ; « 847 000 entrées (-5 % par rapport à 2024) » | https://www.insee.fr/fr/statistiques/8733047 | Conforme, avec réserve : une seule édition (les éditions se révisent) |
| Apprentis en CFA | 1 020 373 (2025) ; 1 049 965 (2024) | « Total 1 049 965 1 020 373 - 2,8 » ; « 1 020 400 apprentis » dans le texte | https://www.education.gouv.fr/sites/default/files/document/deppni-2026-35sifapdf-519078.pdf | Conforme |
| Apprentis 2011-2023 | 13 valeurs | BDM 001775672 relue par l'API ; +2,8 % de 2023 à 2024 cohérent avec la DEPP (calculé) | https://www.insee.fr/fr/statistiques/serie/001775672 | Conforme, avec réserve : deux publications de la même enquête SIFA |
| Part du supérieur | 61,6 % ; CAP 17,3 % | 628 436 / 1 020 373 = 61,6 % (refait) ; « majoritaires (62 %) » | note DEPP (URL ci-dessus) | Conforme |
| Nouveaux contrats | 33,9 / 56,1 / 61,2 / 61,4 % | « de 33,9 % des nouveaux contrats en 2015 à 56,1 % en 2020, 61,2 % en 2022 et 61,4 % en 2023 » | https://www.ccomptes.fr/sites/default/files/2025-01/20250109-Les-mesures-daide-exceptionnelles-une-sortie-de-crise-a-achever-pour-le-budget-de-lEtat.pdf | Conforme, avec réserve : seconde main (Dares via la Cour), secteur privé |
| Part dans l'emploi des moins de 26 ans | 15 valeurs, 29,5 % en 2024 | BDM 010596076 `2024 29.5 DEF` ; fiche 8.i8 : « rupture de série à partir du millésime 2020 » | https://www.insee.fr/fr/statistiques/serie/010596076 | Conforme, avec réserve : rupture de champ en 2020 |
| Dépense d'aide à l'embauche | 3,435 et 3,973 Md€ | « (3 435 M€ en 2025 contre 3 973 M€ en 2024) » ; tableau 7 refait | https://www.ccomptes.fr/sites/default/files/2026-04/NEB-2026-Travail-emploi.pdf | Conforme, avec réserve : programme 103 seul |
| Barème | 6 montants | Onglet « Depuis le 8 mars 2026 » ; montants maximums, 1re année, proratisés | https://entreprendre.service-public.fr/vosdroits/F23556 | Conforme, avec réserve : décret n° 2026-168 non ouvert (Légifrance inaccessible) |
| Phrases de la Cour | citations | Relues dans le rapport public annuel 2025 (p. 59 du PDF) et la note de janvier 2025 (p. 15) | URL des sources 4 et 8 | Conforme |

**Conclusion.** Aucun chiffre du fichier n'est faux ; aucune série n'assemble plusieurs éditions ou plusieurs périmètres.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus. Inaccessibles : la publication de la Dares sur l'apprentissage en 2024 (« Request Rejected »), la page de la note DEPP (403), Légifrance.

## Réserves

- La série homogène des entrées 2018-2025 est dans la publication de la Dares, que le site de la Dares refusait aux scripts : à ouvrir par le PO avant d'allonger la série.
- La Cour des comptes parle du taux d'emploi des jeunes, pas du chômage ; ses deux documents disent « plus de la moitié » et « environ la moitié » : la page cite l'un et l'autre sans arbitrer. En 2022, elle écrivait aussi : « L'effet net sur l'emploi en volume est donc vraisemblablement faible. » (non repris dans les notes).
- Le barème donne des maximums ; le décret n'a pas été lu.
- L'indicateur 8.i8 rapporte des contrats (source administrative) à l'emploi mesuré par l'enquête Emploi, et change de champ en 2020.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert les documents et la BDM.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Insee : Licence Ouverte 2.0, mention « Source : Insee » et date de dernière mise à jour (https://www.insee.fr/fr/information/2008466) ;
  - citation seule : Dares, DEPP, Cour des comptes, DILA, entreprendre.service-public.fr (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
