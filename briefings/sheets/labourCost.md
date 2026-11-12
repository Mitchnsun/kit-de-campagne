# `labourCost` · Coût du travail (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; rangs refaits sur les 27 pays ; réserves de lecture reprises ci-dessous. La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `labourCost`, dossier « Économie et fiscalité » (`economy`), volet « Coût du travail » de la page composite `competitiveness` (voir `competitiveness.md`), page de type comparaison, recherche « Ce qu'on entend » du 09/11/2026 ; « à lire d'abord » dans l'app : le coût d'une heure ne dit pas ce qu'elle produit |
| Données | `briefings/manual/labourCost.json`, saisi le 2026-11-09 depuis l'API d'Eurostat (`lc_lci_lev`, `nama_10_lp_ulc`), l'actualité d'Eurostat du 31/03/2026 et la fiche de l'Insee du 02/07/2026 ; valeurs de l'API lues par script dans les fichiers téléchargés |
| Sources | 1. Eurostat, « Labour cost levels by NACE Rev. 2 activity », jeu `lc_lci_lev`, https://ec.europa.eu/eurostat/databrowser/view/lc_lci_lev/default/table?lang=fr (et `lang=en`), API https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/lc_lci_lev?lcstruct=D1_D4_MD5&unit=EUR&nace_r2=B-S_X_O&time=2024&time=2025 (mise à jour du 23/04/2026), conditions d'Eurostat. 2. Eurostat, « EU hourly labour costs ranged from €12 to €57 in 2025 », https://ec.europa.eu/eurostat/web/products-eurostat-news/w/ddn-20260331-2 (31/03/2026), conditions d'Eurostat, en anglais. 3. Insee, « Salaires et coût du travail en Europe », Insee Références « Emploi, chômage, revenus du travail », https://www.insee.fr/fr/statistiques/8733109?sommaire=8733125 (02/07/2026), Licence Ouverte 2.0, en français. 4. Eurostat, « Labour productivity and unit labour costs - annual data », jeu `nama_10_lp_ulc`, https://ec.europa.eu/eurostat/databrowser/view/nama_10_lp_ulc/default/table?lang=fr (et `lang=en`), API https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/nama_10_lp_ulc?unit=I10&na_item=NULC_PER&geo=FR&geo=DE&geo=EU27_2020&sinceTimePeriod=2010 (mise à jour du 05/11/2026), conditions d'Eurostat. 5. Conseil national de productivité, « Les nouveaux contours de la productivité française », sixième rapport, https://www.strategie-plan.gouv.fr/files/files/Publications/2026/2026-07-01%20-%20CNP%20-%20Rapport%20et%20NS/CNP-2026-Sixi%C3%A8me-Rapport-1juillet15h-FINAL-COUV.pdf (1er juillet 2026), citation seule, en français |
| Séries | `france`, `germany`, `europeanUnion` : coût horaire de la main-d'œuvre, ensemble de l'économie (NACE B à S hors O), entreprises de 10 salariés ou plus, en euros, 2024 et 2025 (France 43,4 et 44,3 ; Allemagne 43,5 et 45,0 ; UE 33,5 et 34,9) ; `euroArea` : zone euro à 21 pays (EA21), 2025 seulement, 38,2. `franceUlc`, `germanyUlc`, `europeanUnionUlc` : coût salarial unitaire nominal par personne employée (NULC_PER), base 100 en 2010, 2010 à 2025, 16 points chacune (2025 : France 128,133 ; Allemagne 152,924 ; UE 136,368), provisoires selon Eurostat : France 2024 et 2025, Allemagne 2023 à 2025 |
| Valeurs par catégorie | `hourlyCostEu` : coût horaire de 2024 des 27, en euros, dans l'ordre décroissant (Luxembourg 54,9 ; Danemark 50,2 ; Belgique 48,2 ; Pays-Bas 45,2 ; Autriche 44,3 ; Allemagne 43,5 ; France 43,4 ; Irlande 42,5 ; Suède 40,2 ; Finlande 37,7 ; Italie 31,0 ; Slovénie 27,1 ; Espagne 25,5 ; Chypre 21,0 ; Estonie 19,6 ; Malte 19,1 ; Slovaquie 18,5 ; Portugal 18,2 ; Tchéquie 18,1 ; Pologne 17,3 ; Grèce 16,8 ; Croatie 16,5 ; Lituanie 16,3 ; Lettonie 15,1 ; Hongrie 14,0 ; Roumanie 12,4 ; Bulgarie 10,6), Autriche et Finlande provisoires. `industry` : coût horaire dans l'industrie (B à E) de l'Insee, 2025 (France 47,7 ; Allemagne 49,8). `nonWageShare` : part des coûts non salariaux dans le coût du travail, 2025 (France 32,3 ; Suède 31,7 ; Slovaquie 28,6 ; zone euro 25,6 ; UE 24,8 ; Malte 5,8 ; Lituanie 5,5 ; Roumanie 4,8) |
| Chiffre clé | 44,3 € de l'heure en France en 2025 (estimation), tendance à la hausse (43,4 € en 2024) |
| Règles | Saisie à la main. Le classement des 27 est celui de 2024, dernière année publiée par les 27 (la Belgique manque en 2025) ; ses rangs, numérotés par la variante `ranking`, sont calculés, ce que dit la note du bloc ; la moyenne de l'UE (33,5 €) est dans la note, pas parmi les pays. Les euros sont écrits au dixième, comme Eurostat (`digits`). Le coût de l'Insee dans l'industrie a un autre champ que celui de l'ensemble de l'économie : bloc et note à part. Les « +28 % », « +53 % » et « +36 % » se lisent sur l'indice (128,1 ; 152,9 ; 136,4 moins 100) : dans l'affirmation et pas en série |
| Première édition | À remplir à la publication |

