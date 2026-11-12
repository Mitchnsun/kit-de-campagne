# `euContribution` · La France et le budget de l'Union (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart sur les chiffres saisis ; réserves de lecture reprises ci-dessous. La licence du jaune budgétaire n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `euContribution`, dossier « Défense et Europe » (`defence`), aussi dans « Économie et fiscalité » (`alsoIn`), page de type comparaison, recherche « Ce qu'on entend » du 09/11/2026 |
| Données | `briefings/manual/euContribution.json`, saisi à la main le 2026-11-09 depuis l'annexe « Relations financières avec l'Union européenne » (jaune n° 13) et le projet de loi de finances pour 2027 |
| Sources | 1. Direction du budget, « Relations financières avec l'Union européenne, annexe au projet de loi de finances pour 2027 », https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1129751/file/13-Jaune%202027%20-%20Relations%20financi%C3%A8res%20avec%20l%27Union%20europ%C3%A9enne.pdf (01/10/2026), citation seule, en français seulement. 2. Assemblée nationale, « Projet de loi de finances pour 2027, n° 3210 », https://www.assemblee-nationale.fr/dyn/opendata/PRJLANR5L17B3210.pdf (01/10/2026), Licence Ouverte 1.0 comme pour `financeBill`, en français seulement |
| Séries | `levyExecuted` : prélèvement sur recettes au profit de l'UE (PSR-UE) exécuté, Md€, 2025, 1 point (22,962) ; `levyBudget` : le même inscrit en loi de finances initiale pour 2026 et au projet pour 2027, Md€, 2 points (28,44 ; 30,906), statut `projection` ; `levyRevised` : prévision révisée pour 2026, Md€, 1 point (28,118), statut `projection` ; `euSpending` : dépenses de l'UE réparties en France hors plan de relance, Md€, 2025, 1 point (16,4) ; `capSpending` : dont politique agricole commune, Md€, 2025, 1 point (9,4) ; `netAccounting` : solde net selon la méthode comptable, Md€, 2025, 1 point (−9,5) ; `netCommission` : solde net selon la méthode de la Commission, Md€, 2025, 1 point (−6,4) |
| Chiffre clé | 22,962 Md€ (écrit 23,0 Md€) de prélèvement exécuté en 2025, contribution brute, sans tendance saisie ; à côté, les deux soldes nets de 2025 |
| Règles | Saisie à la main. Brut et net ne sont jamais confondus : le prélèvement est le chiffre clé, les deux soldes nets sont écrits à côté, chacun avec sa méthode, jamais additionnés ni dans un bloc de barres. Les montants de 2026 et 2027 portent le statut `projection`, dits « prévision ». Le plan de relance n'est pas saisi : il est dans « À savoir ». La série d'exécution 2021-2024 du jaune n'est pas saisie (hors de la recherche vérifiée) |
| Première édition | À remplir à la publication |

## « À savoir »

1. Le prélèvement est la contribution de l'État hors droits de douane, versés directement à l'Union (2,8 Md€ en 2025) ; celui de 2027 est une prévision, révisable après la conciliation de novembre. Source : jaune n° 13, tableau des ressources (« Ressources propres traditionnelles […] 2 842 » en 2025) et § 3.6.3 (« Pour 2027, le prélèvement sur recettes est évalué à 30 906 M€ ») ; conciliation : § 3.6 (procédure budgétaire 2027).
2. Les deux méthodes du solde net. Source : jaune n° 13, § 3.3 (« Selon la méthode dite comptable, le solde net est calculé par simple différence entre la contribution d'un État membre au budget de l'Union européenne au titre de l'ensemble des ressources propres, y compris les RPT (nettes des frais de perception) et le montant des dépenses européennes effectuées dans cet État membre, y compris les dépenses administratives » ; « Selon la méthode dite de la Commission, le solde net dit opérationnel est calculé […] (différence entre la contribution nette hors RPT et les dépenses réparties pour chaque État membre), mais en excluant les dépenses administratives »). Les ressources propres traditionnelles (RPT) sont pour l'essentiel les droits de douane.
3. Le solde net ne retrace pas tous les coûts et bénéfices de l'appartenance à l'Union ; la France est deuxième contributeur selon la méthode comptable, derrière l'Allemagne (−21,8 Md€). Source : jaune n° 13, § 3.3 (« ne saurait à elle seule retracer la totalité des coûts et bénéfices de l'appartenance à l'Union européenne » ; « les gains qu'entraîne l'appartenance à un marché unique » ; « La France est le deuxième contributeur selon la méthode comptable, derrière l'Allemagne (-21,8 Md€) »).
4. Le plan de relance : 34,2 Md€ perçus depuis 2021 au titre de la facilité pour la reprise et la résilience, sur une enveloppe de 40,3 Md€ (37,5 Md€ de cette facilité et 2,8 Md€ de REPowerEU). Source : jaune n° 13, p. 63-64 (« Depuis 2021, la France a perçu 34,2 Md€ de subventions au titre de la FRR, sur une enveloppe totale de 40,3 Md€ ») ; la composition de l'enveloppe vient du même jaune, d'après la contre-vérification.

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Une affirmation dans `briefings/notes/euContribution.json` (clé `claims`), reprise de la recherche vérifiée du 09/11/2026 sans changer sa formulation (le signe moins écrit −) :

