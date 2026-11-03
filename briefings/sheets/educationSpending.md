# `educationSpending` · Dépense intérieure d'éducation (partie de la page « Éducation »)

**Vérifiée le 02/11/2026** : 199,2 Md€, +2,4 Md€ courants, +0,3 Md€ constants, 6,7 % du PIB, conformes à la NI 26.42 ; la note sur le financement précisée (« financement initial »). Double vérification commune aux trois parties de la page « Éducation » : voir `schools.md`.

| Champ | Valeur |
| --- | --- |
| Indicateur | `educationSpending`, partie de la page composite `schools`, dossier « Éducation », ticket #32 (statut `planned`) |
| Données | `briefings/data/educationSpending.json`, écrit par `yarn briefings educationSpending` le 2026-11-02 |
| Source | DEPP, « En 2025, 199,2 milliards d'euros consacrés à l'éducation, soit 6,7 % du PIB », Note d'Information n° 26.42, septembre 2026 (publiée le 29/09/2026 selon Localtis, fichier daté du 23/09/2026 par son serveur), figure 1 ; Licence Ouverte |
| Séries | `spending` : DIE en milliards d'euros constants de 2025 (`base: 2025`), 1980 à 2025 ; `shareOfGdp` : part du PIB ; 2025 provisoire (« 2025p ») |
| Chiffre clé | 199,2 Md€ en 2025, en hausse (198,9 en euros de 2025 en 2024) |
| Règles | Le script refuse des euros constants d'une autre année que la dernière, et un champ autre que « France ». La RERS 2026 donnait 197,1 Md€ et 6,8 % pour 2024 (comptes provisoires, euros courants) : la NI 26.42 révise |
| Première édition | À remplir à la publication |

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
