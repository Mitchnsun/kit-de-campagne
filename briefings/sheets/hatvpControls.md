# `hatvpControls` · Les contrôles de la HATVP (saisie à la main)

**Vérifiée le 25/11/2026** : chaque valeur lue dans les chiffres clés des rapports d'activité ; double vérification ci-dessous.

| Champ | Valeur |
| --- | --- |
| Indicateur | `hatvpControls`, dossier « Institutions » (`institutions`), page de type série, demande du PO du 25/11/2026 |
| Données | `briefings/manual/hatvpControls.json`, saisi à la main le 2026-11-25 |
| Sources | 1. HATVP, Synthèse du rapport d'activité 2025, https://www.hatvp.fr/wordpress/wp-content/uploads/2026/05/HATVP_4-PAGES_dp.pdf (PDF du 19/05/2026) : 10 362 reçues, 5 795 contrôlées, 57 transmissions au parquet, 38,6 %, 641 avis, 3 % d'incompatibilité. 2. HATVP, rapports d'activité 2017 à 2024, bloc « Les chiffres clés de l'année » de chaque page https://www.hatvp.fr/rapports_activite/rapport_<année>/ ; la date retenue est celle du PDF du rapport 2024 (29/04/2025). Les pages de 2015 et 2016 répondent par une erreur (500). Chiffres cités avec leur source |
| Séries | `received` : déclarations de patrimoine et d'intérêts reçues, 2017-2025, 9 points ; `controlled` : déclarations contrôlées, 2019-2025, 7 points |
| Chiffre clé | 5 795 déclarations contrôlées en 2025, en hausse (5 122 en 2024) |
| Règles | `controlled` de 2019 à 2021 additionne les deux lignes des chiffres clés, « déclarations de patrimoine contrôlées » et « déclarations d'intérêts contrôlées » (2 038 + 2 019 ; 1 279 + 1 178 ; 664 + 2 486) ; 2017 et 2018 ne donnent que des contrôles approfondis ou terminés des déclarations de patrimoine, d'un autre périmètre, non repris. Les transmissions au parquet ne forment pas une série : leur définition change selon les années (toutes causes, ou non-dépôt seul, un pourcentage en 2022) |
| Première édition | La prochaine Release qui suit le merge de la PR de l'app |

## « À savoir »

1. Le calendrier politique et 2024 : rapport 2024, chiffres clés (13 103 reçues) et texte de la page (« plus de 13 000 déclarations » déposées, la dissolution et les législatives à elles seules « près de 1 300 », « La formation de trois gouvernements »). La note dit l'année, sans attribuer les 13 000 à ces seuls événements.
2. 57 dossiers transmis, « un chiffre sans précédent depuis la création de l'institution », 38,6 % : synthèse 2025 ; création par la loi du 11 octobre 2013 : synthèse 2025, « La Haute Autorité en bref ».
3. 641 avis sur des mobilités entre secteurs public et privé, plus de 60 % vers le privé, 3 % d'incompatibilité : synthèse 2025.

## Double vérification

Faite le 25/11/2026 par un agent Claude (modèle Sonnet) qui a rouvert la synthèse 2025 et les pages des rapports 2017 à 2024.

| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 5 795 (2025) | 5 795, « un niveau historique, en hausse de 13 % » | synthèse 2025 | Conforme |
| `received` 2017-2025 | 9 valeurs | identiques | chiffres clés de chaque rapport, synthèse 2025 | Conforme |
| `controlled` 2019-2021 | 4 057, 2 457, 3 150 | 2 038 + 2 019, 1 279 + 1 178, 664 + 2 486 | chiffres clés 2019 à 2021 | Conforme |
| `controlled` 2022-2025 | 4 170, 3 536, 5 122, 5 795 | identiques | chiffres clés, synthèse 2025 | Conforme |
| 2017 et 2018 | absents | contrôles « approfondis » ou « terminés » des seules déclarations de patrimoine, d'un autre périmètre | chiffres clés 2017 et 2018 | Omission justifiée |

Corrections reprises : la note sur 2024 ne fait plus des 13 000 déclarations l'effet des seuls événements de l'année ; « passage vers le privé » remplacé par les mobilités entre secteurs public et privé.

**Conclusion.** Toutes les valeurs conformes ; la date des rapports 2017 à 2024 est celle du PDF du rapport 2024, non vérifiée par le second agent.

## Mises à jour

Aucune.

## Relecture

- [x] Le chiffre clé et chaque point de la série recoupés par un second agent.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
