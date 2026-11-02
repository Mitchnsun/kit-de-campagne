# `earlySchoolLeavers` · Sortants précoces (partie de la page « Éducation »)

**Vérifiée le 02/11/2026** : chiffres et drapeaux conformes à Eurostat au 30/10/2026 ; révisions relevées par rapport aux extractions de 2025 et d'avril 2026, dites dans une note. Double vérification commune aux trois parties de la page « Éducation » : voir `schools.md`.

| Champ | Valeur |
| --- | --- |
| Indicateur | `earlySchoolLeavers`, partie de la page composite `schools`, dossier « Éducation », ticket #32 (statut `planned`) |
| Données | `briefings/data/earlySchoolLeavers.json`, écrit par `yarn briefings earlySchoolLeavers` le 2026-11-02 |
| Source | Eurostat, « Jeunes ayant quitté prématurément l'éducation et la formation par statut au regard de l'emploi » (`edat_lfse_14`), API de diffusion, mise à jour le 30/10/2026 ; réutilisation avec mention de la source |
| Séries | `france`, `europeanUnion` (UE à 27), 18-24 ans, depuis 2006, avec les ruptures (`breaks`) : France 2013, 2014, 2021, 2024 ; UE 2006, 2014, 2021. Drapeau `d` (« definition differs ») pour la France depuis 2021, sans cause publiée |
| Chiffre clé | 7,2 % en 2025 (UE 9,1 %), en baisse après 7,9 % |
| Première édition | À remplir à la publication |

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
