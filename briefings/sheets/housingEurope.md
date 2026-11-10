# `housingEurope` · Le logement en Europe (saisi à la main)

**Vérifiée le 10/11/2026** : double vérification sur le web, aucun écart de valeur ; toutes les valeurs d'Eurostat retéléchargées et comparées une à une, les rangs refaits sur les 27 pays (26 pour les prix). Réserves reprises ci-dessous (personnes et non ménages, définition de la surcharge non relue, ruptures). La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `housingEurope`, dossier « Pouvoir d'achat et logement » (`purchasingPower`), volet « En Europe » de la page composite `housing` (voir `housing.md`), page de type comparaison, recherche du 09/11/2026 |
| Données | `briefings/manual/housingEurope.json`, saisi à la main le 2026-11-10 depuis l'API d'Eurostat |
| Sources | 1. Eurostat, « Distribution de la population par statut d'occupation du logement, par type de ménage et par groupe de revenu » (`ilc_lvho02`, tenure=OWN, hhcomp=TOTAL, rskpovth=TOTAL), https://ec.europa.eu/eurostat/databrowser/view/ilc_lvho02/default/table?lang=fr. 2. Eurostat, « Taux de surcharge des coûts du logement par âge, sexe et statut de pauvreté » (`ilc_lvho07a`, age=TOTAL, sex=T), https://ec.europa.eu/eurostat/databrowser/view/ilc_lvho07a/default/table?lang=fr. 3. Eurostat, « Taux de surpeuplement par âge, sexe et statut de pauvreté - population totale » (`ilc_lvho05a`), https://ec.europa.eu/eurostat/databrowser/view/ilc_lvho05a/default/table?lang=fr. 4. Eurostat, « Indice de prix des logements - données annuelles » (`prc_hpi_a`, purchase=TOTAL, unit=RCH_A_AVG), https://ec.europa.eu/eurostat/databrowser/view/prc_hpi_a/default/table?lang=fr. Titres tels que l'API les donne en français ; pages anglaises `?lang=en` ; licence Eurostat (« Source : Eurostat ») |
| Dates de publication | 2026-10-20 (`ilc_lvho02`, `ilc_lvho05a`) ; 2026-10-29 (`ilc_lvho07a`) ; 2026-10-01 (`prc_hpi_a`) : dates de mise à jour des jeux de données |
| Séries | France et UE à 27, 2015 à 2025 : `ownersFrance`/`ownersEu` (61,4 et 68,5 en 2025), `overcostFrance` (sans 2021)/`overcostEu`, `overcrowdingFrance`/`overcrowdingEu` ; 2010 à 2025 : `priceChangeFrance`/`priceChangeEu` (variation annuelle moyenne). Ruptures de la France en 2020 et 2022 (`breaks`) pour les trois indicateurs de l'enquête SRCV ; valeurs de l'UE de 2015 à 2018 estimées (« e »), dit dans une note |
| Ventilations | `owners`, `overcost`, `overcrowding`, `housePrices` (2025) : France, UE à 27 (hachurée), Allemagne, Espagne, Italie. Propriétaires 61,4 / 68,5 / 47,2 / 73,6 / 77,1 ; surcharge 6,4 / 7,6 / 11,2 / 7,2 / 5,0 ; surpeuplement 10,8 / 16,8 / 11,7 / 9,5 / 24,3 ; prix +0,7 / +5,5 / +3,2 / +12,7 / +4,0 |
| Chiffre clé | 61,4 % de la population vit en 2025 dans un logement dont son ménage est propriétaire, en France, en hausse (61,2 % en 2024) ; à côté, l'UE à 27 (68,5 %) |
| Règles | Saisie à la main. Quatre vues, une par indicateur : barres de 2025 pour les cinq territoires, la France et l'UE au tableau. Les 27 valeurs ne sont pas dans le rapport final : pas de classement des 27, les rangs de la France sont dans les notes des blocs et un « À savoir », « calculés ». Décimales fixées au dixième (`digits`), comme Eurostat les écrit (5,0 pour l'Italie). Non saisis : l'indice des prix base 2015 (la variation annuelle suffit), les autres pays |
| Première édition | À remplir à la publication |

