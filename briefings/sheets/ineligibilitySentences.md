# `ineligibilitySentences` · Les peines d'inéligibilité (saisie à la main)

**Vérifiée le 25/11/2026** : chaque valeur lue dans le rapport du Sénat ouvert en entier ; double vérification ci-dessous.

| Champ | Valeur |
| --- | --- |
| Indicateur | `ineligibilitySentences`, dossier « Institutions » (`institutions`), aussi dans « Sécurité et justice » (`security`), page de type série, demande du PO du 25/11/2026 |
| Données | `briefings/manual/ineligibilitySentences.json`, saisi à la main le 2026-11-25 |
| Sources | Sénat, rapport n° 89 (2025-2026) de M. Olivier Bitz au nom de la commission des lois, sur la proposition de loi visant à créer un fichier national des personnes inéligibles, enregistré le 29/10/2025, https://www.senat.fr/rap/l25-089/l25-0891.pdf (pages imprimées), p. 17 : tableau « Nombre de condamnations pour des infractions faisant encourir la peine complémentaire obligatoire d'inéligibilité et taux de prononcé », « éléments transmis par le ministère de la justice au rapporteur » ; p. 18 : décisions d'inéligibilité du Conseil constitutionnel depuis 2021. Chiffres cités avec leur source |
| Séries | `convictions` : condamnations pour une infraction qui fait encourir l'inéligibilité obligatoire, 2020-2024, 5 points ; `pronounced` : celles où la mesure a été prononcée, 2020-2024 ; `rate` : le taux de prononcé, en %, tel que le tableau l'arrondit. 2023 et 2024 « données provisoires » (`provisional`) |
| Chiffre clé | 15 723 condamnations assorties de l'inéligibilité en 2024 (provisoire), en hausse (11 332 en 2023) |
| Règles | Le périmètre est celui du tableau : les seules infractions qui font encourir la peine obligatoire (art. 131-26-2 du code pénal, loi du 15/09/2017), toutes personnes condamnées, élus ou non. Aucun décompte annuel public des élus condamnés, ni des peines avec exécution provisoire |
| Première édition | La prochaine Release qui suit le merge de la PR de l'app |

## « À savoir »

1. La loi de 2017, « un délit mentionné au II du même article ou d'un crime », et moins de 50 condamnations par an entre 2015 et 2017 : rapport, p. 16 (« si, entre 2015 et 2017, moins de 50 condamnations annuelles étaient assorties d'une mesure d'inéligibilité ») ; la décision spécialement motivée : art. 131-26-2, III, du code pénal.
2. Le taux de 42 % et ses deux hypothèses : rapport, note 1 de la p. 16 (la DACG « n'ayant pas accès aux motivations retenues par les juridictions »).
3. Toutes les condamnations concernées, élus ou non : le tableau, p. 17, ne les distingue pas. Aucune série publique des élus condamnés ni des peines avec exécution provisoire n'a été trouvée (recherche du 25/11/2026), ce que la note ne dit pas, faute de source qui l'écrive.
4. Le juge électoral et les 522 décisions du Conseil constitutionnel : rapport, p. 17-18, tableau « Nombre des décisions d'inéligibilité rendues par le Conseil constitutionnel depuis 2021 » (348 pour l'Assemblée nationale en 2023).

## Double vérification

Faite le 25/11/2026 par un agent Claude (modèle Sonnet) qui a rouvert le rapport du Sénat, et l'article 131-26-2 du code pénal sur un miroir de Légifrance (codes.droit.org, édition du 20/11/2026 ; Légifrance refuse les requêtes automatiques).

| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 15 723 (2024) | 15 723 | rapport, p. 17 | Conforme |
| `convictions`, `pronounced`, `rate` 2020-2024 | 15 valeurs | 15 valeurs identiques ; taux recalculés 7,98 / 13,66 / 22,66 / 32,78 / 41,71, arrondis justes | rapport, p. 17 | Conforme |
| 2023 et 2024 provisoires | `provisional` | « * données provisoires » | rapport, p. 17 | Conforme |
| Caractère obligatoire, exception | — | art. 131-26-2, I et III (« décision spécialement motivée ») | codes.droit.org | Conforme |

Corrections reprises : la liste du II ne se limite pas à la probité (violences, escroqueries, faux, fraude fiscale, délits électoraux…) ; « personnes » remplacé par « condamnations » ; retirées, faute de source qui les écrive, l'absence de série publique des élus et de l'exécution provisoire et la mention des législatives de 2022.

**Conclusion.** Toutes les valeurs conformes ; les notes ne disent que ce que le rapport et le code écrivent.

## Mises à jour

Aucune.

## Relecture

- [x] Le chiffre clé et chaque point de la série recoupés par un second agent.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
