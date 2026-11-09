# `justiceStaffEurope` · Juges et policiers en Europe (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web des chiffres de la CEPEJ, un écart de la recherche corrigé (médiane des procureurs de l'UE : 11,4, et non 14,5) ; policiers d'Eurostat relus dans l'API par le coordinateur ; réserves de lecture reprises ci-dessous. La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `justiceStaffEurope`, dossier « Sécurité et justice » (`security`), page de type comparaison, recherche « Ce qu'on entend » du 09/11/2026 |
| Données | `briefings/manual/justiceStaffEurope.json`, saisi à la main le 2026-11-09 depuis l'étude de la CEPEJ pour la Commission européenne (partie 1, tableaux 7.1.1, 7.1.2a, 7.3.1 et 7.3.1a) et l'API d'Eurostat (`crim_just_job`) |
| Sources | 1. CEPEJ, « Study on the functioning of judicial systems in the EU Member States – Facts and figures from the CEPEJ questionnaires 2014 to 2024 », CEPEJ(2025)21rev, partie 1 « Data tables per indicator for all EU Member States », https://commission.europa.eu/document/download/fcd0d760-68af-49dd-a914-cbcfac5e68cf_en?filename=Part%201%20-%20Data%20tables%20per%20indicator%20for%20all%20EU%20Member%20States.pdf (30/01/2026, date imprimée ; mise en ligne par la Commission le 04/06/2026 selon la recherche), citation seule, en anglais. 2. Commission européenne, « The 2026 EU Justice Scoreboard », https://commission.europa.eu/document/download/d1367f58-9eed-4ebd-8eb3-68646b7c7ddc_en?filename=2026_eu_justice_scoreboard.pdf, données https://commission.europa.eu/document/download/926bcd02-9354-4517-889a-557aae16b189_en?filename=2026_EUJS_quantitative.zip (04/06/2026, date du fichier de données lue par la recherche), citation seule, en anglais. 3. Eurostat, « Personnel in the criminal justice system by sex », jeu `crim_just_job`, https://ec.europa.eu/eurostat/databrowser/view/crim_just_job/default/table?lang=fr (et `lang=en`), API https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/crim_just_job?lang=EN&isco08=OC5412&sex=T&unit=P_HTHAB (mise à jour du jeu : 29/04/2026), conditions d'Eurostat |
| Séries | `franceJudges` : juges professionnels pour 100 000 habitants en France (juges judiciaires et administratifs), CEPEJ, tableau 7.1.2a, unité `ratio`, 2014 à 2024, 11 points (10,5 ; 10,5 ; 10,4 ; 10,5 ; 10,9 ; 11,1 ; 11,2 ; 11,2 ; 11,3 ; 11,1 ; 11,6) |
| Valeurs par catégorie | `judges` : juges professionnels pour 100 000 habitants des 27 États membres, 2024, CEPEJ, tableau 7.1.2a, une décimale, dans l'ordre décroissant du tableau (Grèce 44,4 ; Croatie 42,2 ; Slovénie 39,4 ; Luxembourg 36,4 ; Bulgarie 35,4 ; Autriche 29,0 ; Pologne 28,3 ; Tchéquie 27,9 ; Hongrie 27,8 ; Lettonie 27,6 ; Slovaquie 26,3 ; Allemagne 24,9 ; Lituanie 24,7 ; Roumanie 23,4 ; Finlande 21,5 ; Portugal 19,4 ; Estonie 18,1 ; Chypre 16,6 ; Pays-Bas 15,2 ; Belgique 14,9 ; Suède 12,2 ; Italie 12,2 ; France 11,6 ; Espagne 11,1 ; Malte 9,4 ; Danemark 6,7 ; Irlande 3,6). `police` : policiers pour 100 000 habitants de 26 États membres (l'Italie n'a pas de valeur), 2022, Eurostat, `isco08=OC5412`, `sex=T`, `unit=P_HTHAB`, deux décimales comme Eurostat, dans l'ordre décroissant (Chypre 540,78 ; Croatie 536,29 ; Grèce 533,99 ; Portugal 452,78 ; Bulgarie 444,27 ; Malte 407,75 ; Tchéquie 381,09 ; Espagne 379,84 ; Hongrie 378,12 ; Slovaquie 377,74 ; Luxembourg 366,6 ; France 361,25 ; Autriche 356,03 ; Slovénie 347,81 ; Irlande 342,51 ; Belgique 338,29 ; Allemagne 311,06 ; Pays-Bas 291,19 ; Estonie 289,16 ; Pologne 273,74 ; Lituanie 268,64 ; Roumanie 262,61 ; Lettonie 224,18 ; Suède 210,3 ; Danemark 193,48 ; Finlande 137,49) |
| Chiffre clé | 11,6 juges professionnels pour 100 000 habitants en France en 2024, tendance à la hausse (11,1 en 2023) |
| Règles | Saisie à la main. Unité `ratio` pour les taux pour 100 000 habitants, comme `criminalJustice` ; la page écrit les taux de la CEPEJ au dixième, comme elle (`digits` de la présentation), et ceux d'Eurostat au centième. Les deux classements (variante `ranking`) numérotent les pays dans l'ordre décroissant des valeurs : des rangs calculés, qu'aucune source ne publie, dits « calculés » dans la note de chaque bloc. Suède et Italie, ex aequo à 12,2, gardent l'ordre du tableau. La moyenne et la médiane de l'UE ne sont pas des catégories, qui fausseraient la numérotation : la médiane des juges (23,4) est dans la note du bloc. Les juges sont ceux de la CEPEJ, dont les définitions sont communes, pas ceux d'Eurostat (autres champs selon les pays) ; les procureurs, les juges non professionnels et les juges d'Eurostat ne sont que dans « À savoir ». Le taux de policiers ne compte que l'année 2022 : la dernière de la France, et aucune année plus récente d'un autre pays n'est saisie |
| Première édition | À remplir à la publication |

