# `unemploymentBeyond` · Le chômage au-delà du taux (page composite)

La page « Le chômage au-delà du taux » n'a pas de fichier : ses deux volets ont le leur (`unemploymentSituations` et `unemploymentBenefits`, saisis à la main le 2026-11-09, voir `unemploymentSituations.md` et `unemploymentBenefits.md`), dans l'ordre de leurs onglets : « Situations », « Indemnisation ». Cette fiche porte ce qui leur est commun. Onze sources au total, plus que les 8 qu'un fichier accepte : d'où deux volets (5 et 6 sources).

**Vérifiée le 09/11/2026** : aucun chiffre faux dans les fichiers (voir les fiches des volets). La licence des sources n'a pas été vérifiée.

**Valeurs du 2e trimestre 2026** : ce sont celles que l'Insee publie au 09/11/2026 (Informations rapides n° 192 du 07/08/2026). L'Insee publie le 3e trimestre 2026 le 10/11/2026 à 7 h 30 (« Prochaine parution le : 10/11/2026 à 07h30 - troisième trimestre 2026 », page de l'IR n° 192) : la prochaine édition les remplacera, après relecture des révisions des trimestres passés. Les indemnisés du 2e trimestre 2026 (France Travail, données provisoires) et les inscrits du 3e trimestre 2026 (Dares) ne dépendent pas de cette publication.

## Ce que la page dit, et ne dit pas

- Elle ne refait pas la page « Chômage » (`unemployment`) : ni le taux d'ensemble depuis 1975, ni celui des 15-24 ans, ni le taux d'emploi, ni les séries des inscrits en A et en A, B, C, ni les départements. Elle donne les personnes là où la page « Chômage » donne le taux.
- Un chômeur au sens du BIT et un inscrit à France Travail ne sont pas la même chose, et le taux de chômage ne compte ni le halo ni le sous-emploi : c'est le « À savoir » lu en premier (`readFirst`) du premier onglet, celui que la page ouvre (une page composite n'a pas de textes à elle dans l'app). Le volet « Indemnisation » a le sien : un indemnisé n'est pas un chômeur au sens du BIT, et les trois montants de l'allocation ne forment pas une évolution.
- Chômeurs au sens du BIT (2e trimestre 2026, France entière) et inscrits (3e trimestre 2026, France hors Mayotte) ne sont jamais soustraits les uns des autres.
- Chaque part a son dénominateur, dit sur sa ligne : actifs (taux de chômage, chômage de longue durée), population des 15-64 ans (halo), personnes en emploi (sous-emploi). La note du bloc dit qu'elles ne se comparent pas entre elles. Le nombre du halo compte les 15 ans ou plus, sa part les 15-64 ans : jamais divisés l'un par l'autre.
- Les trois montants de l'allocation (droit et versé de France Travail, septembre 2025 ; perçu de l'Insee et de la Dares, décembre 2024) sont dans deux blocs, chacun avec son producteur, sa période et ce qu'il mesure ; aucune comparaison entre eux n'est présentée comme une évolution.
- Les 4,5 Md€ sont une estimation ex ante de l'Unédic (statut `projection`, dit « estimation ex ante » par la page) ; la page dit qu'elle ne porte pas sur un passage à 12 mois.
- La durée des droits (18 mois au plus hors filière seniors, contre 24 ; 16 mois en moyenne) n'est pas en barres : le format des fichiers n'a pas d'unité « mois ». Elle est dans la note du bloc de la réforme et dans un « À savoir ».
- Les calculs (25,1 % des chômeurs en chômage de longue durée, 99 % et 83,1 % de sommes de parts) ne sont jamais dans une série : seulement dans des notes, avec « calculé ».

