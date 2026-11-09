# `publicEmployment` · Emploi public (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; réserves de lecture (deux totaux d'agents, avec ou sans contrats aidés ; niveaux de l'Insee non comparables aux publications antérieures), reprises dans « À savoir ». La licence de la DGAFP n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `publicEmployment`, dossier « Économie et fiscalité » (`economy`), aussi dans « Travail » (`alsoIn: ['work']`), page de type comparaison |
| Données | `briefings/manual/publicEmployment.json`, saisi à la main le 2026-11-09 depuis l'Insee Première n° 2094 (10/02/2026) et les Chiffres clés 2026 de la DGAFP |
| Sources | Insee, « L'emploi dans la fonction publique en 2024 » (Insee Première n° 2094, paru le 10/02/2026), https://www.insee.fr/fr/statistiques/8732435, PDF https://www.insee.fr/fr/statistiques/fichier/8732435/IP2094.pdf, Licence Ouverte 2.0, en français seulement ; DGAFP, « Fonction publique, Chiffres clés, édition 2026 », https://www.fonction-publique.gouv.fr/files/files/publications/publications-dgafp/cc-2026-web.pdf, « citation seule », en français seulement |
| Séries | `publicAgents` : agents de la fonction publique au 31 décembre, contrats aidés compris, France hors Mayotte, postes principaux, 2024, 1 point (5 876 700 ; Insee) ; `contractShare` : part des contractuels parmi les agents publics, %, 2024, 1 point (24,0 ; Insee) ; `publicShareOfEmployment` : part de la fonction publique dans l'emploi total, salarié et non salarié, %, 2024, 1 point (19,8 ; DGAFP) ; `administrationRate` : agents pour 1 000 habitants, hors militaires et hors Mayotte, 2024, 1 point (77 ; DGAFP) |
| Valeurs par catégorie | `bySide` (2024, Insee, contrats aidés compris) : État 2 587 400 ; territoriale 2 039 400 ; hospitalière 1 249 900 (somme 5 876 700). `byStatus` (2024, DGAFP, hors contrats aidés) : fonctionnaires 3 745 800 ; contractuels 1 407 700 ; militaires 312 900 ; autres catégories et statuts 381 900 (somme 5 848 300, « 5,85 millions ») |
| Chiffre clé | 5,9 millions d'agents (5 876 700) dans la fonction publique fin 2024, contrats aidés compris, sans tendance (un seul point saisi ; l'Insee donne + 0,6 % sur un an, dans « À savoir ») |
| Règles | Saisie à la main. Deux producteurs, deux totaux : les versants viennent de l'Insee (contrats aidés compris, 5 876,7 milliers), les statuts de la DGAFP (hors contrats aidés, 5,85 millions), ce que disent les notes des deux blocs. Les parts de contractuels par versant (26, 23 et 22 %) et les taux d'administration par région (93, 85 et 74 ‰) de la recherche ne sont pas saisis : la double vérification ne les a pas relevés. La phrase de la recherche selon laquelle les entreprises publiques ne sont pas dans la fonction publique n'est pas reprise (non lue dans la source) |
| Première édition | À remplir à la publication |

## « À savoir »

1. Les 5,9 millions d'agents de l'Insee comptent les contrats aidés. Selon l'Insee, ces niveaux ne sont pas totalement comparables à ceux de ses publications antérieures ; l'évolution entre 2023 et 2024 l'est : + 0,6 %, soit 32 800 agents de plus. Source : Insee Première n° 2094 (« Fin 2024, 5,9 millions d'agents travaillent dans la fonction publique : c'est 32 800 agents de plus que l'année précédente, soit +0,6 % » ; avertissement sur la comparabilité des niveaux), URL ci-dessus.
2. Les agents par statut viennent de la DGAFP, hors contrats aidés : leur total, 5,85 millions, se rapproche des 5 850 900 agents hors contrats aidés de l'Insee, pas de ses 5 876 700 agents contrats aidés compris. Source : DGAFP, Chiffres clés 2026 (« 5,85 millions d'agents publics travaillent dans les trois versants de la fonction publique au 31 décembre 2024 » ; « La fonction publique emploie 3 745 800 fonctionnaires, 1 407 700 contractuels, 312 900 militaires et 381 900 agents relevant des « autres catégories et statuts ». ») ; Insee Première n° 2094 (5 850,9 milliers hors contrats aidés).
3. Les contractuels représentent 24,0 % des agents publics fin 2024, 0,7 point de plus qu'en 2023 et 7,6 points de plus que dix ans auparavant, selon l'Insee. Source : Insee Première n° 2094 (« la part des contractuels au sein des agents publics s'élève à 24,0 %, soit 0,7 point de plus qu'en 2023 et 7,6 points de plus que dix ans auparavant »).
4. Selon la DGAFP, le taux d'administration est de 77 agents pour 1 000 habitants, hors militaires et hors Mayotte. La part de 19,8 % rapporte la fonction publique à tout l'emploi de 2024, salarié et non salarié, contrats aidés compris. Source : DGAFP, Chiffres clés 2026 (« Le taux d'administration (hors militaires) dans les trois versants de la fonction publique est de 77 agents pour 1 000 habitants (hors Mayotte). » ; « Lecture : En 2024, la fonction publique représente 19,8 % de l'emploi total (salarié et non salarié) en France. » ; champ : 15 ans ou plus, contrats aidés compris, hors Mayotte).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

