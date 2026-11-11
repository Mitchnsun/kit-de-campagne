# `retirees` · Retraités et pensions

**Vérifiée le 11/11/2026** : double vérification sur le Panorama 2026 de la DREES, sans écart sur 2024 et sur les effectifs et les résidents de 2023 ; un écart d'arrondi sur la pension de l'ensemble en 2023, sans doute une révision (section « Double vérification »). Le montant est brut et hors majoration pour trois enfants ou plus : les tableaux de la DREES le disent.

| Champ | Valeur |
| --- | --- |
| Indicateur | `retirees`, premier volet de la page « Retraites » (`pensions`, page à volets), dossier « Travail et retraites » (`work`), page de type série, ticket #28 de l'app ; le second volet est `contributorsPerRetiree` (COR) |
| Données | `briefings/data/retirees.json`, écrit par `yarn briefings retirees` le 2026-11-11 |
| Sources | DREES, « Données de l'enquête annuelle auprès des caisses de retraite » (EACR), page https://data.drees.solidarites-sante.gouv.fr/explore/dataset/donnes_eacr/ ; fichier « 62 EACR diffusée Part 1 - version du 26 mai 2026.xlsx » (https://data.drees.solidarites-sante.gouv.fr/api/explore/v2.1/catalog/datasets/donnes_eacr/attachments/62_eacr_diffusee_part_1_version_du_26_mai_2026_xlsx), feuille `A-Cadrage` ; documentation « documentationeacr_mai2026 » (pièce jointe du même jeu) ; Licence Ouverte 2.0 (Etalab), que la page du jeu cite, avec l'obligation de mentionner la source |
| Séries | `meanPension` : avantage principal de droit direct moyen, brut, mensuel, en euros courants, des retraités de droit direct de tous les régimes, à l'étranger compris (`m1`, `Resid` « Ensemble »), 2004 à 2024, 21 points ; `meanPensionFrance` : le même, des seuls résidents en France (`Resid` « France »), 21 points ; `retirees` : nombre de retraités de droit direct vivants au 31 décembre, à l'étranger compris (`effectifs`), 21 points ; `retireesFrance` : le même, résidents en France, 21 points. Identifiants : `A-Cadrage 0000 ddir <Resid> <colonne>` |
| Chiffre clé | 1 646,9 € bruts par mois fin 2024, en hausse après 1 563,9 € fin 2023 ; 17 298 245 retraités de droit direct ; résidents en France : 1 705 € et 16 429 118 |
| Règles | Le script trouve la première partie de l'EACR parmi les pièces jointes du jeu (identifiant commençant par `62_eacr_diffusee_part_1_`) et date la source par la version de son titre (« version du 26 mai 2026 ») ; il ne charge que la feuille `A-Cadrage` (le classeur fait 272 Mo une fois décompressé) ; il garde les lignes `CC` 0000 « Tous régimes », `Champ` `ddir` (droit direct, vivants au 31/12), `Sexe`, `Liq` et `StatutSNCF` « Ensemble », `PlusRécent` vrai, pour `Resid` « Ensemble » et « France » ; il échoue sur une colonne absente, une année en double, une année manquante, des années différentes entre les deux résidences, un montant ou un effectif hors de l'ordre de grandeur attendu. Aucun montant net : la DREES n'en donne pas dans ce fichier |
| Première édition | À remplir à la publication |

## « À savoir »

