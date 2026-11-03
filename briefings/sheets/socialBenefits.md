# `socialBenefits` · Aides sociales (partie de la page « Pouvoir d'achat »)

**Vérifiée le 02/11/2026** : foyers du RSA identiques à la moyenne de la Cnaf pour le 1er trimestre 2026 ; prime d'activité compatible (mois définitif contre moyenne provisoire). **Écart ouvert** : 3 720 310 personnes couvertes par le RSA en mars 2026 dans le jeu de données, contre une estimation de 3,61 millions par la Cnaf pour le 1er trimestre (environ +3 %), sans explication trouvée. Les notes ne promettent donc aucun rapprochement avec les publications de la Cnaf. Double vérification commune aux trois parties : voir `costOfLiving.md`.

| Champ | Valeur |
| --- | --- |
| Indicateur | `socialBenefits`, partie de la page composite `costOfLiving`, dossier « Pouvoir d'achat », ticket #28 (statut `planned`) |
| Données | `briefings/data/socialBenefits.json`, écrit par `yarn briefings socialBenefits` le 2026-11-02 |
| Sources | CNAF, Cafdata, « Toutes prestations - Répartition des allocataires selon la prestation [National] » (`s_ben_nat`), mis à jour le 09/10/2026 ; Licence Ouverte v2.0 ; en français seulement |
| Séries | `rsaHouseholds`, `rsaPeople` : foyers allocataires et personnes couvertes du RSA ; `activityBonusHouseholds`, `activityBonusPeople` : prime d'activité ; `housingAidHouseholds`, `housingAidPeople` : aides au logement (APL, ALF, ALS) ; mensuelles depuis juin 2016, régime des Caf seulement |
| Chiffre clé | 1 847 267 foyers au RSA en mars 2026, en hausse |
| Première édition | À remplir à la publication |

À actualiser : chaque mois, quand la Cnaf publie un mois consolidé (environ six mois après sa fin).

Non trouvé : le nombre de personnes couvertes par les aides au logement ailleurs que dans le jeu de données.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
