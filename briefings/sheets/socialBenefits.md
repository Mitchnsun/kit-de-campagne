# `socialBenefits` · Aides sociales (partie de la page « Pouvoir d'achat »)

**Vérifiée le 02/11/2026** : foyers du RSA identiques à la moyenne de la Cnaf pour le 1er trimestre 2026 ; prime d'activité compatible (mois définitif contre moyenne provisoire). **Écart expliqué** (03/11/2026) : 3 720 310 personnes couvertes par le RSA en mars 2026 dans le jeu de données, contre 3,61 millions estimés par la Cnaf pour le 1er trimestre (environ +3 %). Le jeu compte tout le foyer Caf, chaque mois ; la Cnaf, dans ses publications sur le RSA, les personnes à charge au sens du RSA, en moyenne trimestrielle (voir « Mises à jour »). Double vérification commune aux trois parties : voir `costOfLiving.md`.

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

- **03/11/2026, écart des personnes couvertes expliqué** (sources lues par le PO). Cafdata (`s_ben_nat`, modèle de données) : chaque colonne `indnbp_*` compte le « nombre de personnes appartenant à un foyer bénéficiaire », soit tout le foyer Caf. RSA Conjoncture 2026T1 : les personnes couvertes y sont comptées « au sens du RSA » (allocataire, conjoint, enfants jusqu'à 25 ans et autres personnes à charge au sens de cette allocation), en moyenne trimestrielle ; au 3e trimestre 2025, 1,80 million d'allocataires, 194 000 conjoints et 1,56 million d'enfants ou personnes à charge, soit environ 3,56 millions. Les deux définitions diffèrent ; la raison exacte des personnes en plus n'est pas écrite par la Cnaf et n'est pas avancée. Aides au logement : la DREES (suivi mensuel de mai 2026) ne donne que des bénéficiaires, c'est-à-dire des foyers (5 539 600 en juin 2026, provisoire) ; seul Cafdata compte les personnes couvertes. Note 3 complétée.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
