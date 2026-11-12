# `businessClimate` · Attractivité et fiscalité des entreprises (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; la moyenne de l'UE du taux d'IS, calculée, est écartée ; réserves de lecture reprises ci-dessous. La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `businessClimate`, dossier « Économie et fiscalité » (`economy`), volet « Attractivité » de la page composite `competitiveness` (voir `competitiveness.md`), page de type comparaison, recherche « Ce qu'on entend » du 09/11/2026 |
| Données | `briefings/manual/businessClimate.json`, saisi le 2026-11-09 depuis l'API de l'OCDE (investissements directs, taux d'IS), le communiqué de Business France et l'API d'Eurostat (`gov_10a_taxag`, `nrg_pc_205`) ; valeurs des API lues par script dans les fichiers téléchargés |
| Sources | 1. OCDE, « FDI main aggregates, BMD4 » (`DSD_FDI@DF_FDI_AGGR_SUMM`), https://data-explorer.oecd.org/vis?lc=fr&df%5Bds%5D=dsDisseminateFinalDMZ&df%5Bid%5D=DSD_FDI%40DF_FDI_AGGR_SUMM&df%5Bag%5D=OECD.DAF.INV (et `lc=en`), données https://sdmx.oecd.org/public/rest/data/OECD.DAF.INV,DSD_FDI@DF_FDI_AGGR_SUMM,1.0/FRA+DEU+ITA+ESP+GBR............?startPeriod=2019&dimensionAtObservation=AllDimensions&format=csvfilewithlabels, données de la Banque de France pour la France ; date de publication non lue, date de lecture (09/11/2026) indiquée ; citation seule. 2. Business France, « Bilan 2025 des investissements internationaux en France », communiqué « Attractivité : malgré l'incertitude internationale, les entreprises étrangères au rendez-vous en 2025… », https://media.businessfrance.fr/download-pdf/697a67084008084a340e33e6 (29/01/2026), citation seule, en français. 3. Eurostat, « Main national accounts tax aggregates », jeu `gov_10a_taxag`, https://ec.europa.eu/eurostat/databrowser/view/gov_10a_taxag/default/table?lang=fr (et `lang=en`), API https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/gov_10a_taxag?unit=PC_GDP&sector=S13_S212&na_item=D29&time=2025 (05/11/2026), conditions d'Eurostat. 4. OCDE, « Corporate income tax (CIT) - statutory and targeted small business rates » (`DSD_TAX_CIT@DF_CIT`), https://data-explorer.oecd.org/vis?lc=fr&df%5Bds%5D=dsDisseminateFinalDMZ&df%5Bid%5D=DSD_TAX_CIT%40DF_CIT&df%5Bag%5D=OECD.CTP.TPS (et `lc=en`), données https://sdmx.oecd.org/public/rest/data/OECD.CTP.TPS,DSD_TAX_CIT@DF_CIT,2.0/.A.CIT_C+CIT_EX_ST.......?startPeriod=2024&dimensionAtObservation=AllDimensions&format=csvfilewithlabels ; date de publication non lue, date de lecture (09/11/2026) indiquée ; citation seule. 5. Eurostat, « Electricity prices for non-household consumers - bi-annual data », jeu `nrg_pc_205`, https://ec.europa.eu/eurostat/databrowser/view/nrg_pc_205/default/table?lang=fr (et `lang=en`), API https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/nrg_pc_205?siec=E7000&unit=KWH&currency=EUR&tax=X_VAT&nrg_cons=MWH2000-19999&nrg_cons=MWH20-499&time=2023-S1&time=2026-S1 (19/10/2026), conditions d'Eurostat. Les pages de l'explorateur de l'OCDE sont construites sur les identifiants des jeux (réponse 200, page dynamique non lue) |
| Séries | `fdiStock` : position d'investissements directs étrangers en France, principe directionnel, Md€ (M€ divisés par 1 000), 2019 à 2025, 7 points (739,9251 ; 776,577 ; 835,7049 ; 901,5321 ; 918,1785 ; 950,7097 ; 987,4757). `fdiFlows` : flux entrants, 2019 à 2025, 7 points (11,7021 ; 9,9452 ; 27,6163 ; 78,1186 ; 38,978 ; 38,3664 ; 19,3877). `electricityFrance`, `electricityEu`, `electricityGermany` : prix de l'électricité des entreprises de 2 000 à 19 999 MWh par an (tranche ID), hors TVA et autres taxes récupérables, €/kWh, premier semestre de 2023 et de 2026, saisis sous leur année (France 0,2235 et 0,1239 ; UE 0,2015 et 0,1559 ; Allemagne 0,2055 et 0,1742, provisoire en 2026) |
| Valeurs par catégorie | `fdiStockShare` : stock en % du PIB, 2025 (France 34,3 ; Allemagne 28,9 ; Italie 24,1 ; Espagne 57,2 ; Royaume-Uni 63,6). `fdiFlowShare` : flux en % du PIB, 2025, deux décimales (France 0,65 ; Allemagne 1,47 ; Italie 1,21 ; Espagne 1,27 ; Royaume-Uni 1,06). `productionTaxes` : autres impôts sur la production (D29), administrations publiques et institutions de l'UE, % du PIB, 2025 (Suède 10,1 ; France 4,4 ; UE 2,3 ; Allemagne 0,9, provisoire). `corporateTax` : taux légal combiné de l'IS, 2025, deux décimales (France 36,13, surtaxes comprises, CIT_C ; France hors surtaxe 25, CIT_EX_ST ; Malte 35 ; Portugal 30,5 ; Allemagne 30,13 ; Italie 27,81 ; Pays-Bas 25,8). `electricitySmallBusiness` : tranche IB (20 à 499 MWh), premier semestre 2026 (France 0,2049 ; UE 0,2165) |
| Chiffre clé | 987,4757 Md€ fin 2025 (affiché 987,5 Md€), tendance à la hausse (950,7097 en 2024) ; à côté : flux entrants de 2025 (19,4 Md€) |
| Règles | Saisie à la main. Les semestres d'Eurostat sont saisis sous leur année (`2026` pour 2026-S1), les titres et notes des blocs disent « premier semestre ». Les prix s'écrivent en euros à quatre décimales, comme Eurostat (`digits`). Le taux d'IS de 36,13 % est un taux maximal : le taux normal (25 %) est à côté, la note le dit ; la moyenne de l'UE (22,17 %, calculée sur 26 pays, publiée ni par l'OCDE ni par la Commission) est écartée ; la valeur de l'Allemagne est celle du fichier arrondie au centième (30,133026). Le poste D29 n'est pas la totalité des impôts des entreprises. Les décisions de Business France ne sont que dans « À savoir » et l'affirmation, sans comparaison avec 2024 (méthode modifiée). Le taux effectif moyen de la Commission (calcul KPMG) n'est pas saisi |
| Première édition | À remplir à la publication |

## « À savoir »

1. Les flux varient avec les rachats et les prêts intragroupe ; le stock se compare en % du PIB ; OCDE, d'après la Banque de France. Source : OCDE, `DF_FDI_AGGR_SUMM` (« T_FA_F RC DI FRA 2025 = 19387.737977137 » ; « LE_FA_F PT_B1GQ DI FRA 2025 = 34.328064986637 ») ; la recherche note que la somme des quatre trimestres donne la même valeur.
2. 1 878 décisions et 47 734 emplois annoncés en 2025 ; méthode modifiée, pas directement comparable. Source : Business France, communiqué du 29/01/2026 (« En 2025, 1 878 décisions d'investissement étrangères ont été enregistrées, permettant la création ou le maintien de 47 734 emplois. » ; « … ne sont ainsi pas directement comparables entre 2025 et les données des années précédentes »).
3. D29 : 4,4 % du PIB en 2025, 2e de l'UE derrière la Suède (rang calculé), taxe foncière des ménages comprise. Source : Eurostat, `gov_10a_taxag` (« FR … 2024 = 4.4 ; 2025 = 4.4 » ; Suède 10,1) ; la composition du poste est celle que relève la contre-vérification (impôts des entreprises et taxe foncière des ménages propriétaires de leur logement).
4. 36,13 % est un taux maximal (plus grandes entreprises, contribution exceptionnelle) ; taux normal 25 % ; 25,825 % en 2024. Source : OCDE, `DF_CIT` (« FRA CIT_C ST S13 2024 = 25.825 ; 2025 = 36.13 ; FRA CIT_EX_ST 2025 = 25 ») ; Légifrance non ouvert pour les seuils de la contribution exceptionnelle.

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Les deux affirmations sont dans `briefings/notes/businessClimate.json` (clé `claims`, français et anglais). Source de chaque chiffre de la réponse :

1. « On entend que la France n'attire plus les investisseurs étrangers. » 987,5 Md€ fin 2025, 34,3 % du PIB, plus haut de la série depuis 2019 : OCDE (stock). 19,4 Md€ contre 38,4 Md€ en 2024, à peu près la moitié (calculé), 0,65 % du PIB, le plus faible des cinq pays : OCDE (flux). 1 878 décisions, méthode modifiée : Business France. Démentie : des investissements continuent d'entrer et le stock augmente ; la réponse dit aussi le recul des flux de 2025.
2. « On entend que les entreprises françaises paient leur électricité plus cher que leurs voisines. » 0,1239 € (France), 0,1559 € (UE), 0,1742 € (Allemagne, provisoire) le kWh au premier semestre 2026, tranche de 2 à 20 GWh ; 0,2049 € et 0,2165 € pour la tranche de 20 à 499 MWh ; 0,2235 € et 0,2015 € au premier semestre 2023 : Eurostat, `nrg_pc_205`, hors TVA et taxes récupérables. Démentie pour 2026 ; la réponse dit qu'en 2023 la France était au-dessus de la moyenne.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-competitivite.md` (CSV SDMX de l'OCDE, API d'Eurostat, PDF de Business France). Les flux et stocks de 2019 à 2024 et la valeur de la Suède en 2025 ont été relus par l'agent de la page dans les fichiers de l'OCDE et d'Eurostat téléchargés par la contre-vérification.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, stock 2025 | 987,4757 Md€ ; 34,3 % du PIB | 987 475,7 M€ ; 34,3 % | OCDE, CSV SDMX | Conforme, avec réserve : date de publication non lue ; Banque de France non ouverte |
| Flux 2025 | 19,3877 Md€ ; 0,65 % ; 2024 : 38,3664 | 19 387,7 ; 0,65 % ; 38 366 | OCDE, CSV SDMX | Conforme, avec réserve |
| Business France | 1 878 ; 47 734 | communiqué relu | communiqué du 29/01/2026 | Conforme, avec réserve : méthode modifiée |
| D29 | 4,4 % ; 2e de l'UE | FR 4,4 (2024 et 2025), Suède 10,1 | `gov_10a_taxag` | Conforme, avec réserve : pas tous les impôts des entreprises |
| Taux d'IS | 36,13 % ; 25 % | CIT_C 2025 = 36,13 ; 2024 = 25,825 ; CIT_EX_ST = 25 | OCDE, CSV SDMX | Conforme, avec réserve : taux maximal ; Légifrance non ouvert |
| Moyenne de l'UE du taux d'IS | non saisie | 22,17 % retrouvés par calcul, publiés par personne | — | Non retenue |
| Électricité | 0,1239 ; 0,1559 ; 0,1742 (2026-S1) | mêmes valeurs, tranche ID, X_VAT | `nrg_pc_205` (19/10/2026) | Conforme, avec réserve : hors TVA et taxes récupérables, autres taxes comprises ; Allemagne provisoire ; hors toutes taxes, France 0,1064 et UE 0,1306 |

**Conclusion.** Aucun chiffre du fichier n'est faux ; le taux d'IS maximal n'est jamais donné sans le taux normal, et le poste D29 sans ce qu'il contient.

**Pages consultées** le 09/11/2026 : les documents et API des URL ci-dessus. Non ouverts : la Banque de France (403), les fichiers de la DG TAXUD (429), Légifrance.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Pas de script : la double vérification a rouvert les fichiers de l'OCDE et d'Eurostat et le communiqué.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Eurostat : réutilisation permise, commerciale comprise, mention « Source : Eurostat » et modifications signalées (https://ec.europa.eu/eurostat/help/copyright-notice) ;
  - citation seule : OCDE, Business France (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
