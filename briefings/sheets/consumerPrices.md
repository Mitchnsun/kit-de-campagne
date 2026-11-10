# `consumerPrices` · Les prix, poste par poste (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, un écart corrigé (le pic de la grande distribution), aucun autre écart ; réserves de lecture reprises ci-dessous. La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `consumerPrices`, dossier « Pouvoir d'achat et logement » (`purchasingPower`), volet « Les prix, poste par poste » de la page composite `householdBudget` (voir `householdBudget.md`), page de type série, recherche « Ce qu'on entend » du 09/11/2026 |
| Données | `briefings/manual/consumerPrices.json`, saisi le 2026-11-09 depuis le fichier des chiffres vérifiés de la recherche (API SDMX de la BDM de l'Insee), séries reprises par script, sans recopie à la main |
| Sources | 1. Insee, « Indice des prix à la consommation », https://www.insee.fr/fr/metadonnees/source/indicateur/p1653/description (et `/en/`), séries de la BDM 011814639, 011814162, 011814260, 011814288, 011814204 (indices annuels, mise à jour du 27/02/2026), 011813719 et 011814632 (glissements annuels, mise à jour du 30/10/2026, https://www.insee.fr/fr/statistiques/serie/011813719), 011818250 et 011818263 (grande distribution, mise à jour du 15/10/2026), 011818265 et 011814388 (hors tabac, 1er quintile et ensemble), Licence Ouverte 2.0. 2. Insee, « En septembre 2026, les prix à la consommation augmentent de 3,1 % sur un an », Informations rapides n° 247, https://www.insee.fr/fr/statistiques/9080209 (en anglais https://www.insee.fr/en/statistiques/9080263), 15/10/2026, Licence Ouverte 2.0. 3. Insee, « En octobre 2026, les prix à la consommation augmenteraient de 3,4 % sur un an », Informations rapides n° 266, https://www.insee.fr/fr/statistiques/9107965 (en anglais https://www.insee.fr/en/statistiques/9107975), 30/10/2026, Licence Ouverte 2.0. 4. Insee, « Indice des prix à la consommation : les changements de l'année 2026 », https://www.insee.fr/fr/statistiques/documentation/IPC_operations_changement_annee_2026.pdf (PDF créé le 02/02/2026, lié à l'Informations rapides n° 32 du 03/02/2026), Licence Ouverte 2.0, en français. 5. Insee, « Le logement dans l'indice des prix à la consommation », Insee Focus n° 152, https://www.insee.fr/fr/statistiques/4126450 (18/04/2019), Licence Ouverte 2.0, en français. 6. Eurostat, « Harmonised index of consumer prices (HICP) - ECOICOP ver.2 - indices and rates of change, annual data », jeu `prc_hicp_ainr`, https://ec.europa.eu/eurostat/databrowser/view/prc_hicp_ainr/default/table?lang=fr (et `lang=en`), API https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/prc_hicp_ainr?geo=FR&geo=EU27_2020&geo=DE&geo=IT&geo=ES&coicop18=TOTAL&coicop18=CP01&unit=INX_A_AVG&sinceTimePeriod=2019 (mise à jour du 17/09/2026), conditions d'Eurostat |
| Séries | `allItemsIndex` (011814639), `foodIndex` (011814162, boissons alcoolisées comprises), `energyIndex` (011814260), `servicesIndex` (011814288), `manufacturedIndex` (011814204) : indices annuels moyens, base 100 = 2025, 2015 à 2025, 11 points chacune (2015 : 82,68 ; 75,06 ; 66,54 ; 84,27 ; 95,77). `foodChange` (011813719) et `allItemsChange` (011814632) : glissement annuel mensuel, en %, janvier 2019 à septembre 2026, 93 points chacune, sans l'estimation provisoire d'octobre 2026 (alimentation : 15,9 en mars 2023, le maximum ; 1,4 en septembre 2026 ; 1,2 en octobre ; ensemble : 3,1 et 3,4). `supermarketIndex` (011818250) : indice des produits d'alimentation industrielle, d'entretien et d'hygiène-beauté dans la grande distribution, France métropolitaine, base 100 = 2025, janvier 2020 à septembre 2026, 81 points (décembre 2021 : 83,39 ; septembre 2026 : 100,08). `supermarketChange` (011818263) : son glissement annuel, en %, janvier 2021 à septembre 2026, 69 points (maximum +15,6 en avril 2023 ; −0,3 en septembre 2026) |
| Chiffre clé | +1,4 % pour les prix de l'alimentation sur un an en septembre 2026, le dernier mois définitif, tendance à la hausse (+1,1 % en août) ; à côté, l'ensemble des prix, +3,1 % |
| Règles | Saisie à la main. Des indices de prix à qualité constante, jamais présentés comme des dépenses. Les mois définitifs seulement : l'estimation provisoire d'octobre 2026 (30/10/2026, définitive le 13/11/2026) n'entre pas, comme pour la page `inflation` (PO, 02/11/2026 : une estimation provisoire du mois n'entre jamais dans une édition). Elle avait été saisie le 09/11/2026, puis retirée le jour même. Les hausses cumulées (2019-2025, +20,0 % de la grande distribution depuis décembre 2021, +15,5 % hors tabac) sont calculées, dans les notes et les affirmations seulement. L'inflation d'ensemble mois par mois a sa page (`inflation`) : la note de la vue y renvoie. Les indices sont écrits au centième, comme l'Insee (`digits`). Le graphique annuel trace l'alimentation et l'ensemble ; l'énergie, les services et les produits manufacturés sont dans le tableau |
| Première édition | À remplir à la publication |