1. Montants bruts, sans montant net dans la série : le Panorama 2026 de la DREES, fiche 05, intitule son tableau 2 « Montant brut mensuel moyen de la pension de droit direct (hors majoration pour trois enfants ou plus) des retraités résidant en France ou à l'étranger, par régime de retraite, en 2024 » (p. 58), et son tableau 1 sépare les colonnes « Brute » et « Nette » (p. 55). Les prélèvements, d'après la note de ce tableau 1 : « La pension nette est calculée après déduction de la CSG, de la CRDS, de la Casa et de la cotisation maladie sur les retraites complémentaires. » La DREES ne publie de net que majoration comprise, pour les résidents en France (non repris, section « Double vérification »). Confirmation du PO du 11/11/2026 : les montants de l'EACR sont toujours bruts. La table `A-Prelev_sociaux` du classeur ne donne que des effectifs par taux de CSG, pas de montant net.
2. Ce que compte `m1` : documentation de l'EACR de mai 2026, présentation de la table A-Cadrage : « L'avantage principal moyen de droit direct (m1) comprend les minima de pension (minimum contributif, minimum garanti ou pension minimale de référence) ; en revanche, il ne comprend pas l'avantage principal de droit dérivé (variable m2), la majoration pour personne à charge […], la majoration de pension pour les parents d'au moins 3 enfants […], les allocations du minimum vieillesse […] ou l'allocation supplémentaire d'invalidité ».
3. Le modèle Ancêtre : même documentation, « la base diffusée est enrichie de données tous régimes issues du modèle ANCETRE de la Drees » ; la colonne `Source` des lignes « Tous régimes » dit « EIR 2004 », « EIR 2008 », « EIR 2012 », « EIR 2016 », « EIR 2020 », et « Ancetre <année> » pour les autres années.
4. Les résidents à l'étranger : variable `Resid`, « précise le lieu de résidence : Ensemble/France. Cette distinction est disponible uniquement pour les données tous régimes » (documentation) ; 17 298 245 − 16 429 118 = 869 127 retraités hors de France fin 2024 (un calcul, arrondi à « environ 870 000 ») ; leur pension moyenne, déduite des deux moyennes (calcul, non écrit dans les notes), est d'environ 549 €, d'où la moyenne de l'ensemble sous celle des résidents.

## Double vérification

Faite le 11/11/2026. Le site de la DREES ne répond pas depuis l'environnement de Claude (data.drees répond) : le PO a fait lire les fiches du Panorama dans son navigateur par un agent, qui a recopié chaque chiffre avec son tableau et sa page, sans calcul ni arrondi (compte rendu du 11/11/2026). Un agent Claude (modèle Opus) a ensuite rapproché ces chiffres du fichier et relu dans le classeur de l'EACR (« version du 26 mai 2026 ») les lignes de 2022 à 2024 : une seule ligne par année et par résidence, `PlusRécent` vrai, aucun millésime antérieur.

Documents : *Les retraités et les retraites – Édition 2026* (Panoramas de la DREES, 14/10/2026), fiche 01 « Les effectifs de retraités de droit direct » et fiche 05 « Le niveau des pensions » ; pour 2023, la fiche 05 de l'édition 2025 (31/07/2025). Le Panorama publie les effectifs en milliers et les pensions à l'euro.

| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
| --- | --- | --- | --- | --- |
| Retraités, ensemble, 2024 | 17 298 245 | 17 298 milliers | Éd. 2026, fiche 01, tableau 1, p. 21 | Conforme |
| Pension, ensemble, 2024 | 1 646,9 € | 1 647 €, brut, hors majoration, « Ensemble, tous régimes » | Éd. 2026, fiche 05, tableau 2, p. 58 | Conforme |
| Retraités, résidents en France, 2024 | 16 429 118 | 16 429 milliers | Éd. 2026, fiche 01, tableau 1, p. 21 | Conforme |
| Pension, résidents en France, 2024 | 1 705 € | 1 705 €, colonne « Pension de droit direct, hors majoration pour 3 enfants ou plus – Brute – Ensemble » | Éd. 2026, fiche 05, tableau 1, p. 55 | Conforme |
| Retraités, ensemble, 2023 | 17 184 263 | 17 184 milliers | Éd. 2026, fiche 01, tableau 1, p. 21 | Conforme |
| Retraités, résidents en France, 2023 | 16 296 183 | 16 296 milliers | Éd. 2026, fiche 01, tableau 1, p. 21 | Conforme |
| Pension, résidents en France, 2023 | 1 621,4 € | 1 621 € (éd. 2026) ; 1 620 € dans l'éd. 2025 | Éd. 2026, fiche 05, tableau 1, p. 55 ; éd. 2025, fiche 05, tableau 1, p. 53 | Conforme à l'éd. 2026, qui a révisé 2023 d'un euro |
| Pension, ensemble, 2023 | 1 563,9 € | 1 563 € (éd. 2025) ; l'éd. 2026 ne donne pas 2023 sur ce champ | Éd. 2025, fiche 05, tableau 2 | Écart d'arrondi (1 563,9 donnerait 1 564) : sans doute la même révision que pour les résidents, entre l'éd. 2025 et l'EACR de mai 2026 ; non prouvé, le classeur ne garde que le dernier millésime |
| Champ | droit direct, tous régimes, vivants au 31/12, hors majoration ; à l'étranger compris pour « Ensemble » | « Retraités ayant perçu une pension de droit direct en 2024 (hors majoration pour trois enfants ou plus), résidant en France ou à l'étranger, vivants au 31 décembre de l'année. » | Éd. 2026, fiche 05, tableau 2, champ | Conforme |
| Brut ou net | brut | colonnes « Brute » et « Nette » du tableau 1 ; tableau 2 « Pension brute de droit direct, hors majoration pour 3 enfants ou plus » | Éd. 2026, fiche 05, p. 55 et 58 | Conforme |
| Évolution sur un an | la page ne montre qu'une tendance (en hausse) | « une progression de 0,8 % par rapport à 2023 », citation de la DREES par la presse | MoneyVox, 26/05/2026 ; Bourse Inside, 27/05/2026 | Hors du fichier : la page n'écrit aucun taux. Non retrouvé dans les fiches relevées ; non repris |
| Licence | Licence Ouverte 2.0 | « Licence Ouverte v2.0 (Etalab) », avec l'obligation de mentionner la source | métadonnées du jeu `donnes_eacr` (API de data.drees) | Conforme |

