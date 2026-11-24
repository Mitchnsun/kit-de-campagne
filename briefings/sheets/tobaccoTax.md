# `tobaccoTax` · Les recettes du tabac (saisie à la main)

**Vérifiée le 24/11/2026** : chaque valeur lue dans un rapport à la Commission des comptes de la Sécurité sociale ouvert en entier, puis relue par un second agent dans chacun des 15 rapports (`research/tobacco-2026-11/verify-sonnet-2.md` dans le dépôt de l'app).

| Champ | Valeur |
| --- | --- |
| Indicateur | `tobaccoTax`, dossier « Économie » (`economy`), aussi dans « Santé » (`health`), page de type série, demande du PO du 24/11/2026 |
| Données | `briefings/manual/tobaccoTax.json`, saisi à la main le 2026-11-24 |
| Sources | 1. CCSS, « Les comptes de la Sécurité sociale », octobre 2026 (PDF du 05/10/2026), encadré 2 p. 63 et tableau 3 p. 65 : 2024, 2025, prévisions 2026 et 2027. 2. Les rapports à la CCSS de 2012 à 2025 (page d'index), chacun pour l'année exécutée qu'il donne : octobre 2012, p. 70 (2010, 2011) ; septembre 2013, p. 107 (2012) ; septembre 2014, p. 57 (2013) ; septembre 2015, p. 63 (2014) ; septembre 2016, p. 59 (2015) ; septembre 2017, p. 59 (2016) ; septembre 2018, p. 51 (2017) ; septembre 2019, p. 59 (2018) ; septembre 2020, p. 57 (2019) ; septembre 2021, p. 57 (2020) ; septembre 2022, p. 57 (2021) ; septembre 2023, p. 59 (2022) ; octobre 2024, p. 48 (2023). Leur date dans le fichier de données est celle du dernier rapport, faute d'une date par rapport. 3. OFDT, « Le coût social des drogues : estimation en France en 2019 » (01/07/2023), p. 1, 9 et 10. 4. Douanes, synthèse de l'étude TAFE (24/09/2025) |
| Série | `excise` : droits de consommation sur les tabacs, en milliards d'euros courants, sans la TVA ni les droits de licence ; 2010-2017 le rendement total des encadrés (tous affectataires), 2018-2025 les tableaux (l'Assurance maladie, seule affectataire depuis 2017) ; 2026 et 2027 en prévision (`projection`, « prévision » sur la page) |
| Chiffre clé | 12,687 Md€ en 2025 (tableau 3), en baisse (12,744 en 2024) |
| Règles | Les valeurs en droits constatés des tableaux quand le rapport en donne, sinon celle du texte (2013 à 2017, arrondies au dixième ou au centième) |
| Première édition | À remplir à la publication |

Valeurs écartées : la TVA sur le tabac (une seule année isolée, 2013) ; les 14 Md€ de « rendement » de l'accise tabac du Bilan de la douane 2025, un autre périmètre ; les 122 Md€ de coût social de la note de 2015 (données de 2010), remplacés par l'estimation de 2019.

## « À savoir »

1. L'affectation : CCSS septembre 2018, p. 52 (« Elle est devenue l'unique affectataire des taxes tabacs ») ; la TVA d'un paquet : OFDT, note de bilan 2026, p. 10 (2,17 €).
2. Le pic de 2020 : CCSS septembre 2021, p. 57.
3. Les prévisions et les droits de licence : CCSS octobre 2026, p. 63 (11,4 et 10,7 Md€ ; 12,6 Md€ net ; 0,3 Md€).
4. Le coût social : OFDT 2023, p. 1 et p. 10 (156 Md€, 73 189 vies, 16,5 Md€ de soins, 13 Md€ de taxes ; le tableau 3 p. 9 donne 16 439 M€).

## « Ce qu'on entend »

1. Le tabac rapporterait plus qu'il ne coûte : OFDT 2023, p. 10 (13 et 16,5 Md€, 1,7 Md€ de déficit, la phrase « infondée »).
2. La contrebande coûterait des milliards : synthèse TAFE (4,3 Md€, de 2,8 à 5,8 Md€ ; « bien loin des scénarios alarmistes ») ; KPMG, résultats 2025, p. 96 (10 369 M€).

## Double vérification

Faite le 24/11/2026 par un agent Claude (modèle Sonnet) qui a rouvert les 15 rapports de la CCSS : les 18 valeurs 2010-2027, chacune à sa page, sont conformes, ainsi que les droits de licence (349 M€) et le fonds de lutte contre les addictions (64 puis 118 M€) ; Kopp 2019 conforme (le coût des soins écrit 16,5 Md€ dans le texte, 16 439 M€ au tableau). Écart non expliqué, sans effet sur la série : les annexes de la CCSS d'octobre 2026 (p. 169 et 173) donnent 13 100 et 13 036 M€ de « taxes tabacs » contre 13 163 et 13 060 p. 63.

## Mises à jour

Aucune. La CCSS de septembre ou d'octobre 2027 donnera l'exécuté 2026.

## Relecture

- [x] Le chiffre clé et chaque point de la série recoupés par un second agent.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée : aucune licence écrite dans les rapports de la CCSS ni sur l'OFDT, chiffres cités.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
