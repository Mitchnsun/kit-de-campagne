# `blankVotes` · Les votes blancs et nuls

**Vérifiée le 25/11/2026** : chaque chiffre lu dans la proclamation du Conseil constitutionnel ou dans le fichier `pastElections` du kit, deux fois (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `blankVotes`, dossier « Électorat » (`electorate`), aussi dans « Institutions », page de type série, ticket #541 de l'app |
| Données | `briefings/manual/blankVotes.json`, saisi à la main le 2026-11-25 (calculs ci-dessous) |
| Sources | Ministère de l'Intérieur, « Données des élections agrégées » (data.gouv.fr), la source de `pastElections`, pour 2017 et 2022, dont les comptes sont ceux que le Conseil constitutionnel a proclamés (le script de `pastElections` échoue sur tout écart pour 2017 ; 2022 relu ci-dessous) ; Conseil constitutionnel, décisions n° 2012-152 PDR du 25 avril 2012, 2012-154 PDR du 10 mai 2012, 2007-139 PDR du 25 avril 2007, 2007-141 PDR du 10 mai 2007, 2002-109 PDR du 24 avril 2002, 2002-111 PDR du 8 mai 2002, https://www.conseil-constitutionnel.fr/decision/AAAA/AAAANNNPDR.htm ; citation seule pour le Conseil (comme ses autres décisions du kit), Licence Ouverte 2.0 pour data.gouv.fr. Un fichier tient 8 sources au plus : les dix proclamations n'y entrent pas toutes |
| Séries | En % des votants, deux décimales, calculées : `firstRound` et `secondRound`, (votants − suffrages exprimés) / votants, aux présidentielles de 2002, 2007, 2012, 2017 et 2022 ; `blankFirstRound` et `blankSecondRound`, bulletins blancs / votants, 2017 et 2022 (comptés à part depuis la loi du 21 février 2014) |
| Chiffre clé | 8,66 % au second tour de 2022, en baisse (11,52 % en 2017) ; le premier tour à côté, 2,20 % |
| Règles | Votants moins exprimés, jamais un « blancs » avant 2014, que les proclamations ne donnent pas |
| Première édition | La prochaine édition du kit |

## Les comptes

| Tour | Votants | Exprimés | Blancs | Blancs et nuls | Part | Source |
| --- | --- | --- | --- | --- | --- | --- |
| 2002, 1er | 29 495 733 | 28 498 471 | | 997 262 | 3,38 % | 2002-109 PDR |
| 2002, 2nd | 32 832 295 | 31 062 988 | | 1 769 307 | 5,39 % | 2002-111 PDR |
| 2007, 1er | 37 254 242 | 36 719 396 | | 534 846 | 1,44 % | 2007-139 PDR |
| 2007, 2nd | 37 342 004 | 35 773 578 | | 1 568 426 | 4,20 % | 2007-141 PDR |
| 2012, 1er | 36 584 399 | 35 883 209 | | 701 190 | 1,92 % | 2012-152 PDR |
| 2012, 2nd | 37 016 309 | 34 861 353 | | 2 154 956 | 5,82 % | 2012-154 PDR |
| 2017, 1er | 37 003 728 | 36 054 394 | 659 997 (1,78 %) | 949 334 | 2,57 % | `pastElections` ; 2017-169 PDR |
| 2017, 2nd | 35 467 327 | 31 381 603 | 3 021 499 (8,52 %) | 4 085 724 | 11,52 % | `pastElections` ; 2017-171 PDR |
| 2022, 1er | 35 923 707 | 35 132 947 | 543 609 (1,51 %) | 790 760 | 2,20 % | `pastElections` ; 2022-195 PDR |
| 2022, 2nd | 35 096 478 | 32 057 325 | 2 233 904 (6,37 %) | 3 039 153 | 8,66 % | `pastElections` ; 2022-197 PDR |

## « À savoir »

1. Tableau ci-dessus (2022-197 PDR : « Bulletins blancs : 2 233 904 », « Bulletins nuls : 805 249 ») ; 11,52 % est le plus haut des dix tours.
2. Code électoral, art. L. 65 : « Les bulletins blancs sont décomptés séparément et annexés au procès-verbal. Ils n'entrent pas en compte pour la détermination des suffrages exprimés, mais il en est fait spécialement mention dans les résultats des scrutins. », lu par un agent Claude (modèle Sonnet) dans la copie de codes.droit.org, non officielle (Légifrance en 403), le 25/11/2026. La règle date de la loi n° 2014-172 du 21 février 2014 (non ouverte). Pour la présidentielle, les proclamations de 2017 et de 2022 donnent les blancs à part, comme la note le dit.
3. Les proclamations de 2002 à 2012 ne donnent ni « blancs » ni « nuls » (relevé de l'agent : « not written »).
4. Rapports du second au premier tour, calculés : 1,6 (2002), 2,9 (2007), 3,0 (2012), 4,5 (2017), 3,9 (2022).

## Double vérification

Les décisions de 2002 à 2012 et de 2022 lues deux fois le 25/11/2026, par deux agents Claude (modèle Sonnet) distincts : la recherche (`research/briefings-quiz-2026-11/verification-regles.md` de l'app, § 4) et une relecture des pages du Conseil. Les deux relevés concordent chiffre pour chiffre. 2017 et 2022 : les comptes du fichier `pastElections` du kit, égaux aux proclamations.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| 2022, 2nd, votants et exprimés | 35 096 478 ; 32 057 325 | Idem | https://www.conseil-constitutionnel.fr/decision/2022/2022197PDR.htm | Conforme |
| 2002, 1er | 29 495 733 ; 28 498 471 | Idem | https://www.conseil-constitutionnel.fr/decision/2002/2002109PDR.htm | Conforme |
| Les dix tours, autre diffuseur | | Conforme | Wikipédia (relevé de la recherche) | Conforme |

**Conclusion.** Les parts sont des calculs de comptes officiels, relus deux fois.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais (l'article L. 65 dans une copie non officielle).
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
