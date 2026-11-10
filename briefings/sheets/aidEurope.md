# `aidEurope` · Les aides aux entreprises en Europe (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart de valeur ; réserves de lecture reprises ci-dessous (définitions de la Commission et de la comptabilité nationale, qui ne couvrent ni l'une ni l'autre l'ensemble des aides). La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `aidEurope`, dossier « Économie et fiscalité » (`economy`), volet « En Europe » de la page composite `businessAid` (voir `businessAid.md`), page de type comparaison, recherche du 09/11/2026 |
| Données | `briefings/manual/aidEurope.json`, saisi à la main le 2026-11-09 depuis la note du State aid Scoreboard 2025 et l'API d'Eurostat (base `gov_10a_main`, opération D3PAY, administrations publiques S13, en % du PIB, lue le 09/11/2026) |
| Sources | 1. Commission européenne (DG Concurrence), « State aid Scoreboard 2025 », note, https://competition-policy.ec.europa.eu/document/download/cc9cdf4e-97e9-4f8e-ac7d-5f094a9fd12d_en?filename=state_aid_scoreboard_note_2025.pdf, en anglais, licence « citation seule » (la Commission n'est pas Eurostat). 2. Eurostat, « Government revenue, expenditure and main aggregates » (`gov_10a_main`), https://ec.europa.eu/eurostat/databrowser/view/gov_10a_main/default/table?lang=fr, API https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/gov_10a_main?format=JSON&lang=EN&na_item=D3PAY&sector=S13&unit=MIO_EUR&unit=PC_GDP&geo=FR&geo=DE&geo=EU27_2020&sinceTimePeriod=2010, page anglaise ?lang=en, licence Eurostat (« Source : Eurostat »). 3. Assemblée nationale, « Rapport relatif aux aides publiques aux entreprises, annexe au projet de loi de finances pour 2027 » (voir `aidAmounts.md`), pour sa phrase sur la comparaison internationale |
| Dates de publication | 2026-01-15 (Scoreboard : publié le 15/01/2026, PDF du 12/01 ; la recherche donnait le 12/01) ; 2026-10-21 (mise à jour de la base d'Eurostat) ; 2026-10-12 (rapport du Gouvernement, date du PDF) |
| Séries | `stateAidFrance` : aides d'État en % du PIB, 2023 et 2024 (1,35 ; 1,17). `stateAidGermany` : 2023 et 2024 (1,26 ; 0,96). `stateAidEu` : Union à 27, 2024 (0,94) ; 2023 n'est pas dans les chiffres vérifiés. `subsidiesFrance`, `subsidiesGermany`, `subsidiesEu` : subventions versées par les administrations publiques (D3) en % du PIB, 2010 à 2025, 16 points chacune, au dixième comme Eurostat (France 1,7 en 2010, 3,1 en 2021, 1,9 en 2025 ; Allemagne 1,3, 2,9, 1,2 ; Union 1,5, 2,6, 1,4) |
| Ventilations | `stateAidAmount` : aides d'État 2024 en Md€, France 34,18, Allemagne 41,37 |
| Chiffre clé | 1,17 % du PIB d'aides d'État en France en 2024, au centième comme la Commission (`digits` 2), en baisse (1,35 % en 2023) ; à côté, l'Allemagne, 0,96 % |
| Règles | Saisie à la main. Deux vues : « Aides d'État » (France, Allemagne et Union en % du PIB, l'Union hachurée, puis France et Allemagne en Md€) et « Subventions » (un groupe par année, de 2025 à 2010, l'Union hachurée ; le tableau avec les seize années). La note du bloc en % du PIB recopie la phrase de la Commission sur les mesures générales. Non saisis : les subventions en M€ (France 2010 à 2025, Allemagne 2023 à 2025), le total de l'Union (168,23 Md€), les parts de la France et de l'Allemagne dans ce total (20 % et environ 25 %, dans la note du bloc), l'écart de 7,19 Md€ (calculé), les aides d'État par objectif (non lisibles), D31 et D39 (la valeur de D31 de 2022 est dans une note), D92, le compte des administrations publiques de l'Insee |
| Première édition | À remplir à la publication |

## « À savoir »

1. Les aides d'État de la Commission mesurent l'avantage procuré à l'entreprise (l'élément d'aide), pas le montant versé. Elles comprennent l'agriculture et la pêche, mais ni les aides de minimis, ni l'essentiel des aides aux chemins de fer et aux services d'intérêt économique général ; le secteur financier est à part. Source : Scoreboard 2025, méthodologie (« The aid element does not represent the nominal amount granted by the public authority, but measures the economic advantage passed on to the undertaking » ; « including agriculture, fisheries, and aquaculture » ; « the data presented in the Scoreboard exclude funding granted under the de minimis rules » ; « exclude most of the aid to railways, services of general economic interest, and schemes approved under the Temporary Union Framework » ; « Aid to railways and aid to the financial sector are covered separately in Annex II and III »).
2. En euros, l'Allemagne verse plus d'aides d'État que la France en 2024 ; en part du PIB, c'est la France. Hors aides de crise, la France est à 1,11 % du PIB, deuxième de l'Union après la Belgique (1,14 %). Les aides fiscales font environ 39 % des aides d'État françaises. Source : Scoreboard 2025 (« Excluding crisis-related measures. the largest spender in relative terms in 2024 is Belgium, with a total State aid expenditure for EU priorities corresponding 1.14 of its 2024 GDP, followed by France, with 1.11%. » ; « Tax advantages represented around 39% of the State aid expenditure in France ») ; 34,18 contre 41,37 Md€, 1,17 contre 0,96 % du PIB (bloc du volet).
3. Les subventions de la comptabilité nationale (D3) ne comptent ni les dépenses fiscales (crédit d'impôt recherche, TVA réduite) ni les exonérations de cotisations, mais des subventions à des entreprises publiques et les boucliers tarifaires de 2021 à 2023 : en France, 35 345 M€ de subventions sur les produits en 2022. Source : Eurostat, `gov_10a_main` (D31PAY France 2022 : 35 345 M€, lu par la recherche) ; précaution de la recherche vérifiée. Les variations de 2013 et de 2019 coïncident avec l'entrée et la transformation du CICE, mais la source ouverte ne l'établit pas : la page ne l'affirme pas.
4. Le rapport du Gouvernement prévient que ses périmètres « ne se prêtent pas à la comparaison internationale : ils reposent sur les normes comptables du budget de l'État et sur une norme fiscale de référence propre à la France ». Source : rapport annexé au projet de loi de finances pour 2027, encadré de la partie 1 (« Les périmètres d'aides de ce rapport ne se prêtent pas à la comparaison internationale : ils reposent sur les normes comptables du budget de l'État et sur une norme fiscale de référence propre à la France. »).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Aucune affirmation : voir `businessAid.md`. « La France aide moins ses entreprises que l'Allemagne » est écartée : vraie en euros pour les aides d'État 2024 (34,18 contre 41,37 Md€), fausse en part du PIB (1,17 contre 0,96 %) et fausse en euros pour les subventions de la comptabilité nationale de 2025 (56,5 contre 52,1 Md€).

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-aides.md` : note du Scoreboard retéléchargée et lue avec `pdftotext`, API d'Eurostat rouverte.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, France 2024 | 1,17 % du PIB | « Smaller reductions are observed in France, that saw its spending decrease by 0.18 percentage points, from 1.35% to 1.17%. » | Scoreboard 2025 (URL ci-dessus) | Conforme |
| Allemagne | 0,96 % ; 1,26 % en 2023 ; 41,37 Md€ | « Germany with EUR 41.37 billion, representing around 25% of the total State aid expenditure in the EU27 » | idem | Conforme |
| France en euros | 34,18 Md€ | « France was the second largest spender, with EUR 34.18 billion (20%) » | idem | Conforme |
| Union à 27 | 0,94 % | « In 2024, EU27 Member States spent EUR 168.23 billion, corresponding to 0.94% of their 2024 GDP » | idem | Conforme |
| Mesures générales exclues | note du bloc | « General measures that do not favour certain enterprises or sectors, and public subsidies that do not affect trade or distort competition, are not covered by the Scoreboard […] » | idem, partie 1.2 | Conforme |
| Subventions D3, 2010 à 2025 | 3 × 16 valeurs | API rouverte (mise à jour du 21/10/2026) : les seize années de la France, de l'Allemagne et de l'Union, en M€ et en % du PIB, identiques au rapport de recherche | Eurostat (URL ci-dessus) | Conforme |

**Conclusion.** Aucun chiffre du fichier n'est faux ; ni les aides d'État ni les subventions ne sont présentées comme le total des aides aux entreprises.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus.

## Réserves

- Les aides d'État excluent les mesures générales : ni les allègements généraux de cotisations ni le crédit d'impôt recherche n'y figurent, dans les deux pays.
- Les subventions D3 comptent les seules subventions de la comptabilité nationale, dont des subventions à des entreprises publiques et les boucliers tarifaires ; elles ne sont pas le total des aides aux entreprises.
- Les périmètres du rapport du Gouvernement ne se comparent pas à ceux de l'Europe (sa propre phrase, note 4).
- Les comptes nationaux de 2025 peuvent encore être révisés ; Eurostat ne marque aucune des valeurs lues comme provisoire.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert la note et l'API.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée : « citation seule » pour la Commission, Eurostat pour la base `gov_10a_main`, `etalab-1.0` pour le rapport annexé au projet de loi.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
