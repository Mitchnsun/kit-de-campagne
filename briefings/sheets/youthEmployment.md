# `youthEmployment` · Les jeunes et l'emploi (page composite)

La page « Les jeunes et l'emploi » n'a pas de fichier : ses quatre volets ont le leur (`youthUnemployment`, `youthActivity`, `apprenticeship` et `youthEurope`, saisis à la main le 2026-11-09, voir `youthUnemployment.md`, `youthActivity.md`, `apprenticeship.md` et `youthEurope.md`), dans l'ordre de leurs onglets : « Chômage des jeunes », « Emploi et NEET », « Apprentissage », « En Europe ». Elle est dans le dossier « Travail et retraites », à côté de la page « Chômage » (`unemployment`, scriptée), qui garde le taux de chômage d'ensemble depuis 1975, le taux des 15-24 ans, le taux d'emploi des 15-64 ans, les inscrits à France Travail et les départements : la page ne les refait pas. Cette fiche porte ce qui est commun aux volets.

**Vérifiée le 09/11/2026** : aucun chiffre faux dans les fichiers (voir les fiches des volets). La licence des sources n'a pas été vérifiée.

**Le 2e trimestre 2026.** Les valeurs du 2e trimestre 2026 (volets `youthUnemployment` et `youthActivity`) sont celles que l'Insee publiait au 09/11/2026 (Informations rapides n° 192 du 07/08/2026). L'Insee publie le 3e trimestre 2026 le 10/11/2026 à 7 h 30 (« La prochaine publication, portant sur le troisième trimestre 2026, est prévue le 10 novembre 2026 à 7h30. ») : la prochaine édition du kit les remplacera, et les trimestres passés peuvent être légèrement révisés (corrections saisonnières).

## Ce que la page dit, et ne dit pas

- Un taux de chômage n'est pas une part de la population. Le taux rapporte les chômeurs aux actifs (21,6 % des actifs de 15 à 24 ans au 2e trimestre 2026), la part de chômage à toute la population du même âge (9,3 %). Les deux sont affichés côte à côte, avec la définition de l'Insee ; c'est le « À savoir » lu en premier (`readFirst`) du premier onglet. Le titre de la série BDM de la part de chômage (« part dans la population de 15 ans ou plus ») est trompeur : la valeur est rapportée aux 15-24 ans (vérifié par le calcul, voir `youthUnemployment.md`).
- Le NEET de l'Insee (trimestriel, 15-29 ans, Mayotte comprise) et celui d'Eurostat (annuel, drapeau « d » pour la France) ne sont pas la même mesure : deux vues séparées, jamais comparées.
- « Son plus haut niveau depuis 1990 » est écrit pour la moyenne 2025 du taux d'activité des 15-24 ans (43,0 %), jamais pour le 2e trimestre 2026.
- Les entrées en apprentissage viennent d'une seule édition de l'Insee (2023 à 2025) : la série 2018-2025 assemblée à partir de cinq éditions n'est pas homogène et n'est pas saisie.
- Les phrases de la Cour des comptes sur l'effet de l'alternance sont citées mot pour mot : elles portent sur le taux d'emploi des jeunes, pas sur leur chômage, et ses deux documents disent « plus de la moitié » et « environ la moitié ».
- Tous les rangs européens sont calculés sur les 27 valeurs d'Eurostat et dits « calculés ». Le taux mensuel d'Eurostat n'est pas celui de l'Insee.
- Le Céreq (une génération de sortants interrogée trois ans après) et l'Insee (des actifs à une date) ne se comparent pas.
- Les calculs (un sur cinq, rangs, somme des programmes 103 et 364) ne sont jamais dans une série : seulement dans des notes ou des réponses, avec « calculé ».

Liens avec le jeu (registre de l'app) : thème « Travail et retraites » seulement. Le rapport proposait `voluntaryMilitaryService` (« Une formation militaire volontaire et rémunérée pour les jeunes, compatible avec les études ») et `fundedPension` (« Une épargne retraite pour chacun, avec 500 € versés par l'État dès le premier emploi ») : aucun chiffre de la page ne porte sur le service militaire ni sur l'épargne retraite, ils ne sont pas liés. Aucune autre mesure ni carte du moteur ne porte sur l'apprentissage, les aides à l'embauche ou le chômage des jeunes. Les chiffres du kit ne contiennent aucune donnée interne du jeu.

## Ce qu'on entend

Cinq affirmations (règle du PO du 09/11/2026 : seules les fausses vérités que les chiffres de la page démentent), chacune dans le volet dont elle cite les chiffres : « un jeune sur quatre est au chômage » et « le diplôme ne protège plus du chômage » (`youthUnemployment`) ; « les jeunes ne veulent plus travailler » (`youthActivity`) ; « l'apprentissage, c'est surtout pour les CAP » (`apprenticeship`) ; « la France a le pire chômage des jeunes d'Europe » (`youthEurope`). Écartées (`excluded` du rapport final) : « l'apprentissage a fait baisser le chômage des jeunes » (ni démentie ni confirmée : la Cour parle d'emploi et juge le lien causal « incertain ») ; les affirmations sur les chômeurs en général (« 6 millions de chômeurs », indemnisation, durée, inscription à France Travail), qui relèvent de la page sur le chômage au-delà du taux.

## Double vérification commune

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-jeunes.md` : chaque source retéléchargée (API SDMX de la BDM de l'Insee, API d'Eurostat, PDF passés à `pdftotext`, classeurs lus avec openpyxl). Le détail ligne à ligne est dans les fiches des volets. Ce qui est commun :

- Producteurs : tous officiels (Insee, Dares, DEPP, Céreq, Cour des comptes, DILA, Eurostat). Écartés comme sources de chiffres : OFCE, iFRAP, Institut Montaigne, chiffres de presse spécialisée.
- Bilan : aucune valeur fausse ni mal lue ; des réserves de lecture (titre BDM trompeur de la part de chômage, « plus haut depuis 1990 » réservé à la moyenne 2025, maximum de 28,0 % depuis 2003 seulement, rupture de l'indicateur ODD en 2020) ; une série retirée (entrées en apprentissage 2018-2025) et une série de dépenses retirée (aides à l'embauche 2019-2025, deux documents de la Cour à périmètres différents).
- Les quatorze séries trimestrielles de la BDM et les séries annuelles relues l'ont été valeur par valeur ; les séries trimestrielles saisies dans le volet `youthActivity` ont été relues de nouveau, le 09/11/2026, contre les fichiers téléchargés par la contre-vérification : identiques.
- Sources à ouvrir par le PO (aucun de leurs chiffres n'est dans les fichiers) : Insee, Informations rapides du 10/11/2026 (3e trimestre) ; Dares Résultats n° 3 de janvier 2026 (série homogène des entrées) ; page de la note DEPP 26.35 (jour de publication) ; graphique 4 du Céreq Bref 487-488 ; décret n° 2026-168 du 6 mars 2026.

**Conclusion.** Les quatre volets sont vérifiés, sans écart numérique ; la page ne doit jamais présenter le taux de chômage des jeunes comme une part de tous les jeunes, ni comparer le NEET de l'Insee à celui d'Eurostat, ni attacher « le plus haut depuis 1990 » au 2e trimestre 2026.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script (voir les fiches des volets).
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais (voir les fiches des volets).
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
