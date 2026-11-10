# `prisonDensity` · Densité carcérale

**Mise à jour le 10/11/2026** : les chiffres du 1er octobre 2026 (90 937 détenus, 63 452 places opérationnelles, 143,3 %, maisons d'arrêt 178,0 %, 8 959 matelas au sol, 108 587 écroués dont 17 650 non détenus) sont retrouvés à l'identique dans les deux PDF du ministère pour ce mois, la brochure mensuelle et « Mesure de l'incarcération » ; notes 1, 2 et 4 passées au 1er octobre (section « Mises à jour »).

**Vérifiée le 02/11/2026** : les chiffres du 1er septembre 2026 (90 020 détenus, 63 348 places opérationnelles, 142,1 %, maisons d'arrêt 176,1 %, 8 347 matelas au sol, 107 700 écroués dont 17 680 non détenus) et huit points de la série sont retrouvés à l'identique dans les PDF mensuels du ministère, et septembre 2026 dans la presse. Corrigé après la vérification : la série d'avant 2019 commence au premier tableau de densité des classeurs, décembre 2013 (son titre, « Nombre de personnes écrouées détenues et densité de population », échappait au script) ; notes précisées.

**Établissements à 120 % ou plus** : le ministère publie trois nombres pour chaque mois, sans expliquer l'écart. Pour le 1er octobre 2026 : 133 (tableau 24, la liste du fichier), 135 (page de synthèse de la même brochure, 40 + 70 + 25) et 137 (« Mesure de l'incarcération ») ; pour le 1er septembre, 136, 138 et 139 (le ticket #31 disait 138). La note dit « 133 à 137 selon la publication » ; la liste en compte 133.

| Champ | Valeur |
| --- | --- |
| Indicateur | `prisonDensity`, ticket #31, dossier « Sécurité et justice » (statut `planned`) |
| Données | `briefings/data/prisonDensity.json`, écrit le 2026-11-10 par `yarn briefings prisonDensity` sur la machine du PO (web.archive.org refuse les connexions de la session de l'agent). Les neuf classeurs d'octobre 2013 à juin 2014, que data.gouv.fr liste encore mais ne sert plus (404), sont lus dans leur copie de l'Internet Archive du 01/04/2026, chacune vérifiée par l'empreinte SHA-1 que data.gouv.fr avait enregistrée ; octobre 2026, absent de data.gouv.fr, vient du classeur de la page 2026 du ministère. Première écriture le 2026-11-02, par les fonctions du script, à partir des classeurs téléchargés à part |
| Source | Ministère de la Justice, « Statistique mensuelle de la population écrouée et détenue en France », data.gouv.fr jusqu'au 1er septembre 2026, et le classeur du 1er octobre 2026 de la page 2026 du ministère, « Mis à jour le 02 novembre 2026 » (la date de la source) ; Licence Ouverte (`fr-lo` sur data.gouv.fr, version 1.0) ; en français seulement |
| Séries | `density`, `detainees`, `operationalPlaces` : de janvier 2023 à octobre 2026 ; `densityUntil2019`, `detaineesUntil2019`, `operationalPlacesUntil2019` : de décembre 2013 à mars 2019 (PDF seulement de mi-2019 à 2022, le trou est montré) ; `floorMattresses` : octobre 2026 |
| Valeurs par catégorie | `densityByQuarterType` : densité par type de quartier au 1er octobre 2026 (maisons d'arrêt 178,0 %, centres de détention 99,8 %…) |
| Liste | `crowdedEstablishments` : les 133 établissements ou quartiers du tableau 24 du 1er octobre 2026, de 284,2 % (CP Majicavo, quartier centre de détention) à 122,5 % (CSL Corbeil-Essonnes) |
| Chiffre clé | 143,3 % au 1er octobre 2026, en hausse (135,8 % un an plus tôt) |
| Première édition | À remplir à la publication |

Particularités du jeu data.gouv.fr au 02/11/2026, traitées par le script : octobre 2025 en double (mêmes chiffres, compté une fois), novembre 2025 absent (pris de la page 2025 du ministère) ; le classeur de décembre 2024 écrit « decembre » sans accent ; les classeurs de 2010 à mi-2013 sont des .xls que le script ne lit pas (avant tout tableau de densité).

À actualiser : chaque mois (environ un mois après la date de situation).

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans ouvrir les classeurs du script ; il a lu les PDF mensuels du ministère, de même origine. Son rapport, tel quel :

Date de la vérification : 2026-11-02. Périmètre : France entière (métropole et outre-mer), au 1er de chaque mois.

### 0. Résumé

- Toutes les valeurs chiffrées de l'instantané sont retrouvées à l'identique : le 1er septembre 2026 (90 020 / 63 348 / 142,1 % / 176,1 % / 8 347 / 107 700 / 17 680) et les 8 points de la série (2015, 2017, 2019, 2023, 2024, 2025, 2026). Aucun chiffre n'est faux.
- Un seul point n'est pas tranché : le nombre d'établissements ou quartiers à 120 % ou plus. Le ministère publie trois nombres pour le 1er septembre 2026 : 136 (tableau 24, liste détaillée), 138 (page « Les chiffres au 1er septembre 2026 » de la même brochure) et 139 (« Mesure de l'incarcération »). 136 et 138 sont donc tous deux « justes », selon la base de comptage.
- Trois libellés de l'instantané sont à corriger ou à nuancer : (a) la note 1 (« norme circulaire, calculée autrement ») est inexacte telle quelle ; (b) la note 3 : « le ministère n'a publié que des PDF » est vrai du format sur data.gouv.fr, mais ces PDF contiennent la densité, et « avant février 2015, pas de tableau de densité » est contredit pour les PDF (tableau de densité dès octobre 2013 au moins) ; (c) « CP Majicavo 273,7 % » est la densité du seul quartier centre de détention du CP (le centre entier est à 230,2 %).
- Fait nouveau : au 1er octobre 2026 (publié fin octobre), le ministère donne 90 937 détenus pour 63 452 places, soit 143,3 %. Le « record » du 1er septembre est déjà dépassé ; l'instantané n'est plus le dernier disponible à la date du jour.

### 1. Méthode et limites

- Aucun classeur mensuel XLSX/XLS (data.gouv.fr ou justice.gouv.fr) n'a été ouvert ni téléchargé. De data.gouv.fr, j'ai seulement lu les métadonnées JSON du jeu de données (licence, titres et formats des ressources) et la liste des licences, sans ouvrir de ressource.
- Les chiffres viennent des PDF mensuels du ministère (« Mesure de l'incarcération », « Statistique des établissements et des personnes écrouées »), lus directement après téléchargement (pdftotext). Attention : ce sont les mêmes données (Genesis, DGAP/SSER) que les classeurs du script, dans un autre format. Cette vérification contrôle donc la lecture et le calcul du script, pas l'exactitude du ministère lui-même. Les sources secondaires (presse, OIP, World Prison Brief) reprennent aussi les chiffres du ministère : elles ne sont pas indépendantes de lui.
- Les statistiques trimestrielles de milieu fermé (STMF) sont des classeurs XLSX trimestriels : je les ai ouverts (openpyxl, Python en mode isolé), car la consigne demandait de recouper avec elles et n'exclut que les classeurs mensuels. Les classeurs du 4e trimestre 2025, du 1er trimestre 2026 et du 3e trimestre 2026 ont été lus. Celui du 2e trimestre 2026 a été téléchargé mais n'est pas lisible par openpyxl (archive incomplète) ; je me suis servi à la place de la note « Infos Rapides Justice » du 16 juillet 2026. Les classeurs de 2025 ont été téléchargés mais pas lus.
- Mentions « résumé de moteur de recherche » : quand une valeur n'est connue que par l'extrait d'un moteur de recherche, ou d'un site que je n'ai pas pu ouvrir, c'est écrit dans la colonne Source.

### 2. Instantané au 1er septembre 2026

Sources principales (PDF du ministère, DGAP, lus directement) :
- P1 = https://www.justice.gouv.fr/sites/default/files/2026-10/mesure_mensuelle_01092026.pdf
- P2 = https://www.justice.gouv.fr/sites/default/files/2026-10/statistique_etablissements_personnes_ecrouees_01092026.pdf
- Presse : Sud Radio (3 octobre 2026) https://www.sudradio.fr/societe/prisons-90-020-detenus-en-france-au-1er-septembre-un-nouveau-record et La Gazette France https://www.lagazettefrance.fr/article/prisons-90-020-detenus-en-france-au-1er-septembre-un-nouveau-record (pages ouvertes ; mêmes phrases, dépêche d'agence non nommée dans les extraits lus)
- En anglais : World Prison Brief https://www.prisonstudies.org/country/france (page ouverte)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Détenus | 90 020 | 90 020 (Métropole 82 944 + Outre-mer 7 076) | P1 ; P2 tableau 1 ; Sud Radio ; World Prison Brief | Conforme |
| Places opérationnelles | 63 348 | 63 348 (métropole 58 636 + outre-mer 4 712) | P1 ; P2 tableau 6 | Conforme |
| Densité globale | 142,1 % | 142,1 % (90 020 / 63 348 = 142,1) | P1 ; P2 ; Sud Radio (« taux de sur-occupation globale 142,1 % ») ; World Prison Brief | Conforme |
| Densité MA/QMA | 176,1 % | 176,1 % (63 151 détenus / 35 863 places, hors places mineurs) | P1 ; P2 tableau 11 ; Sud Radio | Conforme |
| Matelas au sol | 8 347 | 8 347 (+51,8 % sur un an, 5 500 en 2025) | P1 ; P2 ; Sud Radio | Conforme |
| Écroués | 107 700 | 107 700 (101 412 un an plus tôt, +6,2 %) | P2 tableau 1 | Conforme |
| Écroués non détenus | 17 680 | 17 680 = 16 729 DDSE + 951 placements à l'extérieur non hébergés | P1 ; P2 ; World Prison Brief | Conforme |
| Établissements ou quartiers à 120 % ou plus | 136 (ticket du jeu : 138) | 136 (tableau 24) ; 138 (page des chiffres, 32+75+31) ; 139 (Mesure de l'incarcération, 2+6+9+122) | P2 ; P1 (voir § 3.4) | Écart expliqué |
| « CP Majicavo (Mayotte) 273,7 % » | 273,7 % | Ligne « CP MAJICAVO / CD/QCD » : 312 détenus pour 114 places = 273,7 %. L'autre quartier du CP (MA/QMA) est à 200,0 % (328 pour 164). Centre entier : 640 / 278 = 230,2 % (calcul à partir des deux lignes ; 278 places confirmées par Mayotte Hebdo pour mai 2026, résumé de moteur de recherche) | P2 tableau 24 | Conforme (réserve : nommer le quartier) |
| « MA La Roche-sur-Yon 270,6 % » | 270,6 % | 46 détenus pour 17 places opérationnelles = 270,6 %. La capacité norme circulaire est de 39 : 46 / 39 = 117,9 % | P2 tableau 24 | Conforme (réserve : voir note 1) |
| Tête de liste | Majicavo puis La Roche-sur-Yon | Ordre confirmé : 273,7 ; 270,6 ; puis Le Puy-en-Velay 255,6 ; Carcassonne 245,3 ; Fontenay-le-Comte 243,6 | P2 tableau 24 (136 lignes relues par script) | Conforme |
| « Chiffre clé 142,1 %, en hausse » | hausse | 134,7 % au 1er septembre 2025 (+7,4 points) ; 141,6 % au 1er août 2026 ; 143,3 % au 1er octobre 2026 | P1 ; https://www.justice.gouv.fr/sites/default/files/2026-08/mesure_mensuelle_01082026.pdf ; https://www.justice.gouv.fr/sites/default/files/2026-11/mesure_mensuelle_01102026.pdf | Conforme |

Autres valeurs relevées (utiles pour les textes) : 28 241 détenus en surnombre (23 545 un an plus tôt) ; 1 569 places libres ; 63 814 détenus hébergés dans une structure à plus de 120 % et 53 609 à plus de 150 % (P1) ; 24 539 prévenus, soit 27,3 % des détenus (P2) ; capacité « norme circulaire » 64 328 (P2 tableau 6).

### 3. Série depuis 2023

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2023-11 | 75 130 / 60 975 (123,2 %) | 75 130 / 60 975 / 123,2 % (surnombre 17 064) | https://www.justice.gouv.fr/sites/default/files/2023-11/mesure_mensuelle_01112023.pdf (lu) | Conforme |
| 2024-08 | 78 397 / 62 021 (126,4 %) | 78 397 / 62 021 / 126,4 % | https://www.justice.gouv.fr/sites/default/files/2024-08/Mesure_mensuelle_2024-08-01.pdf (lu) ; colonne « 2024 » de https://www.justice.gouv.fr/sites/default/files/2025-08/mesure_mensuelle_01082025.pdf | Conforme |
| 2025-05 | 83 681 / 62 570 (133,7 %) | 83 681 / 62 570 / 133,7 % | https://www.justice.gouv.fr/sites/default/files/2025-05/Mesure_mensuelle_2505.pdf (lu) ; colonne « 2025 » de https://www.justice.gouv.fr/sites/default/files/2026-05/mesure_mensuelle_01052026.pdf | Conforme |
| 2025-12 | 86 229 / 63 613 (135,6 %) | 86 229 / 63 613 / 135,6 % (135,55 au calcul, arrondi du ministère) | https://www.justice.gouv.fr/sites/default/files/2025-12/mesure_mensuelle_01122025.pdf (lu) | Conforme |
| 2026-04 | 88 145 / 63 353 (139,1 %) | 88 145 / 63 353 / 139,1 % | https://www.justice.gouv.fr/sites/default/files/2026-04/mesure_mensuelle_01042026.pdf (lu) ; la Gazette du Palais https://www.labase-lextenso.fr/gazette-du-palais/2026-n17/vers-une-forme-de-regulation-carcerale-GPL490x5 donne les mêmes chiffres (résumé de moteur de recherche, page payante non ouverte) | Conforme |

Les nombres de détenus de 2025-05, 2025-12 et 2026-04 sont aussi dans le tableau 2 de P2 (aucune révision a posteriori). Recoupements presse (résumés de moteur de recherche, non ouverts) : Europe 1 et Brut pour 2025-05 et 2025-12 ; 75secondes pour 2024-08. L'OIP confirme le 1er juin 2025 (84 447 détenus, capacité opérationnelle 62 566) : https://oip.org/communique/nouveau-record-du-nombre-de-personnes-detenues-jusqua-lasphyxie/ (page ouverte).

### 4. Série d'avant 2019

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2015-02 | 66 310 / 57 844 (114,6 %) | 66 310 / 57 844 / 114,6 % (norme circulaire : 58 616) | https://www.justice.gouv.fr/sites/default/files/2023-05/mensuelle_fevrier_2015.pdf (lu) | Conforme |
| 2017-04 | 70 230 / 58 670 (119,7 %) | 70 230 / 58 670 / 119,7 % (norme circulaire : 60 072) | https://www.justice.gouv.fr/sites/default/files/2023-05/mensuelle_avril_2017.pdf (lu) ; « record » : Sud Radio https://www.sudradio.fr/faits-divers/plus-de-70-000-personnes-en-prison-au-1er-avril-2017-un-record (résumé de moteur de recherche) | Conforme |
| 2019-01 | 70 059 / 60 151 (116,5 %) | 70 059 / 60 151 / 116,5 % | https://www.justice.gouv.fr/sites/default/files/2023-05/Mesure_mensuelle_incarceration_janvier2019.pdf (lu) ; colonne « 2019 » de https://www.justice.gouv.fr/sites/default/files/2023-04/Mesure_incarceration_janvier2020.pdf | Conforme |
| Fin de série : 2019-03 | (dernier point du fichier) | 71 037 / 60 867 / 116,7 % | https://www.justice.gouv.fr/sites/default/files/2023-05/mensuelle_mars_2019.pdf (lu) | Conforme (point ajouté pour information) |
| Trou « mi-2019 à 2022 » : PDF seuls | PDF seuls | Sur data.gouv.fr : 45 classeurs XLSX de janvier 2023 à septembre 2026 ; 32 PDF de juillet 2019 à décembre 2022 (en 2019-2020, seulement un mois par trimestre, puis tous les mois dès octobre 2020) ; XLSX jusqu'à « 1er mars 2019 » | https://www.data.gouv.fr/api/1/datasets/statistique-mensuelle-de-la-population-ecrouee-et-detenue-en-france/ (métadonnées seulement) | Conforme pour le format, à nuancer (voir note 3) |
| Les PDF 2019-2022 donnent la densité | non dit | Oui : 117,7 % au 1er avril 2019 ; 115,7 % au 1er janvier 2020 ; 103,4 % au 1er janvier 2021 ; 104,9 % au 1er février 2022 | https://www.justice.gouv.fr/sites/default/files/2023-05/Mesure_mensuelle_incarceration_avril2019.pdf ; .../2023-04/Mesure_incarceration_janvier2020.pdf ; .../2023-04/Mesure_incarceration_janvier_2021_v3.pdf ; .../2023-04/Mesure_mensuelle_01022022.pdf | Écart (la phrase de la note 3 laisse croire à un vide de données) |
| « Avant février 2015, les classeurs n'ont pas de tableau de densité » | pas de tableau | Pour les PDF de la même publication, c'est faux : « Tableau 6 : nombre de personnes écrouées détenues et densité de population » existe en octobre 2013, juin 2014 et décembre 2014 (116,0 % au 1er décembre 2014 : 67 105 / 57 854). Avant 2013 (PDF d'août 2009 et décembre 2010), pas de tableau de densité mais le nombre de places opérationnelles (53 323 ; 56 463) et la répartition des établissements par tranche de densité. Pour les classeurs eux-mêmes, non vérifiable (je n'ai pas le droit de les ouvrir) | https://www.justice.gouv.fr/sites/default/files/2023-05/mensuelle_octobre_2013.pdf ; .../mensuelle_juin_2014.pdf ; .../mensuelle_decembre_2014.pdf ; .../mensuelle_inTERnet_dec2010.pdf ; .../mensuelle_inTERnet_aout09.pdf | Non trouvé pour les classeurs ; Écart pour les PDF |

### 5. Points précis

#### 5.1 Concordance avec d'autres publications, écarts mensuel / trimestriel

Concordance mensuel / PDF / presse : 90 020, 63 348, 142,1 %, 176,1 %, 8 347 sont identiques dans « Mesure de l'incarcération », dans « Statistique des établissements et des personnes écrouées » (brochure de 43 tableaux), dans la presse (Sud Radio, La Gazette France) et chez le World Prison Brief. Aucune révision du chiffre de septembre dans l'édition d'octobre (tableau 2 de https://www.justice.gouv.fr/sites/default/files/2026-11/statistique_etablissements_personnes_ecrouees_01102026.pdf : 90 020).

Les statistiques trimestrielles de milieu fermé (STMF, https://www.justice.gouv.fr/documentation/etudes-et-statistiques/statistiques-trimestrielles-milieu-ferme) ne donnent ni places ni densité (sommaire du classeur du 1er trimestre 2026 : population par catégorie pénale, âge, nationalité, région, entrants, sortants). Elles ne servent donc qu'à contrôler les effectifs. Un résumé de moteur de recherche annonçait « 84 741 détenus et densité 136,1 % au 1er janvier 2026 » en STMF : le 84 741 est exact, mais aucune densité n'existe dans ces classeurs ; le 136,1 % n'est trouvé dans aucune publication ministérielle lue (le mensuel donne 135,8 % au 1er janvier 2026).

| Date | Détenus, mensuel (France entière) | STMF hors collectivités d'outre-mer (COM) | + Polynésie française et Nouvelle-Calédonie (tableau 20) | Somme | Écart |
|---|---|---|---|---|---|
| 1er janv. 2026 | 86 140 (tableau 2 de P2) | 84 741 | 1 386 | 86 127 | mensuel supérieur de 13 |
| 1er avr. 2026 | 88 145 | 86 686 | 1 445 | 88 131 | mensuel supérieur de 14 |
| 1er juil. 2026 | 89 446 | 87 961 (classeur du 3e trim.) ; note du 16 juillet : 88 000 + 1 500 = 89 500 | n.l. | n.l. | arrondi à la centaine |
| 1er oct. 2026 | 90 937 | 89 401 | 1 522 | 90 923 | mensuel supérieur de 14 |

Sources : https://www.justice.gouv.fr/sites/default/files/2026-01/STMF_2026_1_1.xlsx ; https://www.justice.gouv.fr/sites/default/files/2026-04/STMF_2026_4_1.xlsx ; https://www.justice.gouv.fr/sites/default/files/2026-10/STMF_2026_10_1.xlsx ; Infos Rapides Justice n°45 (15 octobre 2026) https://www.justice.gouv.fr/documentation/etudes-et-statistiques/au-1er-octobre-2026-7-personnes-detenues (« 89 400 hors COM, 1 500 en COM, 90 900 au total ») ; n°42 (16 juillet 2026) https://www.justice.gouv.fr/documentation/etudes-et-statistiques/au-1er-juillet-2026-52-personnes-detenues (« 88 000 hors COM, 1 500 en COM, 89 500 au total »). n.l. = non lu.

Explication des écarts :
- Champ : le STMF compte les établissements « France, hors collectivités d'outre-mer » (note de champ de chaque tableau) et traite à part la Polynésie française et la Nouvelle-Calédonie (tableaux 20 à 22). Le mensuel couvre « Métropole et Outre-Mer » (P2). C'est la cause principale (environ 1 400 à 1 500 détenus).
- Résidu de 13 à 14 détenus (le mensuel est plus haut) : le STMF compte « les personnes condamnées exécutant une peine d'emprisonnement ferme et les personnes en détention provisoire ». Les sources lues n'expliquent pas ce résidu. Il est inférieur à 0,02 %.
- Arrondi : les notes « Infos Rapides Justice » arrondissent à la centaine et additionnent des termes arrondis (le total de juillet, 89 500, correspond au mensuel 89 446 à 100 près).
- Date : mêmes dates de référence (1er du mois), mais la note du 1er octobre est publiée le 15 octobre, alors que les PDF mensuels de septembre portent une date de création du 23-24 septembre (métadonnées des PDF).
- Non détenus : au 1er octobre, 17 425 + 225 (COM) = 17 650, identique au mensuel (17 650). Au 1er avril, 19 218 + 237 = 19 455 contre 19 406 au mensuel : écart de 49, non expliqué par les sources.

#### 5.2 Définition de la densité, norme circulaire, écroués et détenus

Densité (ministère, P1 « Définitions ») : « Densité carcérale : rapport entre le nombre de personnes détenues et le nombre de places opérationnelles. » (P2 tableau 6 : « ce ratio s'obtient en rapportant le nombre de détenus à la capacité opérationnelle »). La densité de l'instantané est donc bien détenus / places opérationnelles : 90 020 / 63 348 = 142,1 %.

Places opérationnelles (P1) : « nombre de places en fonction de la superficie au plancher (circ. AP8805G B402 du 3 mars 1988, définissant le mode de calcul de la capacité de chaque établissement) et effectivement disponibles (les places en travaux ne sont donc pas comptabilisées) ». P2 tableau 6 : « Capacité opérationnelle : nombre de places effectivement disponibles » et « Capacité norme circulaire : la circulaire A.P. 88.05G du 17 mai 1988 définit le mode de calcul de la capacité des établissements pénitentiaires ». Remarque : P1 date la circulaire du 3 mars 1988, P2 du 17 mai 1988 ; je n'ai pas trouvé la circulaire elle-même.

Conséquence pour la note 1 : les deux capacités reposent sur le calcul de la même circulaire. La capacité « norme circulaire » est le chiffre théorique ; la capacité opérationnelle en retire les places indisponibles (travaux). L'écart au 1er septembre 2026 est de 980 places (64 328 contre 63 348 ; métropole 59 589 / 58 636, outre-mer 4 739 / 4 712). Sur la norme circulaire, la densité serait de 139,9 % (calcul à partir de P2 tableau 6, le ministère ne publie pas ce ratio). Dire que la norme circulaire est « calculée autrement » est donc inexact ; le ministère ne dit pas explicitement que l'écart est dû aux travaux, c'est l'inférence la plus directe de ses deux définitions. Exemple parlant : MA La Roche-sur-Yon, norme circulaire 39, opérationnelle 17 (270,6 %, mais 117,9 % sur 39).

Écroué, détenu (P2 « Définitions et abréviations ») : « Est écrouée toute personne ayant fait l'objet d'une mise sous écrou […] hébergée au sein d'un établissement pénitentiaire ou non. » ; « Est détenue toute personne faisant l'objet d'une mesure privative de liberté à l'intérieur d'un établissement pénitentiaire. » ; « Est non détenue toute personne ayant fait l'objet d'une mise sous écrou mais ne faisant pas l'objet d'une mesure privative de liberté à l'intérieur d'un établissement pénitentiaire. Il s'agit des personnes placées en détention à domicile sous surveillance électronique ou en placement à l'extérieur sans hébergement. » Au 1er septembre 2026 : 107 700 écroués = 90 020 détenus + 17 680 non détenus (16 729 DDSE, 951 placements à l'extérieur non hébergés). La note 2 est conforme. Les semi-libertés (2 573) et placements à l'extérieur hébergés (211) restent comptés parmi les détenus. Le World Prison Brief le rend ainsi : « excludes 17,680 people not detained in penal institutions (écroués non détenus) ».

Maisons d'arrêt (P2) : « reçoivent les personnes prévenues en détention provisoire ainsi que les personnes condamnées dont la peine ou le reliquat de peine n'excède pas deux ans » : la note 4 est conforme. Le taux de 176,1 % est calculé hors places mineurs (note 1 du tableau 11). Réserve de méthode : l'OIP soutient que les moyennes officielles sont « largement sous-estimées » parce qu'elles mélangent quartiers d'hommes, de femmes, de mineurs, de semi-liberté (communiqué du 30 mai 2024, via Le Courrier de l'Atlas https://www.lecourrierdelatlas.com/surpopulation-carcerale-les-chiffres-du-gouvernement-sont-sous-estimes-selon-loip/ , page ouverte).

#### 5.3 Records et évolution sur un an

- Le 1er septembre 2026 est le plus haut niveau de toutes les séries lues : tableau 2 de P2 (24 mois, du 1er septembre 2024 au 1er septembre 2026, tous inférieurs, maximum antérieur 89 668 au 1er août 2026) et tableau d'évolution de P1 (septembres de 2016 à 2026, maximum antérieur 84 311 en 2025). C'est la première fois au-dessus de 90 000 (89 668 en août). La presse écrit « un nouveau record » (Sud Radio et La Gazette France, pages ouvertes). Les deux PDF du ministère lus n'emploient pas le mot « record » ; les notes « Infos Rapides Justice » lues non plus.
- Évolution sur un an (P2, page des chiffres) : détenus +6,8 % (84 311 à 90 020) ; écroués +6,2 % ; non détenus +3,4 % ; prévenus +9,7 % ; places opérationnelles +1,2 % (62 614 à 63 348) ; matelas au sol +51,8 % (5 500 à 8 347). Densité : 134,7 % à 142,1 %. La note trimestrielle du 15 octobre 2026 titre « + 7 % de personnes détenues sur un an » au 1er octobre.
- Le record est déjà battu. Au 1er octobre 2026 : 90 937 détenus (+7,2 % sur un an, 84 862), 63 452 places, densité 143,3 %, MA/QMA 178,0 %, 8 959 matelas au sol, 108 587 écroués (« Mesure de l'incarcération » d'octobre : https://www.justice.gouv.fr/sites/default/files/2026-11/mesure_mensuelle_01102026.pdf). Si le jeu fige septembre, il faut écrire « au 1er septembre 2026 » partout et ne pas laisser « record » sans date.

#### 5.4 Établissements ou quartiers à 120 % ou plus : 136, 138 ou 139 ?

Trois comptages officiels existent pour le 1er septembre 2026, dans deux documents du même ministère :

| Comptage | Valeur | Où | Détail |
|---|---|---|---|
| Tableau 24 (liste détaillée) | 136 | P2, dernière ligne du tableau 24 : « Au total, 63938 détenus et 136 établissements ou quartiers sont concernés » ; 136 lignes recomptées par script (31 à 200 % ou plus, 74 de 150 à 200 %, 31 de 120 à 150 %) | 121 MA/QMA, 9 CSL/QSL, 6 CD/QCD ; aucun MC/QMC ; 63 938 détenus |
| Page « Les chiffres au 1er septembre 2026 » | 138 | P2 : « 32 établissements ou quartiers ≥ 200 % ; 75 de 150 à 200 % ; 31 de 120 à 150 % » (32+75+31) ; les 280 structures de cette page : 32+75+31+22+120 | 32 et 75 au lieu de 31 et 74 du tableau 24 |
| « Mesure de l'incarcération », descriptif | 139 | P1 : 2 MC/QMC + 6 CD/QCD + 0 SAS + 9 CSL/QSL + 122 MA/QMA + 0 EPM/QM, soit 139 sur 324 structures ; 63 814 détenus | Compte 2 MC/QMC que le tableau 24 ne liste pas |

Le même décalage existe aux deux autres mois lus : au 1er août 2026, 134 (tableau 24), 136 (page des chiffres : 33+75+28), 138 (Mesure) ; au 1er octobre 2026, 133, 135 (40+70+25), 137. La page des chiffres dépasse toujours de 2 le tableau 24 ; la Mesure dépasse la page des chiffres de 1 à 2.

Explication : non écrite par le ministère. Hypothèse cohérente avec les chiffres : le tableau 24 ne liste que les « quartiers administratifs » (note sous le tableau : « les places femmes et mineurs sont ainsi comptabilisées au sein des quartiers QMA, QCD, QSL, SAS ou QMC »), alors que la Mesure compte « hors places mineurs » et inclut 2 quartiers maison centrale (205 à 210 détenus chaque mois), absents du tableau 24. L'écart de 2 entre le tableau 24 et la page des chiffres, constant sur trois mois, est le nombre de MC/QMC ; je n'ai pas pu le prouver. Aucune source de presse lue ne donne ce nombre.

Lequel est juste ? Le 136 est le seul qu'on peut vérifier ligne à ligne (liste publiée avec noms, places et densités) et il correspond au fichier du jeu. Le 138 est celui de la page de synthèse de la même brochure, d'où le ticket. Aucun des deux n'est une erreur. Recommandation : citer la liste (136) en disant « au moins 120 % », ou écrire « 136 à 139 selon la publication ». Détail à corriger : une ligne du tableau 24 est à 120,0 % exactement (CP Béziers, quartier de semi-liberté, 24 détenus pour 20 places) : « dépassent 120 % » est inexact, « atteignent ou dépassent » ou « au moins 120 % » est correct.

#### 5.5 Licence et version anglaise

Voir la section 7.

### 6. Notes « À savoir » : verdict et rédaction proposée (320 caractères au plus)

| N° | Verdict | Remarque | Rédaction proposée (nombre de caractères) |
|---|---|---|---|
| 1 | À corriger | Première moitié exacte (densité = détenus / places opérationnelles, celles « effectivement disponibles »). « Calculée autrement » est inexact : les deux capacités viennent du calcul de la même circulaire AP 88-05 G ; l'opérationnelle retire les places indisponibles (travaux). Source : P1 et P2 tableau 6 | « La densité carcérale rapporte les détenus aux places opérationnelles, soit celles effectivement disponibles (hors places en travaux). La capacité « norme circulaire » est plus large : 64 328 places contre 63 348 au 1er septembre 2026, soit 139,9 % de densité au lieu de 142,1 %. » (278) |
| 2 | Confirmée | Définitions du ministère reprises presque mot pour mot ; 17 680 = 16 729 + 951 ; 107 700 écroués | « Détenus et écroués diffèrent : les 107 700 écroués comptent aussi 17 680 personnes non détenues, en détention à domicile sous surveillance électronique (16 729) ou en placement à l'extérieur sans hébergement (951), au 1er septembre 2026. » (237) |
| 3 | À nuancer | « Que des PDF » : vrai du format sur data.gouv.fr (juillet 2019 à décembre 2022), mais ces PDF contiennent la densité ; le trou est celui des classeurs, pas des chiffres. « Avant février 2015, pas de tableau de densité » : contredit pour les PDF (tableau de densité dès octobre 2013 au moins), non vérifiable pour les classeurs : à retirer ou à limiter à « la courbe commence en février 2015 » | « De mi-2019 à 2022, data.gouv.fr ne propose que des PDF, pas de classeurs : la courbe montre ce trou au lieu de le combler, alors que ces PDF donnent la densité (103,4 % au 1er janvier 2021). Avant février 2015, elle n'est pas tracée. » (233) |
| 4 | À nuancer | 176,1 % et définition de la maison d'arrêt exacts ; 136 est un des trois comptages ; « dépassent » est faux pour une ligne à 120,0 % | « La moyenne nationale masque les maisons d'arrêt, où sont les prévenus et les condamnés à de courtes peines : 176,1 % au 1er septembre 2026. Selon la publication du ministère, 136 à 139 établissements ou quartiers ont une densité d'au moins 120 %. » (246) |

Si une des notes cite un établissement en tête : « CP Majicavo, quartier centre de détention : 273,7 % » (et non le centre entier, à 230,2 %), et pour La Roche-sur-Yon « 17 places opérationnelles seulement ».

### 7. Licence et version anglaise

Licence du jeu de données (métadonnées lues dans l'API de data.gouv.fr, https://www.data.gouv.fr/api/1/datasets/statistique-mensuelle-de-la-population-ecrouee-et-detenue-en-france/ ; page https://www.data.gouv.fr/datasets/statistique-mensuelle-de-la-population-ecrouee-et-detenue-en-france) :
- Producteur : Ministère de la Justice. Licence : identifiant `fr-lo`. Dernière mise à jour du jeu : 13 octobre 2026. Fréquence : mensuelle. 188 ressources (106 xlsx, 50 xls, 32 pdf).
- Liste des licences de la plateforme (https://www.data.gouv.fr/api/1/datasets/licenses/) : `fr-lo` = « Licence Ouverte / Open Licence » (sans numéro de version, lien historique vers `Licence_Ouverte.pdf`, 2014) ; `lov2` = « Licence Ouverte / Open Licence version 2.0 » (https://www.etalab.gouv.fr/licence-ouverte-open-licence). Ce sont deux identifiants distincts, et le jeu porte le premier, pas `lov2`.
- Donc, non, ce n'est pas la version 2.0 au sens de la plateforme. Que `fr-lo` désigne la version 1.0 (publiée par Etalab en octobre 2011, selon des résumés de moteur de recherche) est probable, mais je n'ai trouvé aucune page de data.gouv.fr qui l'écrive : l'ancien lien PDF redirige désormais vers une ressource du jeu « licence-ouverte-2-0 » (https://static.data.gouv.fr/resources/licence-ouverte-2-0/20240711-152120/licence-ouverte.pdf, illisible avec mes outils). Le pied de page de la page du jeu parle de « Open Licence 2.0 » : c'est le texte général du site, pas le champ de licence du jeu. À citer dans le jeu : « Licence Ouverte / Open Licence » avec la mention du producteur, sans écrire « 2.0 » sauf vérification.
- Obligation d'attribution (version 2.0, https://www.data.gouv.fr/pages/legal/licences/etalab-2.0/) : mentionner la source (a minima le nom du concédant) et la date de dernière mise à jour des informations ; compatible avec CC-BY. Texte de la version 1.0 non lu.
- Point de vigilance : les mentions légales de justice.gouv.fr (https://www.justice.gouv.fr/mentions-legales, lues) disent que les contenus sont « proposés sous licence ouverte » (lien vers la version 2.0), puis ajoutent trois conditions (intégrité, citation du ministère avec la date, « droits de reproduction réservés et strictement limités ») et « toutes diffusions ou utilisations à des fins commerciales ou publicitaires est interdite ». Cela semble contredire la Licence Ouverte 2.0, qui autorise la réutilisation y compris commerciale (je le tiens de ma connaissance de la licence : le texte n'a pas pu être relu ici). Pour les PDF hébergés sur justice.gouv.fr, ce texte s'applique ; pour les ressources du jeu de data.gouv.fr, la licence du jeu s'applique. Un jeu éducatif non commercial n'est concerné par aucune des deux restrictions ; si le jeu devenait payant ou publicitaire, il faudrait demander une précision au ministère.
- Version anglaise : aucune version anglaise du jeu de données ni des PDF mensuels (descriptions et libellés en français). La licence existe en anglais : les liens de l'API ont `.../2014/05/Open_Licence.pdf` (pour `fr-lo`) et `.../2018/11/open-licence.pdf` (pour `lov2`) ; le titre officiel est bilingue. Pour un texte anglais des chiffres : World Prison Brief, https://www.prisonstudies.org/country/france (90 020 détenus, « official capacity » 63 348, « occupancy level (based on official capacity) » 142,1 %, 17 680 « écroués non détenus » exclus, au 1er septembre 2026) ; il ne définit pas la capacité. Les libellés anglais du jeu doivent donc être traduits par le jeu lui-même : « operational places / capacity » et « prison density / occupancy rate » sont raisonnables ; « écroué » n'a pas d'équivalent exact (World Prison Brief le garde en français).

### 8. Conclusion

#### Écarts, du plus important au moins important

1. Décompte des établissements à 120 % ou plus (Écart expliqué) : 136 (tableau 24), 138 (page des chiffres), 139 (Mesure de l'incarcération). Pas d'erreur du script ; choisir une base et la nommer, ou dire « 136 à 139 ». La formule « dépassent 120 % » est inexacte (une ligne à 120,0 %).
2. Note 1, « norme circulaire, calculée autrement » (Écart) : même circulaire de calcul ; l'opérationnelle exclut les places indisponibles ; 64 328 contre 63 348.
3. Note 3 (Écart) : les PDF de 2019 à 2022 donnent la densité, donc le trou est celui du format ; « avant février 2015, pas de tableau de densité » est contredit par les PDF (octobre 2013 à décembre 2014), invérifiable pour les classeurs.
4. Record (Écart de date) : 90 020 est un record au 1er septembre 2026, mais le 1er octobre 2026 donne 90 937 (143,3 %). L'instantané n'est plus le dernier chiffre publié à la date du jour.
5. Intitulé « CP Majicavo 273,7 % » (réserve) : c'est le quartier centre de détention (230,2 % pour le CP entier). « MA La Roche-sur-Yon 270,6 % » repose sur 17 places opérationnelles (117,9 % sur la capacité norme circulaire de 39).
6. Licence (à signaler) : `fr-lo` n'est pas `lov2` (version 2.0) ; les mentions légales du ministère interdisent l'usage commercial ou publicitaire, ce qui semble en contradiction avec la Licence Ouverte (texte non relu ici).
7. Mensuel / trimestriel (Écart expliqué) : 13 à 14 détenus d'écart après ajout de la Polynésie française et de la Nouvelle-Calédonie, cause du résidu non documentée ; 49 non détenus d'écart au 1er avril 2026, non expliqués. Aucune densité dans les statistiques trimestrielles.
8. Aucune source de presse lue ne donne le nombre d'établissements à 120 % ou plus ; les sources secondaires reprennent toutes le ministère.

Tout le reste est Conforme : les 7 chiffres de septembre 2026, le classement de tête, les 5 points de 2023 à 2026 et les 3 points de 2015, 2017 et 2019, chacun lu dans le PDF du ministère.

#### URL consultées

PDF du ministère (justice.gouv.fr/sites/default/files/) :
- 2026-10/mesure_mensuelle_01092026.pdf ; 2026-10/statistique_etablissements_personnes_ecrouees_01092026.pdf
- 2026-08/mesure_mensuelle_01082026.pdf ; 2026-08/statistique_etablissements_personnes_ecrouees_01082026.pdf
- 2026-11/mesure_mensuelle_01102026.pdf ; 2026-11/statistique_etablissements_personnes_ecrouees_01102026.pdf
- 2026-05/mesure_mensuelle_01052026.pdf ; 2026-04/mesure_mensuelle_01042026.pdf
- 2025-12/mesure_mensuelle_01122025.pdf ; 2025-08/mesure_mensuelle_01082025.pdf ; 2025-05/Mesure_mensuelle_2505.pdf
- 2024-08/Mesure_mensuelle_2024-08-01.pdf ; 2023-11/mesure_mensuelle_01112023.pdf
- 2023-04/Mesure_mensuelle_01022022.pdf ; 2023-04/Mesure_incarceration_janvier_2021_v3.pdf ; 2023-04/Mesure_incarceration_janvier2020.pdf
- 2023-05/Mesure_mensuelle_incarceration_avril2019.pdf ; 2023-05/mensuelle_mars_2019.pdf ; 2023-05/Mesure_mensuelle_incarceration_janvier2019.pdf ; 2023-05/mensuelle_avril_2017.pdf ; 2023-05/mensuelle_fevrier_2015.pdf
- 2023-05/mensuelle_decembre_2014.pdf ; 2023-05/mensuelle_juin_2014.pdf ; 2023-05/mensuelle_octobre_2013.pdf ; 2023-05/mensuelle_inTERnet_dec2010.pdf ; 2023-05/mensuelle_inTERnet_aout09.pdf

Statistiques trimestrielles et notes (justice.gouv.fr) :
- https://www.justice.gouv.fr/documentation/etudes-et-statistiques/statistiques-trimestrielles-milieu-ferme
- https://www.justice.gouv.fr/sites/default/files/2026-01/STMF_2026_1_1.xlsx ; .../2026-04/STMF_2026_4_1.xlsx ; .../2026-07/STMF_2026_7_1.xlsx (non lisible) ; .../2026-10/STMF_2026_10_1.xlsx ; .../2025-10/STMF_2025_10.xlsx, .../2025-07/STMF_2025_07.xlsx, .../2025-04/STMF_2025_04.xlsx (téléchargés, non lus)
- https://www.justice.gouv.fr/documentation/etudes-et-statistiques/au-1er-octobre-2026-7-personnes-detenues ; https://www.justice.gouv.fr/documentation/etudes-et-statistiques/au-1er-juillet-2026-52-personnes-detenues
- https://www.justice.gouv.fr/mentions-legales

Presse et autres :
- https://www.sudradio.fr/societe/prisons-90-020-detenus-en-france-au-1er-septembre-un-nouveau-record ; https://www.lagazettefrance.fr/article/prisons-90-020-detenus-en-france-au-1er-septembre-un-nouveau-record
- https://www.lnc.nc/print/1431274 (article du 2 juin 2026 sur les chiffres du 1er mai 2026, qui cite l'AFP selon un résumé de moteur de recherche : 88 654 ; 140 % ; MA 172,6 % ; 33 établissements à 200 % ou plus ; page ouverte)
- https://oip.org/communique/nouveau-record-du-nombre-de-personnes-detenues-jusqua-lasphyxie/ ; https://www.lecourrierdelatlas.com/surpopulation-carcerale-les-chiffres-du-gouvernement-sont-sous-estimes-selon-loip/
- https://www.mayottehebdo.com/actualite/breves/majicavo-la-plus-surpeuplee-des-prisons-francaises (article de 2023, 278,1 % ; non utilisé pour 2026)
- https://www.prisonstudies.org/country/france
- Résumés de moteur de recherche seulement (pages non ouvertes) : https://www.labase-lextenso.fr/gazette-du-palais/2026-n17/vers-une-forme-de-regulation-carcerale-GPL490x5 ; https://www.sudradio.fr/faits-divers/plus-de-70-000-personnes-en-prison-au-1er-avril-2017-un-record ; Europe 1, Brut, 75secondes
- Sans apport : https://www.senat.fr/questions/base/2024/qSEQ241001313.html ; https://www.assemblee-nationale.fr/dyn/16/questions/QANR5L16QE18331.pdf (question retirée, sans réponse)

data.gouv.fr et licence :
- https://www.data.gouv.fr/datasets/statistique-mensuelle-de-la-population-ecrouee-et-detenue-en-france ; https://www.data.gouv.fr/api/1/datasets/statistique-mensuelle-de-la-population-ecrouee-et-detenue-en-france/ ; https://www.data.gouv.fr/api/1/datasets/licenses/
- https://www.data.gouv.fr/pages/legal/licences/etalab-2.0/ ; https://www.etalab.gouv.fr/licence-ouverte-open-licence ; https://www.etalab.gouv.fr/wp-content/uploads/2014/05/Licence_Ouverte.pdf (redirigé) ; https://static.data.gouv.fr/resources/licence-ouverte-2-0/20240711-152120/licence-ouverte.pdf (illisible)

## Mises à jour

**10/11/2026** (#307 de l'app) : le 1er octobre 2026.
- **Le script** (`scripts/briefings/prisonDensity.ts`, PR Mitchnsun/moi-president#334) tournait court : data.gouv.fr liste encore à leur ancienne adresse de stockage (`www.data.gouv.fr/storage/f/2014-07-08T…`) les neuf classeurs d'octobre 2013 à juin 2014, qui répondent 404 ; sa dernière vérification les lisait le 15/02/2026. Décembre 2013 à juin 2014 sont les sept premiers mois de `densityUntil2019`. Le script lit désormais la copie de l'Internet Archive du 01/04/2026, seulement si son empreinte SHA-1 est celle que data.gouv.fr avait enregistrée (`analysis:checksum`) ; une série qui ne commence plus à son premier mois (2013-12, 2023-01) fait échouer le script. Le ministère n'a que des PDF pour ces mois ; aucune autre copie des classeurs n'a été trouvée.
- **Octobre 2026** : data.gouv.fr s'arrête à septembre ; le classeur du 1er octobre vient de la page « Statistiques mensuelles de la population détenue et écrouée pour l'année 2026 » du ministère, « Mis à jour le 02 novembre 2026 » (https://www.justice.gouv.fr/sites/default/files/2026-11/statistique_etablissements_personnes_ecrouees_01102026.xlsx).
- **L'instantané** : les séries d'avant 2019 sont inchangées, de décembre 2013 à mars 2019 ; les séries depuis 2023 gagnent octobre 2026 (143,3 %, 90 937 détenus, 63 452 places) ; la liste du tableau 24 compte 133 lignes ; densités par type de quartier et matelas au sol au 1er octobre.
- **Double vérification**, sur les deux PDF du ministère pour le 1er octobre 2026, lus avec `pdftotext` :
  - « Mesure de l'incarcération » (https://www.justice.gouv.fr/sites/default/files/2026-11/mesure_mensuelle_01102026.pdf) : 63 452 places opérationnelles, densité 143,3 %, MA/QMA 178,0 %, 8 959 matelas au sol, 108 587 écroués, 90 937 détenus, 17 650 non détenus, 137 établissements ou quartiers à 120 % ou plus ;
  - la brochure mensuelle (`statistique_etablissements_personnes_ecrouees_01102026.pdf`) : capacité norme circulaire 64 326 et capacité opérationnelle 63 452 (tableaux par direction interrégionale), 16 693 en détention à domicile sous surveillance électronique et 957 en placement à l'extérieur sans hébergement (17 650), MA/QMA 178,0 %, et dans le tableau 24 (rangé par direction interrégionale, que le fichier trie par densité) CP Majicavo (CD/QCD) à 284,2 %, CP Faaa Nuutania (MA/QMA) à 270,9 %, MA La Roche-sur-Yon à 270,6 % et, la plus basse, CSL Corbeil-Essonnes à 122,5 % ; sa dernière ligne : « Au total, 64199 détenus et 133 établissements ou quartiers sont concernés ».
  - Conforme.
- **Notes** : 1 (64 326 places contre 63 452), 2 (108 587 écroués, 17 650 non détenus, 16 693 et 957) et 4 (178,0 %, 133 à 137 établissements) passées au 1er octobre 2026 ; 3 inchangée.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