## « À savoir »

1. Le coût du travail comprend les salaires et les coûts non salariaux, surtout les cotisations des employeurs ; entreprises de 10 salariés ou plus, hors agriculture et administration publique ; 2025 est une estimation. Source : Eurostat, actualité du 31/03/2026 (« In 2025, the average hourly labour costs in the whole economy … were estimated to be €34.9 in the EU and €38.2 in the euro area ») et jeu `lc_lci_lev` (champ B-S hors O) ; la contre-vérification note que l'estimation extrapole l'enquête de 2020.
2. La Belgique n'est pas publiée pour 2025 (48,2 € en 2024) ; France 7e des 27 en 2024, 6e des 26 pays publiés en 2025 ; rangs calculés. Source : `lc_lci_lev`, valeurs de 2024 et 2025 des 27, triées (contre-vérification : « LU, DK, BE, NL, AT, DE, FR (43,4) »).
3. Industrie hors construction : 47,7 € en France contre 49,8 € en Allemagne en 2025, selon l'Insee, autre champ que les 44,3 €. Source : Insee, fiche du 02/07/2026 (« Dans l'industrie, le coût horaire français est inférieur à celui de l'Allemagne depuis plusieurs années (47,7 euros en 2025, contre 49,8 euros) ») ; recoupé dans `lc_lci_lev`, NACE B à E (47,7 et 49,8).
4. Le coût salarial unitaire dépend des salaires et de la productivité ; ses dernières années sont provisoires ; en 2025, le coût horaire a augmenté de 2,0 % en France, la plus faible hausse de la zone euro. Source : `nama_10_lp_ulc` (drapeaux « p ») ; actualité d'Eurostat du 31/03/2026 (« the lowest were in France (+2.0%) and Italy (+3.2%) »).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Les deux affirmations sont dans `briefings/notes/labourCost.json` (clé `claims`, français et anglais). Source de chaque chiffre de la réponse :

