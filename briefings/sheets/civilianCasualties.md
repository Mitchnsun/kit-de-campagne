# `civilianCasualties` · Victimes civiles en Ukraine (saisi à la main)

**Vérifiée le 11/11/2026** : le PDF a été rouvert (`pdftotext`) et chaque chiffre contrôlé ; la presse ne donne pas les cumuls (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `civilianCasualties`, dossier « Défense et Europe » (`defence`), page de type comparaison, ticket #349 de l'app |
| Données | `briefings/manual/civilianCasualties.json`, saisi à la main le 2026-11-11 depuis la mise à jour de septembre 2026 de « Protection of Civilians in Armed Conflict » |
| Sources | Mission de surveillance des droits de l'homme des Nations unies en Ukraine (HRMMU), HCDH, « Protection of Civilians in Armed Conflict — September 2026 », publié le 16/10/2026 (date de la page), page https://ukraine.un.org/en/324561-protection-civilians-armed-conflict-%E2%80%94-september-2026, PDF https://ukraine.un.org/en/download/218480/324561 (5 pages), aucune licence indiquée (« © Copyright 2026 United Nations in Ukraine »), citation seule |
| Séries | `killed`, `injured`, `casualties` : depuis le 24 février 2022, un point (2026-09) : 17 605 ; 55 846 ; 73 451 (page « Civilian casualties since 24 February 2022 ») ; `killedByYear`, `injuredByYear` : par année, 2022 à 2026 (2026 : janvier à septembre), 5 points chacune (tués 8 423 ; 1 975 ; 2 088 ; 2 549 ; 2 570 ; blessés 12 670 ; 6 651 ; 9 138 ; 12 176 ; 15 211) (page « 1. By year ») |
| Chiffre clé | 17 605 civils tués depuis le 24 février 2022 (septembre 2026), sans tendance saisie ; à côté, les blessés et le total |
| Règles | Saisie à la main. Le PDF ne porte pas la mention « au moins » sur ces cumuls (elle est sur les chiffres de septembre) ; la page dit « minimum vérifié » et reprend la réserve de l'ONU. Le PDF ne dit pas « au 30 septembre » : c'est la mise à jour de septembre 2026, avec les chiffres de janvier à septembre pour 2026. Les chiffres par année ne sont pas écrits en toutes lettres dans le texte extrait : le graphique « By year » donne les deux colonnes, rapprochées par somme (tués 8 423 + 1 975 + 2 088 + 2 549 + 2 570 = 17 605 ; blessés 12 670 + 6 651 + 9 138 + 12 176 + 15 211 = 55 846) et par le texte (2026 : 2 570 tués, 15 211 blessés) |
| Première édition | À remplir à la publication |

## « À savoir »

1. 17 605 tués, 55 846 blessés, 73 451 en tout depuis le 24 février 2022, publiés le 16/10/2026. Source : PDF, page « Civilian casualties since 24 February 2022 » ; page de la publication (« 16 October 2026 »).
2. Réserve de l'ONU : « The actual extent of civilian harm – both casualties and infrastructure damage – is likely considerably higher as many reports of civilian harm, particularly from the period immediately after the full-scale armed attack of 24 February 2022, have not been possible to verify due to the large number of reports and the lack of access to relevant areas. » Source : PDF, page « The UN Human Rights Monitoring Mission in Ukraine ».
3. Seuls les civils, cas vérifiés selon la norme « reasonable grounds to believe » ; chiffres révisables (note 3 : la hausse d'une mise à jour peut venir de cas antérieurs confirmés). Source : PDF, même page et note 3.
4. Septembre 2026 : 18 tués et 44 blessés en territoire occupé inclus dans les chiffres vérifiés ; déclarations russes d'au moins 87 tués et 436 blessés en territoire occupé et d'au moins 53 tués et 462 blessés en Russie, pour l'essentiel non vérifiées. Source : PDF, page 1 (« Summary »).

Les quatre points en anglais disent la même chose que le français ; le deuxième cite la réserve de l'ONU en anglais, entre guillemets.

## Double vérification

Faite le 11/11/2026 par un agent Claude : le PDF rouvert avec `pdftotext`, la page de la publication ouverte, puis des recherches dans la presse d'octobre 2026.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Tués depuis 2022 | 17 605 | 17 605 | PDF ci-dessus (texte et graphique) | Conforme |
| Blessés depuis 2022 | 55 846 | 55 846 | PDF ci-dessus | Conforme |
| Total | 73 451 | 73 451 (17 605 + 55 846) | PDF ci-dessus | Conforme |
| Par année | voir « Séries » | somme des colonnes égale aux cumuls ; 2026 janvier-septembre : 2 570 et 15 211 | PDF ci-dessus, « 1. By year » | Conforme |
| Septembre 2026 (hors fichier) | — | 328 tués et 2 105 blessés ; janvier-septembre 2026 : 2 570 tués et 15 211 blessés | https://www.stripes.com/theaters/europe/2026-10-16/ukraine-civilian-casualties-rise-23173114.html | Conforme |
| Mise à jour précédente | — | « at least 16,431 civilians killed and 48,613 injured » (juillet 2026, résumé de recherche d'une dépêche de l'ONU) | https://news.un.org/en/story/2026/07/1167935 | Cohérent avec la hausse (non ouverte) |
| Cumuls de septembre dans la presse | — | non retrouvés : les articles ouverts donnent les chiffres du mois et de l'année 2026 seulement | recherche web | Non trouvé |

**Conclusion.** Chaque chiffre est celui du PDF de l'ONU, et ses sommes sont cohérentes ; la presse ne reprend pas les cumuls.

**Pages consultées** le 11/11/2026 : le PDF, la page de la publication, https://www.stripes.com/theaters/europe/2026-10-16/ukraine-civilian-casualties-rise-23173114.html, des résumés de recherche web.

## Réserves

- Ce sont des minimums vérifiés, non un recensement.
- Aucune licence n'est indiquée : les chiffres sont cités avec leur source, sans redistribuer le fichier.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : le PDF a été rouvert, la presse recoupe le mois et l'année 2026.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande : aucune licence indiquée, « © United Nations in Ukraine » ; citation seule.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
