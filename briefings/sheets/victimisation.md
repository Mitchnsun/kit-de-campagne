# `victimisation` · Subi ou enregistré ? (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; des réserves de lecture (enquête déclarative, révision possible, champ des 18 ans ou plus, rupture de source et définitions des homicides), reprises dans « À savoir », dans les notes des blocs et dans « Ce qu'on entend ». La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `victimisation`, dossier « Sécurité et justice » (`security`), page de type comparaison, recherche du 09/11/2026 |
| Données | `briefings/manual/victimisation.json`, saisi à la main le 2026-11-09 depuis la fiche « Insécurité, victimation » de France, portrait social (Insee, 18/11/2025), la présentation des bases de la délinquance enregistrée (SSMSI, 08/07/2026), la base des séries chronologiques du SSMSI (mise à jour du 14/10/2026) et la base `crim_off_cat` d'Eurostat (mise à jour du 29/04/2026) |
| Sources | 1. Insee, « Insécurité, victimation – France, portrait social », https://www.insee.fr/fr/statistiques/8612552, fichier https://www.insee.fr/fr/statistiques/fichier/8612552/FPORSOC25-F24.xlsx, Licence Ouverte 2.0, en français seulement (chiffres du SSMSI, enquête Vécu et ressenti en matière de sécurité). 2. SSMSI, « Présentation des bases communale, départementale et régionale de la délinquance enregistrée », https://static.data.gouv.fr/resources/bases-statistiques-communale-departementale-et-regionale-de-la-delinquance-enregistree-par-la-police-et-la-gendarmerie-nationales/20260709-120136/fichier-metadonnees-data-gouv-geographie-delinquance-juillet2026.pdf, Licence Ouverte 2.0, en français seulement. 3. SSMSI, « Base des séries chronologiques », https://www.data.gouv.fr/datasets/service-statistique-ministeriel-de-la-securite-interieure-base-des-series-chronologiques/ (page du jeu de données, déduite du chemin du fichier), fichier https://static.data.gouv.fr/resources/service-statistique-ministeriel-de-la-securite-interieure-base-des-series-chronologiques/20261014-150536/serieschrono-datagouv.csv (cette adresse datée renvoie 404 depuis la version du 10/11/2026 ; le registre donne l'adresse stable de data.gouv.fr, https://www.data.gouv.fr/datasets/r/631cff69-f0da-4890-b4fc-97aeada1476f, qui suit la dernière version, Mitchnsun/moi-president#357), Licence Ouverte 2.0, en français seulement. 4. Eurostat, « Police-recorded offences by offence category » (`crim_off_cat`), https://ec.europa.eu/eurostat/databrowser/view/crim_off_cat/default/table?lang=fr, API https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/crim_off_cat?geo=FR&iccs=ICCS0101&lang=EN, licence d'Eurostat |
| Séries | `physicalViolenceVictims` : victimes de violences physiques déclarées, nombre, 2023, 1 point (643 000 ; le chiffre clé). `domesticViolenceRecorded` : victimes de violences conjugales enregistrées, nombre, 2016 et 2022, 2 points (114 721 ; 244 301). `homicideRate` : homicides volontaires enregistrés pour 100 000 habitants selon Eurostat (`ICCS0101`, unité `P_HTHAB`), unité `ratio` de l'app, 2008, 2020, 2023 et 2024, 4 points (1,52 ; 1,03 ; 1,30 ; 1,28). `homicides` : victimes d'homicide enregistrées selon le SSMSI, nombre, 2008, 2016 et 2025, 3 points (1 140 ; 911 ; 975), rupture en 2016. `attemptedHomicides` : victimes de tentatives d'homicide enregistrées, nombre, 2016 et 2025, 2 points (2 259 ; 4 501) |
| Valeurs par catégorie | `victimsDeclared` (2023) : violences physiques 643 000, violences sexuelles physiques 325 000, cambriolage ou tentative 1 516 000 (personnes dont le ménage a été touché, résidence principale). `victimsShare` (2023) : 1,2 %, 0,6 %, 2,9 %. `insecurityWomen`, `insecurityMen`, `insecurityAll` (2024) : insécurité dans le quartier ou le village 25 / 19 / 22 %, au domicile 18 / 12 / 15 %, renoncement à sortir seul 31 / 10 / 21 %. `forcesSatisfaction` (2024) : action nationale 56 %, action de proximité 53 %. `complaintRate` (période « 2018 », moyenne 2011-2018) : violences sexuelles hors ménage 12 %, cambriolages 74 % |
| Chiffre clé | 643 000 victimes de violences physiques déclarées, période « 2023 » (enquête de 2024), sans tendance (un seul point) |
| Règles | Saisie à la main, rien n'est lu par script. Seules les valeurs du fichier vérifié du 09/11/2026 sont saisies : les séries d'Eurostat et du SSMSI ne gardent que les années qu'il cite, sans les années intermédiaires. Le taux d'Eurostat est publié par Eurostat (non calculé) ; l'app n'a pas d'unité « pour 100 000 », il est saisi en `ratio` (deux décimales, comme Eurostat les écrit) et le titre du bloc dit l'unité. Les taux de plainte sont une moyenne 2011-2018 : la période saisie est « 2018 » (dernière année de la moyenne), la note du bloc dit la moyenne. Le « doublement » des tentatives d'homicide n'est pas saisi : 4 501 / 2 259 = 1,99 est un calcul, la page et l'affirmation donnent les deux valeurs. Non saisis : la comparaison européenne de 2024 (comparabilité limitée selon Eurostat, taux français sans les coups mortels), l'ancienne enquête Cadre de vie et sécurité (série irrégulière, sans intervalle de confiance) |
| Première édition | À remplir à la publication |

