# `socialFraud` · Fraude sociale (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; plusieurs réserves de lecture, reprises dans « À savoir » et « Ce qu'on entend ». La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `socialFraud`, dossier « Économie et fiscalité » (`economy`), volet de la page composite `fraud` (voir `fraud.md`), page de type comparaison |
| Données | `briefings/manual/socialFraud.json`, saisi à la main depuis la note annuelle du HCFiPS (13/01/2026) et « La sécurité sociale 2026 » de la Cour des comptes (27/05/2026) le 2026-11-09 |
| Sources | HCFiPS, « Note annuelle de suivi et d'évaluation des fraudes sociales » (synthèse, infographie et note complète, 13/01/2026) ; Cour des comptes, « La sécurité sociale 2026 » (rapport du 27/05/2026) ; licence « citation seule » pour les deux, en français seulement |
| Séries | `evaluated` : fraude sociale évaluée, Md€, 2025, 1 point ; `detected` : sommes détectées, Md€, 2022 à 2024, 3 points ; `avoided` : fraudes évitées, Md€, 2023 et 2024, 2 points ; `recovered` : sommes recouvrées, Md€, 2021, 2023 et 2024, 3 points (tableau n° 2 de la note ; la série saute 2022) |
| Valeurs par catégorie | `byNature` (2025) : travail dissimulé 52 %, prestations 48 % ; `byAuthor` (2025) : entreprises 52 %, assurés 36 %, professionnels 12 % ; `byBranch` (2025) : Urssaf 50 %, famille 30 %, maladie 17 %, MSA 2 %, retraite 1 % ; `recoveryRate` (2024) : travail dissimulé 8 %, maladie 53 %, famille 53 %, retraite 70 % |
| Chiffre clé | 14 Md€ de fraude sociale évaluée, période « 2025 », sans tendance saisie (13 Md€ à l'évaluation précédente) |
| Règles | Saisie à la main, rien n'est lu par script. 14 Md€ est une évaluation, pas une somme détectée. La période « 2025 » est celle de l'évaluation actualisée le 4 décembre 2025, dont les millésimes varient selon la caisse. « 52 % » entreprises est « plus de 52 % » dans le texte du HCFiPS. « Professionnels » désigne les professionnels de santé. Retraite : « environ 70 % » dans la Cour des comptes. Détecté et recouvré comptent fautes et fraudes. Sommes recouvrées 2022 : la note n'a pas de colonne 2022, le point est absent ; le recouvrement de 2021 ne compte pas la MSA. Les estimations par prestation (RSA, prime d'activité…) et les montants des caisses ne sont pas saisis |
| Première édition | À remplir à la publication |

## « À savoir »

1. 14 Md€ est un montant évalué, pas une somme détectée ni récupérable. Il ne couvre pas les micro-entrepreneurs, les indépendants « classiques », les établissements de santé (T2A) ni la PUMa, et les caisses n'ont pas toutes le même millésime. Source : HCFiPS, synthèse du 13/01/2026, https://www.strategie-plan.gouv.fr/files/files/Publications/2026/2026-01-13%20-%20HCFiPS%20-%20note%20annuelle%20fraude%20sociale/HCFIPS%20-%20Synth%C3%A8se%20Fraude%20sociale%202025%20-%20Version%20finalis%C3%A9e_0.pdf (« aboutit à un montant de fraudes de 14 Md€, contre 13 Md€ lors de l'évaluation précédente ». Le HCFiPS écrit que le chiffre « pourrait être amené à évoluer » ; le mot « minimum » n'est pas de lui, il n'est pas repris).
2. L'évaluation précédente donnait 13 Md€. Selon le HCFiPS, la hausse s'explique à 65 % par les bases, à 25 % par le périmètre et à 10 % par la prévalence. Source : la même synthèse et la note complète, https://www.strategie-plan.gouv.fr/files/files/Publications/2026/2026-01-13%20-%20HCFiPS%20-%20note%20annuelle%20fraude%20sociale/Note%20annuelle%20de%20suivi%20et%20d%27%C3%A9valuation%20des%20fraudes%20sociales%20VF.pdf (retrouvé à la double vérification).
3. Les montants détectés et recouvrés comptent les fautes avec les fraudes (« préjudices subis et constatés », « indus frauduleux ou fautifs »). Le recouvrement de 2021 ne compte pas la MSA. Source : la note du HCFiPS (page 16 ; le graphique 4 compte « Faute, fraude, abus » pour la Cnam et « Faute et fraude » pour la Cnav ; le tableau n° 2 est intitulé « recouvrement des indus frauduleux ou fautifs (en M€) », colonnes 2021, 2023 et 2024, « LCTI MSA n.c. » en 2021, « Données retraite et MSA non réévaluées »). Relu dans le document d'origine le 09/11/2026 par le coordinateur. La phrase sur les « détections de plusieurs années » a été retirée de la note.
4. Selon la Cour des comptes, la fraude à la résidence n'est pas évaluée. Source : « La sécurité sociale 2026 », https://www.ccomptes.fr/sites/default/files/2026-05/20260527-RALFSS-2026_0.pdf (« La fraude à la résidence n'est pas évaluée. »).

