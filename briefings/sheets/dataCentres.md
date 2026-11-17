# `dataCentres` · Data centers (page composite)

La page « Data centers » n'a pas de fichier : ses deux volets ont le leur, dans l'ordre de leurs onglets : « Consommation » (`dataCentreConsumption`, écrit par `yarn briefings dataCentreConsumption` le 2026-11-17, voir `dataCentreConsumption.md`) et « Réseau » (`dataCentreGridQueue`, saisi à la main le 2026-11-17, voir `dataCentreGridQueue.md`). Décision du PO du 17/11/2026 : une page composite dans le dossier « Écologie et énergie », aussi dans « Économie et fiscalité ». Cette fiche porte ce qui leur est commun.

**Vérifiée le 17/11/2026** : chiffres relus dans les documents originaux téléchargés (xlsx et page du SDES, page et deux PDF de RTE), double vérification sur le web sans écart de valeur sur les chiffres publiés (voir les fiches des volets). Un écart entre deux publications de RTE (les projections) est non expliqué : les chiffres concernés sont restés hors du kit (voir `dataCentreGridQueue.md`).

## Ce que la page dit, et ne dit pas

- Deux mesures, deux producteurs, jamais sur une même courbe : la consommation mesurée par le SDES (data centers de plus de 1 GWh par an, France métropolitaine, 2018 à 2024) et la puissance réservée sur le réseau de RTE avec les projections de son Bilan prévisionnel 2025 (data centers sur sites dédiés, raccordés au réseau de transport ou de distribution). Le texte lu d'abord (`readFirst`) du premier onglet le dit.
- Une puissance (GW) n'est pas une énergie (TWh) : la puissance réservée n'est pas une consommation, les data centers raccordés n'utilisant en moyenne que 20 % de ce qu'ils ont demandé (RTE).
- Les estimations de la consommation de tous les data centers sont des fourchettes et des périmètres différents : 4,3 à 6 TWh en 2024 (SDES, avec les petits centres), 4 à 5 TWh (RTE, sites dédiés, 2024), 5 à 10 TWh (RTE, avec les salles serveurs des entreprises), « environ 10 TWh » (page « chiffres clés » de RTE, sans année). Seule la série mesurée du SDES est une série ; les fourchettes sont dans les notes.
- Pas de « Ce qu'on entend » : aucune affirmation entendue que ces chiffres réfutent sans nuance n'a été retenue.

## Parties écartées (17/11/2026)

- Fiscalité de l'électricité (tarif réduit d'accise des centres de données, CIBS) : Légifrance refuse les requêtes du script (403) ; le tarif et le coût de la dépense fiscale n'ont été vus que dans des pages secondaires. Non publiés.
- Investissements annoncés (Choose France 2026, sommet de 2025) : des annonces d'entreprises nommées, sans total officiel propre aux data centers (la DGE donne 93 Md€ toutes filières), des montants « pouvant atteindre ». Non publiés.
- Comparaison européenne (CSO pour l'Irlande, 22 % de l'électricité mesurée en 2024 ; CBS pour les Pays-Bas, 4,6 %) : les sources sont lisibles, mais la France n'a pas de chiffre de même nature (le SDES donne une fourchette, 1 à 1,5 %, estimée) et les définitions diffèrent. Non publiée.

Liens avec le jeu (registre de l'app) : thèmes « Écologie et énergie » et « Économie et fiscalité » pour la page ; la carte `campusFarmland` sur la consommation, la carte `factoryWaits` sur le réseau. Les cartes `nightGenerators`, `foreignHost` et `serverPool` ne sont liées à aucun volet : aucun chiffre de la page ne les éclaire (au PO de choisir). Les chiffres du kit ne contiennent aucune donnée interne du jeu.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source (voir les fiches des volets).
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
