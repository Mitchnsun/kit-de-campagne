# `competitiveness` · Compétitivité (page composite)

La page « Compétitivité » n'a pas de fichier : ses quatre volets ont le leur (`foreignTrade`, `labourCost`, `productionCapacity` et `businessClimate`, saisis à la main le 2026-11-09, voir `foreignTrade.md`, `labourCost.md`, `productionCapacity.md` et `businessClimate.md`). Cette fiche porte ce qui leur est commun.

**Vérifiée le 09/11/2026** : aucun chiffre faux dans les fichiers (voir les fiches des volets). La licence des sources n'a pas été vérifiée.

## Ce que la page dit, et ne dit pas

- Quatre volets, chacun avec ses sources (8 au plus par fichier) : « Commerce » (Douanes, Eurostat), « Coût du travail » (Eurostat, Insee, Conseil national de productivité), « Production » (Eurostat, Conseil national de productivité, Direction générale des Entreprises, Office européen des brevets), « Attractivité » (OCDE, Business France, Eurostat).
- Les rangs (7e des 27 pour le coût horaire de 2024, 8e pour la productivité de 2025, 23e-24e pour la part de l'industrie, 2e pour les autres impôts sur la production, 6e au monde pour les brevets…) sont calculés en triant les valeurs publiées : aucun producteur ne les publie tels quels. Les classements des 27 (variante `ranking`) numérotent les pays ; la note de chaque bloc dit « rangs calculés ». Aucune moyenne de l'UE n'est mise parmi les 27, qui fausserait la numérotation.
- Les évolutions en pourcentage (+25 % de valeur ajoutée manufacturière en volume depuis 2000, −0,8 % de productivité horaire en volume depuis 2019…) sont calculées sur deux valeurs publiées de la même série : dites « calculé » dans les notes et les affirmations, jamais saisies en série.
- Champs différents, jamais rapprochés sans le dire : le solde commercial des Douanes (biens) n'est pas le solde des transactions courantes (biens, services, revenus) ; le coût horaire de l'Insee dans l'industrie (47,7 €) n'est pas celui d'Eurostat pour l'ensemble de l'économie (44,3 €) ; le taux d'IS de 36,13 % est un taux maximal, le taux normal est de 25 %.
- Chiffres écartés par la contre-vérification, absents de la page : la moyenne de l'UE du taux légal d'IS (22,17 %, calculée, publiée par personne) ; les soldes courants de l'UE et de la zone euro (mesurés hors UE, non comparables à celui de la France) ; un rang de 2025 du coût horaire sur 27 pays (Belgique non publiée) ; les croissances de productivité de l'OCDE pour l'Allemagne et les États-Unis ; le solde de −69,2 Md€ comme valeur courante (première publication, dite dans une note).
- Chiffres du rapport non repris : coin socio-fiscal de l'OCDE, PIB par heure de l'OCDE, taux effectif moyen d'IS de la Commission (calcul KPMG), poids des entreprises sous contrôle étranger (Insee Focus 368). Ils ne manquent à aucune affirmation.
- Le registre porte la page sans source propre (`sources` vide) ; les sources sont celles des volets.

Liens avec le jeu (registre de l'app) : thème « Économie » ; mesures `productionTax`, `businessPact`, `reinvestedProfitTax`, `banLayoffs`, `end35Hours`, `leaveElectricityMarket`. Pas de carte (`factoryClosure` est déjà nommée par `unemployment`). Les chiffres du kit ne contiennent aucune donnée interne du jeu.

## Double vérification commune

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-competitivite.md` : chaque valeur relue dans la source brute (API JSON d'Eurostat, CSV SDMX de l'OCDE, PDF passés à `pdftotext`, fichiers XLS et XLSX convertis, pages HTML), les rangs refaits sur les 27 pays de l'UE. Le détail est dans les fiches des volets. Ce qui est commun :

- Producteurs : tous publics (Douanes, Eurostat, Insee, Conseil national de productivité, Direction générale des Entreprises, OCDE, Business France, Office européen des brevets). Aucun baromètre privé (EY, Kearney, IMD, Forum économique mondial), aucun chiffre de think tank ni de presse.
- Bilan : aucun écart sur les chiffres retenus. Réserves de lecture reprises dans les notes et les réponses : données révisables (Douanes), estimations (coût horaire de 2025), valeurs provisoires (Eurostat), données provisoires (baromètre de l'État), méthode modifiée (Business France), taux maximal (IS).
- Sources fermées aux scripts le 09/11/2026 : Banque de France (balance des paiements, investissements directs) et DG TAXUD de la Commission (taux légaux d'IS). Les chiffres de la Banque de France viennent d'Eurostat et de l'OCDE, qui les reçoivent d'elle ; aucun chiffre de la DG TAXUD n'est dans les fichiers.
- Séries complètes : le rapport de contre-vérification relit les valeurs citées ; les autres points des séries (solde commercial de 1971 à 2018, soldes courants de 2000 à 2024, coûts horaires des 27 en 2024, coûts salariaux unitaires de 2010 à 2025, productivité de la France de 2015 à 2024 et des 27 en 2025, investissements directs de 2019 à 2024) ont été relus par l'agent de la page, par script, dans les fichiers bruts téléchargés par la recherche et la contre-vérification, le 09/11/2026.

**Conclusion.** Les quatre volets sont vérifiés, sans écart numérique ; chaque rang et chaque évolution calculés sont dits tels, et deux chiffres de champs différents ne sont jamais rapprochés sans le dire.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script (voir les fiches des volets).
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais (voir les fiches des volets).
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée (seule la mention des Douanes a été lue : « source : douanes françaises, résultats de [mois année] »).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
