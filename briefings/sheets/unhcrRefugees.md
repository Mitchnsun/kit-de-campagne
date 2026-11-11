# `unhcrRefugees` · Réfugiés sous mandat du HCR

**Vérifiée le 11/11/2026** : double vérification sur le web avec réserves (section « Double vérification »). **Réserve sur la licence** : la page des conditions d'utilisation des jeux de données du HCR n'a pas pu être ouverte (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `unhcrRefugees`, dossier « Défense et Europe » (`defence`), volet de la page `ukrainianRefugees` (page de type volets), deuxième onglet, ticket #349 de l'app |
| Données | `briefings/data/unhcrRefugees.json`, écrit par `yarn briefings unhcrRefugees` le 2026-11-11 |
| Sources | HCR (UNHCR), « Refugee Data Finder, Refugee Population Statistics Database », page https://www.unhcr.org/refugee-statistics/, API https://api.unhcr.org/population/v1/population/?limit=100&coo=UKR&coa=FRA (la requête de référence ajoute `&yearFrom=2021`, que l'API ignore), licence Creative Commons Attribution 4.0 (CC BY 4.0) |
| Séries | `refugees` : réfugiés sous mandat du HCR, pays d'origine l'Ukraine (`coo=UKR`), pays d'asile la France (`coa=FRA`), fin d'année, de 2021 à 2025, 5 points (2 801 ; 69 302 ; 68 181 ; 68 929 ; 75 695) |
| Chiffre clé | 2025 : 75 695, en hausse sur 2024 (68 929) |
| Règles | Le script garde les années à partir de 2021 (l'API répond depuis 1995) et échoue si la réponse a plusieurs pages, un autre pays, une année manquante ou sans chiffre. La date de publication de la source est celle du rapport « Global Trends » du HCR qui a publié les chiffres de fin d'année, que l'API ne donne pas : le 11/06/2026 pour la fin 2025 ([rapport](https://www.unhcr.org/sites/default/files/2026-06/global-trends-report-2025.pdf), Africanews du 12/06/2026). Le script échoue sur une année dont la date de sortie n'est pas inscrite (`RELEASES`) |
| Première édition | À remplir à la publication |

## « À savoir »

1. Réfugiés d'Ukraine sous mandat du HCR vivant en France à la fin de chaque année ; ne s'additionne pas avec le décompte d'Eurostat. Source : l'API (champs `refugees`, `coo`, `coa`) ; le glossaire de la base de données du HCR n'a pas été ouvert.
2. 2 801 fin 2021, 69 302 fin 2022, puis entre 68 181 et 75 695 jusqu'à fin 2025. Source : l'API.

Les deux points en anglais disent la même chose que le français.

## Licence : ce qui a été lu

- Portail opérationnel du HCR, https://data.unhcr.org/en/disclaimer/ (ouvert le 11/11/2026), « Data terms and conditions of usage » : « Except where otherwise indicated, the datasets made available by UNHCR on the Operational Data Portal are licensed under the Creative Commons Attribution 4.0 International Public License. » Ce texte vise le portail opérationnel, non le Refugee Data Finder.
- Conditions d'utilisation des jeux de données du HCR (https://www.unhcr.org/terms-use-datasets, https://www.unhcr.org/what-we-do/reports-and-publications/data-and-statistics/terms-use-datasets, https://www.unhcr.org/refugee-statistics/copyright) : **non ouvertes**, ces pages répondent 403 (contrôle anti-robot) aux scripts. Un résumé de recherche web (non une lecture de la page) donne : licence Creative Commons Attribution 4.0 International pour les jeux de données de la base de statistiques de population, mention « UNHCR Refugee Population Statistics Database » et, en cas de partage, l'adresse de ces conditions ; données de tiers éventuellement soumises à d'autres conditions ; interdiction de laisser croire que le HCR cautionne l'usage. **À lire par le PO** avant publication.

## Double vérification

Faite le 11/11/2026 par un agent Claude (modèle Opus) qui cherche sur le web.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, 2025 | 75 695 | 75 695 (réponse de l'API, valeur du PO) | API ci-dessus | Conforme (même source) |
| 2022, 2023, 2024 | 69 302 ; 68 181 ; 68 929 | les mêmes (valeurs du PO) | API ci-dessus | Conforme (même source) |
| Situation Ukraine du HCR | — | Le portail opérationnel prend les bénéficiaires de la protection temporaire dans l'Union auprès d'Eurostat ; ses chiffres sont des estimations opérationnelles qui peuvent différer des statistiques officielles | https://data.unhcr.org/en/working-group/437 (résumé de recherche) | Non comparable : autre décompte, pas de chiffre de la France retrouvé |

**Conclusion.** Les chiffres sont ceux de l'API du HCR ; aucune autre publication n'a pu être ouverte pour les recouper, et la licence du Refugee Data Finder n'est pas lue à la source.

**Pages consultées** le 11/11/2026 : l'API, https://data.unhcr.org/en/disclaimer/, des résumés de recherche web.

## Mises à jour

Aucune.

## Relecture

- [ ] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Non : seule l'API du HCR a été lue.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. **Non vérifiée à la source** pour le Refugee Data Finder (403) ; la mention proposée est « UNHCR Refugee Population Statistics Database ».
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
