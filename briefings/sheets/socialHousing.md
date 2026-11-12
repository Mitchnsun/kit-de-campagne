# `socialHousing` · Le logement social (saisi à la main)

**Vérifiée le 10/11/2026** : double vérification sur le web, aucun écart de valeur ; le graphique 1 de la Cour des comptes rendu en image pour l'appariement des années et des valeurs. Réserves reprises ci-dessous (demandes déclaratives, absence de chiffre par nationalité, article R. 441-1 non ouvert). La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `socialHousing`, dossier « Pouvoir d'achat et logement » (`purchasingPower`), volet « Logement social » de la page composite `housing` (voir `housing.md`), page de type comparaison, recherche du 09/11/2026 |
| Données | `briefings/manual/socialHousing.json`, saisi à la main le 2026-11-10 depuis le Datalab RPLS du SDES, le chapitre I-4 du rapport public annuel 2026 de la Cour des comptes (graphique 1) et la fiche F869 |
| Sources | 1. SDES, « 5,4 millions de logements locatifs sociaux en France au 1er janvier 2025 », https://www.statistiques.developpement-durable.gouv.fr/54-millions-de-logements-locatifs-sociaux-en-france-au-1er-janvier-2025, PDF https://www.statistiques.developpement-durable.gouv.fr/media/8939/download?inline, Licence Ouverte 2.0 (non vérifiée). 2. Cour des comptes, « Faciliter le parcours d'accès au logement social dans les territoires, Rapport public annuel 2026 », https://www.ccomptes.fr/sites/default/files/2026-03/20260325-RPA-2026-I-4-Faciliter-le-parcours-d-acces-au-logement-social_0.pdf, citation seulement. 3. DILA, service-public.gouv.fr, « Quelles sont les conditions pour obtenir un logement social ? » (F869), https://www.service-public.gouv.fr/particuliers/vosdroits/F869, citation seulement. 4. Ministère de l'Intérieur, « Réponse à la question écrite n° 6521, Journal officiel du 5 mars 2024 », https://www.assemblee-nationale.fr/dyn/16/questions/QANR5L16QE6521.pdf, citation seulement. 5. Insee, « Conditions de logement, Immigrés et descendants d'immigrés en France, Insee Références, édition 2023 » (fiche 5.5), https://www.insee.fr/fr/statistiques/fichier/6793286/IMMFRA23-F32.pdf, Licence Ouverte 2.0 |
| Dates de publication | 2026-01-20 (RPLS) ; 2026-03-25 (Cour des comptes) ; 2026-09-11 (F869, « Vérifié le 11 septembre 2026 ») ; 2024-03-05 (JO) ; 2023-03-27 (fiche de l'Insee : aucune date dans le PDF, date de modification du fichier, à remplacer par la date de parution de l'édition quand le PO l'aura lue) |
| Séries | `socialStock` : logements locatifs sociaux au 1er janvier, 2024 (5 367 000) et 2025 (5 396 300). `requests` : demandes actives au 31 décembre, 2018 à 2024 (2 107 000 … 2 760 000). `allocations` : attributions de l'année, 2018 à 2024 (462 000 … 383 857). Les valeurs rondes sont celles du graphique de la Cour |
| Ventilations | `incomeCeiling` (2026) : revenu maximum d'une personne seule, revenus de 2024, cas général, hors outre-mer : Paris et Île-de-France 34 996 €, autres régions 30 424 € |
| Chiffre clé | 5 396 300 logements locatifs sociaux au 1er janvier 2025, en hausse (5 367 000 au 1er janvier 2024) ; à côté, les demandes actives fin 2024 (2,76 millions) |
| Règles | Saisie à la main. Quatre vues : « Le parc », « Demandes », « Attributions » (un stock et un flux, chacun dans sa vue, jamais rapportés l'un à l'autre), « Conditions d'accès » (le revenu maximum, les règles citées dans la note). Le délai moyen (19 mois, 39,5 en Île-de-France) est dans une note et un « À savoir » (pas d'unité « mois »). Non saisis : les ménages éligibles (72 %, une confusion entre éligibilité et occupation écartée par le rapport), le loyer moyen, la vacance et la mobilité du parc social, les ménages extra-communautaires parmi les bénéficiaires des APL (ce n'est pas un chiffre d'attributions), la loi SRU |
| Première édition | À remplir à la publication |

## « À savoir »

