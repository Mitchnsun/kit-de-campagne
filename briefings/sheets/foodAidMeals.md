# `foodAidMeals` · Les repas de l'aide alimentaire (saisie à la main)

**Vérifiée le 19/11/2026** : chaque valeur lue dans un document de l'association ouvert en entier (rapport annuel ou communiqué), et recoupée par un second document de l'association ou par la presse, sans écart non expliqué (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `foodAidMeals`, dossier « Pouvoir d'achat et logement » (`purchasingPower`), aussi dans « Économie » (`economy`), page de type série, demande du PO du 19/11/2026 après le débat présidentiel du 16/11/2026 dans un entrepôt de l'association |
| Données | `briefings/manual/foodAidMeals.json`, saisi à la main le 2026-11-19 depuis les rapports annuels et le communiqué ci-dessous |
| Sources | Les Restos du Cœur : communiqué « Les Restos du Cœur lancent leur 42e campagne » (16/11/2026) ; rapports annuels 2023-2024, 2022-2023, 2020-2021, 2019-2020 ; rapport moral 2016-2017 ; extraits du rapport moral 2014-2015. Chiffres cités (`citation-only`), en français seulement. Les dates de publication des rapports sont celles de leur fichier PDF |
| Série | `meals` : repas distribués sur la campagne, l'année étant celle où finit la campagne (2026 pour 2025-2026). 9 points : 2015, 2017, 2020 à 2026 |
| Chiffre clé | 186 millions de repas en 2025-2026, en hausse (161 millions en 2024-2025) |
| Règles | Seules les campagnes dont un document de l'association, ouvert, donne le nombre de repas ; aucune valeur déduite d'une évolution (« +3 % ») ni lue dans un seul résumé de recherche |
| Première édition | À remplir à la publication |

Valeurs écartées : 75 millions « à vingt ans » (2005) et 100 millions en 2008, que la chronologie des rapports ne rattache à aucune campagne précise ; 130 millions, cité dans le rapport moral 2016-2017 pour une année antérieure non nommée ; 81,5 millions (2006-2007), 115 millions (2011-2012), vus dans la presse ou un résumé seulement.

## « À savoir »

1. Les repas d'une association, pas un compte des pauvres : 1,4 million de personnes accueillies en 2025-2026 (communiqué du 16/11/2026) ; 9,8 millions de personnes pauvres en 2024 (Insee, `poverty.json` du kit, série `poorPeople`).
2. Les « +37 % » : le communiqué du 16/11/2026 écrit « entre 2018 et 2025, le nombre de personnes vivant dans la grande pauvreté a augmenté de 37 % », avec un renvoi à l'étude « L'extrême pauvreté dans les pays riches : analyse empirique sur données françaises » (Bruneel-Zupanc, Gaillard, Hellwig, Wangner, Werquin), dont le résumé (NBER, 2 août 2026, https://conference.nber.org/conf_papers/f247458.pdf) dit s'appuyer sur « a novel administrative data set from France's largest food assistance charity ». Le champ est celui des personnes accueillies par l'association. L'Insee : 9 004 000 personnes pauvres en 2018, 9 817 000 en 2024 (+9 %, `poverty.json`).
3. Comparabilité : rapport annuel 2021-2022 (https://www.restosducoeur.org/wp-content/uploads/2016/04/ra_2021-2022.pdf), « Ces chiffres sont arrêtés au 30 avril 2022 » ; communiqué du 12/11/2025 (https://presse.restosducoeur.org/download-pdf/691dfe7282655ca76a0685b0), « les mesures contraignantes que nous avons été tenus de prendre sur la plus grande partie de l'exercice ont exclu de l'aide alimentaire un certain nombre de personnes démunies ».
4. 8,5 millions de repas lors de la première campagne : rapport 2023-2024 (« Plus de 5 000 bénévoles distribuent 8,5 millions de repas durant l'hiver ») et page de présentation de l'association (« En 1985-1986, les Restos distribuaient 8,5 millions de repas »).

## Double vérification

Faite le 19/11/2026 par l'agent principal (PDF téléchargés et lus avec `pdftotext`) et deux agents Claude (modèle Sonnet) qui cherchent sur le web.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| 2025-2026 (chiffre clé) | 186 000 000 | « distribué 186 millions de repas à travers la France, contre 161 lors de la campagne de 2024/2025 » ; « En 2025-2026, les Restos du Cœur ont servi 186 millions de repas » ; Public Sénat, 186 millions contre 161 | https://presse.restosducoeur.org/actualites/les-restos-du-coeur-lancent-leur-42e-campagne-dc4fc-f88ce.html ; https://www.restosducoeur.org/presentation/ | Conforme |
| 2024-2025 | 161 000 000 | « Lors de l'exercice 2024-2025, les Restos du Cœur ont accueilli 1,3 million de personnes et distribué gratuitement 161 millions de repas » (communiqué du 12/11/2025) ; 161 dans le communiqué du 16/11/2026 | https://presse.restosducoeur.org/download-pdf/691dfe7282655ca76a0685b0 | Conforme. Un document de conseillers financiers (ideas.asso.fr, 05/12/2025) donne 163 millions pour 2024-2025, vu en résumé seulement : écarté, les deux communiqués de l'association disent 161 |
| 2023-2024 | 163 000 000 | « En 2023-2024, ce sont 163 millions de repas qui ont été servis » (rapport annuel) ; « 1,3 million de personnes qui ont été accueillies et 163 millions de repas distribués » (plaquette de la 40e campagne) | https://www.restosducoeur.org/wp-content/uploads/2016/04/ra-23_24-complet-bd.pdf ; https://restosducoeur.org/wp-content/uploads/2024/11/plaquette-de-campagne_40.pdf | Conforme |
| 2022-2023 | 171 000 000 | « En 2022-2023, ce sont 171 millions de repas qui ont été servis, contre 142 millions l'année précédente » | https://www.restosducoeur.org/wp-content/uploads/2023/11/v17-ra_2022_2023_reduit_01-presentation-1.pdf | Conforme |
| 2021-2022 | 142 000 000 | « près de 142 millions de repas » (rapport 2021-2022, chiffres arrêtés au 30 avril 2022) ; « contre 142 millions l'année précédente » (rapport 2022-2023) | https://www.restosducoeur.org/wp-content/uploads/2016/04/ra_2021-2022.pdf | Conforme, « près de » |
| 2020-2021 | 142 000 000 | « En 2020-2021, ce sont près de 142 millions de repas qui ont été distribués à plus de 850 000 personnes durant la campagne d'hiver » | https://www.restosducoeur.org/wp-content/uploads/2016/04/ra_2020-2021_partie-1_association.pdf | Conforme, « près de ». Deux campagnes de suite à « près de 142 millions » : les deux rapports le disent |
| 2019-2020 | 136 500 000 | « En 2019-2020, ce sont plus de 136,5 millions de repas qui ont été distribués » ; Carenews, 136,5 millions, vu en résumé | https://www.restosducoeur.org/wp-content/uploads/2016/04/ra_2019-2020_partie-association.pdf | Conforme, « plus de » |
| 2016-2017 | 135 800 000 | « près de 136 millions de repas (135,8 millions exactement) qui ont été distribués, +3% par rapport à la campagne précédente » ; « En 2016-2017, ce sont près de 136 millions de repas » (rapport, partie association) | https://www.restosducoeur.org/wp-content/uploads/2017/10/4-Rapport-Annuel-2016-2017_Le-rapport-moral.pdf ; https://www.restosducoeur.org/wp-content/uploads/2016/04/1-Rapport-Annuel-2016-2017_Lassociation.pdf | Conforme |
| 2014-2015 | 128 500 000 | « 128,5 millions de repas distribués en 2015, 8,5 millions en 1985 » ; « les 128,5 millions de repas distribués et 950 000 personnes accueillies » | https://www.restosducoeur.org/wp-content/uploads/2016/04/Rapport_Annuel_2014-2015_Extraits_du_rapport_moral.pdf | Conforme |
| « +37 % » | Note 2 | Voir « À savoir », point 2. La presse le reprend tantôt comme une hausse des personnes accueillies, tantôt comme une hausse de la grande pauvreté dans le pays ; le communiqué de l'association parle de grande pauvreté, sur les données de ses accueillis | Communiqués de l'association ; résumé de l'étude (NBER) ; maire-info.com, linfodurable.fr (vus en résumé) | Écart expliqué : c'est le champ de l'étude, pas la population |

**Conclusion.** Neuf campagnes, chacune lue dans un document de l'association ; la série est lacunaire (2016, 2018, 2019 et les campagnes avant 2015 manquent) mais aucune valeur n'est estimée.

**Pages consultées** le 19/11/2026 : les documents cités ci-dessus, et https://www.restosducoeur.org/presentation/.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande : chiffres cités, aucun document reproduit.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