## « À savoir »

1. Eurostat compte des personnes (61,4 % en 2025), l'Insee des ménages (57,3 % en 2026) : ne se comparent pas. Source : `ilc_lvho02` (cellule FR 2025) ; Insee Focus n° 388 (volet `housingStock`).
2. Rangs de la France en 2025 sur les 27 (calculés) : 24e pour les propriétaires, 12e pour la surcharge, 17e pour le surpeuplement. Source : classements refaits par la contre-vérification (propriétaires : SK 93,8 en tête, FR 24e devant DK, AT, DE ; surcharge : EL 26,4 en tête, FR 12e après NL 6,5 ; surpeuplement : RO 40,4 en tête, DE 16e, FR 17e, ES 20e), sans ex æquo touchant la France.
3. Prix +0,7 % en France en 2025, +5,5 % dans l'UE ; 25e hausse sur 26 (Grèce absente, rang calculé) ; indice d'Eurostat, pas Notaires-Insee. Source : `prc_hpi_a` (RCH_A_AVG) ; classement refait (HU 18,3 provisoire en tête, SE 1,0 24e, FR 25e, FI −2,3 26e).
4. Ruptures de la France en 2020 et 2022 ; pas de surcharge française en 2021 ; surpeuplement selon la norme d'Eurostat ; UE 2015-2018 estimée. Source : drapeaux « b » et « e » de l'API.

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Aucune affirmation dans ce volet : celle sur les propriétaires (« les Français sont presque tous propriétaires ») est dans le volet `housingStock`, qui cite aussi la source `ilc_lvho02`.

## Double vérification

Faite le 10/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-logement.md` : API d'Eurostat rouverte, classements refaits par programme.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 61,4 % (France, 2025) | `ilc_lvho02` FR 2025 61.4 | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/ilc_lvho02?lang=fr&sinceTimePeriod=2015&rskpovth=TOTAL&hhcomp=TOTAL&tenure=OWN&unit=PC | Conforme |
| Séries 2015-2025 | 8 séries | Toutes les valeurs comparées une à une (aucun écart) | API d'Eurostat | Conforme |
| Surcharge | 6,4 ; 12e | FR 6,4 ; rang refait | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/ilc_lvho07a?lang=fr&sinceTimePeriod=2015&age=TOTAL&sex=T&rskpovth=TOTAL&unit=PC | Conforme, avec réserve : définition non relue (métadonnées introuvables) |
| Surpeuplement | 10,8 ; 17e | FR 10,8 ; rang refait | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/ilc_lvho05a?lang=fr&sinceTimePeriod=2015&age=TOTAL&sex=T&rskpovth=TOTAL&unit=PC | Conforme (rang calculé) |
| Prix | +0,7 ; 25e sur 26 | FR 0,7 ; Grèce absente | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/prc_hpi_a?lang=fr&sinceTimePeriod=2010&purchase=TOTAL&unit=RCH_A_AVG | Conforme (rang calculé) |

**Conclusion.** Aucun chiffre du fichier n'est faux ; chaque rang est calculé et dit tel.

**Pages consultées** le 10/11/2026 : les API des URL ci-dessus.

## Réserves

- Le taux de propriétaires d'Eurostat porte sur des personnes, celui de l'Insee sur des ménages.
- La définition du taux de surcharge des coûts du logement n'a pas pu être relue (page de métadonnées en 404) : la page n'en donne pas d'autre que « selon la définition d'Eurostat », et ne le rapproche pas du taux d'effort de l'Insee.
- Le surpeuplement d'Eurostat n'est pas celui de l'Insee (9,0 % des ménages début 2024, non saisi).

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert l'API d'Eurostat.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée : licence Eurostat (« Source : Eurostat »).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