1. « On entend que la France donne 30 milliards à l'Europe. » 30,9 Md€ prévus en 2027 : jaune n° 13 (30 906 M€) et projet de loi de finances, état A (ligne « Prélèvement sur les recettes de l'État au profit de l'Union européenne 28 440 28 118 30 906 »). 16,4 Md€ de dépenses en France, −9,5 et −6,4 Md€ : jaune n° 13, § 3.3 et p. 63-64. Réserve : le solde net n'est pas le prélèvement moins les dépenses en France ; la réponse le dit en donnant les deux méthodes, et la page l'explique dans « À savoir ».

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-finances.md` : le jaune et le projet de loi rouverts par `curl` et `pdftotext`, le fichier « EU spending and revenue 2000-2025 » de la Commission européenne ouvert pour contrôle. Aucun écart sur les chiffres saisis.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, prélèvement 2025 | 22,962 Md€ | « Le montant du PSR-UE pour 2025 s'élève à 22 962 M€ » | jaune n° 13 (URL ci-dessus) | Conforme |
| Prélèvement 2026 et 2027 | 28,44 (loi de finances) ; 28,118 (révisé) ; 30,906 Md€ (projet) | « 28 440 28 118 30 906 » au projet de loi ; le jaune donne 28 440 et 30 906, et « environ 28 118 M€ » pour la prévision révisée | projet de loi de finances (URL ci-dessus), ligne 1144 | Conforme, avec réserve : la contre-vérification situe le 28,1 au projet de loi seulement ; le jaune le donne aussi, précédé d'« environ » |
| Soldes nets | −9,5 (comptable) ; −6,4 Md€ (Commission) | phrase du § 3.3 identique ; contrôle sur le fichier de la Commission : 16 391,3 − 25 865,2 = −9 473,9 M€ | jaune n° 13 ; https://commission.europa.eu/document/download/9f334bee-d097-4b68-8f93-2225eabeb631_en?filename=eu_budget_spending_and_revenue_2000-2025.xlsx | Conforme |
| Dépenses de l'UE en France | 16,4 Md€, dont PAC 9,4 | « les dépenses réalisées en France se sont élevées à 16,4 Md€ (hors crédits du plan de relance NGEU) » ; « près de 57 % du total des retours français (9,4 Md€) » ; le fichier donne 9 461,3 M€ (57,7 %) | jaune n° 13, p. 63-64 | Conforme, avec réserve d'arrondi sur la PAC |
| Plan de relance | 34,2 sur 40,3 Md€ (note) | phrase identique ; 40,3 = 37,5 (FRR) + 2,8 (REPowerEU) | jaune n° 13 | Conforme, avec réserve : l'enveloppe mélange deux dispositifs, la note le dit |

**Conclusion.** Aucun chiffre du fichier n'est faux. Brut et net sont deux chiffres différents, et les deux soldes nets aussi.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus.

## Réserves

- Le prélèvement de 2027 est une prévision, révisable après la conciliation de novembre sur le budget de l'Union.
- Le solde net exclut le plan de relance (NextGenerationEU) et ne retrace pas tous les coûts et bénéfices de l'appartenance à l'Union.
- La France est la première bénéficiaire en volume des dépenses de l'Union en 2023, 2024 et 2025 et 21e par habitant (238 €) : non repris sur la page.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source. Il n'y a pas de script : la contre-vérification a rouvert les documents et le fichier de la Commission.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Assemblée nationale : la « Licence Ouverte 1.0 » du registre est déduite ; les mentions légales du site (https://www.assemblee-nationale.fr/dyn/info-site, lues le 12/11/2026) interdisent la réutilisation commerciale et ne permettent la reproduction que si sa diffusion est gratuite. Le PO a décidé le 12/11/2026 de citer ces documents depuis la Direction du budget : en attente de la lecture de budget.gouv.fr ;
  - citation seule : Direction du budget (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
