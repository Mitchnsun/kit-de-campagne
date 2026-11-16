# `defenceStaff` · Les effectifs et la réserve (saisi à la main)

**Vérifiée le 16/11/2026** : double vérification sur le web par un agent Claude (modèle Sonnet), 15/11/2026, sans écart de valeur (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `defenceStaff`, dossier « Défense et Europe » (`defence`), troisième volet (« Effectifs ») de la page composite `defenceMeans` (voir `defenceMeans.md`), page de type comparaison, ticket #442 de l'app |
| Données | `briefings/manual/defenceStaff.json`, saisi à la main le 2026-11-16 depuis le projet annuel de performances 2027 de la mission « Défense » |
| Sources | Direction du budget, « Projet annuel de performances 2027, mission « Défense » », https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128221/file/PAP%202027%20-%20D%C3%A9fense.pdf (01/10/2026), Licence Ouverte 2.0, en français seulement. Le document écrit « ministère des Armées » (et « ministère des armées » dans l'indicateur 4.1) ; la source de l'indicateur 4.1 est l'« État-major des Armées / Division Cohésion nationale (EMA/DCN) » |
| Séries | `reservists` : réservistes opérationnels au 31 décembre, annuelle, indicateur 4.1 « Réserve opérationnelle » (p. 106) : 43 797 (2024) et 48 801 (2025) réalisés, puis les cibles 52 000 (2026, « Cible PAP 2026 »), 57 500 (2027), 64 000 (2028), 71 500 (2029) ; 2026 à 2029 en `projection`, dits « prévision » par la page. Les 80 000 de 2030 ne sont pas un point de la série : le projet annuel parle d'un « objectif de recruter 80 000 réservistes et 10 000 appelés du service national en 2030 » (p. 92), un nombre à recruter, que la note 1 cite tel quel. `staffTotal` : plafond d'emplois demandé pour 2027, 277 877,45 ETPT (`projection`), p. 237 |
| Répartition | `staff2027` : le même plafond par catégorie d'emplois, en ETPT, dans l'ordre du tableau « Emplois rémunérés par le programme » du programme 212 (p. 236-237, colonne « Plafond demandé pour 2027 ») : catégorie A 19 887,96 ; B 17 422,94 ; C 18 973,08 ; ouvriers de l'État 9 072,38 ; officiers 37 074,27 ; sous-officiers 92 816,13 ; militaires du rang 74 665,86 ; volontaires 884,08 ; volontaires stagiaires du SMV 1 300,00 ; apprentis militaires 1 780,75 ; appelés du service national 4 000,00 ; somme 277 877,45, le total du tableau |
| Chiffre clé | 48 801 réservistes fin 2025, en hausse (43 797 fin 2024) ; à côté, la cible de 71 500 en 2029 et les 277 877 emplois du projet pour 2027, « prévision » |
| Règles | Saisie à la main. Réservistes : ceux de la réserve opérationnelle de premier niveau sous contrat d'engagement à servir dans la réserve (ESR), « soldés par le ministère », au 31 décembre ; « Les cibles sont celles de la LPM 2024-2030 pour le périmètre du ministère des armées » (mode de calcul de l'indicateur). Ni la réserve opérationnelle de deuxième niveau, ni la réserve de la gendarmerie, ni la réserve citoyenne. Les ETPT du budget ne se comparent ni aux ETP des cibles de la loi (268 400 en 2027, 275 000 en 2030, apprentis, volontaires du SMV et appelés exclus) ni aux militaires de l'OTAN (202 000 en 2026, estimation) |
| Première édition | À remplir à la publication |

## « À savoir »

1. Qui sont les réservistes comptés, et les cibles. Source : indicateur 4.1, p. 106 (« Sont comptabilisés les effectifs des réservistes sous contrat d'engagement à servir dans la réserve (ESR) de la réserve opérationnelle de premier niveau (RO1) au 31 décembre. Le chiffre correspond aux réservistes soldés par le ministère des armées ») ; p. 92 (80 000 en 2030) ; loi n° 2026-791, rapport annexé (« L'objectif d'atteindre, à l'horizon 2035, un militaire réserviste pour deux militaires d'active »). Les 105 000 réservistes de 2035 que citent l'audition du général Crach (commission de la défense, 03/12/2025) et des députés ne sont pas dans le texte de la loi de 2026 : la note dit « un réserviste pour deux militaires d'active », comme la loi.
2. ETPT et ETP. Source : p. 236-237 (277 877,45 ETPT ; « Le plafond demandé pour 2027 s'élève à 277 877 ETPT, en hausse de +5 598 ETPT par rapport à 2026 ») ; militaires 212 521 (officiers, sous-officiers, militaires du rang, volontaires, volontaires stagiaires du SMV, apprentis militaires, appelés) et civils 65 356 (catégories A, B, C, ouvriers de l'État), calculés ; loi n° 2026-791, article 5 (« les emplois financés par les crédits de personnel du ministère de la défense, à l'exclusion des apprentis civils et militaires, des volontaires du service militaire volontaire et des appelés du service national […] s'élèveront à 268 400 équivalents temps plein en 2027 et à 275 000 équivalents temps plein en 2030 »).
3. Le service national. Source : p. 237 (« Il intègre une nouvelle catégorie d'emplois afin d'assurer le suivi des appelés du service national (objectif de 3 000 recrutements en 2026 et 4 000 en 2027) », lu le 16/11/2026, hors de la recherche) ; loi n° 2026-791, rapport annexé (« Appelés du service national 3 000 4 000 5 000 7 500 10 000 » de 2026 à 2030 ; « le nouveau service national (2,3 milliards d'euros sur la période 2026-2030 […]) »). Le chiffrage de la mesure `voluntaryMilitaryService` du jeu (2,3 Md€ de 2026 à 2030) est le même.
4. Retiré le 16/11/2026 (voir « Mises à jour ») ; pour mémoire, les militaires de l'OTAN : fichier de l'OTAN de juillet 2026 (`def-exp-2026-en.xlsx`, « Table 7 », « Thousands », France 2026e : 202,0 ; note : « peacetime strength of military personnel, which excludes trained reserves held at high readiness »), cité en texte, crédité à l'OTAN.

Les quatre points en anglais disent la même chose que le français.

## Double vérification

Faite le 15/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web (rapport `check-gap-g2.md`, § 2), le projet annuel de performances et la loi retéléchargés et relus avec `pdftotext`.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, réservistes fin 2025 | 48 801 | indicateur 4.1, p. 106 : 43 797 (2024), 48 801 (2025), cibles 52 000 ; 57 500 ; 64 000 ; 71 500 | projet annuel de performances 2027 « Défense » (URL ci-dessus) | Conforme |
| Objectif 2030 | 80 000 | p. 92 : « recruter 80 000 réservistes et 10 000 appelés du service national en 2030 » (absent du tableau de l'indicateur) | idem | Conforme ; un nombre à recruter, pas un effectif : hors de la série depuis le 16/11/2026, cité tel quel par la note 1 |
| Autre source sur la réserve | 48 801 au 31/12/2025 | audition du général Crach : « environ 48 600 réservistes au 31 octobre 2025 », « en avance sur l'objectif de 47 600 à fin 2025 » ; « de 40 000 il y a deux ans à 80 000 en 2030, puis 105 000 à l'horizon 2035 » | https://www.assemblee-nationale.fr/dyn/17/comptes-rendus/cion_def/l17cion_def2526022_compte-rendu.pdf | Conforme (deux dates différentes, pas de contradiction) |
| Emplois par catégorie | 11 catégories, 277 877,45 | identiques ligne par ligne, 2026 : 272 279,09 ; « 277 877 ETPT, +5 598 » ; 4 000 appelés | projet annuel de performances 2027, p. 236-237 | Conforme |
| Cibles de la loi | 268 400 et 275 000 ETP (note) | article 5 : identiques, apprentis, SMV et appelés exclus | https://www.assemblee-nationale.fr/dyn/17/textes/l17t0325_texte-adopte-seance.pdf | Conforme |
| Service national | 3 000 → 10 000 ; 2,3 Md€ (note) | rapport annexé : tableau des appelés et « 2,3 milliards d'euros sur la période 2026-2030 » | idem | Conforme |
| Militaires de l'OTAN | 202 000 en 2026 (note) | Table 7 : 201,3 ; 201,7 ; 202,0 milliers ; note « excludes trained reserves held at high readiness » | https://www.nato.int/content/dam/nato/webready/documents/finance/def-exp-2026-en.xlsx | Conforme |

**Conclusion.** Les valeurs sont celles du projet annuel de performances 2027 ; les cibles de 2026 à 2030 sont des cibles de la programmation, et les emplois de 2027 un plafond demandé, pas un effectif.

**Pages consultées** le 15/11/2026 (et le 16/11/2026 pour les pages 92, 106, 236 et 237 du projet annuel) : les URL ci-dessus.

## Mises à jour

- **16/11/2026** (#442 de l'app, suite de la double vérification sur le web par un agent Claude (modèle Sonnet), 16/11/2026 (rapport `check-defence-notes.md`, § 4)) : les 80 000 de 2030 sont un « objectif de recruter 80 000 réservistes » (projet annuel, p. 92), pas un effectif au 31 décembre : le point 2030 quitte la série `reservists` (2024 à 2029 désormais) et la note 1 cite le verbe du document ; à côté du chiffre clé, la cible de 2029. La note 4 (les 202 000 militaires comptés par l'OTAN) est retirée tant que le volet `natoShare` attend la réponse de l'OTAN (décision du PO du 16/11/2026, voir `natoShare.md`) : la page ne montre plus aucun chiffre de l'OTAN. Trois notes restent.

## Relecture

- [x] Le chiffre clé et quelques points recoupés ailleurs que dans le document saisi (audition du 03/12/2025, loi).
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO (les 105 000 réservistes de 2035, absents de la loi de 2026, ne sont pas repris).