Sources du Panorama : le tableau 2 de la fiche 05 cite « Drees, EACR, modèle ANCETRE », le tableau 1 de la fiche 01 et celui de la fiche 05 « Drees, EIR, modèle ANCETRE ». Les chiffres des résidents viennent donc d'une autre base que le classeur que lit le script, et coïncident avec lui. La presse (MoneyVox, Bourse Inside) donne les mêmes chiffres de 2024 ; elle n'est plus la source de la vérification.

Non repris :

- Les montants majoration comprise, que la DREES met en avant : pour les résidents en France, 1 752 € bruts et 1 626 € nets fin 2024 (1 667 € et 1 548 € fin 2023), et 1 693 € bruts pour l'ensemble (éd. 2026, fiche 05, p. 54-55). C'est le seul net publié : aucun net hors majoration, ni pour les résidents ni pour l'ensemble. Le net des années 2020 à 2022 a été révisé dans l'édition 2026 (« correction d'une erreur dans les taux de prélèvement appliqués », note du tableau 1).
- La pension nette réversion comprise des résidents en France, 1 785 € fin 2024 (éd. 2026, fiche 05, p. 54), et la pension moyenne tous droits citée par la presse (1 567 € pour 18,2 millions d'assurés), qui comptent la réversion et un autre champ.
- L'estimation d'un net à 92,5 % du brut donnée par le PO comme un ordre d'idée, qui n'est pas un chiffre publié.

**Conclusion.** Les chiffres de 2024 et ceux de 2023, effectifs et pension des résidents, sont ceux du Panorama 2026 ; la pension de l'ensemble en 2023 diffère de l'édition 2025 d'un dixième à l'arrondi. Le montant est brut et hors majoration pour trois enfants ou plus.

**Pages consultées** (le 11/11/2026) :

- https://drees.solidarites-sante.gouv.fr/publications-communique-de-presse/panoramas-de-la-drees/261014-les-retraites-et-les-retraites-edition-2026 (lue par l'agent du PO)
- https://drees.solidarites-sante.gouv.fr/sites/default/files/2026-10/RR2026%20-%20Fiche%2001%20-%20Les%20effectifs%20de%20retrait%C3%A9s%20de%20droit%20direct.pdf (lue par l'agent du PO)
- https://drees.solidarites-sante.gouv.fr/sites/default/files/2026-10/RR2026%20-%20Fiche%2005%20-%20Le%20niveau%20des%20pensions.pdf (lue par l'agent du PO)
- https://drees.solidarites-sante.gouv.fr/sites/default/files/2025-07/Fiche%2005%20-%20Le%20niveau%20des%20pensions.pdf (édition 2025, lue par l'agent du PO)
- https://data.drees.solidarites-sante.gouv.fr/api/explore/v2.1/catalog/datasets/donnes_eacr (métadonnées, licence) et ses pièces jointes (classeur et documentation de mai 2026)
- https://www.moneyvox.fr/retraite/actualites/108976/touchez-vous-plus-que-la-pension-moyenne (26/05/2026)
- https://bourseinside.fr/?p=10084 (Bourse Inside, 27/05/2026, qui cite MoneyVox : pas une source indépendante de lui)

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
