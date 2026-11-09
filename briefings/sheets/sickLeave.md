# `sickLeave` · Les arrêts maladie (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; réserves de lecture reprises dans les notes des vues, dans « À savoir » et dans « Ce qu'on entend ». La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `sickLeave`, dossier « Travail et retraites » (`work`), aussi dans « Santé » (`alsoIn: ['health']`), page de type série |
| Données | `briefings/manual/sickLeave.json`, saisi à la main le 2026-11-09 depuis le rapport d'évaluation des politiques de sécurité sociale (REPSS) « Maladie » de 2026, indicateur 2.13.1, p. 210-213 |
| Sources | 1. Direction de la sécurité sociale, « Rapport d'évaluation des politiques de sécurité sociale, Maladie, édition 2026 » (annexe 1 au projet de loi d'approbation des comptes de la sécurité sociale 2025, indicateur 2.13.1, p. 210-213), https://evaluation.securite-sociale.fr/files/live/sites/Repss/files/M%C3%A9diath%C3%A8que/Rapports/PLACSS%202025%20-%20Edition%202026/PLACSS%202025%20Annexe%201%20-%20REPSS%20Maladie%202026.pdf ; 2. Cour des comptes, « La sécurité sociale 2024 » (chapitre V, p. 190 et tableau n° 24, p. 195), https://www.ccomptes.fr/sites/default/files/2024-05/20240529-RALFSS-2024.pdf ; 3. Commission des comptes de la sécurité sociale, « Les comptes de la Sécurité sociale, octobre 2026 » (fiche 2.3, tableau 1 ; synthèse pour le plafond des IJ AT-MP), https://www.securite-sociale.fr/files/live/sites/SSFR/files/medias/CCSS/2026/CCSS-octobre-2026_assemble_VDEF.pdf ; 4. DILA, service-public.gouv.fr, « Arrêt maladie : indemnités journalières versées au salarié » (F3053, vérifié le 01/06/2026), https://www.service-public.gouv.fr/particuliers/vosdroits/F3053 ; 5. DILA, service-public.gouv.fr, « La durée des arrêts de travail plafonnée depuis le 1er septembre » (A18962, publié le 16/06/2026, mis à jour le 01/09/2026), https://www.service-public.gouv.fr/particuliers/actualites/A18962 ; 6. DILA, service-public.gouv.fr, « Arrêts maladie : baisse de la durée d'indemnisation de certains arrêts longs » (A19066, publié le 24/09/2026, mis à jour le 20/10/2026), https://www.service-public.gouv.fr/particuliers/actualites/A19066. Licence « citation seule » pour les six, en français seulement |
| Dates de publication | 2026-05-26 (REPSS : date de création du PDF) ; 2024-05-29 (Cour des comptes : date du nom du fichier) ; 2026-10-05 (CCSS : date de création du PDF, comme pour `socialSpending`) ; 2026-06-01 (F3053 : « Vérifié le », la page ne donne pas d'autre date) ; 2026-09-01 et 2026-10-20 (A18962 et A19066 : dates de mise à jour des pages lues) |
| Séries | Toutes du REPSS, indicateur 2.13.1, Md€ courants, régime général y compris anciens affiliés du RSI, France entière, périmètre Ondam, montants bruts remboursés en date de soins, hors crise sanitaire. `total` : 2014, 2019 et 2025, 3 points (6,8 ; 8,2 ; 11,3), les seuls totaux écrits dans le texte (« hors crise sanitaire, grippe et professions libérales ») ; `shortTerm` (arrêts de moins de 3 mois), `longTerm` (plus de 3 mois) et `selfEmployed` (indépendants) : 2014 à 2025, 12 points chacun, lus sur les étiquettes du graphique 1 (moins de 3 mois : 3,9 ; 4,0 ; 4,2 ; 4,4 ; 4,5 ; 4,7 ; 4,9 ; 5,1 ; 5,6 ; 5,9 ; 6,2 ; 6,1 ; plus de 3 mois : 2,7 ; 2,8 ; 2,9 ; 3,0 ; 3,2 ; 3,3 ; 3,6 ; 3,8 ; 4,0 ; 4,1 ; 4,5 ; 4,8 ; indépendants : 0,3 ; 0,2 ; 0,2 ; 0,2 ; 0,2 ; 0,3 ; 0,3 ; 0,3 ; 0,3 ; 0,4 ; 0,4 ; 0,4) |
| Chiffre clé | 11,3 Md€ d'indemnités journalières maladie hors crise sanitaire en 2025, en hausse (8,2 Md€ au point précédent de la série, 2019) ; à côté, 6,1 Md€ pour les arrêts de moins de 3 mois et 4,8 Md€ pour ceux de plus de 3 mois |
| Règles | Saisie à la main, une seule source pour les séries : le REPSS de 2026. Jamais raccordée à une autre série (comptes de la CCSS, données ouvertes de la Cnam, Cour des comptes) : périmètres différents. Le total n'est saisi que pour les trois années que le texte écrit ; aucune somme des composantes n'est calculée. Les montants Covid et le nombre d'arrêts de 2022 (Cour des comptes) et le montant de la CCSS sont dans les notes, avec leur année. La colonne `act_dnb` de la Cnam (« journées », non confirmée) n'est pas utilisée. Des cinq règles récentes, quatre sont dans deux « À savoir » ; le plafond des IJ AT-MP est ici seulement (voir plus bas) |
| Première édition | À remplir à la publication |

## « À savoir »

1. Les arrêts liés au Covid sont hors de cette série. Selon la Cour des comptes, ils ont coûté au régime général 2,1 Md€ en 2020, 0,85 Md€ en 2021 et 1,7 Md€ en 2022. Cette année-là, la Cour dénombre 8,9 millions d'arrêts de travail pour maladie indemnisés. Source : Cour des comptes, « La sécurité sociale 2024 », tableau n° 24, p. 195 (« Sous-total IJM covid 19 2,1 0,85 1,7 4,6 », « dans le régime général », d'après la CCSS) et p. 190 (« La même année, 8,9 millions d'arrêts de travail pour maladie indemnisés ont été dénombrés. » ; le champ « régime général » est celui de la phrase précédente, la note ne le répète pas).
2. La Commission des comptes de la sécurité sociale compte 11,1 Md€ d'indemnités journalières maladie du régime général en 2025, en soins de ville. La série de la Direction de la sécurité sociale écarte la grippe et les professions libérales et corrige les variations saisonnières : les deux ne se raccordent pas. Sources : CCSS, octobre 2026, fiche 2.3, tableau 1 (« IJ Maladie 11 122 11 204 » ; « Données cjo […] France Entière, Régime général + anciens affiliés RSI ») ; REPSS, p. 212-213 (« ne comprend pas ceux des professions libérales et de grippe » ; « corrigées des variations saisonnières (cvs) et des jours ouvrés (cjo) »).
3. Pour un salarié du privé, l'indemnité de la Sécurité sociale vaut 50 % du salaire journalier de base, calculé sur un salaire plafonné à 1,4 Smic pour les arrêts débutés depuis le 1er avril 2025 (1,8 Smic avant), soit 42,97 € bruts par jour au plus, versés après 3 jours de carence. Source : F3053 (« Les indemnités journalières (IJ) sont égales à 50 % du salaire journalier de base. » ; « plafonné à 1,4 fois le montant du Smic » ; « Les IJ ne peuvent pas dépasser 42,97 € bruts. » ; « Pour les arrêts ayant débuté avant le 1ᵉʳ avril 2025, l'ancien plafond reste applicable : […] 1,8 fois le montant du Smic » ; « Les IJ sont versées après un délai de carence de 3 jours. »).
4. Depuis le 1er septembre 2026, un premier arrêt est prescrit pour 31 jours au plus et chaque prolongation pour 62 jours, prolongeables si l'état de santé le nécessite. Depuis le 15 octobre 2026, certains arrêts de plus de 6 mois sont indemnisés 1 an au plus au lieu de 3 ans, qui restent la règle en ALD. Sources : A18962 (« la durée d'un arrêt maladie ne pourra plus dépasser 31 jours (pour la première prescription) ; chaque prolongation d'arrêt ne pourra pas dépasser 62 jours » ; « Il sera possible de prolonger l'arrêt maladie au-delà de la durée plafonnée si le professionnel de santé estime que l'état de santé du salarié le nécessite ») ; A19066 (« abaisse de 3 à 1 an la durée maximale dérogatoire d'indemnisation des arrêts de travail pour certains assurés atteints d'une affection […] supérieur à 6 mois, mais qui ne découle pas d'un accident du travail, d'une maladie professionnelle ou d'une affection de longue durée (ALD) » ; « reste aussi fixée à 3 ans maximum pour les assurés atteints d'une ALD »).