Liens avec le jeu (registre de l'app) : thème « Travail et retraites » ; mesures `unemploymentReform` (la durée des droits et la réforme de 2023, que le volet « Indemnisation » situe), `banLayoffs` (9,5 % des chômeurs de 2025 ont été licenciés, dont un peu moins de la moitié pour motif économique), `fourDayWeek` et `end35Hours` (le sous-emploi : des personnes à temps partiel qui souhaitent travailler plus) ; carte `factoryClosure` (les licenciements, dont économiques). La carte garde sa ligne « En vrai » de la page « Chômage », placée avant dans le registre. Les chiffres du kit ne contiennent aucune donnée interne du jeu.

## Ce qu'on entend

Aucune affirmation (règle du PO du 09/11/2026 : seules les fausses vérités que les chiffres de la page démentent). Le rapport final (`final-jeunes.json`) n'a aucune affirmation de ce thème dans `claims` : ses cinq affirmations portent sur les jeunes et vont à la page `youthEmployment`. Affirmations écartées (`excluded`) qui touchent ce thème : « il y a 6 millions de chômeurs » (démentie pour les chômeurs au sens du BIT, 2 677 000, mais un chiffre voisin existe dans une autre mesure officielle : 5 847 500 inscrits en A, B, C et 6 587 600 en A à E ; l'écart est de définition), « la plupart des chômeurs sont indemnisés » (46,9 % des inscrits en A, B, C sont indemnisés, mais 67,9 % sont indemnisables, et ce sont des inscrits), « au chômage, on touche autant qu'en travaillant » (aucun taux de remplacement net lu), « les chômeurs le sont pour longtemps » (aucun seuil), « tous les jeunes chômeurs sont inscrits à France Travail » (propos non attesté). Leurs chiffres restent sur la page, sans affirmation.

## Double vérification commune

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-jeunes.md` : API SDMX de la BDM, `pdftotext` pour les PDF, pages de l'Insee et de France Travail en texte brut, tout retéléchargé. Bilan : aucune valeur du rapport de recherche fausse ni mal lue, aucun « Non retrouvé » parmi les chiffres retenus. Le détail ligne à ligne est dans les fiches des volets. Ce qui est commun :

- Producteurs : Insee (enquête Emploi, ECRT 2026), Dares et France Travail pour leurs propres statistiques, Unédic pour ses seuls chiffres d'assurance chômage. Écartés : les think tanks (OFCE, iFRAP, Institut Montaigne) et le « 6,7 Md€ » de l'Unédic vu dans un résumé de recherche (deux réformes cumulées).
- Erreurs de méthode du rapport de recherche corrigées par la contre-vérification : le montant versé de France Travail (1 090 € brut, septembre 2025) n'avait pas été relevé ; le champ du dossier D1 de l'Insee est la France hors Mayotte (2024), quand les chômeurs de 2026 sont France entière : rien n'est soustrait ; licences « etalab-2.0 » et « eurostat » écrites sans source dans les documents ouverts (le registre suit la règle du projet : Insee en `etalab-2.0`, le reste en citation seule).
- Relu à la saisie, le 09/11/2026 : la page de l'IR n° 192 (2 677 ; 1,9 million ; 4,4 % ; 671 000 ; 2,1 % ; 17,2 % ; « Prochaine parution le : 10/11/2026 »), la fiche F9 (47,0 ; 9,5 ; 8,4 ; 6,7 ; 11,5 %), la fiche F11 (1 075 euros ; 64 % ; 755 ; 48 % et 67 %), la page STMT de France Travail (5 847 500 ; 3 353 400 ; 6 587 600 ; 597 000 ; 386 100 ; inscription automatique depuis janvier 2025), les pages des notes 26.014 (67,9 %, 69,0 %, 46,9 %) et 26.015 (3 040 400) de France Travail. Les adresses anglaises des pages de l'Insee (`/en/statistiques/<même numéro>`) répondent 404 : sources marquées « en français seulement ».

**Conclusion.** Les deux volets sont vérifiés, sans écart numérique ; la page ne doit jamais soustraire les chômeurs des inscrits, ni comparer des parts de dénominateurs différents, ni présenter les trois montants comme une évolution.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script (voir les fiches des volets).
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais (voir les fiches des volets).
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