1. « On entend que la France a le coût du travail le plus élevé d'Europe. » 44,3 € (France), 45,0 € (Allemagne), 34,9 € (UE) en 2025 : `lc_lci_lev` et actualité du 31/03/2026. 7e en 2024, derrière le Luxembourg, le Danemark, la Belgique, les Pays-Bas, l'Autriche et l'Allemagne : `lc_lci_lev`, rang calculé. 47,7 € et 49,8 € dans l'industrie : Insee. 32,3 %, la part la plus élevée de l'UE : actualité d'Eurostat (« the highest in France (32.3%), Sweden (31.7%) and Slovakia (28.6%) »). Démentie : la France n'a pas le coût horaire le plus élevé ; la réponse dit aussi ce qui va dans l'autre sens (les coûts non salariaux).
2. « On entend que les coûts de production ont explosé en France par rapport à l'Allemagne. » +28 % (128,1), +53 % (152,9), +36 % (136,4) de 2010 à 2025 : `nama_10_lp_ulc`, NULC_PER, base 2010 (« FR 2025 = 128.133p ; DE 2025 = 152.924p »). La France « a progressivement regagné en compétitivité-prix vis-à-vis de l'Allemagne » depuis le début des années 2010, et « une partie du gain observé résulte de la dégradation de la position relative de l'Allemagne » : Conseil national de productivité, rapport du 1er juillet 2026. Démentie : le coût unitaire a augmenté moins vite en France qu'en Allemagne.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-competitivite.md` (API JSON d'Eurostat, page de l'Insee et PDF du CNP relus). Les valeurs des 27 de 2024 et les points des coûts unitaires que le rapport ne cite pas ont été relus par l'agent de la page, par script, dans les réponses de l'API d'Eurostat téléchargées par la recherche et la contre-vérification.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, coût horaire 2025 | France 44,3 ; UE 34,9 ; Allemagne 45,0 ; zone euro 38,2 | mêmes valeurs ; 38,2 = EA21 (EA20 : 38,6) | `lc_lci_lev` (23/04/2026) | Conforme : estimation, entreprises de 10 salariés ou plus, B-S hors O |
| Rang 2024 | 7e des 27 | « LU, DK, BE, NL, AT, DE, FR (43,4) » | `lc_lci_lev` | Conforme, avec réserve : rang calculé ; 2025 incomplet (Belgique) |
| Industrie | 47,7 / 49,8 | phrase de l'Insee relue ; Eurostat B à E : 47,7 / 49,8 | page de l'Insee | Conforme : autre champ que 44,3 € |
| Coûts non salariaux | 32,3 % (UE 24,8) | phrase relue | actualité du 31/03/2026 | Conforme, avec réserve : Belgique non publiée |
| Coût salarial unitaire | 128,133 / 152,924 (2025) | NULC_PER base 2010, « p » | `nama_10_lp_ulc` (05/11/2026) | Conforme, avec réserve : provisoire ; lecture de l'indice |
| Constat du CNP | compétitivité-prix regagnée | phrases relues (page « compétitivité-prix ») | rapport du CNP | Conforme |

**Conclusion.** Aucun chiffre du fichier n'est faux ; le rang est calculé sur la dernière année complète, et le coût de l'industrie n'est jamais rapproché de celui de l'ensemble de l'économie.

**Pages consultées** le 09/11/2026 : les documents et API des URL ci-dessus.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Pas de script : la double vérification a rouvert l'API d'Eurostat, la page de l'Insee et le rapport du CNP.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Eurostat : réutilisation permise, commerciale comprise, mention « Source : Eurostat » et modifications signalées (https://ec.europa.eu/eurostat/help/copyright-notice) ;
  - Insee : Licence Ouverte 2.0, mention « Source : Insee » et date de dernière mise à jour (https://www.insee.fr/fr/information/2008466) ;
  - citation seule : Conseil national de productivité (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