L'affirmation est dans `briefings/notes/publicEmployment.json` (clé `claims`, français et anglais), reprise des affirmations relues du rapport de recherche du 09/11/2026. Source de chaque chiffre de la réponse :

1. « On entend qu'il y a trop de fonctionnaires, 5,9 millions de fonctionnaires. » 5,9 millions d'agents fin 2024 : Insee Première n° 2094. 3 745 800 fonctionnaires, 1 407 700 contractuels, 312 900 militaires et 381 900 agents d'autres statuts, hors contrats aidés : DGAFP, Chiffres clés 2026. 24,0 % de contractuels : Insee. 19,8 % de l'emploi total et 77 agents pour 1 000 habitants hors militaires : DGAFP. La réponse de la recherche est réécrite pour nommer chaque producteur et dire que les statuts sont hors contrats aidés (leur somme, 5,85 millions, n'est pas les 5,9 millions de l'Insee). La presse (franceinfo, « Vrai ou faux », 08/09/2026) écrit que « les 3,7 millions … ne sont pas autant de bureaucrates » : contexte seulement, aucun chiffre repris.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web (rapport `verify-social.md`) : les deux PDF rouverts et passés à `pdftotext`. Producteurs officiels seulement. Aucun écart de valeur, aucun chiffre non retrouvé.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, agents | 5 876 700 (2024) | 5 876,7 milliers ; État 2 587,4, territoriale 2 039,4, hospitalière 1 249,9 (somme refaite) ; 5 850,9 hors contrats aidés ; avertissement de non-comparabilité des niveaux retrouvé | https://www.insee.fr/fr/statistiques/fichier/8732435/IP2094.pdf | Conforme avec réserve : niveaux non comparables aux publications antérieures |
| Agents par statut | 3 745 800 / 1 407 700 / 312 900 / 381 900 | retrouvés ; somme 5 848 300 ≈ 5,85 millions | https://www.fonction-publique.gouv.fr/files/files/publications/publications-dgafp/cc-2026-web.pdf | Conforme |
| Part des contractuels | 24,0 % | « s'élève à 24,0 %, soit 0,7 point de plus qu'en 2023 » ; 1 407 700 / 5 876 700 = 24,0 % refait | Insee Première n° 2094 | Conforme |
| Part dans l'emploi total | 19,8 % | « Lecture : En 2024, la fonction publique représente 19,8 % de l'emploi total … » | DGAFP, Chiffres clés 2026 | Conforme |
| Taux d'administration | 77 ‰ | « … 77 agents pour 1 000 habitants (hors Mayotte). » | DGAFP, Chiffres clés 2026 | Conforme |
| Dates de publication | 2026-02-10 (Insee), 2026-10-05 (DGAFP) | Insee : « Paru le 10/02/2026 », relu sur la page https://www.insee.fr/fr/statistiques/8732435 le 09/11/2026 par l'agent qui a écrit la page ; DGAFP : date du fichier | URL ci-dessus | Conforme avec réserve : la date de la DGAFP est celle du PDF |

**Conclusion.** Aucun chiffre du fichier n'est faux ; un agent public n'est pas forcément fonctionnaire, et les deux totaux (avec ou sans contrats aidés) ne se mélangent pas.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus. La comparaison internationale de l'OCDE (Panorama des administrations publiques) était inaccessible et n'est pas utilisée ; la figure 1 des Chiffres clés (série depuis 1989) n'est pas lisible en texte.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert les deux documents ; les statuts de la DGAFP recoupent le total de l'Insee hors contrats aidés.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée : le registre dit « Licence Ouverte 2.0 » pour l'Insee, « citation seule » pour la DGAFP.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
