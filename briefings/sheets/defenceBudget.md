# `defenceBudget` · Le budget et la programmation militaire (saisi à la main)

**Vérifiée le 16/11/2026** : double vérification sur le web par un agent Claude (modèle Sonnet), 15/11/2026, sans écart de valeur ; un écart de 0,2 Md€ entre deux documents, non expliqué, dit dans une note (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `defenceBudget`, dossier « Défense et Europe » (`defence`), premier volet (« Budget ») de la page composite `defenceMeans` (voir `defenceMeans.md`), page de type série, ticket #442 de l'app |
| Données | `briefings/manual/defenceBudget.json`, saisi à la main le 2026-11-16 depuis le projet annuel de performances 2027 de la mission « Défense » et l'article 3 de la loi n° 2026-791 |
| Sources | 1. Direction du budget, « Projet annuel de performances 2027, mission « Défense » », https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128221/file/PAP%202027%20-%20D%C3%A9fense.pdf (01/10/2026, avec le projet de loi de finances pour 2027), Licence Ouverte 2.0 comme le projet de loi de finances (`financeBill`, `stateBudget`), en français seulement. 2. Assemblée nationale, « Loi n° 2026-791 du 16 août 2026 actualisant la programmation militaire pour les années 2024 à 2030 et portant diverses dispositions intéressant la défense », dossier https://www.assemblee-nationale.fr/dyn/17/dossiers/PJL_actualisation_loi_programmation_militaire_annees_2024_2030_diverses_dispositions_defense (« Loi n°2026-791 du dimanche 16 août 2026 […] Publiée au Journal Officiel du mardi 18 août 2026 »), texte définitif lu : T.A. n° 325 du 1er juillet 2026, https://www.assemblee-nationale.fr/dyn/17/textes/l17t0325_texte-adopte-seance.pdf ; daté du 18/08/2026, sa publication au Journal officiel ; citation seule (Légifrance, qui porte la Licence Ouverte, a refusé l'accès aux scripts : défi Cloudflare) |
| Séries | Toutes annuelles, en milliards d'euros courants, crédits de paiement de la mission « Défense ». `missionCredits` : contributions au compte « Pensions » comprises, 2026 (loi de finances, 66,475476236) et 2027 (projet, 73,153440797, `projection`), récapitulation des crédits, p. 23. `missionCreditsExPensions` : hors pensions, 2027 seulement (63,4, `projection`), présentation stratégique, p. 10. `lpmUpdated` : trajectoire de la loi de 2026, 2024 à 2030 (47,2 ; 50,5 ; 57,1 ; 63,3 ; 69,5 ; 72,6 ; 75,7), 2027 à 2030 en `projection`. `lpmInitial` : trajectoire initiale de 2023, mêmes années (47,2 ; 50,5 ; 53,7 ; 56,9 ; 60,4 ; 63,9 ; 67,4), article 3 de la loi de 2026 (tableau qui remplace celui de l'article 4 de la loi n° 2023-703), hors contribution au CAS « Pensions » |
| Chiffre clé | 66,5 Md€ votés pour 2026 (`missionCredits`, 2026), pensions comprises, la convention de `stateBudget` (le total de chaque mission, contributions aux pensions comprises) ; sans tendance (aucune autre loi de finances saisie). À côté : le projet pour 2027, 73,2 Md€ pensions comprises et 63,4 Md€ hors pensions, « prévision » |
| Règles | Saisie à la main. Avec ou sans pensions, toujours dit, jamais additionné ; les trajectoires de la loi ne sont jamais dessinées avec les crédits du budget. Pas de série « hors pensions » pour 2026 : 56,90 Md€ n'est qu'un calcul (66 475,5 − 9 576,2 M€), dit dans une note. 2025 exécuté (62,12 Md€ pensions comprises) n'est pas repris : il est dans `stateBudget`, et un exécuté ne se met pas dans la même série qu'un voté. Les montants de l'OTAN en euros ne sont pas saisis |
| Première édition | À remplir à la publication |

## « À savoir »

