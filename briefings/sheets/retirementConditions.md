# `retirementConditions` · Les conditions de départ (partie de la page « Retraites »)

**Vérifiée le 17/11/2026** : le fichier du script concorde avec une lecture indépendante de la même feuille et avec les ordres de grandeur publiés par la DREES et la CNAV, à un écart de champ près (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `retirementConditions`, quatrième volet de la page « Retraites » (`pensions`), dossier « Travail et retraites » (`work`), page de type comparaison, recherche du 17/11/2026 (#21) |
| Données | `briefings/data/retirementConditions.json`, écrit par `yarn briefings retirementConditions` le 2026-11-17 |
| Source | DREES, « Données de l'enquête annuelle auprès des caisses de retraite » (EACR), page https://data.drees.solidarites-sante.gouv.fr/explore/dataset/donnes_eacr/ ; fichier « 62 EACR diffusée Part 2 - version du 26 mai 2026.xlsx », feuille `H-Conditions_liq` ; documentation « DocumentationEACR_mai2026.pdf » (pièce jointe du jeu), section « Table H-Conditions_liq » ; Licence Ouverte 2.0 |
| Séries | Champ : CNAV (codes 0010 jusqu'en 2019, 0015 depuis 2020), `Champ_FluxStock` « Flux », `Sexe` et `Age` « Ensemble ». `longCareers` : départs anticipés pour carrière longue (`liq_racl`, taux plein), 2005 à 2024, 20 points ; `departures` : tous les départs (« Ensemble », « Ensemble »), 20 points ; `discount` : départs avec décote, 20 points ; `bonus` : départs avec surcote, 19 points (pas de ligne en 2020). Répartitions de 2024 : `byMotive` (neuf motifs de la partition, du plus grand au plus petit), `byRate` (taux plein, décote, surcote) |
| Chiffre clé | 113 096 départs pour carrière longue en 2024, en baisse après 122 964 en 2023 |
| Règles | Le script trouve la seconde partie de l'EACR parmi les pièces jointes et la date par sa version ; il ne charge que la feuille `H-Conditions_liq` ; il échoue sur une colonne absente, un code de la CNAV inconnu, un motif de la fonction publique à la CNAV, une ligne en double, une année manquante, moins de 15 années, des motifs ou des taux de la dernière année qui ne font pas exactement le total, des taux d'une année qui ne font pas son total quand les trois y sont, des carrières longues qui ne sont pas toutes au taux plein. Le compte professionnel de prévention n'est pas un motif (sorti de la partition en 2024) |
| Première édition | À remplir à la publication |

À actualiser : à chaque version de l'EACR (mai).

## « À savoir »

1. La partition des motifs : documentation, « Le total des départs se ventile en 12 motifs », de l'amiante aux « Départs de droit commun », « Pour les assurés éligibles à plusieurs motifs d'obtention du taux plein, le motif retenu est déterminé dans l'ordre de priorité ci-dessus » ; les motifs 6 à 8 (motif familial, catégories active et insalubre) n'existent pas à la CNAV ; les neuf autres font 648 346 en 2024 (vérifié par le script).
2. Carrières longues : 113 096 sur 648 346 en 2024 (17,4 %, calcul) ; 24 440 en 2009 et 166 912 en 2017 (feuille).
3. Décote et surcote : 86 776 (13,4 %, calcul) et 122 368 (18,9 %, calcul) en 2024 ; aucune ligne de surcote à la CNAV en 2020.
4. Le C2P : documentation, note 6, « La table présente une rupture de série en 2024 pour la catégorie Cpte Perso Penibilite. En effet cette catégorie faisait auparavant partie de la partition puis en a été retirée en 2024 » ; 2 864 départs en 2024 (feuille).

## Double vérification

Faite le 17/11/2026 par un agent Claude (modèle Opus) : une lecture de la feuille par un script Python indépendant (openpyxl), puis la recherche web.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Toutes les valeurs | — | Identiques, et la recherche du 17/11/2026 lisait les mêmes (113 096 ; 86 776 ; 122 368 ; 648 346) | Lecture Python du classeur | Conforme (même source) |
| Part des carrières longues, 2022 | 128 703 / 693 238 = 18,6 % (calcul) | « un peu moins de 19 % » des départs au régime général en 2022 | DREES, Les retraités et les retraites, édition 2024, fiche 17 (https://www.drees.solidarites-sante.gouv.fr/sites/default/files/2024-10/RR24%20-%20Fiche%2017%20-%20Les%20conditions%20de%20liquidation%20de%20la%20retraite.pdf), d'après un résumé de moteur (le site répond 503) | Conforme (résumé) |
| Carrières longues, 2024 | 113 096 sur 648 346 | « 114 000 départs anticipés pour carrière longue » pour 658 481 nouveaux retraités ; ou « plus de 118 000 » sur « environ 650 000 » | Chiffres de la CNAV repris par https://www.jechange.fr/credit/news/carriere-longue-un-homme-sur-quatre-une-femme-sur-dix et https://www.sapiendo-retraite.fr/sapiendo-acteur-de-la-retraite/actualites-sapiendo-retraite/chiffres-clefs-cnav-2024 (résumés de moteur) | Écart expliqué : la CNAV publie ses attributions de l'année (champ et date d'extraction différents de l'EACR) ; même ordre de grandeur |

**Conclusion.** Aucun écart non expliqué ; le chiffre de la CNAV elle-même reste à lire dans ses « chiffres clés » 2024.

**Pages consultées** le 17/11/2026 : celles du tableau.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
