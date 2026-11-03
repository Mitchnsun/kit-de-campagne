# `pisaScores` · PISA (partie de la page « Éducation »)

**Vérifiée le 02/11/2026** : toutes les valeurs conformes à l'annexe Excel de l'OCDE (`https://stat.link/mrq53f`) ; notes corrigées (résultats du prochain cycle en 2030, sciences non significatif). Double vérification commune aux trois parties de la page « Éducation » : voir `schools.md`.

| Champ | Valeur |
| --- | --- |
| Indicateur | `pisaScores`, partie de la page composite `schools`, dossier « Éducation », ticket #32 (statut `planned`) |
| Données | `briefings/data/pisaScores.json`, écrit par `yarn briefings pisaScores` le 2026-11-02 |
| Sources | DEPP, Notes d'Information n° 26.40 (compréhension de l'écrit, culture mathématique) et n° 26.39 (culture scientifique), septembre 2026, PDF et XLSX ; publiées le 08/09/2026 avec les résultats de l'OCDE, fichiers datés du 04/09/2026 par leur serveur (les pages du ministère refusent les scripts) ; Licence Ouverte |
| Séries | `readingFrance`, `readingOecd`, `mathematicsFrance`, `mathematicsOecd`, `scienceFrance`, `scienceOecd` : scores moyens depuis le premier cycle de chaque domaine, France et moyenne des 24 pays de l'OCDE présents à tous les cycles |
| Valeurs par catégorie | 2025 : `franceScores` 456,33 / 457,66 / 483,42, `franceStandardErrors` 3,24 / 3,00 / 3,21, `oecdScores` (38 pays) 460,94 / 463,02 / 481,91, `oecdStandardErrors` 0,45 / 0,42 / 0,44 (écrit, maths, sciences) |
| Chiffre clé | 458 points en culture mathématique en 2025, en baisse (474 en 2022) |
| Première édition | À remplir à la publication |

À actualiser : le cycle PISA 2029, résultats en 2030.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
