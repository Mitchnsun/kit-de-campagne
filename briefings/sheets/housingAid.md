# `housingAid` · Les aides au logement et l'hébergement (saisi à la main)

**Vérifiée le 10/11/2026** : double vérification sur le web, aucun écart de valeur ; le tableau T311 des séries longues relu ligne à ligne (16 années × 4 lignes). Réserves reprises ci-dessous (périmètre large, études de champs et de dates différents, sans-domicile de 2012, places de seconde main). La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `housingAid`, dossier « Pouvoir d'achat et logement » (`purchasingPower`), volet « Aides et hébergement » de la page composite `housing` (voir `housing.md`), page de type comparaison, recherche du 09/11/2026 |
| Données | `briefings/manual/housingAid.json`, saisi à la main le 2026-11-10 depuis les « Séries longues Aides » du compte du logement (onglet T311), le rapport du compte du logement 2025 et les autres publications citées |
| Sources | 1. SDES, « Rapport du compte du logement 2025 », https://www.statistiques.developpement-durable.gouv.fr/rapport-du-compte-du-logement-2025, « Séries longues Aides » https://www.statistiques.developpement-durable.gouv.fr/media/9738/download?inline, Licence Ouverte 2.0 (non vérifiée). 2. Économie et Statistique, « Pourquoi les ménages à bas revenus paient-ils des loyers de plus en plus élevés ? L’incidence des aides au logement en France (1973-2002), n° 381-382 », https://www.insee.fr/fr/statistiques/fichier/1376573/es381-382b.pdf : l'article d'une chercheuse publié dans la revue de l'Insee, citation seulement. 3. Insee, « L’impact des aides au logement sur le secteur locatif privé, Insee Analyses n° 19 », https://www.insee.fr/fr/statistiques/fichier/version-html/1521337/ia19.pdf, Licence Ouverte 2.0. 4. CGEDD (aujourd'hui IGEDD), « Test de l’effet haussier de la partie progressive par rapport au loyer du barème des aides personnelles au logement », https://www.igedd.developpement-durable.gouv.fr/IMG/pdf/effet-haussier-apl_cle59af18.pdf, citation seulement. 5. Insee, « L’hébergement des sans-domicile en 2012, Insee Première n° 1455 », https://www.insee.fr/fr/statistiques/1281324, Licence Ouverte 2.0. 6. Assemblée nationale, « Rapport n° 1996 sur le projet de loi de finances pour 2026, annexe n° 5 : Cohésion des territoires, logement et hébergement d'urgence », https://www.assemblee-nationale.fr/dyn/17/rapports/cion_fin/l17b1996-tiii-a5_rapport-fond.pdf, p. 46, citation seulement |
| Dates de publication | 2026-09-14 (compte du logement) ; 2005-01-01 (Économie et Statistique n° 381-382 : l'année seule, le 1er janvier par convention) ; 2014-11-01 (« Novembre 2014 » : le mois seul) ; 2020-08-01 (« août 2020 » : le mois seul) ; 2013-07-02 (Insee Première n° 1455) ; 2025-10-23 (rapport enregistré à la présidence de l'Assemblée) |
| Séries | `allAid` (T311, ligne « ENSEMBLE DES AIDES AU LOGEMENT »), `apl`, `als`, `alf` (lignes 6 à 8) : 2010 à 2025, en milliards d'euros courants (les M€ du tableau ÷ 1 000 : 45 878 → 45,878). `personalAid` : 16,4 Md€ en 2025, le chiffre du texte du rapport (« Le montant de ces trois aides s’élève à 16,4 Md€ en 2025 »). `homeless` : 141 500 (2012). `shelterPlaces` : 203 000 (2026, statut `projection`, dit « prévision ») |
| Ventilations | `aidComponents` (2025, Md€) : prestations sociales 20,093 ; subventions d'investissement 5,832 ; avantages fiscaux 16,423 ; avantages de taux 3,304 ; subventions d'exploitation 0,226 (somme : 45,878) |
| Chiffre clé | 45,878 Md€ d'aides au logement en 2025, écrit « 45,9 Md€ », en hausse (43,484 en 2024) ; à côté, les aides personnelles (16,4 Md€) |
| Règles | Saisie à la main. Deux vues : « Les aides » (par nature, puis APL, ALS et ALF ; les quatre séries au tableau), « Sans-domicile et hébergement » (deux blocs séparés, sans tableau : deux natures, deux dates). Les études sur l'effet des aides sont dans les notes, chacune avec son champ et sa date ; l'article de 2005 n'est pas attribué à « l'Insee ». Non saisis : les bénéficiaires des aides personnelles (déjà dans « Pouvoir d'achat », unité non écrite), les aides de l'Anah, la part des dépenses courantes couverte, les nuitées hôtelières |
| Première édition | À remplir à la publication |

## « À savoir »

1. « entre 50 % et 80 % des allocations logement » des ménages à bas revenus « auraient été absorbées par les augmentations de leurs loyers » ; réforme du début des années 1990 ; enquêtes Logement 1973-2002 ; publié en 2005 dans Économie et Statistique, la revue de l'Insee. Source : article, résumé (phrase recopiée).
2. Loyers privés de la zone II plus hauts « de 5,3 % sur la période 2005-2012 » (Insee Analyses n° 19, 2014, zone II contre zone III autour du seuil de 100 000 habitants, intervalle de confiance à 95 % de 1,6 à 8,9 %) ; note du CGEDD (2020) : l'effet de la partie du barème qui croît avec le loyer est « faible s'il existe », un seul mécanisme testé. Sources : Insee Analyses n° 19 (« Les loyers dans la zone II sont en effet plus élevés, toutes choses égales par ailleurs, de 5,3 % sur la période 2005-2012, soit 25 euros par mois ») ; note du CGEDD (« On en conclut donc que l’effet haussier de la partie du barème des aides progressive par rapport au loyer est faible s’il existe »). Les études ne mesurent pas la même chose : la note ne les oppose pas.
3. Environ 141 500 sans-domicile début 2012 en France métropolitaine, enfants compris, dernière estimation ; l'enquête de 2025 sans résultats publiés. Source : Insee Première n° 1455 (« On estime qu’environ 141 500 personnes étaient sans domicile en France métropolitaine ») ; présentation de l'enquête Sans Domicile 2025 (https://www.insee.fr/fr/metadonnees/source/operation/s2125/presentation), sans date de résultats.
4. 203 000 places d'hébergement généraliste, capacité financée en moyenne annuelle depuis 2021, maintenue en 2026 au PLF ; chiffre du Gouvernement cité par le rapporteur spécial. Source : rapport n° 1996, annexe 5, p. 46 (« Ces crédits devraient permettre de financer le maintien des capacités d’accueil à hauteur de 203 000 places en moyenne annuelle depuis 2021 »).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Aucune affirmation : « Les aides au logement font monter les loyers » est mixte (estimé pour deux périodes, jugé « faible s'il existe » pour un mécanisme), écartée par le rapport final.

## Double vérification

Faite le 10/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-logement.md` : classeur des séries longues lu avec openpyxl, PDF passés à `pdftotext`, page de l'Insee Première relue.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 45,878 Md€ (2025) | T311 « ENSEMBLE DES AIDES AU LOGEMENT » : 45 878,0 ; « ces aides représentent, en 2025, 45,9 milliards d'euros » | https://www.statistiques.developpement-durable.gouv.fr/media/9738/download?inline | Conforme |
| Séries 2010-2025 | 4 × 16 valeurs | Lignes 56, 6, 7, 8 comparées une à une | idem | Conforme |
| Aides personnelles | 16,4 Md€ ; 7,519 + 5,610 + 3,298 | Texte du chapitre 5 ; 7 519,1 + 5 610,4 + 3 298,2 | https://www.statistiques.developpement-durable.gouv.fr/rapport-du-compte-du-logement-2025 | Conforme |
| Par nature | 5 valeurs, somme 45,878 | T311, 2025 | idem | Conforme |
| Sans-domicile | 141 500 (2012) | Phrase de l'Insee Première n° 1455 | https://www.insee.fr/fr/statistiques/1281324 | Conforme, avec réserve : non comparable à 2001 |
| Places | 203 000 (2026, prévision) | Rapport n° 1996, p. 46 | https://www.assemblee-nationale.fr/dyn/17/rapports/cion_fin/l17b1996-tiii-a5_rapport-fond.pdf | Conforme, avec réserve : de seconde main, capacité financée |

**Conclusion.** Aucun chiffre du fichier n'est faux ; le total mêle versements et dépenses fiscales, et les notes le disent.

**Pages consultées** le 10/11/2026 : les URL ci-dessus.

## Réserves

- Le total des aides au logement a un périmètre large (prestations, subventions, avantages fiscaux et de taux) : les avantages fiscaux sont des recettes en moins, pas des versements ; euros courants.
- Les trois études ont des champs, des méthodes et des dates différents ; aucune n'est d'aujourd'hui.
- 141 500 sans-domicile est une estimation de 2012, la dernière publiée ; à remplacer dès la parution de l'enquête de 2025.
- 203 000 places : le Gouvernement cité par le rapporteur ; le projet annuel de performances n'a pas été ouvert.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert le classeur et les publications.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée : Licence Ouverte 2.0 (SDES, Insee), citation seulement (Économie et Statistique, CGEDD, Assemblée nationale).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