1. 35 % des immigrés de 18 à 59 ans vivent en logement social, contre 11 % des personnes sans ascendance migratoire (2019-2020, France métropolitaine) ; une occupation, pas une attribution, « largement liée aux moindres revenus et à l'âge plus jeune » ; un immigré peut être devenu Français. Source : fiche 5.5 de l'Insee (« c’est l’inverse pour les immigrés (28 % contre 35 %) » ; « Cette surreprésentation en logement social est largement liée aux moindres revenus et à l’âge plus jeune des immigrés et descendants d’immigrés par rapport au reste de la population ») ; définition de l'Insee : « personne née étrangère à l'étranger et résidant en France ». La note tient en 316 caractères (320 au plus) avec les trois précisions demandées.
2. 19 mois en moyenne en 2024, 39,5 en Île-de-France ; moyenne des demandes satisfaites ; 55,1 % satisfaites en moins d'un an. Source : Cour des comptes, chapitre I-4 (« La durée moyenne d’obtention d’un logement en 2024 sur l’ensemble du territoire était de 19 mois […] soit 39,5 mois » ; « un peu plus de la moitié (55,1 %) des demandes sont satisfaites en moins d’un an »).
3. Dénombrement « fragile » ; près de 900 000 des 2,76 millions de demandes de ménages déjà logés dans le parc social ; « près de 1,9 million » hors mutation. Source : Cour des comptes, chapitre I-4 (phrases recopiées).
4. Parc RPLS hors foyers et résidences sociales ; logements loués : 15,9 % des résidences principales ; les 17,3 % de l'Insee sont une autre mesure. Source : Datalab RPLS (« La part des logements sociaux loués parmi l’ensemble des résidences principales est de 15,9 % ») ; BDM 001791251 (volet `housingStock`).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Dans `briefings/notes/socialHousing.json` (clé `claims`). Règle du PO (09/11/2026) pour une affirmation que rien de mesuré ne tranche : l'affirmation, la réponse des instances officielles, et « Ce n'est pas parce que ce n'est pas évalué que c'est vrai. » Source de chaque élément de la réponse, dans son ordre :

1. « On entend que les HLM vont d'abord aux étrangers. »
   - « il faut en faire la demande et ne pas dépasser un revenu maximum » et « au minimum fournir la copie d'un titre de séjour » : F869 (« Pour obtenir un logement social (ou logement HLM), il faut en faire la demande et ne pas dépasser un revenu maximum » ; « Vous êtes d'une autre nationalité. Vous devez au minimum fournir la copie d'un titre de séjour »).
   - « Les étrangers en situation irrégulière ne peuvent demander l'accès à un logement social » : réponse du ministère de l'Intérieur à la question écrite n° 6521, JO du 5 mars 2024 (phrase recopiée).
   - Aucun chiffre officiel des attributions selon la nationalité n'est publié : recherche du rapport final (F869, chapitre I-4 de la Cour des comptes, qui ne contient aucun des mots « nationalité », « étranger », « séjour », publications de l'Insee, réponses ministérielles) ; l'infocentre du SNE est à accès réservé (absence de preuve, pas preuve d'absence).
   - La phrase du PO, telle quelle.
   Le chiffre d'occupation des immigrés n'est pas dans la réponse : il est dans l'« À savoir » n° 1, avec son explication. La phrase « la nationalité n'est pas un critère », qu'aucune source ouverte ne contient, n'est pas reprise.

## Double vérification

Faite le 10/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-logement.md` : PDF du RPLS, de la Cour des comptes (page 170 rendue en image), de la réponse ministérielle et de la fiche de l'Insee passés à `pdftotext` ; F869 relue.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 5 396 300 (1er janvier 2025) | « le parc locatif social compte 5 396 300 logements » ; tableau 1 : 5 367 000 au 1er janvier 2024 | https://www.statistiques.developpement-durable.gouv.fr/54-millions-de-logements-locatifs-sociaux-en-france-au-1er-janvier-2025 | Conforme |
| Demandes et attributions | 2 × 7 valeurs | Graphique 1, étiquettes lues sous leurs années ; « Fin 2024, le nombre de demandes actives était de 2,76 millions » | Cour des comptes, chapitre I-4 | Conforme, avec réserve : valeurs rondes du graphique, dénombrement « fragile » |
| Délai | 19 mois ; 39,5 | Phrase de la Cour | idem | Conforme |
| Revenu maximum | 34 996 € ; 30 424 € | F869, cas général, une personne | https://www.service-public.gouv.fr/particuliers/vosdroits/F869 | Conforme, avec réserve : plafond de Paris lu pour l'Île-de-France |
| Séjour régulier | Phrase du ministère | Réponse publiée au JO du 05/03/2024 | https://www.assemblee-nationale.fr/dyn/16/questions/QANR5L16QE6521.pdf | Conforme, avec réserve : l'article R. 441-1 du CCH n'a pas été ouvert (Légifrance refuse les scripts) |
| Occupation (note) | 35 % ; 11 % | Tableau 1 et phrase de la fiche 5.5 | https://www.insee.fr/fr/statistiques/fichier/6793286/IMMFRA23-F32.pdf | Conforme, avec réserve : occupation, pas attribution ; date de parution à confirmer |

**Conclusion.** Aucun chiffre du fichier n'est faux ; aucun chiffre d'attributions selon la nationalité n'est donné, faute d'en trouver un publié.

**Pages consultées** le 10/11/2026 : les URL ci-dessus.

## Réserves

- Les demandes sont un stock déclaratif, les attributions un flux : jamais de ratio.
- La condition de séjour régulier est rapportée par le ministère, pas lue dans le code : le PO doit ouvrir l'article R. 441-1 du CCH.
- La date de publication de la fiche de l'Insee est celle du fichier (2023-03-27), pas une date de parution lue.
- L'édition du RPLS au 1er janvier 2026 est attendue en janvier 2027.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert les publications.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - SDES : licence ouverte du décret n° 2017-638, réutilisation commerciale permise, mention « Service des données et études statistiques (SDES) » et date de dernière mise à jour (https://www.statistiques.developpement-durable.gouv.fr/mentions-legales) ;
  - Insee : Licence Ouverte 2.0, mention « Source : Insee » et date de dernière mise à jour (https://www.insee.fr/fr/information/2008466) ;
  - citation seule : Cour des comptes, DILA, service-public.gouv.fr, Ministère de l'Intérieur (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
