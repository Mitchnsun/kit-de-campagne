# `smoking` · Le tabagisme (saisie à la main)

**Vérifiée le 24/11/2026** : chaque valeur lue dans un document ou un jeu de données du producteur ouvert en entier, puis relue par un second agent (`research/tobacco-2026-11/verify-sonnet.md` dans le dépôt de l'app) ; les séries d'Odissé interrogées aussi par l'agent principal, par leur API.

| Champ | Valeur |
| --- | --- |
| Indicateur | `smoking`, dossier « Santé » (`health`), page de type série, demande du PO du 24/11/2026 (lot du tabac) |
| Données | `briefings/manual/smoking.json`, saisi à la main le 2026-11-24 |
| Sources | 1. Santé publique France, synthèse « Tabagisme » du Baromètre 2024 (publiée le 24/11/2025, mise à jour le 06/10/2026), p. 7 : 18,2 % en 2024. 2. Odissé, « Tabac : Prévalence selon le sexe » (modifié le 10/01/2025, Licence ouverte 2.0) : 2000 à 2023. 3. OFDT, Tendances n° 155, ESCAPAD 2022 (communiqué du 09/03/2023), figure 1 : les fumeurs quotidiens à 17 ans. 4. Odissé, « Vapotage : Prévalence » (modifié le 09/01/2025, Licence ouverte 2.0) : 2014 à 2023. 5. Santé publique France, synthèse « Vapotage » du Baromètre 2024 (11/12/2025), p. 6 : 6,5 % en 2024. 6. Santé publique France, « Les décès attribuables au tabagisme », Le point sur du 16/02/2026 (notes et réponses). 7. Eurostat, `hlth_ehis_sk1e` (données du 01/04/2022) : la comparaison européenne. Les PDF de Santé publique France et de l'OFDT : chiffres cités (`citation-only`) |
| Séries | `daily` : part des 18-75 ans qui fument chaque jour, France hexagonale, années d'enquête 2000, 2005, 2010, 2014 à 2024 (valeurs d'Odissé à deux décimales, 2024 de la synthèse). `daily17` : à 17 ans, France métropolitaine, années d'ESCAPAD 2000 à 2022. `vapingDaily` : vapotage quotidien des 18-75 ans, 2014 à 2024 |
| Chiffre clé | 18,2 % en 2024, en baisse (23,12 % en 2023) |
| Règles | Seules les années d'enquête ; aucune valeur interpolée. 2015 (Baromètre Cancer), 2022 (échantillon réduit) et 2023 (EROPP, OFDT) sont dans la série de Santé publique France sur le même champ. 2024 vient de la nouvelle méthode, sur le champ comparable (18-75 ans, Hexagone), pas sur le champ élargi (17,4 %, 18-79 ans avec quatre DROM) |
| Première édition | À remplir à la publication |

Valeurs écartées : le « 25 % » de 2014 de la page « Données » du dossier Tabac de Santé publique France (les documents disent 28,5 %) ; le « 31,8 % en 2021 » de la p. 472 du BEH 2022, une coquille (31,9 %) ; les 75 000 décès que la synthèse de 2024 cite encore, remplacés par l'estimation de février 2026.

## « À savoir »

1. Changement de méthode en 2024 : synthèse « Tabagisme » 2024, p. 2 et p. 7 (« leur interprétation doit être faite avec précaution »).
2. Les années d'autres enquêtes : BEH 2022 n° 26, p. 470-473 ; BEH 2023 n° 9-10, p. 153 (3 229 personnes) ; Le point sur EROPP 2023 (19/11/2024), p. 2.
3. Diplôme et situation financière : synthèse « Tabagisme » 2024, p. 4 (13,0 %, 20,9 %, 30,0 %, 18-79 ans).
4. Décès : Le point sur du 16/02/2026, p. 4 (68 021, 10,9 %) et p. 7 (la baisse « aussi due à la mise à jour des paramètres ») ; communiqué du 16/02/2026 (« première cause de mortalité évitable »).

## « Ce qu'on entend »

1. 75 000 décès : Le point sur du 16/02/2026, p. 4, p. 7 et p. 9 (49 361 hommes, 18 660 femmes ; la mortalité des femmes « toujours en hausse » à méthode identique).
2. Les jeunes : Tendances n° 155, p. 1 et figure 1 (41,1 % en 2000, 25,1 % en 2017, 15,6 % en 2022).
3. Les voisins : Eurostat `hlth_ehis_sk1e`, 2019 (18,5 % et 19,3 %) ; synthèse « Tabagisme » 2024, p. 8 (« au-dessus de la moyenne européenne de 3 points », Eurobaromètre 2023).
4. La baisse de 2024 : synthèse « Tabagisme » 2024, p. 7 (ventes en baisse de 12 % et de 24 %).
5. Le vapotage : synthèse « Vapotage » 2024, p. 1 et p. 6 ; Odissé (2,97 % en 2014).

## Double vérification

Faite le 24/11/2026 par un agent Claude (modèle Sonnet) qui a rouvert chaque source (`verify-sonnet.md`, section R4a) : série 2000-2023, 18,2 % de 2024, 68 021 décès, ESCAPAD, vapotage 2023 et 2024, EHIS : conformes. Les séries d'Odissé ont été relues par l'agent principal par leur API le même jour (prévalence 2000-2023 et vapotage 2014-2023 : conformes). Non ouvert : le portail de l'Eurobaromètre (page JavaScript), en attente du passage dans un navigateur.

## Mises à jour

Aucune. Prochaine édition du Baromètre de Santé publique France : 2026 (il devient bisannuel).

## Relecture

- [x] Le chiffre clé et quelques points de chaque série recoupés dans une seconde source.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée : Licence ouverte 2.0 pour Odissé, chiffres cités pour les PDF.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
