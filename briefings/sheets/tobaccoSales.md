# `tobaccoSales` · Les ventes de tabac (saisie à la main)

**Vérifiée le 24/11/2026** : chaque valeur lue dans un document du producteur ouvert en entier, puis relue valeur par valeur par un second agent (`research/tobacco-2026-11/verify-sonnet-2.md` dans le dépôt de l'app).

| Champ | Valeur |
| --- | --- |
| Indicateur | `tobaccoSales`, dossier « Santé » (`health`), aussi dans « Économie » (`economy`), page de type série, demande du PO du 24/11/2026 |
| Données | `briefings/manual/tobaccoSales.json`, saisi à la main le 2026-11-24 |
| Sources | 1. OFDT, « Tabagisme et arrêt du tabac en 2025 », Notes de bilan (27/05/2026), p. 2-3 et 9-11 : 2017 à 2025 en tonnes, les buralistes, la remise, le chiffre d'affaires. 2. OFDT, série « Ventes de tabac et de cigarettes - Evolution depuis 2000 » (04/06/2025), tableau du graphique : 2000 à 2016, en milliers de tonnes. 3. OFDT, série « Vente annuelle et prix annuel moyen du paquet […] de la marque la plus vendue » (04/06/2025) : les prix 2000-2024, 2025 dans la note de bilan, p. 10. 4. Douanes, Bilan de la douane 2025 (19/02/2026), p. 18-19 : 22 200 buralistes. 5. Assemblée nationale, réponse à la question écrite n° 92077 (JO du 15/02/2011, p. 1494) : 32 850 débits en 2002. 6. Douanes, synthèse de l'étude TAFE (24/09/2025). 7. KPMG pour Philip Morris Products SA, résultats 2025 (03/06/2026), p. 97 |
| Séries | `total` : tout tabac livré aux buralistes de France continentale, en tonnes (2000-2016 : milliers de tonnes à une décimale, × 1 000 ; 2017-2025 : tonnes exactes). `cigarettes` : en tonnes, une cigarette pour 1 g (2000-2024 : milliards d'unités à une décimale, × 1 000 ; 2025 : 23 326 t). `packPrice` : prix moyen annuel du paquet de 20 de la marque la plus vendue, en euros |
| Chiffre clé | 30 165 tonnes en 2025, en baisse (32 846 en 2024) |
| Règles | Les livraisons de Logista aux buralistes (source des douanes), pas les achats des fumeurs ; aucune valeur mensuelle (le fichier mensuel des douanes, depuis 2018, reste en réserve) |
| Première édition | À remplir à la publication |

Valeurs écartées : « 25 492 débits fin 2015 », dans le texte d'une question écrite sans réponse ; le prix « moyen » du paquet de la CCSS (12,54 € en 2025), une autre définition que la marque la plus vendue ; les 22 800 buralistes de l'OFDT (source non précisée), au profit des 22 200 des douanes.

## « À savoir »

1. Logista et le poids d'une cigarette : note de bilan 2026, p. 2 (note 2) et p. 19.
2. Les deux chutes après les hausses de prix : série « Ventes » (constat) ; bilan OFDT 2020 (mars 2021), p. 2 : « la baisse des ventes est ainsi de -15,6 % ».
3. Les buralistes : Bilan de la douane 2025, p. 18-19 ; QE 92077 ; note de bilan 2026, p. 9 (remise brute 10,29 % et 9,44 %).
4. Le chiffre d'affaires : note de bilan 2026, p. 9 (18,4 et 18,1 Md€).

## « Ce qu'on entend »

1. « Une cigarette sur deux » : KPMG p. 97 (26,54 / 49,54 = 53,6 % ; 6,02 / 49,54 = 12,2 % d'achats légaux à l'étranger ; calculs sur le tableau lu en image, la couche de texte du PDF contenant des chiffres d'une version antérieure) ; note de bilan 2026, p. 11 (10 à 20 %) ; synthèse TAFE (17,7 %, achats transfrontaliers).
2. La contrebande et les prix : bilan OFDT 2020, p. 2 ; synthèse TAFE (« la principale source de contournement fiscal » ; rue 366 t sur environ 45 700 t, moins de 1 %).
3. Les buralistes : QE 92077 ; Bilan de la douane 2025 ; note de bilan 2026, p. 9.

## Double vérification

Faite le 24/11/2026 par deux agents Claude (modèle Sonnet) : `verify-sonnet.md` (R2 et R4b : KPMG p. 97, TAFE, note de bilan 2026) et `verify-sonnet-2.md` (les 50 valeurs de la série 2000-2024, les 46 prix 2000-2024, 2025, les 9 tonnes exactes 2017-2025, 22 800, 10,29 / 9,44 %, 18,4 / 18,1 Md€, la QE 92077, le Bilan 2025) : conformes. Le texte du fichier des prix porte une coquille (« 23,90 € en 2022 » pour le tabac à rouler), le graphique dit 2024 : la page ne montre pas le tabac à rouler.

## Mises à jour

Aucune.

## Relecture

- [x] Le chiffre clé et chaque point de chaque série recoupés par un second agent.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée : etalab-2.0 pour les douanes, chiffres cités pour l'OFDT, l'Assemblée et KPMG.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