## « À savoir »

1. Un indice de prix suit le prix des mêmes produits à qualité constante, il ne dit ni ce que les ménages dépensent ni ce qu'ils achètent ; indices annuels en moyenne de l'année, base 100 en 2025 ; « alimentation » comprend les boissons alcoolisées. Source : BDM (indices annuels, base 2025) ; pondérations : « 1 338 pour la division 01 + 147 pour l'alcool = 1 485 », relues sur la BDM par la contre-vérification.
2. Seuls les mois définitifs entrent : l'estimation provisoire d'octobre 2026, définitive le 13/11/2026, n'y est pas ; elle n'est pas à utiliser pour des revalorisations contractuelles. Source : Informations rapides n° 266 (« les indices provisoires ne doivent pas être utilisés pour des revalorisations contractuelles ») et page de l'Informations rapides n° 247 (« Prochaine parution le : 13/11/2026 »).
3. En 2026, l'alimentation pèse 1 485 sur 10 000, boissons alcoolisées comprises (dont 170 pour les produits frais), l'énergie 764. Source : Informations rapides n° 247, tableau des pondérations (« Alimentation 1 485 … Produits frais 170 … Énergie 764 »).
4. L'indice de la grande distribution est une nouvelle série depuis 2026, remontée à janvier 2020 : un indice de prix, pas le coût d'un panier ; +20,0 % de décembre 2021 à septembre 2026 (calculé). Source : « Les changements de l'année 2026 » (« À compter de 2026, les anciens indices sont remplacés par trois nouvelles séries dont la méthodologie a été actualisée ») ; BDM 011818250 (83,39 puis 100,08).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Les quatre affirmations sont dans `briefings/notes/consumerPrices.json` (clé `claims`, français et anglais). Source de chaque chiffre de la réponse :