## « À savoir »

1. Le chiffre de la France ne compte ni ses 2 225 procureurs (3,2 pour 100 000 habitants, médiane de l'UE 11,4), ni ses 22 836 juges non professionnels, ni ses 445 juges professionnels siégeant à titre occasionnel (2024). Source : CEPEJ, partie 1, tableau 7.1.1 (« France 7 968 445 NA No 22 836 NA »), tableaux 7.3.1 (2 225) et 7.3.1a (« France 3,2 ; Average 11,4 ; Median 11,4 ») et résumé (« an average and median of 11,4 prosecutors per 100 000 inhabitants »). La fiche France de la partie 2 écrit « Prosecutors 2 225 3,2 14,5 » : le 14,5 est la médiane du personnel non procureur (tableau 7.4.3), relevé par la contre-vérification ; la note suit le tableau 7.3.1a.
2. Les rangs sont calculés à partir de l'ordre des tableaux ; aucune source ne publie de classement ; Suède et Italie à égalité. Source : tableau de bord 2026, figure 36 (« Number of judges, 2014, 2022 – 2024 (*) (per 100 000 inhabitants) (source: CEPEJ study) », ordre des barres « EL HR SI LU BG AT PL CZ HU LV SK DE LT RO FI PT EE CY NL BE SE IT FR ES MT DK IE ») et note (« It does not present an overall single ranking. ») ; égalité : 12,22 (Suède) et 12,20 (Italie) dans le fichier du tableau de bord, 12,2 et 12,2 dans l'étude ; policiers : valeurs de 2022 de l'API d'Eurostat triées.
3. Pour la France, la police municipale est comprise ; 2022 est la dernière année de la France ; pas de valeur de l'Italie en 2022. Source : Eurostat, métadonnées « Crime and criminal justice (crim) », 15.1, https://ec.europa.eu/eurostat/cache/metadata/en/crim_sims.htm (« FR: Local police is included. ») ; API (France : dernière année 2022 ; Italie : dernière année 2020). La gendarmerie n'y est ni incluse ni exclue par écrit : la note n'en dit rien.
4. Eurostat compte 7 654 juges professionnels en France en 2024 (11,15 pour 100 000 habitants), la CEPEJ 7 968. Source : API d'Eurostat, `isco08=OC2612A` (chiffres de la page `criminalJustice`, vérifiés avec elle) ; CEPEJ, tableau 7.1.1 et fiche France (« the total number of professional judges sitting in courts (all instances) in France is 7 968 », soit 6 530 juges judiciaires et 1 438 juges administratifs). La recherche écarte les juges d'Eurostat pour comparer les pays : champs différents selon les pays.

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

L'affirmation est dans `briefings/notes/justiceStaffEurope.json` (clé `claims`, français et anglais). Source de chaque chiffre de la réponse :

1. « On entend que la France a moins de policiers que ses voisins européens. » 361,25 (France), 311,06 (Allemagne), 338,29 (Belgique), 366,6 (Luxembourg), 379,84 (Espagne) policiers pour 100 000 habitants en 2022 : Eurostat, API `crim_just_job` (`OC5412`, `P_HTHAB`), relue par le coordinateur le 09/11/2026. 12e sur 26 : rang calculé sur les 26 États membres qui ont une valeur en 2022. « Police municipale comprise » : métadonnées d'Eurostat (« FR: Local police is included. »). « Les définitions nationales diffèrent » : la recherche relève les précautions qu'Eurostat écrit pour d'autres pays (Belgique, Allemagne, Estonie, Irlande, Lettonie).

Aucune affirmation sur les juges : la recherche en proposait deux (« plus de juges », « plus de procureurs » que les voisins), formulées pour être démenties, mais ce qu'on entend dans le débat est le manque de juges, que les chiffres confirment ; ils sont montrés, pas « démentis » (consigne du 09/11/2026, d'après la règle du PO).

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-isf-juges.md` : documents retéléchargés (`curl`), PDF lus avec `pdftotext`, fichier du tableau de bord avec openpyxl. Les policiers d'Eurostat ne sont pas dans ce rapport : relus par le coordinateur dans l'API d'Eurostat le 09/11/2026.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Juges 2024, 27 pays (et chiffre clé) | Grèce 44,4 … France 11,6 … Irlande 3,6 | les 27 valeurs identiques au PDF (tableau 7.1.2a, comparaison par script) et au XLSX du tableau de bord (France 11,614…) | partie 1 et fichier du tableau de bord (URL ci-dessus) | Conforme, avec réserve : champs différents selon les pays ; Grèce + 15,2 % en un an ; Suède et Italie ex aequo |
| France, 2014 à 2024 | 10,5 … 11,1 ; 11,6 | ligne « France » du tableau 7.1.2a : « 10,5 10,5 10,4 10,5 10,9 11,1 11,2 11,2 11,3 11,1 11,6 » | partie 1 | Conforme |
| Nombre de juges, France | 7 968 (« À savoir » 4) | tableau 7.1.1 ; fiche France : 6 530 + 1 438 | partie 1 ; partie 2, https://commission.europa.eu/document/download/7c78ce9e-4504-49a3-9610-e5ccd0c55ef2_en?filename=Part%202%20-%20Country%20fiches%20for%20each%20EU%20Member%20States.pdf | Conforme |
| Médiane de l'UE, juges | 23,4 (note du bloc) | moyenne 22,6 et médiane 23,4, recalculées sur les 27 valeurs ; le résumé écrit « average » pour des médianes (21,5 → 23,4) | partie 1 | Conforme |
| Procureurs | 2 225 ; 3,2 ; médiane 11,4 | tableaux 7.3.1 et 7.3.1a ; la fiche France écrit 14,5 | partie 1 et partie 2 | Écart corrigé : 11,4 |
| Juges non professionnels et occasionnels | 22 836 ; 445 | tableau 7.1.1 | partie 1 | Conforme |
| Précautions de la CEPEJ et de la Commission | « dépend beaucoup de l'organisation de la justice », « pas de classement unique » | « This number depends considerably on the organisation of the judicial system and the existence of occasional judges, non-professional judges or even Rechtspfleger. » ; « It does not present an overall single ranking. » | partie 1 (résumé) ; tableau de bord, figure 36 | Conforme, mot pour mot |
| Rang de la France, juges | 23e sur 27 (numéro du classement) | déduit de l'ordre du tableau et des barres de la figure 36, publié nulle part | tableau de bord (URL ci-dessus) | Conforme, avec réserve : calculé |
| Policiers 2022, 26 pays | Chypre 540,78 … France 361,25 … Finlande 137,49 | cellules `OC5412 · T · P_HTHAB · <pays> · 2022` ; Italie sans valeur en 2022 | API d'Eurostat (URL ci-dessus) | Conforme (relecture du coordinateur, sans contre-vérification séparée) |

**Conclusion.** Aucun chiffre du fichier n'est faux. Les rangs sont calculés et dits tels ; la médiane des procureurs suit le tableau 7.3.1a, pas la fiche France.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus. CEPEJ-STAT et la fiche France du Conseil de l'Europe (https://www.coe.int/en/web/cepej/cepej-stat, https://rm.coe.int/france-country-fiche/48802c1521) n'ont pas pu être ouverts (403).

## Réserves

- L'étude ne dit pas si les juges sont comptés en personnes ou en équivalents temps plein ; le tableau de bord écrit « judges working full-time, according to the CEPEJ methodology ».
- La Commission « does not guarantee the accuracy of the data included in this study ». Aucune licence n'est écrite dans l'étude : citation seule.
- Les dates de mise en ligne (étude et tableau de bord, 04/06/2026) viennent de la recherche et n'ont pas été vérifiées par la contre-vérification ; seule la date imprimée de l'étude (30/01/2026) l'a été.
- Eurostat ne marque aucune rupture dans la série française des policiers, mais la recherche relève des sauts (+ 15 % en 2013, + 11 % en 2019) : la page ne montre que 2022.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la contre-vérification a rouvert l'étude et le fichier du tableau de bord ; les policiers ont été relus dans l'API d'Eurostat.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée : le registre dit « citation seule » pour l'étude et le tableau de bord (la recherche lit « CC BY 4.0 » pour le tableau de bord), et les conditions d'Eurostat pour son jeu.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
