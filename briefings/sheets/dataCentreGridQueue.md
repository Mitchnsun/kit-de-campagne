# `dataCentreGridQueue` · Les raccordements des data centers (saisi à la main)

**Vérifiée le 17/11/2026** : double vérification sur le web, sans écart non expliqué sur les chiffres du fichier (section « Double vérification ») ; un écart entre deux publications de RTE a fait écarter les projections de sa page « chiffres clés ».

| Champ | Valeur |
| --- | --- |
| Indicateur | `dataCentreGridQueue`, dossier « Écologie et énergie » (`ecology`), second volet (« Réseau ») de la page composite `dataCentres` (voir `dataCentres.md`), page de type comparaison |
| Données | `briefings/manual/dataCentreGridQueue.json`, saisi à la main le 2026-11-17 depuis les trois documents ci-dessous |
| Sources | 1. RTE, « Les data centers en chiffres clés », https://www.rte-france.com/bases-electricite/consommation-electricite/essor-data-centers-france (adresse donnée par le SDES : https://www.rte-france.com/wiki-energie/data-centers-11-chiffres-sur-leur-essor-france-leurs-besoins-electricite, redirigée), page mise à jour le 01/06/2026 (« Publication : 21/05/2025 »), datée du 01/06/2026 dans le fichier. 2. RTE, « Bilan prévisionnel 2025-2035, principaux résultats », PDF créé le 16/12/2025, https://assets.rte-france.com/prod/public/2025-12/2025-12-16-bilan-previsionnel-principaux-resultats-2025.pdf. 3. RTE, « Bilan prévisionnel 2025-2035 », chapitre « La consommation d'électricité », PDF du 23/12/2025, https://assets.rte-france.com/prod/public/2025-12/2025-12-23-bilan-previsionnel-2025-consommation.pdf. Licence : citées, comme les rapports de RTE de `electricityProduction` (`citation-only`) ; aucun fichier de RTE n'est redistribué. Pages en français seulement (aucune version anglaise déclarée par la page) |
| Séries | `reserved` : 18 GW en mai 2026 (« En mai 2026, RTE avait réservé près de 18 GW de capacité, pour environ 80 projets », source 1, section « Près de 18 GW de demandes de raccordement signées ») ; `reservedEnd2024` : 5 GW, saisi `2024-12` (« Fin 2024, il y avait une quarantaine de projets totalisant environ 5 GW », même section) ; `reservedNov2025` : 14 GW, saisi `2025-11` (« au 1er novembre 2025 […] une puissance cumulée de l'ordre de 30 GW (environ 14 GW pour des centres de données, y compris ceux s'inscrivant dans une procédure fast track […]) », source 2, p. 21, avec la figure 12 (p. 20) « situation au 1er novembre 2025 » et la note 6 : « Au sens de signature de la proposition technique et financière ») ; `outlookSlow` et `outlookRapid` : consommation des centres de données sur sites dédiés, trajectoires « Décarbonation lente » (10 TWh en 2030, 21 en 2035) et « Décarbonation rapide » (15 TWh en 2030, 32 en 2035), statut `projection` (source 3, figure 2.10, p. 28, étiquettes lues sur l'image de la page, et texte : « près de 32 TWh en 2035 dans la trajectoire de décarbonation rapide contre 21 TWh dans la trajectoire de décarbonation lente ») |
| Répartitions | `byRegion`, mai 2026 : total 18, Île-de-France 7, Hauts-de-France 6 GW (« environ 7 GW de capacité réservée », « environ 6 GW de capacité réservée », source 1, section « 2 territoires qui concentrent la majorité des projets ») ; `bySector`, novembre 2025 : centres de données 14, hydrogène 9,5, industrie 6,5, total 30 GW (source 2, p. 21 : « 9,5 GW pour des unités de production d'hydrogène bas-carbone et de ses dérivés, et 6,5 GW pour des projets d'électrification dans l'industrie ou de nouveaux sites industriels ») |
| Chiffre clé | 18 GW en mai 2026, sans tendance (une seule date dans sa série) ; à côté, fin 2024, 5 GW |
| Règles | Les chiffres « environ » et « près de » sont saisis comme RTE les écrit ; aucune somme, aucun reste calculé (la part des autres régions n'est pas donnée). Le reste de la France n'est donc pas une ligne. « Fin 2024 » est saisi en décembre 2024, « au 1er novembre 2025 » en novembre 2025 |
| Première édition | À remplir à la publication |

## Écart entre deux publications de RTE (projections écartées)

La page « chiffres clés » (source 1, section « 4 % de la consommation française en 2035 ? ») écrit : « Selon notre Bilan prévisionnel 2025-2035, dans une trajectoire de décarbonation rapide, la consommation électrique des datacenters pourrait suivre la trajectoire suivante […] : entre 15 et 20 TWh en 2030 […], puis entre 23 et 28 TWh en 2035 ». Le Bilan prévisionnel (source 3, figure 2.10) donne 15 TWh en 2030 et « près de 32 TWh en 2035 » dans cette même trajectoire, et la synthèse (source 2, figure 16, p. 25) environ 5 TWh en 2024 plus 10 TWh d'ici 2030. RTE n'explique pas l'écart (autre périmètre, mise à jour de 2026 ?). Le fichier garde les chiffres du Bilan, dont le périmètre est écrit (« centres de données sur sites dédiés », y compris ceux raccordés au réseau de distribution, § 2.5.2) ; les chiffres de la page ne sont pas publiés. De même, la page « environ 10 TWh » de consommation actuelle, sans année, n'est pas reprise : la note 4 de `dataCentreConsumption` cite les fourchettes du Bilan. À reposer à RTE.

## « À savoir »

1. Réservé n'est pas consommé : « RTE constate que les data centers raccordés à son réseau depuis deux à trois ans ne consomment pour l'instant, en moyenne, que 20 % de la puissance qu'ils ont demandée » ; « les principaux opérateurs estiment qu'il faudra dix à quinze ans pour atteindre environ 80 % de cette consommation ». Source 1, section « Un développement très progressif de la consommation sur 10 à 15 ans ».
2. Projets : « environ 80 projets » en mai 2026, « une quarantaine de projets totalisant environ 5 GW » fin 2024 ; « La majorité d'entre eux sollicitent une puissance de 100 à 200 MW » ; « Une dizaine de projets "hors normes" visent des puissances supérieures à 400 MW ». Source 1.
3. Projections : figure 2.10 de la source 3 ; « un taux de concrétisation d'environ 60 % (4,3 GW) pour les projets ayant demandé un raccordement au réseau de transport d'électricité et dont la mise en service est prévue avant 2030 (avec une hypothèse de taux moyen d'utilisation de la puissance de raccordement de 20 % à cet horizon) », source 3, § 2.5.3, p. 27-28.
4. File d'attente : source 2, p. 21 (les 30, 14, 9,5 et 6,5 GW) ; « Le système de demande d'accès au réseau et de raccordement, qui nécessite aujourd'hui peu d'engagements de la part des porteurs de projet, ne permet pas à RTE de disposer d'une information fiable pour distinguer les projets matures des projets "fantômes" ou en situation d'échec », source 2, p. 21.

Les quatre points en anglais disent la même chose que le français.

## Double vérification

Faite le 17/11/2026 par un agent Claude (modèle Opus) : documents retéléchargés et relus (HTML nettoyé, `pdftotext`, images des pages 20, 25 et 28), puis recherche sur le web hors des sources du fichier.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, mai 2026 | 18 GW | « près de 18 GW de capacité en mai 2026 », « quelque 80 projets » (18/06/2026) ; « environ 18 GW » (11/09/2026) | https://www.les-energies-renouvelables.eu/article/actualites/energies/datacenters-ia-electrification-france-rte-856/ ; https://www.jechange.fr/energie/electricite/news/facture-electricite-ia-data-centers-cout-cache | Conforme |
| Fin 2024 | 5 GW | « une quarantaine de projets de datacenters pour environ 5 GW » | les-energies-renouvelables.eu, ci-dessus | Conforme |
| Régions | 7 et 6 GW | « environ 7 gigawatts de capacité réservée », « près de 6 gigawatts » (30/06/2026) | https://www.france-epargne.fr/news/data-centers-en-france-la-penurie-de-reseau-electrique-fait-flamber-une-nouvelle-classe-dactifs | Conforme. La même page de RTE écrit aussi « En Île-de-France, par exemple, la puissance demandée (6,5 GW) » : demandée et non réservée, l'écart de 0,5 GW n'est pas expliqué et le fichier garde le chiffre réservé |
| 14 GW sur 30 GW | 14 ; 30 | « environ 30 GW à fin 2025, dont 14 GW pour des centres de données » (recherche, reprises du Bilan électrique de février 2026) | résumé de recherche, non rouvert | Conforme (presse) |
| Hydrogène, industrie | 9,5 ; 6,5 | Non trouvé ailleurs que dans la source 2 | — | Non trouvé (recherche sur le web, 17/11/2026) |
| Projections | 10 et 15 TWh (2030) ; 21 et 32 TWh (2035) | Synthèse du Bilan (source 2, figure 16) : environ 5 TWh en 2024, +6 TWh (lente) et +10 TWh (rapide) d'ici 2030, soit 11 et 15 ; page « chiffres clés » : 15 à 20 et 23 à 28 TWh | sources 1 et 2 | 2030 rapide conforme ; voir « Écart entre deux publications de RTE » |
| Taux d'utilisation | 20 % | « ne consomment en moyenne que 20 % de la puissance qu'ils ont demandée » | les-energies-renouvelables.eu, ci-dessus ; source 2, figure 14, p. 23 | Conforme |

**Conclusion.** Les puissances réservées et les trajectoires du Bilan prévisionnel sont conformes ; les projections de la page « chiffres clés » de RTE, qui s'écartent du Bilan sans explication, restent hors du fichier.

**Pages consultées** le 17/11/2026 : les URL ci-dessus.

## Mises à jour

Aucune. À actualiser : la page « chiffres clés » de RTE (mise à jour sans calendrier), le Bilan prévisionnel 2026 (décembre). `yarn kit:build` signale ce fichier comme en retard (sa plus ancienne série, fin 2024) : c'est voulu, chaque date est une série d'un point.

## Relecture

- [x] Les chiffres clés recoupés ailleurs que dans les documents saisis.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée (citées, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO (dont l'écart des projections de RTE).