Les quatre points en anglais disent la même chose que le français.

**Règle gardée dans la fiche seulement** : le plafond du salaire de référence des indemnités journalières des accidents du travail et maladies professionnelles est abaissé à 1,8 Smic au 1er novembre 2026 (CCSS, octobre 2026, synthèse : « abaissement au 1er novembre de 0,834 % du plafond annuel de la sécurité sociale à 0,226 %, soit 1,8 SMIC » ; la Cour des comptes, « La situation financière de la sécurité sociale », 20/10/2026, chiffre l'économie à 0,2 Md€, relu dans la copie de l'auteur, décret n° 2026-909).

Notes des vues (dans l'app) : la vue « Ensemble » dit le champ du total (régime général, anciens indépendants compris, France entière, hors crise sanitaire, grippe et professions libérales, euros courants) et qu'il n'est publié que pour 2014, 2019 et 2025 ; la vue « Selon la durée de l'arrêt » dit que les valeurs sont lues sur le graphique, arrondies au dixième, et que leur somme peut différer du total de 0,1 Md€.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/sickLeave.json` (clé `claims`, français et anglais). Ne restent que les fausses vérités que les chiffres de la page démentent (décision du PO du 09/11/2026). Source de chaque chiffre de la réponse :

1. « On entend que la hausse des dépenses d'arrêts maladie vient uniquement du Covid. » 6,8 Md€ (2014), 8,2 Md€ (2019) et 11,3 Md€ (2025), hors crise sanitaire : REPSS, p. 210 (« passant de 6,8 Md€ en 2014 à 11,3 Md€ en 2025 » ; « Entre 2014 et 2019, les dépenses d'IJ sont passées de 6,8 Md€ à 8,2 Md€ »). Les facteurs cités sont ceux du REPSS, p. 210 (croissance et vieillissement de la population active, durée moyenne des arrêts, salaires, Smic et SMPT, taux de recours). L'affirmation du rapport de recherche disait « la hausse des arrêts maladie » : précisée en « des dépenses d'arrêts maladie », puisque les chiffres sont des dépenses, pas un nombre d'arrêts. Le surcoût Covid de 2,3 Md€ (REPSS) n'est pas cité : la page donne celui de la Cour des comptes.
2. « On entend que la Sécurité sociale paie l'arrêt maladie en totalité, dès le premier jour. » 50 %, 1,4 Smic, 42,97 € bruts, 3 jours de carence : F3053. L'affirmation du rapport de recherche disait « l'arrêt maladie est payé en totalité et dès le premier jour » : précisée en « la Sécurité sociale paie », car le complément de l'employeur ou de la convention collective peut, pour certains salariés, porter le total plus haut ; les chiffres de la page démentent l'affirmation pour l'indemnité de la Sécurité sociale seulement.
3. « On entend qu'un arrêt maladie n'a aucune limite de durée. » 3 ans en ALD, 1 an pour certains arrêts de plus de 6 mois depuis le 15 octobre 2026 : A19066. 31 et 62 jours depuis le 1er septembre 2026, prolongeables : A18962 (qui note qu'« initialement, la durée des arrêts de travail n'était pas soumise à un plafonnement légal » : la réponse met donc d'abord la durée maximale d'indemnisation).

Affirmation du rapport de recherche non retenue : « On entend que la dépense d'indemnités journalières maladie s'envole encore chaque année. » Les chiffres (+ 2,3 % en 2025 hors Covid, + 0,7 % prévu en 2026) la nuancent sans la démentir : la dépense augmente encore.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web (rapport `verify-nonrecours-arrets.md`) : le REPSS retéléchargé (identique octet pour octet à la copie de l'auteur) et son graphique relu sur l'image de la page, la Cour des comptes et la CCSS retéléchargées, les pages de service-public.gouv.fr rouvertes. Aucun écart de valeur.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé et totaux | 6,8 (2014), 8,2 (2019), 11,3 (2025) Md€ | phrases exactes du texte, « multipliées par 1,7 » | REPSS (URL ci-dessus) | Conforme |
| Composantes 2014-2025 | 36 valeurs du graphique 1 | étiquettes relues sur l'image : toutes conformes | REPSS, graphique 1, p. 210 | Conforme avec réserve : arrondies au dixième (somme 6,9 contre 6,8 en 2014, 8,3 contre 8,2 en 2019) ; le texte dit « hors grippe », la légende « courte durée (yc grippe) » : ambiguïté non levée |
| Covid (note) | 2,1 ; 0,85 ; 1,7 Md€ | tableau n° 24 relu | Cour des comptes, « La sécurité sociale 2024 » | Conforme |
| Arrêts indemnisés 2022 (note) | 8,9 millions | phrase relue | idem, p. 190 | Conforme avec réserve : champ « régime général » implicite |
| CCSS 2025 (note) | 11,1 Md€ | 11 122 M€ | CCSS, octobre 2026, fiche 2.3 | Conforme |
| Règles de calcul (note) | 50 %, 1,4 Smic, 42,97 €, 3 jours | page rouverte, vérifiée le 01/06/2026 | F3053 | Conforme |
| Durées (note) | 31 et 62 jours ; 3 ans à 1 an | pages rouvertes | A18962, A19066 | Conforme ; la réduction à 1 an ne vise que certains arrêts hors ALD, AT et MP |
| Plafond AT-MP (fiche) | 1,8 Smic au 1er novembre 2026 | synthèse de la CCSS retéléchargée ; Cour relue dans la copie de l'auteur | CCSS, octobre 2026 | Conforme |

**Conclusion.** Aucun chiffre du fichier n'est faux ; quatre mesures différentes des mêmes indemnités existent (REPSS, CCSS, comptes de la CNAM, données ouvertes de la Cnam) : la page n'en trace qu'une et cite la CCSS dans une note qui dit pourquoi elle diffère.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus. Le descriptif des variables de la Cnam (`act_dnb`) était derrière un contrôle anti-robot : la série de la Cnam n'est pas utilisée.

## Réserves

- Les composantes sont des étiquettes de graphique, arrondies au dixième ; le total n'est publié que pour 2014, 2019 et 2025.
- Ambiguïté sur la grippe : le texte du REPSS l'écarte (« hors crise sanitaire, grippe et professions libérales » ; « ne comprend pas ceux des professions libérales et de grippe »), la légende du graphique dit « courte durée (yc grippe) ».
- La croissance de 2024 n'est pas reprise : le REPSS écrit + 6,4 % (« Résultats ») et + 6,6 % (corps du texte).
- Le suivi des IJ Covid est arrêté en 2025 ; le motif d'un arrêt n'est pas toujours renseigné (REPSS, « Précisions méthodologiques »).
- Non utilisés : la série des données ouvertes de la Cnam (unité « journées » non confirmée, Covid non isolé, années 2011-2024 non revérifiées), les comptes de la CCSS 2013-2023 (périmètre changeant), les euros constants (calcul de l'auteur), la décomposition de la hausse 2017-2022 par la Cour.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a relu le REPSS et l'image de son graphique.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée : le registre dit « citation seule » (chiffres cités, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