1. « On entend que l'inflation de 2026 vient de l'alimentation. » +3,1 % en septembre, l'énergie à +21,3 %, le gazole à +44,1 %, l'alimentation à +1,4 %, les produits frais à +9,5 % (« notamment sous l'effet des vagues de chaleur »), le reste de l'alimentation à +0,4 %, les produits manufacturés à −0,3 %, les pondérations 170 et 1 315 : Informations rapides n° 247 (« la hausse de l'inflation s'explique par la nouvelle accélération des prix de l'énergie »). Démentie : la hausse vient de l'énergie.
2. « On entend que l'inflation frappe beaucoup plus les ménages modestes que les autres. » +3,3 % pour le 1er quintile et +3,1 % pour l'ensemble, hors tabac, en septembre 2026 : Informations rapides n° 247 (« Ménages du 1er quintile … Ensemble hors tabac 9 735 103,22 -0,2 3,3 » ; « Ensemble hors tabac 9 832 103,07 -0,3 3,1 »). +15,5 % de 2019 à 2025 pour les deux : BDM 011818265 et 011814388 (86,60 puis 100,0), calculé. 22,1 % et 12,2 % pour le logement, 18,3 % et 14,2 % pour l'alimentation : Insee Focus n° 203, enquête Budget de famille 2017, la dernière publiée (volet « Ce qu'ils achètent »). Démentie : l'écart est de 0,2 point en septembre 2026 et nul de 2019 à 2025 ; la réponse dit aussi ce qui va dans l'autre sens, la structure des budgets.
3. « On entend que l'inflation officielle ne tient pas compte du logement. » Loyers, charges, énergie et petits travaux comptés, achat et gros travaux exclus comme investissement, loyers imputés exclus : Insee Focus n° 152 (« il exclut en revanche l'investissement en logement (achat ou gros travaux) » ; « les achats en logement ne constituent pas de la consommation » ; l'indice « y compris loyers imputés » est un autre indice). 1 548, 672 et 446 sur 10 000 : pondérations 2026 de la BDM (011815629, 011815638, 011815804). Démentie : le logement pèse 15,5 % de l'indice ; la réponse ne compare pas ce poids aux parts des comptes nationaux.
4. « On entend que les prix de l'alimentation ont augmenté plus en France que chez nos voisins européens. » +27,0 % (France), +38,7 % (UE), +40,5 % (Allemagne), +29,7 % (Italie), +37,9 % (Espagne), ensemble +18,6 % et +26,5 % : `prc_hicp_ainr`, indices annuels moyens 2019 (2025 = 100 : FR 78,72 ; UE 72,11 ; DE 71,19 ; IT 77,10 ; ES 72,52), calculés (100 / indice 2019 − 1). Démentie : la hausse est plus faible en France que dans l'UE et chez ces trois voisins.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-panier.md` (API SDMX de la BDM, API d'Eurostat, textes des Informations rapides relus).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, alimentation sur un an | +1,4 % (septembre 2026) ; +1,1 % (août) | « +1,4 % en septembre 2026 après +1,1 % en août » | Informations rapides n° 247 | Conforme (octobre, provisoire, non repris) |
| Pic de l'alimentation | 15,9 % (mars 2023) | « 2023-03 : 15.9 », maximum de 011813719 et de la série arrêtée 001761326 | API SDMX de la BDM | Conforme |
| Ensemble sur un an | 3,1 (septembre) ; 6,3 (février 2023) | mêmes valeurs | BDM 011814632 | Conforme |
| Indices annuels | ensemble 82,68 (2015), 86,18 (2019) ; alimentation 79,62 (2019)… | valeurs relues année par année | BDM | Conforme |
| Grande distribution | 83,39 (décembre 2021) ; 100,08 (septembre 2026) ; maximum du glissement +15,6 (avril 2023) | mêmes valeurs ; mars 2023 : +15,4 | BDM 011818250 et 011818263 | Écart corrigé : le rapport de recherche donnait le pic en mars à +15,4 % |
| Hausses 2019-2025 de l'IPCH | +27,0 ; +38,7 ; +40,5 ; +29,7 ; +37,9 % | indices 2019 relus, calculs refaits | API `prc_hicp_ainr` (17/09/2026) | Conforme : calculé |
| Hors tabac | +3,3 % / +3,1 % ; +15,5 % pour les deux | tableau relu ; 86,60 puis 100,0 | Informations rapides n° 247 ; BDM | Conforme |

**Conclusion.** Aucun chiffre du fichier n'est faux ; le pic de la grande distribution est celui d'avril 2023, chaque hausse cumulée est calculée et dite telle, et un indice de prix n'est jamais lu comme une dépense.

**Pages consultées** le 09/11/2026 : les documents et API des URL ci-dessus.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Pas de script : la double vérification a rouvert la BDM et les publications.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
