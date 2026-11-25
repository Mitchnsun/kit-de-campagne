# `energyLabels` · Les passoires thermiques

**Vérifiée le 25/11/2026** : chiffres relus dans les fichiers XLSX et la publication du SDES par l'agent principal, après la recherche d'un agent Claude (modèle Sonnet) ; un second producteur n'a pas été ouvert (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `energyLabels`, volet de « Le logement » (`housing`), dossier « Pouvoir d'achat et logement » (`purchasingPower`), page de type série, ticket #541 de l'app |
| Données | `briefings/manual/energyLabels.json`, saisi à la main le 2026-11-25 depuis deux fichiers XLSX du SDES |
| Sources | SDES-ONRE, « Le parc de logements par classe de performance énergétique au 1er janvier 2025 », publié le 12/11/2025, https://www.statistiques.developpement-durable.gouv.fr/le-parc-de-logements-par-classe-de-performance-energetique-au-1er-janvier-2025 , fichier https://www.statistiques.developpement-durable.gouv.fr/media/8810/download?inline (feuille `Ensemble`, colonnes « DPE 2024 » et « DPE 2025 Résidences principales ») et publication https://www.statistiques.developpement-durable.gouv.fr/media/8813/download?inline ; SDES-ONRE, « … au 1er janvier 2023 », publié le 20/11/2023, https://www.statistiques.developpement-durable.gouv.fr/le-parc-de-logements-par-classe-de-performance-energetique-au-1er-janvier-2023 , fichier https://www.statistiques.developpement-durable.gouv.fr/media/6806/download?inline (feuille `Ensemble`, colonnes « DPE 2023 Résidences principales ») ; licence ouverte (mentions légales du site, décret n° 2017-638), https://www.statistiques.developpement-durable.gouv.fr/mentions-legales |
| Séries | Résidences principales, France métropolitaine, au 1er janvier 2023, 2024 et 2025 : `poorShare` (part des étiquettes F et G, ligne « Passoires », en %, arrondie au dixième), `poorCount` (leur nombre, en milliers dans le fichier, arrondi au millier), `labelA` à `labelG` (part de chaque étiquette, en %, arrondie au dixième ; les sept font 99,8 à 100,0 % à l'arrondi) |
| Chiffre clé | 12,7 % au 1er janvier 2025 (0,12665 dans le fichier), en baisse (13,9 % en 2024) ; le nombre à côté, 3 915 000 (3 914,7 milliers) |
| Règles | 2024 et 2025 lus dans l'édition 2025, qui donne les deux ; 2023 dans l'édition 2023 ; le 1er janvier 2022 de l'édition 2023 (données révisées, Fidéli 2020) n'est pas repris. Pas d'édition au 1er janvier 2026 au 25/11/2026 : la suivante aura une rupture (coefficient de l'électricité), à dire en note |
| Première édition | La prochaine édition du kit |

## « À savoir »

1. 12,7 % et 15,7 %, environ 3,9 millions : fichiers ci-dessus. « Estimation » : la publication de 2025, p. 1 (méthode : DPE de l'Ademe d'octobre à mars, extrapolés au parc avec Fidéli).
2. Publication de 2025, p. 1 : « Près de 40 % de la baisse par rapport au 1er janvier 2024 est imputable à la réforme du calcul du DPE pour les petites surfaces » ; « réforme des seuils du DPE pour les logements de petites surfaces (moins de 40 m2) » ; « entrée en vigueur le 1er juillet 2024 ».
3. Publication de 2025, encadré 2 et p. 1 : de 2,3 à 1,9 au 1er janvier 2026 (« un arrêté du 13 août 2025 »), « une baisse du nombre de passoires énergétiques au sein du parc de résidences principales d'environ 700 000 logements » ; 1,7 au 1er janvier 2027 : communiqué du ministère de la Transition écologique du 31/08/2026, https://www.ecologie.gouv.fr/presse/dpe-audits-energetiques-publication-larrete-abaissant-facteur-conversion-lelectricite-17-1er (lu par l'agent de recherche).
4. Publication de 2025, p. 2 : « 15,1 % pour les maisons et 9,7 % pour les appartements » ; « parc social (5,8 %, soit 284 000 logements » ; « parc locatif privé avec 13,8 % ».

## Double vérification

Faite le 25/11/2026 : la recherche d'un agent Claude (modèle Sonnet, rapport `research/briefings-quiz-2026-11/verification-regles.md` de l'app), puis la relecture des cellules et du PDF par l'agent principal.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Passoires 2025 | 12,7 % | 12,7 % (« 12,7 % ») | Page de l'édition 2025 et sa publication | Conforme |
| Passoires 2024 | 13,9 % ; 4 242 000 | 4 242 milliers, 13,9 % | Édition 2024 (fichier `/media/7941`) | Conforme |
| Passoires 2023 | 15,7 % ; 4 751 000 | baisse de 836 000 depuis 2023 (4 751 − 3 915) | Publication de 2025, p. 1 | Conforme |
| Un autre producteur (Ademe, Anah) | | Non ouvert | | Non trouvé : le SDES est la source statistique de référence, l'Ademe fournit les DPE bruts |

**Conclusion.** Les chiffres sont ceux du SDES, cohérents d'une édition à l'autre et avec le texte de la publication.

**Pages consultées** le 25/11/2026 : celles du tableau.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