## « À savoir »

1. L'enquête Vécu et ressenti en matière de sécurité est déclarative : elle compte ce que les personnes de 18 ans ou plus en logement ordinaire disent avoir subi, en métropole, en Martinique, en Guadeloupe et à La Réunion. Celle de 2024 compte les victimes de 2023 et le sentiment d'insécurité de 2024. Source : Insee, fichier `FPORSOC25-F24.xlsx` (champ des figures 1 à 3).
2. Le SSMSI aurait révisé sa synthèse de l'enquête de 2024 en décembre 2025, et l'enquête de 2025 est parue en octobre 2026 : ces pages n'ont pas pu être lues, des valeurs plus récentes peuvent exister. Les violences physiques ne comptent ni celles commises lors d'un vol, ni les violences sexuelles. Source : rapport de contre-vérification (pages de l'Intérieur bloquées, 403) ; définition : Insee, même fichier (« Elles ne prennent en compte ni les violences commises dans le cadre d'un vol, ni les violences sexuelles. »).
3. Les taux de plainte sont une moyenne des enquêtes Cadre de vie et sécurité de 2011 à 2018, en France métropolitaine ; cette enquête s'est arrêtée en 2021. Les violences conjugales sont des faits enregistrés, et leur série s'arrête en 2022 dans le fichier du SSMSI. Source : SSMSI, présentation des bases (« ...selon ces enquêtes en moyenne sur la période 2011-2018 seules 12 % des victimes de violences sexuelles hors ménage portent plainte, contre 74 % pour les victimes de cambriolages. ») ; base des séries chronologiques.
4. La série française d'Eurostat ne compte pas les coups et blessures suivis de mort, que le SSMSI compte : 882 homicides en 2024 pour Eurostat, 976 pour le SSMSI. La série du SSMSI change de source en 2016 : les chiffres d'avant et d'après ne se comparent pas sans réserve. Source : métadonnées d'Eurostat (« Not included 01031 which is serious assault leading to death ») ; base des séries chronologiques du SSMSI (état 4001 jusqu'en 2015, base des victimes depuis 2016).

Le « À savoir » lu d'abord (`readFirst`, dans les textes de l'app) cite la phrase du SSMSI : « la propension à déposer plainte a un impact sur le niveau de la délinquance enregistrée » (présentation des bases, juillet 2026). Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/victimisation.json` (clé `claims`, français et anglais), reprise des affirmations relues du fichier vérifié. Source de chaque chiffre de la réponse :

1. « On entend que les homicides explosent. » 1,52 (2008) et 1,28 (2024) pour 100 000 habitants : Eurostat, `crim_off_cat`. 2 259 (2016) et 4 501 (2025) victimes de tentatives d'homicide : SSMSI, base des séries chronologiques. Le rapport des deux valeurs (1,99) est un calcul : la réponse donne les deux valeurs, pas un « doublement ».
2. « On entend que les chiffres de la délinquance montent, donc qu'il y a plus de délinquance. » 12 % et 74 % : SSMSI, présentation des bases. 114 721 (2016) et 244 301 (2022) : SSMSI, base des séries chronologiques. 643 000 (2023) : Insee, fiche « Insécurité, victimation ».
3. « On entend que le sentiment d'insécurité ne repose sur rien, ou que tout le monde a peur. » 22 %, 21 %, 31 % et 10 % (2024) : Insee, fiche « Insécurité, victimation », figure 3 (« il arrive à 31 % des femmes de renoncer à sortir seules de chez elles, contre 10 % des hommes seulement »).

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web : chaque source rouverte (fichiers de l'Insee et de data.gouv.fr, API d'Eurostat, PDF passés à `pdftotext`), d'après le rapport `verify-securite.md`. Tous les producteurs sont officiels (Insee, SSMSI, Eurostat).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, violences physiques | 643 000 (2023) | Figure 2 : « Violences physiques 643 47 3,4 0,3 1,2 » (milliers ; 1,2 % des 18 ans ou plus) | https://www.insee.fr/fr/statistiques/fichier/8612552/FPORSOC25-F24.xlsx | Conforme, avec réserve : révision possible (SSMSI, 17/12/2025, non ouverte) |
| Violences sexuelles physiques | 325 000 ; 0,6 % | « ...ils concernent respectivement 264 000, 296 000 et 325 000 victimes en 2023 » | même fichier | Conforme, avec la même réserve |
| Cambriolage ou tentative | 1 516 000 ; 2,9 % | Figure 1 : « Vols ou tentatives de vol avec effraction (résidence principale) 1 516 2,9 » | même fichier | Conforme, avec la même réserve ; unité : personne dont le ménage a été touché |
| Sentiment d'insécurité | 22 / 15 / 21 % ; femmes 25 / 18 / 31 ; hommes 19 / 12 / 10 | Figure 3, colonnes femmes, hommes, 18 ans ou plus | même fichier | Conforme, avec la même réserve |
| Satisfaction envers les forces de sécurité | 56 % ; 53 % | « Satisfaction envers l'action nationale des FSI 55 57 43 67 56 » ; « ... de proximité 51 56 46 60 53 » | même fichier | Conforme, avec la même réserve |
| Taux de plainte | 12 % ; 74 % | Phrase citée au point 3 de « À savoir » | PDF de présentation des bases (URL de la source 2) | Conforme |
| Violences conjugales enregistrées | 114 721 (2016) ; 244 301 (2022) | Série « Violences conjugales (ensemble) enregistrées par les services de sécurité », victimes | CSV du SSMSI (URL de la source 3) | Conforme ; la série s'arrête en 2022 dans ce fichier |
| Taux d'homicide, Eurostat | 1,52 ; 1,03 ; 1,30 ; 1,28 | Valeurs de l'API, unité `P_HTHAB` ; taux publié par Eurostat | API d'Eurostat (URL de la source 4) | Conforme, avec réserve : la série française exclut les coups et blessures suivis de mort |
| Homicides, SSMSI | 1 140 (2008) ; 911 (2016) ; 975 (2025) | Séries « Homicides enregistrés par les services de sécurité », victimes, attentats compris | CSV du SSMSI | Conforme, avec réserve : rupture de source en 2016 |
| Tentatives d'homicide | 2 259 (2016) ; 4 501 (2025) | Série « Tentatives d'homicide enregistrées par les services de sécurité », victimes | CSV du SSMSI | Conforme ; « doublement » calculé (1,99), non publié |
| Dates de publication | 2025-11-18, 2026-07-08, 2026-10-14, 2026-04-29 | Fiche de l'Insee parue le 18/11/2025 ; PDF créé le 08/07/2026 ; fichier du 14/10/2026 ; mise à jour d'Eurostat du 29/04/2026 | URL des sources | Conforme |

**Conclusion.** Aucun chiffre du fichier n'est faux. Trois lectures sont à garder : l'enquête est déclarative et peut avoir été révisée ; les taux de plainte sont une moyenne ancienne (2011-2018) ; les homicides d'Eurostat et du SSMSI n'ont pas la même définition, et la série du SSMSI change de source en 2016.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus. Les pages de l'Intérieur (enquête VRS 2025, avertissement de révision du 17/12/2025, violences conjugales 2025) étaient inaccessibles (403) et ne servent à aucun chiffre du fichier.

## Mises à jour

**09/11/2026** : le bloc « Ce qu'on entend » ne garde que les fausses vérités que les chiffres de la page démentent (décision du PO) : reformulées : « On entend que la violence explose et que la délinquance est hors de contrôle. » devient « On entend que les homicides explosent. ».

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert les fichiers et documents eux-mêmes.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Insee : Licence Ouverte 2.0, mention « Source : Insee » et date de dernière mise à jour (https://www.insee.fr/fr/information/2008466) ;
  - SSMSI : Licence Ouverte 2.0, déclarée sur la page du jeu de données (https://www.data.gouv.fr/datasets/bases-statistiques-communale-departementale-et-regionale-de-la-delinquance-enregistree-par-la-police-et-la-gendarmerie-nationales) ;
  - SSMSI : Licence Ouverte 2.0, déclarée sur la page du jeu de données (https://www.data.gouv.fr/datasets/service-statistique-ministeriel-de-la-securite-interieure-base-des-series-chronologiques) ;
  - Eurostat : réutilisation permise, commerciale comprise, mention « Source : Eurostat » et modifications signalées (https://ec.europa.eu/eurostat/help/copyright-notice).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
