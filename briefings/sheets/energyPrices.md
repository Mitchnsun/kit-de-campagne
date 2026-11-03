# `energyPrices` · Prix de l'énergie (partie de la page « Pouvoir d'achat »)

**Vérifiée le 02/11/2026** : glissement annuel et indices conformes au fichier de données de l'IPC de l'Insee. Les prix moyens concordent avec l'Insee tel que d'autres sites le republient, mais n'ont pas pu être contrôlés à la source sans la BDM. Notes corrigées : prix attribués à l'Insee et non au ministère, la cause des mois manquants de 2020 n'est pas avancée. Double vérification commune aux trois parties : voir `costOfLiving.md`.

| Champ | Valeur |
| --- | --- |
| Indicateur | `energyPrices`, partie de la page composite `costOfLiving`, dossier « Pouvoir d'achat » (aussi dans « Écologie et énergie » par sa page), ticket #28 (statut `planned`) |
| Données | `briefings/data/energyPrices.json`, écrit par `yarn briefings energyPrices` le 2026-11-02 |
| Sources | Insee, Indice des prix à la consommation, résultats définitifs de septembre 2026 publiés le 30/10/2026 (l'estimation provisoire d'octobre n'est pas reprise) ; Insee, Prix moyens mensuels de vente au détail en métropole, mis à jour le 15/10/2026 ; séries de la BDM ; Licence Ouverte (Insee) |
| Séries | `energyAnnualChange` : glissement annuel de l'IPC de l'énergie (BDM 011813866) ; `electricityIndex`, `gasIndex`, `fuelIndex` : indices base 2025 de l'électricité (04.5.1), du gaz (04.5.2), des carburants et lubrifiants pour véhicules personnels (07.2.2), mensuels depuis janvier 2000 (BDM 011815807, 011815822, 011816628) ; `dieselPrice`, `unleadedPrice` : prix moyens du gazole et du SP95-E10, le litre ; `heatingOilPrice` : fioul domestique, 1 000 litres livrés à domicile ; mensuels depuis janvier 2021 (BDM 000442588, 010596132, 000442573) |
| Chiffre clé | Prix de l'énergie en septembre 2026 : +21,3 % sur un an, en hausse |
| Première édition | À remplir à la publication |

À actualiser : chaque mois, avec les résultats définitifs de l'IPC (octobre 2026 le 13/11/2026). Les prix moyens de l'Insee manquent certains mois de 2020 (décembre pour le gazole et le SP95-E10, cinq mois pour le fioul) : le kit les prend à partir de janvier 2021.

Écart connu : les prix hebdomadaires du ministère de la Transition écologique diffèrent de ceux de l'Insee (gazole 2,3255 contre 2,34 en septembre 2026), et le fioul du ministère vaut pour des livraisons de 2 000 à 4 999 litres. Le kit ne cite que l'Insee.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