Les quatre points en anglais (relus le 09/11/2026) disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/socialFraud.json` (clé `claims`, français et anglais). Source de chaque chiffre de la réponse :

1. « On entend que l'État récupère 13 ou 14 milliards de fraude sociale. » 14 Md€ et 13 Md€ : synthèse du HCFiPS. 2,06 Md€ constatés en 2024 (« fautes et fraudes ») et 0,5 Md€ évités : note du HCFiPS, p. 16. 681 M€ recouvrés (« indus frauduleux ou fautifs ») : tableau 2 de la note (212 + 26 + 314 + 120 + 9). Le texte de la note dit « près de 700 M€ » et, à un endroit, « 680 M€ ».
2. « On entend que la fraude sociale, c'est d'abord celle des allocataires. » 52 %, 36 % et 12 % : synthèse du HCFiPS (« plus de 52 % de la fraude évaluée » ; 36 % assurés ; 12 % professionnels).
3. « On entend que les arrêts maladie, c'est de la fraude. » 1,8 % et 230 M€ sur environ 7 000 arrêts tirés au hasard : note du HCFiPS, p. 12 (« Le taux de fraude estimé s'élève à 1,8 % (230 M€). »).
4. « On entend que la lutte contre la fraude financera le programme. » 8 %, 53 % et 53 % en 2024 : Cour des comptes, « La sécurité sociale 2026 » (« le recouvrement des indus frauduleux est très variable »). La conclusion (« une fraude détectée n'est pas toujours recouvrée ») est une lecture de ces taux, pas une phrase de la source.
5. « On entend que les étrangers fraudent les prestations. » « La fraude à la résidence n'est pas évaluée » : Cour des comptes, « La sécurité sociale 2026 ». La réponse dit seulement que les répartitions montrées ici (par nature, par auteur, par branche) ne portent pas sur la nationalité : un constat sur la page, qui se lit dans les répartitions saisies, non une phrase de la source.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web : chaque URL du rapport de recherche rouverte (PDF passés à `pdftotext`), sans passer par un fichier de données. Tous les producteurs sont officiels (HCFiPS, Cour des comptes). Aucun écart numérique, aucun chiffre non retrouvé parmi ceux du fichier. Verdicts : Conforme, ou Conforme avec la réserve dite dans la colonne.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, fraude évaluée | 14 Md€ (2025) | 14 Md€, contre 13 Md€ avant ; hausse : 65 % bases, 25 % périmètre, 10 % prévalence. Évaluation actualisée le 4 décembre 2025, millésimes variables | https://www.strategie-plan.gouv.fr/files/files/Publications/2026/2026-01-13%20-%20HCFiPS%20-%20note%20annuelle%20fraude%20sociale/HCFIPS%20-%20Synth%C3%A8se%20Fraude%20sociale%202025%20-%20Version%20finalis%C3%A9e_0.pdf | Conforme, avec réserve : montant évalué, pas détecté ; le HCFiPS ne dit pas « minimum » |
| Par nature | 52 % travail dissimulé, 48 % prestations | 52 % et 48 % (infographie) | https://www.strategie-plan.gouv.fr/files/files/Publications/2026/2026-01-13%20-%20HCFiPS%20-%20note%20annuelle%20fraude%20sociale/HCFIPS%20-%20infographie%20Fraude%20sociale%202025%20-%20Version%20finalis%C3%A9e_0.pdf | Conforme |
| Par auteur | 52 / 36 / 12 % | « plus de 52 % », 36 %, 12 % | synthèse du HCFiPS (URL ci-dessus) | Conforme, avec réserve : « plus de 52 % » |
| Par branche | Urssaf 50, famille 30, maladie 17, MSA 2, retraite 1 % | 50, 30, 17, 2, 1 % (infographie) ; le graphique 2 de la note donne 16 % Cnam, 1 % Cnav, 1 % France Travail | infographie et note du HCFiPS (URL ci-dessus et https://www.strategie-plan.gouv.fr/files/files/Publications/2026/2026-01-13%20-%20HCFiPS%20-%20note%20annuelle%20fraude%20sociale/Note%20annuelle%20de%20suivi%20et%20d%27%C3%A9valuation%20des%20fraudes%20sociales%20VF.pdf) | Conforme (écart 16 / 17 % de la source signalé) |
| Détecté | 1,3 (2022), 1,65 (2023), 2,06 (2024) Md€ | « 2,06 Md€ en 2024 après 1,65 Md€ de sommes détectées en 2023 et 1,3 Md€ en 2022 » | note du HCFiPS, p. 16 (URL ci-dessus) | Conforme, avec réserve : fautes et fraudes comptées ensemble (Cnam, Cnav) |
| Évité | 0,47 (2023), 0,5 (2024) Md€ | « 0,5 Md€, montant proche de celui de l'année précédente (0,47 Md€) » | note du HCFiPS (URL ci-dessus) | Conforme |
| Recouvré | 0,542 (2021), 0,611 (2023), 0,681 (2024) Md€ | Tableau 2 : « Total 542 611 681 » ; 2024 = 212 + 26 + 314 + 120 + 9 ; colonnes 2021, 2023, 2024 | note du HCFiPS (URL ci-dessus) | Conforme, avec réserve : indus frauduleux ou fautifs ; le texte dit aussi « 680 M€ » ; MSA non comptée en 2021 (« n.c. »). Années des colonnes (2021, 2023, 2024) confirmées le 09/11/2026 par relecture du tableau n° 2 dans le document d'origine ; la note n'a pas de colonne 2022 : Non trouvé dans les sources lues |
| Taux de recouvrement 2024 | 8 / 53 / 53 / 70 % | « 8 % pour le travail dissimulé, 53 % pour l'assurance maladie, 53 % pour la branche famille, environ 70 % des montants redressés s'agissant des retraites » | https://www.ccomptes.fr/sites/default/files/2026-05/20260527-RALFSS-2026_0.pdf | Conforme, avec réserve : retraite « environ 70 % », saisi 70 |
| 1,8 % et 230 M€ (arrêts de travail) | texte de la réponse 3 | « Le taux de fraude estimé s'élève à 1,8 % (230 M€). » ; échantillon d'environ 7 000 arrêts | note du HCFiPS, p. 12 (URL ci-dessus) | Conforme |
| C2S, non-recours | 31 % et 66 % (estimation de 2021) | « 31 % pour sa version gratuite et 66 % pour sa version participative » ; note 250 : DSS, rapport annuel 2024 sur la C2S | https://www.ccomptes.fr/sites/default/files/2026-05/20260527-RALFSS-2026_0.pdf | Conforme, avec réserve : seconde main (Cour des comptes d'après la DSS, que la double vérification n'a pas ouverte) |
| Fraude à la résidence | « non évaluée » | « La fraude à la résidence n'est pas évaluée. » | https://www.ccomptes.fr/sites/default/files/2026-05/20260527-RALFSS-2026_0.pdf | Conforme |
| Dates de publication | 2026-01-13 (HCFiPS), 2026-05-27 (Cour) | PDF du HCFiPS daté du 13/01/2026 (dossier de l'URL) ; PDF de la Cour daté du 27/05/2026 (URL et métadonnées, créé le 27/05/2026) | URL des deux documents | Conforme |

**Conclusion.** Aucun chiffre du fichier n'est faux. Trois lectures sont à garder : 14 Md€ est évalué et non détecté ; détecté et recouvré mêlent fautes et fraudes ; les millésimes des caisses ne sont pas les mêmes.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus (HCFiPS : synthèse, infographie, note ; Cour des comptes : rapport du 27/05/2026). Les sources de la liste « à confirmer » du rapport (Ameli, DREES, Urssaf, bilan du gouvernement) étaient inaccessibles (403, 503, connexion coupée) et ne servent à aucun chiffre du fichier.

## Mises à jour

**09/11/2026** : le bloc « Ce qu'on entend » ne garde que les fausses vérités que les chiffres de la page démentent (décision du PO) : affirmations retirées : « On entend que des milliards d'aides ne sont jamais réclamés. ».

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert les documents eux-mêmes ; les points de la série `recovered` n'ont d'autre source que la note du HCFiPS.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais. Les quatre points le sont (le point 3 réécrit d'après la source) ; les versions anglaises des notes et des affirmations ont été relues et concordent avec le français.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée : le registre dit « citation seule » (aucune licence trouvée, chiffres cités, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
