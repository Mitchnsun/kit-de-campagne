# `rentIndices` · Loyers (partie de la page « Pouvoir d'achat »)

**Vérifiée le 02/11/2026** : IRL et ILH conformes aux publications de l'Insee. Notes précisées après la vérification : période et territoires du plafond de 3,5 %, champ des ILH, trimestre affiché. Double vérification commune aux trois parties : voir `costOfLiving.md`.

| Champ | Valeur |
| --- | --- |
| Indicateur | `rentIndices`, partie de la page composite `costOfLiving`, dossier « Pouvoir d'achat », ticket #28 (statut `planned`) |
| Données | `briefings/data/rentIndices.json`, écrit par `yarn briefings rentIndices` le 2026-11-02 |
| Sources | Insee, Indice de référence des loyers (IRL), Informations rapides du 15/10/2026 (T3 2026) ; Insee, Indices des loyers d'habitation (ILH), Informations rapides du 15/09/2026 (juillet 2026) ; séries de la BDM, valeurs définitives ; Licence Ouverte (Insee) |
| Séries | `irlAnnualChange` : variation annuelle de l'IRL, trimestrielle, depuis 2002-T4 (BDM 001515334) ; `rentIndex`, `privateRentIndex`, `socialRentIndex` : ILH tous secteurs, secteur libre, secteur social, France métropolitaine, base 100 en janvier 2019, depuis 1986-T4 (BDM 010600365, 010600351, 010600358) |
| Chiffre clé | IRL du 3e trimestre 2026 : +1,57 % sur un an, en hausse (148,06) |
| Première édition | À remplir à la publication |

À actualiser : l'IRL chaque trimestre (mi-janvier, avril, juillet, octobre), les ILH chaque trimestre (l'indice de juillet paraît en septembre). Le trimestre des ILH suit l'Insee : 2026-T2 est l'indice de juillet 2026.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
