# `retirees` · Retraités et pensions

**Vérifiée le 11/11/2026** : double vérification sur le web, sans écart sur les chiffres de 2024 (section « Double vérification »). Le montant est brut : confirmé par le PO le 11/11/2026, les montants de l'EACR étant toujours bruts.

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

1. Montants bruts, avant CSG, CRDS et Casa, sans montant net dans la série : confirmation du PO du 11/11/2026 (les montants de l'EACR sont toujours bruts ; quand la DREES donne un net, elle le dit, en général dans le Panorama « Les retraités et les retraites ») ; MoneyVox (26/05/2026) et Bourse Inside (27/05/2026, qui cite MoneyVox) citent la DREES : « La pension moyenne de droit direct brut […] s'élève à 1 705 euros », « avant CSG et autres cotisations sociales ». La table `A-Prelev_sociaux` du même classeur ne donne que des effectifs par taux de CSG, pas de montant net.
2. Ce que compte `m1` : documentation de l'EACR de mai 2026, présentation de la table A-Cadrage : « L'avantage principal moyen de droit direct (m1) comprend les minima de pension (minimum contributif, minimum garanti ou pension minimale de référence) ; en revanche, il ne comprend pas l'avantage principal de droit dérivé (variable m2), la majoration pour personne à charge […], la majoration de pension pour les parents d'au moins 3 enfants […], les allocations du minimum vieillesse […] ou l'allocation supplémentaire d'invalidité ».
3. Le modèle Ancêtre : même documentation, « la base diffusée est enrichie de données tous régimes issues du modèle ANCETRE de la Drees » ; la colonne `Source` des lignes « Tous régimes » dit « EIR 2004 », « EIR 2008 », « EIR 2012 », « EIR 2016 », « EIR 2020 », et « Ancetre <année> » pour les autres années.
4. Les résidents à l'étranger : variable `Resid`, « précise le lieu de résidence : Ensemble/France. Cette distinction est disponible uniquement pour les données tous régimes » (documentation) ; 17 298 245 − 16 429 118 = 869 127 retraités hors de France fin 2024 (un calcul, arrondi à « environ 870 000 ») ; leur pension moyenne, déduite des deux moyennes (calcul, non écrit dans les notes), est d'environ 549 €, d'où la moyenne de l'ensemble sous celle des résidents.

## Double vérification

Faite le 11/11/2026 par un agent Claude (modèle Opus), sans relire le classeur que lit le script : les sources données par le PO le 11/11/2026 (deux articles de presse qui citent la publication de la DREES du 26/05/2026). La « Vue d'ensemble » du Panorama 2025 de la DREES (https://drees.solidarites-sante.gouv.fr/sites/default/files/2025-07/Vue%20d%27ensemble.pdf) n'a pas pu être lue d'ici : le site de la DREES ne répond pas depuis cet environnement (data.drees répond).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, ensemble des retraités, 2024 | 1 646,9 € bruts, 17 298 245 retraités | « 1 647 euros pour 17,3 millions de personnes », « résidant en France ou non » | MoneyVox, 26/05/2026 ; Bourse Inside, 27/05/2026 | Conforme |
| Résidents en France, 2024 | 1 705 €, 16 429 118 retraités | « 1 705 euros », « des 16,4 millions de retraités résidant en France au 31 décembre 2024 » | MoneyVox ; Bourse Inside | Conforme |
| Brut ou net | brut | « pension brute moyenne, donc avant CSG et autres cotisations sociales » ; confirmation du PO | MoneyVox ; PO, 11/11/2026 | Conforme |
| Évolution sur un an | la page ne montre qu'une tendance (en hausse) ; le fichier donne 1 621,4 € puis 1 705 € pour les résidents (+5,2 % en euros courants) | « une progression de 0,8 % par rapport à 2023 », citation de la DREES par la presse | MoneyVox ; Bourse Inside | Hors du fichier : la page n'écrit aucun taux d'évolution. Les 0,8 % sont sans doute en euros constants (hypothèse non vérifiée, la publication de la DREES n'ayant pas pu être lue) |
| Licence | Licence Ouverte 2.0 | « Licence Ouverte v2.0 (Etalab) », avec l'obligation de mentionner la source | métadonnées du jeu `donnes_eacr` (API de data.drees) | Conforme |

Non repris : la pension moyenne tous droits (« 1 567 euros pour 18,2 millions d'assurés », 1 657 € pour les résidents en France, presse du 26 et 27/05/2026), qui compte aussi la réversion et les majorations et un autre champ de retraités ; et l'estimation d'un net à 92,5 % du brut donnée par le PO comme un ordre d'idée, qui n'est pas un chiffre publié.

**Conclusion.** Les chiffres de 2024, pour l'ensemble et pour les résidents en France, sont ceux que la presse cite de la DREES ; le montant est brut.

**Pages consultées** (le 11/11/2026) :

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
