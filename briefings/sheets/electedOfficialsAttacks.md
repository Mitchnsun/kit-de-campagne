# `electedOfficialsAttacks` · Les atteintes aux élus (saisie à la main)

**Vérifiée le 25/11/2026** : chaque valeur lue dans le rapport d'activité 2025 du Calaé ouvert en entier ; double vérification ci-dessous.

| Champ | Valeur |
| --- | --- |
| Indicateur | `electedOfficialsAttacks`, dossier « Institutions » (`institutions`), aussi dans « Sécurité et justice » (`security`), page de type série, demande du PO du 25/11/2026 |
| Données | `briefings/manual/electedOfficialsAttacks.json`, saisi à la main le 2026-11-25 |
| Sources | Ministère de l'Intérieur, Centre d'analyse et de lutte contre les atteintes aux élus (Calaé), rapport d'activité 2025, publié sur vie-publique.fr, https://www.vie-publique.fr/rapport/304298 (PDF https://www.vie-publique.fr/files/rapport/pdf/304298.pdf), p. 6 « Les chiffres clés, données au 31 décembre 2025 », p. 7-9. Date : le rapport, présenté au ministre le mardi 30/06/2026 selon une dépêche AFP reprise par Maire-info le 01/07/2026 ; le PDF ne porte aucune date imprimée. Chiffres cités avec leur source. Le site du ministère de l'Intérieur refuse les requêtes automatiques (403) : le rapport a été lu sur vie-publique.fr |
| Séries | `procedures` : nombre de procédures pour des atteintes aux élus, 2022-2025, 4 points ; `closed` : nombre de procédures clôturées, 2022-2025 |
| Chiffre clé | 2 478 procédures en 2025, stable (2 501 en 2024, −0,9 %) |
| Règles | Les procédures judiciaires que compte le Calaé, créé en 2023 ; les séries antérieures du SSMSI ou de la gendarmerie ne sont pas reprises (autre méthode) |
| Première édition | La prochaine Release qui suit le merge de la PR de l'app |

## « À savoir »

1. 68 % de menaces et outrages, 27 % par voie cyber (24 % en 2024) : rapport 2025, p. 6.
2. Les victimes, au niveau national (la section suit un développement sur l'agglomération parisienne, dont le tableau donne une autre répartition) : maires 65 %, adjoints et conseillers municipaux 19 %, parlementaires 13 % : rapport 2025, p. 9.
3. Les procédures, pas les faits non signalés : le tableau compte des « procédures » (p. 6) ; la « zone grise de faits […] qui ne seraient pas portés à la connaissance » des autorités, rapport 2023-2025, p. 10 ; création du Calaé en 2023 : éditorial, p. 5 (« bientôt trois années d'existence ») et la dépêche AFP (« Créé en mai 2023 »).
4. 2023, le pic (2 759, 53 par semaine) et le plan national de juillet 2023 : p. 6 et éditorial, p. 5.

## Double vérification

Faite le 25/11/2026 par un agent Claude (modèle Sonnet) qui a rouvert le rapport d'activité 2025 sur vie-publique.fr et la dépêche AFP de Maire-info.

| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 2 478 (2025) | 2 478 | rapport 2025, p. 5 et 6 | Conforme |
| `procedures` 2022-2025 | 2 430, 2 759, 2 501, 2 478 | identiques | p. 6 | Conforme |
| `closed` 2022-2025 | 1 080, 1 149, 1 293, 1 190 | identiques | p. 6 | Conforme |
| Date | 30/06/2026 | « présenté mardi » dans la dépêche du 01/07/2026, un mardi ; aucune date dans le PDF | Maire-info | Écart expliqué : date déduite de la dépêche |

Corrections reprises : « judiciaires » retiré (le tableau dit « procédures ») ; les parts de victimes dites nationales.

**Conclusion.** Toutes les valeurs conformes ; la date de publication est celle de la présentation au ministre, déduite d'une dépêche.

## Mises à jour

Aucune.

## Relecture

- [x] Le chiffre clé et chaque point de la série recoupés par un second agent.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