1. La loi du 16 août 2026 : 435,7 Md€ contre 400 Md€ en 2023 ; 413,3 Md€ de besoins programmés. Source : loi n° 2026-791, article 3 (« Le montant des besoins physico-financiers programmés pour la période 2024-2030 était fixé en 2023 à 413,3 milliards d'euros » ; « Le total du budget de la programmation militaire actualisée est de 435,7 milliards d'euros » ; « Les totaux du tableau sont arrondis à l'unité supérieure ») ; avis n° HCFP-2026-1, § 7 (400 Md€ de crédits) et § 14 (« les besoins programmés excédaient de 13,3 Md€ le total des crédits de paiement » ; ces besoins « seraient financés d'une part par des ressources extra-budgétaires, d'autre part par de moindres dépenses sur les autres ministères », d'où « en partie » dans la note).
2. Avec ou sans pensions : 66,48 Md€ dont 9,58 Md€ de contributions au compte « Pensions » (projet annuel de performances 2027, p. 23 : « 66 475 476 236 » ; « Contributions d'équilibre au CAS Pensions : 9 576 217 747 ») ; 56,90 Md€ calculé ; 57,1 Md€ pour 2026 dans la loi (article 3). L'écart de 0,2 Md€ n'est pas expliqué par les documents lus : la note donne les deux chiffres sans en tirer de conclusion.
3. Le projet pour 2027 : 73,15 Md€ pensions comprises (p. 23 : « 73 153 440 797 », « +10,05 % ») ; « 63,4 Md€ en CP hors pensions, soit une augmentation de +6,5 Md€ en CP par rapport à la LFI 2026 à périmètre courant […] La hausse correspond aux +3,2 Md€ déjà prévue par la LPM 2024-2030 auxquels s'additionnent +3,3 Md€ de crédits supplémentaires conformément à la loi du 16 août 2026 » (p. 10).
4. Les restes à payer : avis n° HCFP-2026-1 du 19/03/2026 sur le projet de loi, https://www.hcfp.fr/sites/default/files/2026-04/Avis%20sur%20le%20PLAPM%202026-2030_sign%C3%A9.pdf, synthèse (« l'élévation notable des restes à payer (passés de 60 Md€ fin 2019 à environ 140 Md€ prévus en 2026 comme en 2030) […] signifie que les engagements pris se traduiront par une poursuite de paiements importants au-delà de l'horizon financier du PLAPM ») ; citation seule.

Les quatre points en anglais disent la même chose que le français.

## Double vérification

Faite le 15/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web (rapport `check-gap-g2.md`, § 2), les documents retéléchargés et relus avec `pdftotext`.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, loi de finances pour 2026 | 66,475476236 Md€ (2026) | « 66 475 476 236 », p. 23 ; autorisations d'engagement 92 828 480 008 € | projet annuel de performances 2027 « Défense » (URL ci-dessus) | Conforme |
| Projet pour 2027, pensions comprises | 73,153440797 Md€ | « 73 153 440 797 », « +10,05 % », p. 23 | idem | Conforme |
| Projet pour 2027, hors pensions | 63,4 Md€ | « 78,7 Md€ en AE et 63,4 Md€ en CP hors pensions […] +6,5 Md€ […] +3,2 Md€ […] +3,3 Md€ », p. 10 | idem | Conforme |
| Contributions au CAS « Pensions » | 9,576 et 9,744 Md€ (notes) | 9 576 217 747 et 9 744 219 699 | idem | Conforme |
| Trajectoires de 2023 et de 2026 | 7 + 7 valeurs, 400 et 436 | identiques, « En milliards d'euros courants », totaux « arrondis à l'unité supérieure », 435,7 et 413,3 | https://www.assemblee-nationale.fr/dyn/17/textes/l17t0325_texte-adopte-seance.pdf, p. 4 | Conforme |
| Hors pensions | trajectoires | note 5 de l'avis : « Hors contribution de la mission Défense au compte d'affectation spéciale Pensions » | https://www.hcfp.fr/sites/default/files/2026-04/Avis%20sur%20le%20PLAPM%202026-2030_sign%C3%A9.pdf | Conforme |
| Projet de loi contre loi | 69,5 ; 72,6 ; 75,7 (2028-2030) | projet : 68,3 ; 72,8 ; 76,3 (tableau 1 de l'avis) : le Parlement a modifié le profil | idem | Écart expliqué (le fichier suit la loi votée) |
| 2024 et 2025 respectés, LFI 2026 « par anticipation » | 47,2 ; 50,5 ; 57,1 | § 8 et § 16 de l'avis | idem | Conforme |
| LFI 2026 hors pensions | 56,90 (calculé, note) contre 57,1 (loi) | 66 475,5 − 9 576,2 = 56 899 M€ ; le projet annuel lui-même écrit 63,4 − 6,5 = 56,9 | projet annuel de performances 2027 | Écart réel de 0,2 Md€, non expliqué par les documents lus : dit dans la note 2 |
| Loi promulguée, publiée | 16/08/2026, JO du 18/08/2026 | « Loi n°2026-791 du dimanche 16 août 2026 […] Publiée au Journal Officiel du mardi 18 août 2026 » | dossier de l'Assemblée (URL ci-dessus) | Conforme |
| Décision n° 2026-907 DC du 6 août 2026 | aucune censure | saisine du 6 juillet 2026 par des députés ; contestés au fond : certaines dispositions des articles 25, 31, 32, 33 et 35 ; article 41 contesté pour sa place dans la loi ; dispositif : « Sont conformes à la Constitution » ; l'article 3 (la trajectoire) n'est pas en cause | https://www.conseil-constitutionnel.fr/decision/2026/2026907DC.htm | Conforme (le rapport de recherche écrivait « 31 à 35 » : le 34 n'est pas contesté) |
| Restes à payer (note 4) | 60 → environ 140 Md€ | synthèse et § 13 de l'avis | avis n° HCFP-2026-1 | Conforme |

**Conclusion.** Les valeurs saisies sont celles des documents ; l'écart de 0,2 Md€ entre la loi et la loi de finances pour 2026, hors pensions, n'est pas expliqué et la page le montre sans le commenter.

**Pages consultées** le 15/11/2026 (et le 16/11/2026 pour la décision n° 2026-907 DC et les pages 10, 23, 92, 106, 236 et 237 du projet annuel) : les URL ci-dessus ; https://www.hcfp.fr/liste-avis/avis-ndeg-2026-1-loi-de-programmation-militaire-plapm.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans le document saisi (avis du HCFP, décision du Conseil constitutionnel).
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
