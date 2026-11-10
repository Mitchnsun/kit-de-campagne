# `housing` · Le logement (page composite)

La page « Le logement » n'a pas de fichier : ses six volets ont le leur (`housingStock`, `housingConstruction`, `housingCosts`, `socialHousing`, `housingAid` et `housingEurope`, saisis à la main le 2026-11-10, voir leurs fiches), dans l'ordre de leurs onglets : « Le parc », « Construire », « Prix, taux d'effort, encadrement », « Logement social », « Aides et hébergement », « En Europe ». Elle est dans le dossier « Pouvoir d'achat et logement », à côté de la page « Pouvoir d'achat » (`costOfLiving`), qui garde l'IRL et l'ILH (volet `rentIndices`) et les foyers aidés par les CAF (volet `socialBenefits`) : la page ne les refait pas. Cette fiche porte ce qui est commun aux volets.

**Vérifiée le 10/11/2026** : aucun chiffre faux dans les fichiers (voir les fiches des volets). La licence des sources n'a pas été vérifiée. Page de la recherche du 09/11/2026 (« Ce qu'on entend ») ; les chiffres ont été relevés et contre-vérifiés le 10/11/2026 (rapport `verify-logement.md`), d'où la date de récupération des fichiers.

## Ce que la page dit, et ne dit pas

- Un logement vacant n'est pas forcément un logement disponible, et un taux de propriétaires dépend de ce qu'on compte (ménages pour l'Insee, personnes pour Eurostat) : c'est le « À savoir » lu en premier (`readFirst`) du premier onglet. Les 2,9 millions de vacants de l'Insee comprennent la vacance de rotation : c'est le chiffre vrai, pas un gisement ; la vacance de plus de deux ans du parc privé (LOVAC) est une autre source, à ruptures de série.
- Les logements commencés et autorisés par an sont des sommes des mois publiés par le SDES, calculées et dites telles ; « le plus bas depuis 2002 » est écrit « le plus bas de la série, qui commence en 2002 (calculé) ».
- Le taux d'effort brut du quart le plus modeste baisse (40,8 → 39,0 %), le net monte (31,0 → 32,1 %) : la page ne présente jamais 39,0 % comme une hausse.
- Les loyers de l'IPC face à l'ensemble des prix sont calculés : dans une note seulement, avec « calculé ».
- L'effet de l'encadrement des loyers (−2 à −4 %) est toujours donné avec la baisse de 8 % de l'offre locative privée (DG Trésor), et la fin de l'expérimentation avec ses deux dates (23 novembre 2026 à Lyon et Villeurbanne, 24 ailleurs).
- Les demandes de logement social (un stock) et les attributions (un flux) sont dans deux vues séparées, sans ratio.
- Le chiffre d'occupation des immigrés en logement social (Insee) n'est que dans un « À savoir » du volet `socialHousing`, avec l'explication de l'Insee, la mention « occupation, pas attribution » et le rappel qu'un immigré peut être devenu Français.
- Les études sur l'effet des aides sur les loyers sont chacune données avec leur champ et leur date ; l'article de 2005 est attribué à la revue Économie et Statistique, pas à « l'Insee ».
- Les rangs européens sont calculés et dits tels.
- Aucun nom de personne réelle dans les textes ni dans les fichiers.

Liens avec le jeu (registre de l'app) : thème « Pouvoir d'achat et logement » ; mesures `affordableHousing` (« 400 000 logements abordables par an », « la réquisition des logements vacants » : la construction, l'objectif, la vacance), `rentControl` (« Encadrer strictement les loyers » : les neuf territoires et l'effet), `socialHousingPriority` (« Les logements sociaux attribués d'abord aux Français » : les règles d'accès, l'affirmation sur les étrangers), `residenceForBenefits` (« Les prestations non contributives après cinq ans de résidence » : les aides personnelles au logement) ; carte `coldSnap` (« Chiffrer un plan d'hébergement d'urgence » : les sans-domicile et les places d'hébergement). Non lié : `insulation` (« Rénover 700 000 logements par an ») : aucun chiffre de la page ne porte sur la rénovation, le parc par classe de DPE n'ayant pas été revérifié. Les chiffres du kit ne contiennent aucune donnée interne du jeu.

## Ce qu'on entend

Deux affirmations (règles du PO du 09/11/2026 : seules les fausses vérités que les chiffres de la page démentent ; pour un stéréotype que rien de mesuré ne tranche, la réponse des instances officielles et « Ce n'est pas parce que ce n'est pas évalué que c'est vrai. »), chacune dans le volet dont elle cite les chiffres : « les Français sont presque tous propriétaires » (`housingStock`) et « les HLM vont d'abord aux étrangers » (`socialHousing`). Écartées (`excluded` du rapport final) : « il y a 3 millions de logements vides » (le compte est juste), « les loyers explosent », « on ne construit plus », « les aides au logement font monter les loyers », « 2,8 millions de familles attendent un HLM », « le logement social, c'est pour les plus pauvres » (toutes mixtes) ; les loyers des observatoires locaux, la loi SRU, les passoires du parc social et les 5,4 millions de logements F-G, les bénéficiaires des aides personnelles (déjà dans « Pouvoir d'achat »), le chiffre de la DSED et ceux de l'USH.

## Double vérification commune

Faite le 10/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-logement.md` : chaque source retéléchargée (API SDMX de la BDM de l'Insee, API d'Eurostat, CSV de DiDo et de LOVAC, PDF passés à `pdftotext`, classeurs lus avec openpyxl, une page de PDF rendue en image). Le détail est dans les fiches des volets. Ce qui est commun :

- Producteurs : officiels (Insee, SDES, ministères, DILA, DG Trésor, Cour des comptes, CGEDD, Assemblée nationale, Eurostat). Écartés : l'USH (fédération professionnelle), une note de l'IPP, l'hébergement associatif du rapport d'évaluation de l'encadrement.
- Écarts du rapport de recherche, corrigés : taux d'effort brut du quart modeste « en hausse » (il baisse) ; fin de l'encadrement « le 24 novembre » pour tous (23 novembre à Lyon et Villeurbanne) ; effet de l'encadrement sans la baisse de l'offre ; étude de 2005 attribuée à « l'Insee » ; « la nationalité n'est pas un critère », phrase qu'aucune source ouverte ne contient (non reprise).
- Séries relues valeur par valeur : 8 séries BDM du parc × 45 valeurs, 2 × 66 trimestres de prix, 2 × 24 années de construction (sommes refaites), 4 × 16 années d'aides, les séries d'Eurostat 2015-2025.
- Sources à rouvrir par le PO avant publication : l'article R. 441-1 du CCH sur Légifrance (séjour régulier) ; le Trésor-Éco n° 405 et le rapport d'évaluation de l'encadrement sur un site officiel ; le sort de la prolongation de l'encadrement (Sénat, PPL « Rapports locatifs ») avant le 23 novembre 2026 ; la date de parution de « Immigrés et descendants d'immigrés en France », édition 2023 ; les métadonnées d'Eurostat du taux de surcharge (`ilc_lvho07a`) ; la date des résultats de l'enquête Sans Domicile 2025 ; la date de situation du millésime LOVAC 2026.

**Conclusion.** Les six volets sont vérifiés, sans écart numérique non expliqué ; la page ne doit jamais présenter les vacants comme un gisement, comparer les propriétaires de l'Insee et d'Eurostat, ni rapporter les demandes de logement social aux attributions.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script (voir les fiches des volets).
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais (voir les fiches des volets).
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
