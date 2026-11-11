# `unhcrRefugees` · Réfugiés sous mandat du HCR

**Vérifiée le 11/11/2026** : double vérification sur le web avec réserves (section « Double vérification »). **Licence** : CC BY 4.0 avec les conditions d'utilisation des jeux de données du HCR, lues par le PO le 11/11/2026 (section « Licence : ce qui a été lu »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `unhcrRefugees`, dossier « Défense et Europe » (`defence`), volet de la page `ukrainianRefugees` (page de type volets), deuxième onglet, ticket #349 de l'app |
| Données | `briefings/data/unhcrRefugees.json`, écrit par `yarn briefings unhcrRefugees` le 2026-11-11 |
| Sources | HCR (UNHCR), « UNHCR Refugee Population Statistics Database » (la mention que demandent ses conditions, mot pour mot), page https://www.unhcr.org/refugee-statistics/, API https://api.unhcr.org/population/v1/population/?limit=100&coo=UKR&coa=FRA (la requête de référence ajoute `&yearFrom=2021`, que l'API ignore), licence Creative Commons Attribution 4.0 (CC BY 4.0) |
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
- Conditions d'utilisation des jeux de données du HCR, https://www.unhcr.org/what-we-do/reports-and-publications/data-and-statistics/terms-use-datasets : la page répond 403 aux scripts (contrôle anti-robot) ; **lue par le PO dans son navigateur le 11/11/2026**. Point 1 : sauf mention contraire, les jeux de données de la base « UNHCR Refugee Population Statistics Database » sont publiés sous Creative Commons Attribution International License 4.0 (liens vers https://creativecommons.org/licenses/by/4.0/ et /legalcode). Ses conditions propres, qui l'emportent sur celles du site en cas de conflit (point 2) :
  - attribution (point 3) : créditer le HCR et ses fournisseurs avec la mention exacte « UNHCR Refugee Population Statistics Database », la publication de la source dans le registre de l'app ;
  - lien vers les conditions (point 4) : qui partage les données ou y donne accès renvoie aussi vers cette page ; la note de source de l'app l'affiche, « Conditions d'utilisation » (`termsUrl`), et le `LICENSE` du kit la cite ;
  - pas de caution (point 5) : ne pas laisser entendre que le HCR participe au jeu, le soutient ou l'approuve ;
  - données de tiers (point 6) : un jeu de données d'un autre fournisseur suit ses propres conditions, écrites dans ses métadonnées. Le fichier `footnotes.csv` du téléchargement de l'API (pays d'origine l'Ukraine, pays d'asile la France, téléchargé le 11/11/2026) est **vide** : aucune condition de tiers pour ces chiffres ;
  - nom et emblème (point 7) : protégés, jamais repris ; le jeu n'affiche aucun logo de producteur.

## Double vérification

Faite le 11/11/2026 par un agent Claude qui cherche sur le web.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, 2025 | 75 695 | 75 695 (réponse de l'API, valeur du PO) | API ci-dessus | Conforme (même source) |
| 2022, 2023, 2024 | 69 302 ; 68 181 ; 68 929 | les mêmes (valeurs du PO) | API ci-dessus | Conforme (même source) |
| Situation Ukraine du HCR | — | Le portail opérationnel prend les bénéficiaires de la protection temporaire dans l'Union auprès d'Eurostat ; ses chiffres sont des estimations opérationnelles qui peuvent différer des statistiques officielles | https://data.unhcr.org/en/working-group/437 (résumé de recherche) | Non comparable : autre décompte, pas de chiffre de la France retrouvé |

**Conclusion.** Les chiffres sont ceux de l'API du HCR ; aucune autre publication n'a pu être ouverte pour les recouper, et la licence du Refugee Data Finder a été lue à la source par le PO (11/11/2026).

**Pages consultées** le 11/11/2026 : l'API, https://data.unhcr.org/en/disclaimer/, des résumés de recherche web.

## Mises à jour

Aucune.

## Relecture

- [ ] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Non : seule l'API du HCR a été lue.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande : CC BY 4.0 et les conditions du HCR, lues par le PO le 11/11/2026 ; la mention « UNHCR Refugee Population Statistics Database » et le lien vers les conditions.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
