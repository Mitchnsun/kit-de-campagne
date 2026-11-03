# `crime` · Délinquance enregistrée

**Vérifiée le 02/11/2026** : 14 séries sur 16 conformes au bilan « Insécurité et délinquance en 2025 » du SSMSI (juillet 2026), à l'arrondi à la centaine près ; homicides et tentatives exacts. La somme des régions est bien le « France » du bilan (métropole et DROM). Chiffre clé corrigé : 975 homicides en 2025 est « stable » (0 %), comme l'écrit le SSMSI. Notes corrigées : la part des amendes forfaitaires (majoritaire depuis 2022, 70 % en 2025), les taux de plainte, les autres causes de la hausse des violences enregistrées.

**Écarts ouverts** : les escroqueries du fichier sont 0,6 % sous le bilan chaque année (445 463 contre 448 300 en 2025), et les mis en cause pour trafic de stupéfiants de 0,3 % au-dessus. Les évolutions sont les mêmes ; aucune source lue n'explique ces écarts. Les taux départementaux n'ont pas de source indépendante publiée (seul l'Atlas départemental, non ouvert, les donnerait) ; un taux d'homicides peut reposer sur une seule victime (Aube, 0,003 ‰), alors que le bilan masque ses propres effectifs de 1 à 4.

| Champ | Valeur |
| --- | --- |
| Indicateur | `crime`, ticket #30, dossier « Sécurité et justice » (statut `planned`) ; l'avertissement « la délinquance enregistrée n'est pas toute la délinquance » est dans les locales de l'app (PO, 02/11/2026) |
| Données | `briefings/data/crime.json`, écrit par `yarn briefings crime` le 2026-11-02, puis le 2026-11-03 avec les effectifs par département (voir « Mises à jour ») |
| Source | SSMSI, « Bases statistiques communale, départementale et régionale de la délinquance enregistrée par la police et la gendarmerie nationales », data.gouv.fr, fichiers « REG » et « DEP » de l'édition mise à jour le 09/07/2026 ; Licence Ouverte 2.0 ; en français seulement |
| Séries | Les 18 indicateurs des bases, France = somme des régions (métropole et DROM), annuels de 2016 à 2025, chacun dans son unité de compte (victimes, infractions, véhicules, mis en cause), dont l'usage de stupéfiants avec et hors amende forfaitaire délictuelle |
| Valeurs par département | Pour 2025, le taux pour 1 000 habitants de chaque indicateur (pour 1 000 logements pour les cambriolages), selon le lieu de commission, et le nombre sur lequel repose chaque taux (`counts`, colonne `nombre` du fichier « DEP », dans l'unité de compte de l'indicateur) : la carte masque un taux fondé sur 1 à 4 faits (décision du PO du 03/11/2026) |
| Chiffre clé | 975 homicides en 2025, stable (976 en 2024) |
| Première édition | À remplir à la publication |

À actualiser : chaque été, à la nouvelle édition des bases (les données de l'année sont consolidées jusqu'en mai). Ne pas confondre avec la « première photographie » de janvier (982 homicides pour 2025).

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans télécharger les fichiers du jeu data.gouv.fr. Il a lu en entier le bilan annuel du SSMSI. Son rapport, tel quel :

Date de la vérification : 2026-11-02. Vérification faite uniquement sur le web, sans ouvrir les CSV « REG » et « DEP » du jeu data.gouv.fr 621df2954fa5a3b5a023e23c (aucun fichier de ce jeu n'a été téléchargé, l'Atlas départemental PDF compris).

### 0. Sources utilisées et limites de la vérification


URL de [Bilan] : https://statistiques.interieur.gouv.fr/ssmsi/files/ssmsi/2026-07/Ins%C3%A9curit%C3%A9%20et%20d%C3%A9linquance%20en%202025%20-%20Bilan%20statistique%20-%20%C3%A9dition%202026%20-%20SSMSI.pdf
(Copie miroir sur le site du ministère, trouvée par recherche, non ouverte : https://www.interieur.gouv.fr/fr/content/download/139762/1102438/file/Ins%C3%A9curit%C3%A9%20et%20d%C3%A9linquance%20en%202025%20-%20Bilan%20statistique%20-%20%C3%A9dition%202026%20-%20SSMSI.pdf)

**Ce que je n'ai pas pu faire**
- Les pages HTML de interieur.gouv.fr et de statistiques.interieur.gouv.fr (page de la publication, communiqué du 09/07/2026, page anglaise `/ssmsi/en/node/1488`) répondent 403 (écran « Attention Required » de Cloudflare). Je ne les ai pas contournées. Ce qui en est dit ci-dessous vient donc seulement de **résumés du moteur de recherche** et est signalé comme tel.
- Le « fichier de données complémentaires » du bilan (valeurs exactes, non arrondies) n'a pas été ouvert (c'est un fichier du jeu de données). Le bilan donne ses effectifs 2025 arrondis à la centaine (sauf homicides et tentatives d'homicide) : tolérance de comparaison de ±50 pour les valeurs du fichier.
- Taux départementaux : voir section 4 (« Non trouvé » comme source indépendante). L'Atlas départemental 2025 (PDF, ressource du jeu de données) existe mais je ne l'ai pas ouvert, conformément à la règle « pas ses fichiers ».

### 1. Concordance des totaux France 2016, 2023, 2024, 2025

#### 1.1 Champ géographique du bilan (point 1)

- [Bilan] p.6 : « Les résultats portent sur la France (France métropolitaine et départements et régions d'outre-mer). » Les données sont « définitives et ne seront plus révisées, sauf évolution éventuelle du périmètre des indicateurs de référence ».
- [Bilan] p.67 (Sources et méthodes, « B) Le champ géographique ») : les bases du SSMSI couvrent tout le territoire de la République (métropole, DROM et **collectivités d'outre-mer**), « Toutefois dans cet ouvrage, le champ retenu est limité à la France métropolitaine et aux départements et régions d'outre-mer. Les collectivités d'outre-mer font l'objet d'un traitement spécifique dans l'Atlas départemental ». « Les faits commis à l'étranger sont exclus des bases statistiques du SSMSI. »
- Réponse au point 1 : le SSMSI publie la « France » du bilan **avec les DROM** (Guadeloupe, Martinique, Guyane, La Réunion, Mayotte : Mayotte et la Guyane sont citées dans les analyses et la population de Mayotte vient du recensement 2017, p.73) et **sans les COM**. Le tableau des taux (Figure 9, p.21) sépare « France », « France métropolitaine » et « DROM ».
- Description du jeu data.gouv.fr (API, métadonnées seulement) : l'historique mentionne une « extension aux DROM » ; la couverture spatiale affichée est « France métropolitaine » (métadonnée incohérente avec l'historique) ; l'Atlas 2024 est décrit comme couvrant « tous les territoires (métropole, DROM, COM) ». Je n'ai pas pu vérifier si les fichiers REG/DEP contiennent des COM.
- Constat : pour 14 séries sur 16, la somme des régions du fichier est égale au total « France » du bilan à l'arrondi près. Le périmètre de la somme des régions est donc le même que celui du bilan (métropole + DROM) pour ces séries. Aucun écart lié aux COM n'est visible.
- Révisions : l'édition de juillet 2026 est la version définitive, consolidée avec les requalifications jusqu'en mai 2026 ([Bilan] p.6, p.71). Pas de décalage de révision entre le fichier (édition du 09/07/2026) et le bilan. Les chiffres de la « première photographie » de janvier 2026 sont plus anciens (voir 1.4).
- Précision importante pour les homicides : [Bilan] p.63, note 2 : « le nombre d'homicides publié ne correspond pas à celui issu de la base victime car ce dernier est retraité ». Les valeurs du fichier (911, 996, 976, 975) sont égales aux valeurs publiées (retraitées), pas à un brut.

#### 1.2 Tableaux par indicateur (source des valeurs « trouvées » : [Bilan] Annexe 1, p.186, et Figure 1, p.7)

Verdict « Conforme » = égal à l'arrondi près (±50, ou exact pour homicides et tentatives).

**Homicides (victimes)**
| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2016 | 911 | 911 | [Bilan] Annexe 1 p.186 | Conforme |
| 2023 | 996 | 996 | idem | Conforme |
| 2024 | 976 | 976 | idem | Conforme |
| 2025 | 975 | 975 (« stable par rapport à 2024 (976) ») | idem + p.7 (Lecture) | Conforme |
| Chiffre clé « en baisse » | « 975 en 2025, en baisse » | SSMSI : « stable », évolution 2025 = 0 %, « mettant fin à l'évolution observée entre 2020 et 2023 » (p.7, p.10) ; Avant-propos, p.3 : « 12 sont en hausse, 5 en baisse et un, celui des homicides, est stable » | [Bilan] p.3, 7, 10 | **Écart** (formulation, voir conclusion) |

**Tentatives d'homicide (victimes)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 2 259 | 2 259 | [Bilan] Annexe 1 | Conforme |
| 2023 | 4 015 | 4 015 | idem | Conforme |
| 2024 | 4 290 | 4 290 | idem | Conforme |
| 2025 | 4 477 | 4 477 | idem | Conforme |

**Violences physiques intrafamiliales (victimes)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 113 821 | 113 800 | [Bilan] Annexe 1 | Conforme (arrondi) |
| 2023 | 238 211 | 238 200 | idem | Conforme (arrondi) |
| 2024 | 244 360 | 244 400 | idem | Conforme (arrondi) |
| 2025 | 256 681 | 256 700 | idem + p.7 | Conforme (arrondi) |

**Violences physiques hors cadre familial (victimes)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 163 447 | 163 400 | [Bilan] Annexe 1 | Conforme (arrondi) |
| 2023 | 205 896 | 205 900 | idem | Conforme (arrondi) |
| 2024 | 205 459 | 205 500 | idem | Conforme (arrondi) |
| 2025 | 215 728 | 215 700 | idem | Conforme (arrondi) |

**Violences sexuelles (victimes)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 51 913 | 51 900 | [Bilan] Annexe 1 | Conforme (arrondi) |
| 2023 | 114 079 | 114 100 | idem | Conforme (arrondi) |
| 2024 | 122 444 | 122 400 | idem | Conforme (arrondi) |
| 2025 | 132 143 | 132 100 | idem | Conforme (arrondi) |

**Vols avec armes (infractions)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 10 907 | 10 900 | [Bilan] Annexe 1 | Conforme (arrondi) |
| 2023 | 8 679 | 8 700 | idem | Conforme (arrondi) |
| 2024 | 8 582 | 8 600 | idem | Conforme (arrondi) |
| 2025 | 7 913 | 7 900 | idem | Conforme (arrondi) |

**Vols violents sans arme (infractions)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 94 758 | 94 800 | [Bilan] Annexe 1 | Conforme (arrondi) |
| 2023 | 54 270 | 54 300 | idem | Conforme (arrondi) |
| 2024 | 48 292 | 48 300 | idem | Conforme (arrondi) |
| 2025 | 49 193 | 49 200 | idem | Conforme (arrondi) |

**Vols sans violence contre des personnes (victimes entendues)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 709 436 | 709 400 | [Bilan] Annexe 1 | Conforme (arrondi) |
| 2024 | 607 772 | 607 800 | idem | Conforme (arrondi) |
| 2025 | 622 059 | 622 100 | idem | Conforme (arrondi) |

**Cambriolages de logement (infractions ; unité « logements » dans la déclinaison territoriale)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 248 887 | 248 900 | [Bilan] Annexe 1 | Conforme (arrondi) |
| 2024 | 218 156 | 218 200 | idem | Conforme (arrondi) |
| 2025 | 211 596 | 211 600 | idem | Conforme (arrondi) |

**Vols de véhicule (véhicules)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 164 797 | 164 800 | [Bilan] Annexe 1 | Conforme (arrondi) |
| 2024 | 137 580 | 137 600 | idem | Conforme (arrondi) |
| 2025 | 124 816 | 124 800 | idem | Conforme (arrondi) |

**Vols dans les véhicules (véhicules)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 272 984 | 273 000 | [Bilan] Annexe 1 | Conforme (arrondi) |
| 2024 | 256 060 | 256 100 | idem | Conforme (arrondi) |
| 2025 | 233 440 | 233 400 | idem | Conforme (arrondi) |

**Vols d'accessoires sur véhicules (véhicules)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 107 486 | 107 500 | [Bilan] Annexe 1 | Conforme (arrondi) |
| 2024 | 96 053 | 96 100 | idem | Conforme (arrondi) |
| 2025 | 95 311 | 95 300 | idem | Conforme (arrondi) |

**Destructions et dégradations volontaires (infractions)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 626 565 | 626 600 | [Bilan] Annexe 1 | Conforme (arrondi) |
| 2024 | 528 849 | 528 800 | idem | Conforme (arrondi) |
| 2025 | 539 112 | 539 100 | idem | Conforme (arrondi) |
| Périmètre | « crimes et délits » implicite | Le bilan écrit « (y compris contraventions) » pour cet indicateur (p.10) ; il est construit sur NFI 05.C1, 05.C2, 02.F5.2.1, 02.F5.2.2 (Figure 5, p.70) | [Bilan] p.10, p.70 | Conforme, nuance à savoir |

**Escroqueries et fraudes aux moyens de paiement (victimes)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 249 477 | 250 900 | [Bilan] Annexe 1 | **Écart** : -1 423 (-0,57 %) |
| 2024 | 414 653 | 417 300 | idem | **Écart** : -2 647 (-0,63 %) |
| 2025 | 445 463 | 448 300 | idem | **Écart** : -2 837 (-0,63 %) |
| Évolution 2024-2025 | +7,43 % | +7 % (417 300 → 448 300 = +7,43 %) | [Bilan] p.7 | Conforme |

Le fichier est inférieur au bilan d'environ 0,6 % chaque année : l'écart est stable, la dynamique est identique. Aucune source lue n'explique cet écart. Indices utiles, sans valeur d'explication : [Bilan] p.167 (note sous la Figure 9) précise que, contrairement aux autres indicateurs (déclinés selon le lieu de commission), les escroqueries sont déclinées selon **le lieu de résidence de la victime** « compte tenu de la prévalence des escroqueries sur internet » ; p.39 (Éclairage 2, note 1) : le taux d'élucidation par département des escroqueries est lui aussi décliné par département de résidence de la victime. Une piste à vérifier par le producteur du fichier (pas une explication sourcée) : des victimes sans région d'attribution dans les fichiers régionaux (lieu de commission ou de résidence inconnu, hors DROM) seraient comptées dans le total national mais pas dans la somme des régions.

**Trafic de stupéfiants (mis en cause)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 40 823 | 40 700 | [Bilan] Annexe 1 | **Écart** : +123 (+0,30 %) |
| 2024 | 52 437 | 52 300 | idem | **Écart** : +137 (+0,26 %) |
| 2025 | 57 287 | 57 100 | idem + p.150 | **Écart** : +187 (+0,33 %) |
| Évolution 2024-2025 | +9,25 % | +9 % | [Bilan] p.7 | Conforme |

**Usage de stupéfiants (mis en cause)**
| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| 2016 | 182 543 | 182 400 | [Bilan] Annexe 1 | **Écart** : +143 (+0,08 %) |
| 2024 | 290 756 | 290 700 | idem | Écart minime : +56 (+0,02 %), à la limite de l'arrondi |
| 2025 | 309 854 | 309 800 | idem + p.150 | Écart minime : +54 (+0,02 %), à la limite de l'arrondi |
| dont AFD 2016 | 0 | 0 : les AFD pour usage n'existent pas avant 2020 (graphique p.155 : ligne à 0 de 2016 à 2019 ; environ 30 000 en 2020) | [Bilan] p.155 | Conforme |
| dont AFD 2024 | 196 601 | 196 600 | [Bilan] p.155 (Figure 5) | Conforme |
| dont AFD 2025 | 217 651 | 217 700 (« 70 % des mis en cause pour usage ») | [Bilan] p.155 | Conforme (arrondi) |
| hors AFD 2024 | 94 155 | 94 100 | [Bilan] p.155 | Conforme (arrondi) |
| hors AFD 2025 | 92 203 | 92 200 | [Bilan] p.155 | Conforme |

Pour les mis en cause (trafic, usage), le fichier est légèrement au-dessus du bilan (de 0,02 % à 0,33 %). Pas d'explication dans les sources lues. Piste non sourcée : le bilan compte les mis en cause « avec dédoublonnage » au niveau national ([Bilan] Figure 5, p.70 ; une même personne peut être mise en cause dans plusieurs infractions, p.68) ; une somme de régions peut compter deux fois une personne mise en cause dans deux régions. Pour les escroqueries c'est l'inverse (fichier plus bas), donc cette piste ne l'explique pas.

**Cohérence interne vérifiée** : AFD + hors AFD = usage (217 651 + 92 203 = 309 854 ; 196 601 + 94 155 = 290 756).

#### 1.3 Évolution 2024-2025 : point 2 (source : [Bilan] Figure 1, p.7, et texte p.6-13)

| Indicateur | Évolution 2025 selon le SSMSI | Calcul sur les valeurs du fichier (2024 → 2025) | Verdict |
|---|---|---|---|
| Homicides | 0 % (stable) | -0,1 % (976 → 975) | Conforme (le mot « en baisse » est à corriger) |
| Tentatives d'homicide | +4 % | +4,4 % | Conforme |
| Violences physiques (total) | +5 % | non fourni dans le fichier | n/a |
| Violences physiques intrafamiliales | +5 % | +5,0 % | Conforme |
| Violences physiques hors cadre familial | +5 % | +5,0 % | Conforme |
| Violences sexuelles | +8 % (dont viols et tentatives +9 %) | +7,9 % | Conforme |
| Vols avec armes | -8 % | -7,8 % | Conforme |
| Vols violents sans arme | +2 % (première hausse depuis 2016) | +1,9 % | Conforme |
| Vols sans violence contre des personnes | +2 % | +2,3 % | Conforme |
| Cambriolages de logement | -3 % | -3,0 % | Conforme |
| Vols de véhicule | -9 % | -9,3 % | Conforme |
| Vols dans les véhicules | -9 % | -8,8 % | Conforme |
| Vols d'accessoires sur véhicules | -1 % | -0,8 % | Conforme |
| Destructions et dégradations volontaires | +2 % | +1,9 % | Conforme |
| Usage de stupéfiants | +7 % | +6,6 % | Conforme |
| Trafic de stupéfiants | +9 % | +9,3 % | Conforme |
| Escroqueries et fraudes aux moyens de paiement | +7 % | +7,4 % | Conforme |

Synthèse du SSMSI ([Bilan] p.3) : sur les 18 indicateurs suivis, 12 sont en hausse, 5 en baisse (vols avec armes, cambriolages, vols de véhicule, vols dans les véhicules, vols d'accessoires) et 1 (homicides) est stable. Le bilan note aussi que plusieurs indicateurs restent à des niveaux inférieurs à ceux d'avant la crise sanitaire. Évolutions annuelles moyennes 2016-2025 ([Bilan] Figure 2, p.9) : homicides +1 %, tentatives +8 %, violences physiques intrafamiliales +9 %, hors cadre familial +3 %, violences sexuelles +11 %, vols avec armes -4 %, vols violents sans arme -7 %, cambriolages -2 %, usage +6 %, trafic +4 %, escroqueries +7 %.

#### 1.4 Valeurs de janvier 2026 (« première photographie ») et de juillet 2026 : à ne pas confondre

Le bilan définitif a révisé les chiffres de janvier 2026 ([Bilan] Figure 7, p.72). Les médias de février ou janvier citent encore les valeurs provisoires :

| Indicateur | Janvier 2026 (A) | Juillet 2026 (B) | Évolution 2025 (A → B) |
|---|---|---|---|
| Homicides | 982 | 975 | +1 % → 0 % |
| Tentatives d'homicide | 4 501 | 4 477 | +5 % → +4 % |
| Violences physiques intrafamiliales | 256 900 | 256 700 | +5 % → +5 % |
| Violences sexuelles | 132 300 | 132 100 | +8 % → +8 % |
| Vols avec armes | 8 000 | 7 900 | -7 % → -8 % |
| Usage de stupéfiants | 307 200 | 309 800 | +6 % → +7 % (changement de date retenue pour les AFD : +2 614 personnes) |
| Trafic de stupéfiants | 56 600 | 57 100 | +8 % → +9 % |
| Escroqueries | 448 700 | 448 300 | +8 % → +7 % |

Les valeurs du fichier correspondent à juillet (B), pas à janvier (A). Presse confirmant les valeurs de janvier (lues en entier) : https://www.connexionfrance.com/news/crime-in-france-in-2025-burglaries-and-car-thefts-fall-but-fraud-rises/767821 (982 homicides, 56 600 mis en cause pour trafic, usage « just over 307,000 ») ; https://www.banquedesterritoires.fr/les-atteintes-aux-personnes-la-hausse-celles-aux-biens-en-baisse-en-2025 (29 janvier 2026).

Presse sur le bilan définitif : https://www.cnews.fr/france/2026-07-09/insecurite-viols-violences-physiques-tentatives-dhomicide-plusieurs-indicateurs (page en 403 : **résumé du moteur de recherche seulement** : « jeudi 9 juillet », 975 homicides stables, tentatives +4 %, escroqueries +7 %) ; https://france-statistiques.fr/evolution-homicides-france-2017-2025/ (site secondaire, lu : 975 en 2025, 996 en 2023, 826 en 2017, « France métropolitaine et DROM », « tableau de synthèse ... édition juillet 2026 »). Un chiffre discordant de 1 268 homicides en 2025 (Yahoo Actualités) n'apparaît que dans un résumé de moteur de recherche, hors bilan, non vérifié : ne pas l'utiliser.

### 2. Notes « À savoir » : confirmer, corriger ou nuancer

#### Note 1 : « Ce sont les crimes et délits enregistrés par la police et la gendarmerie : une partie seulement de la délinquance, car beaucoup de victimes ne portent pas plainte. »

**Verdict : confirmée, avec deux nuances (périmètre et stupéfiants).**

Citations du bilan :
- p.6 : « Le bilan ne couvre toutefois pas encore l'intégralité de la délinquance enregistrée : 87 % des crimes et 74 % des délits non routiers y sont suivis. » et « de nombreuses personnes ne portent pas plainte, ce qui tend à sous-estimer l'ampleur de la délinquance à partir des infractions enregistrées par la police et la gendarmerie nationales. »
- p.65 : la délinquance enregistrée « ne permet pas de mesurer exhaustivement le niveau de la délinquance : sous-estime parfois lourdement les infractions pour lesquelles les taux de plainte sont faibles (atteintes aux personnes) ; dépend des pratiques et des consignes de gestion et/ou de saisie ; dépend des évolutions juridiques ».
- p.8-9 (taux de dépôt de plainte estimés en 2023, enquête Vécu et ressenti en matière de sécurité, 18 ans et plus, métropole, Martinique, Guadeloupe, La Réunion) : violences physiques (hors vol) 21 % ; violences sexuelles physiques 6 % ; violences sexuelles non physiques 2 % ; violences conjugales 16 % ; cambriolage avec effraction de la résidence principale 41 % (vols : 57 %) ; vol de voiture 33 % ; vol avec violence ou menace 25 % ; arnaques avec perte d'argent 14 % ; débits frauduleux 11 %.
- p.67 (champ) : les polices municipales, les opérateurs de transport (SNCF, RATP), une grande partie de la délinquance environnementale, certaines formes de délinquance douanière, économique et financière, les mains courantes sont **hors champ** des bases. Les contraventions sont incluses dans certains indicateurs (destructions et dégradations volontaires, p.10), donc « crimes et délits » est un raccourci (le bilan écrit « crimes et délits essentiellement », p.6).
- p.65 : les infractions sans victime directe (stupéfiants) ne sont pas mesurables par enquête de victimation ; elles sont constatées à l'initiative des services (p.61 : « mais aussi sur l'initiative des forces de sécurité intérieure »). Pour elles, « car beaucoup de victimes ne portent pas plainte » ne s'applique pas (voir note 2 et 3).

Rédaction proposée : « Ce sont les infractions enregistrées par la police et la gendarmerie nationales (des crimes et des délits pour l'essentiel), pas toute la délinquance : beaucoup de victimes ne portent pas plainte (en 2023, 21 % des victimes de violences physiques et 6 % de celles de violences sexuelles physiques l'avaient fait, selon l'enquête de victimation du SSMSI). »

#### Note 2 : « Les chiffres suivent aussi les plaintes et l'activité des services : la hausse des violences sexuelles et intrafamiliales enregistrées traduit en partie une plus grande propension à porter plainte. »

**Verdict : confirmée dans l'esprit, à nuancer (« en partie » est juste mais incomplet) et à séparer en deux (plaintes / activité des services).**

Citations du bilan :
- Fiche 4 (violences sexuelles), p.103 : « le nombre de victimes enregistrées par les forces de sécurité reflète non seulement l'évolution de la délinquance, mais aussi de la propension à porter plainte – variable selon la nature de l'infraction –, de l'évolution des comportements dans la société et enfin des dispositifs d'accueil, de protection et de sanction mis en place. » Et : « La hausse constatée en 2025 s'inscrit ainsi dans une tendance de fond initiée dès 2018, dans le contexte de libération de la parole impulsé par le mouvement #MeToo à compter de 2017-2018, mais également de l'amélioration de l'accueil des victimes par les services de sécurité. »
- Synthèse p.11-12 (« En dix ans, une forte hausse des violences sexuelles et intrafamiliales enregistrées dans un contexte de libération de la parole ») : contexte du Grenelle des violences conjugales de 2019, du renforcement des dispositifs de protection, de l'attention aux mineurs (Code de la justice pénale des mineurs 2021, OFMIN 2023, affaire Notre-Dame de Bétharram), « d'une progression des signalements et des dépôts de plainte, notamment pour des faits anciens ». Ces évolutions « sont susceptibles d'avoir contribué à une meilleure identification des faits dans les statistiques enregistrées ». Et : « Ces évolutions restent à analyser de manière plus approfondie ».
- Éléments chiffrés p.10-11 et p.103 : délai médian de dépôt de plainte de 185 jours pour les violences sexuelles ; part des violences sexuelles commises plus d'un an avant le dépôt de plainte : 29 % en 2016, 41 % en 2025 ; plus de 5 ans avant : 9 % en 2016, 17 % en 2025.
- Limite à ne pas omettre : p.12 : « Les premiers résultats de l'enquête Vécu et ressenti en matière de sécurité (VRS) font état d'une hausse des violences physiques déclarées depuis 2021 » : la hausse n'est donc pas qu'un effet de signalement. Les enquêtes servent « à distinguer les évolutions des comportements de signalement, de celles des phénomènes eux-mêmes » (séries longues de victimation attendues à l'automne 2026).
- Autre facteur législatif (p.103) : la loi du 21 avril 2021 « a redéfini et élargi le périmètre des atteintes sexuelles (actes sexuels consentis), contribuant à la croissance des actes enregistrés ».
- « Activité des services » : le SSMSI l'applique aux stupéfiants (p.152 : « Les statistiques relatives aux infractions à la législation sur les stupéfiants reflètent l'activité des services de sécurité intérieure et sont donc sensibles aux orientations des politiques publiques et à l'intensité de l'activité opérationnelle ») et, pour 2024, aux Jeux olympiques de Paris (p.10 : hausse 2024 « en partie » due à « l'augmentation du nombre de mis en cause pendant les mois de juillet et août 2024, en lien avec la mobilisation exceptionnelle des forces de sécurité intérieure »). Pour les violences, le bilan parle plutôt d'accueil et de dispositifs que d'« activité ».

Rédaction proposée : « Les chiffres comptent les faits portés à la connaissance de la police et de la gendarmerie. La hausse des violences sexuelles et intrafamiliales enregistrées reflète en partie une plus grande propension à signaler les faits et un meilleur accueil des victimes (le SSMSI parle d'un contexte de libération de la parole) ; les enquêtes de victimation indiquent toutefois aussi une hausse des violences physiques déclarées depuis 2021. Pour les stupéfiants, les chiffres suivent surtout l'activité des services. »

#### Note 3 : « Pour l'usage de stupéfiants, on compte les personnes mises en cause ; depuis sa généralisation en septembre 2020, l'amende forfaitaire délictuelle en représente la majorité. »

**Verdict : exacte sur le fond mais inexacte dans le « depuis » (la majorité n'est atteinte qu'à partir de 2022). À corriger.**

Éléments vérifiés :
- Personnes mises en cause : [Bilan] Fiche 7, p.150 : l'indicateur « mesure le nombre de personnes physiques mises en cause par les services de police et de gendarmerie nationales pour au moins une infraction liée à la législation sur les stupéfiants élucidée » ; p.68 : un auteur n'est compté qu'une fois pour les stupéfiants (« méthodologie permettant de ne comptabiliser qu'une fois l'auteur »). Compte : 309 800 pour usage, 57 100 pour trafic, 16 200 pour les deux.
- Date d'introduction : le bilan écrit « introduction des amendes forfaitaires délictuelles pour usage de stupéfiants au mois de septembre 2020 » (p.151), « déploiement des amendes forfaitaires délictuelles (AFD) à partir de septembre 2020 » (p.13), « mise en place en septembre 2020 » (p.24), et dans les définitions (p.169) : « Depuis septembre 2020, cette procédure a été élargie aux infractions d'usage de stupéfiants (application de la loi n° 2019-222 du 23 mars 2019) ». La date de généralisation est confirmée par le ministère de la Justice (communiqué du 31/08/2020, mis à jour le 13/04/2023, lu en entier) : https://www.justice.gouv.fr/node/4109 : expérimentation à partir du 16 juin 2020 dans les ressorts de Rennes, Reims, Créteil, Lille et Marseille, **généralisation au 1er septembre 2020** sur tout le territoire. Le bilan ne dit pas « généralisation en septembre 2020 » mais parle de « généralisation des AFD » sans date (p.152).
- Part des AFD dans l'usage (lecture du graphique [Bilan] Figure 5, p.155, page rendue en image et vérifiée) : 2020 : environ 30 000 (année de lancement, minoritaire) ; 2021 : environ 105 000 sur 221 200 (minoritaire) ; 2022 : 142 900 sur 251 300 (57 %) ; 2023 : 161 800 sur 262 100 (62 %) ; 2024 : 196 600 sur 290 700 (68 %) ; 2025 : 217 700 sur 309 800 (70 % : « 70 % des mis en cause pour usage de stupéfiants, soit 217 700 personnes, ont fait l'objet d'une amende forfaitaire délictuelle », p.155). Les lectures de 2020 et 2021 sont approximatives (valeurs non écrites dans le texte).
- Limite : l'AFD ne concerne que les majeurs et l'usage d'une faible quantité de cannabis, de cocaïne ou d'ecstasy (p.155 : 94 % cannabis, 5 % cocaïne, 1 % ecstasy ; 73 % des majeurs).
- Autre point : depuis cette édition la date retenue pour les AFD est la date d'élucidation, pas la date des faits (p.69, p.72-73 : +2 614 personnes par rapport à janvier 2026).

Rédaction proposée : « Pour l'usage de stupéfiants, on compte les personnes mises en cause. L'amende forfaitaire délictuelle, généralisée à tout le territoire le 1er septembre 2020, représente aujourd'hui la majorité de ces cas (70 % en 2025). Ces chiffres suivent donc beaucoup l'activité des services. »

#### Note 4 : « Les taux départementaux rapportent les faits commis dans le département à sa population (à ses logements pour les cambriolages). »

**Verdict : confirmée pour les taux de commission, à nuancer pour les escroqueries.**

Éléments vérifiés :
- La page du jeu de données (API data.gouv.fr, lue) décrit les bases « selon le lieu de commission » : https://www.data.gouv.fr/api/1/datasets/621df2954fa5a3b5a023e23c/ et https://www.data.gouv.fr/datasets/bases-statistiques-communale-departementale-et-regionale-de-la-delinquance-enregistree-par-la-police-et-la-gendarmerie-nationales
- [Bilan] : les graphiques territoriaux donnent « le nombre d'infractions par habitant selon le lieu de commission » ; **exception : les escroqueries**, « selon le lieu de résidence de la victime, compte tenu de la prévalence des escroqueries sur internet » (note sous la Figure 9 de la Fiche 8, p.167). De même, les taux d'élucidation départementaux sont déclinés « par département de commission », sauf escroqueries « par département de résidence de la victime » (Éclairage 2, note 1). Fiche 1 (homicides) : le champ est « la France, en lieu de commission » (p.76).
- Dénominateurs : habitants pour tous les indicateurs ; **logements** pour les cambriolages de logement (Figure 9, p.21 : « Cambriolages de logement (pour 1 000 log.) » ; p.128 : « 5,6 cambriolages de logement pour 1 000 logements »). Population : recensement de la population 2023 de l'Insee (1er janvier 2023), 2017 pour Mayotte (p.73).
- La presse reprenant l'étude du SSMSI confirme « le lieu de commission des faits, et non du domicile des victimes » (Banque des Territoires, https://www.banquedesterritoires.fr/violences-physiques-et-sexuelles-toujours-de-fortes-disparites-departementales, source secondaire, lue en entier).
- Homicides : le bilan exprime ces taux **pour 100 000 habitants** (Figure 9, p.21 : 1,4 pour 100 000 en France) et, pour ses cartes départementales, utilise une **moyenne 2022-2025** (homicides p.82, tentatives, violences sexuelles) plutôt qu'une année isolée ; le bilan ne donne pas de justification explicite, mais ce sont des indicateurs à petits effectifs.

Rédaction proposée : « Les taux départementaux rapportent les faits commis dans le département à sa population (à son nombre de logements pour les cambriolages). Seules les escroqueries sont rapportées au département de résidence de la victime, car beaucoup se font sur internet. » (À retirer si les escroqueries ne sont pas affichées par département.)

### 3. Licence, publication, version anglaise (point 3)

**Date de publication de l'édition 2026 des bases**
- Jeu de données data.gouv.fr (API, lue ; WebFetch de la page) : dernière modification et dernière mise à jour 2026-07-09T12:01:37Z. Les ressources REG et DEP (créées le 2026-01-27) et toutes les autres sont marquées modifiées le 2026-07-09. Atlas départemental « Édition juillet 2026 » : créé 2026-06-29, modifié 2026-07-09. Fréquence : annuelle. Couverture temporelle : 2016-01-01 à 2025-12-31. Création du jeu : 2022-03-01.
- Bilan statistique : « Date de publication : juillet 2026 » ; PDF créé le 08/07/2026. La date du 09/07/2026 (jeudi) apparaît dans la liste des communiqués du ministère (résumé du moteur de recherche, page en 403) et dans l'URL de CNews. Conforme à la date de l'instantané.
- Le bilan indique que l'Atlas départemental est « publié simultanément » (p.6) et que ses données « sont actualisées concomitamment ».

**Licence** : Licence Ouverte / Open Licence version 2.0 (« lov2 » dans l'API). Conforme. Réserve : la reproduction du bilan PDF lui-même est soumise à une mention distincte, « © SSMSI 2026 : Reproduction partielle autorisée sous réserve de la mention de la source et de l'auteur » (page de garde). Citer « SSMSI, bases statistiques ... » suffit dans les deux cas.

**Version anglaise** : non trouvée pour le bilan 2025 ni pour les bases.
- La page data.gouv.fr est en français uniquement (titre, description, ressources).
- Le bilan est en français.
- Le site Interstats a quelques pages en anglais (résultats de recherche seulement, pages en 403 pour moi) : « Measuring Criminal Behaviour », « [ENGLISH] Welcome to the SSMSI Data Visualisation Space », « [ENGLISH] Data Sources that Complement and Enhance Each Other » (https://www.interieur.gouv.fr/Interstats/Sources-et-methodes-statistiques/La-mesure-de-la-delinquance/Measuring-Criminal-Behaviour ; https://mobile.interieur.gouv.fr/Interstats/Datavisualisation/ENGLISH-Welcome-to-the-SSMSI-Data-Visualisation-Space). Le site du SSMSI a une interface `/ssmsi/en/` (page `node/1488` listée avec le titre en français, non ouverte).
- Presse anglophone sur les chiffres de janvier : Connexion France (lue). Un catalogue tiers (api.store) affiche un titre anglais machine-traduit pour le jeu ; non officiel.
- Conséquence pour le jeu : les libellés anglais des indicateurs doivent être traduits par le projet ; le bilan fournit les libellés français officiels (Figure 1, p.7).

### 4. Taux départementaux 2025 (point « Aube, Aude, Aveyron »)

| Élément | Valeur du fichier | Valeur trouvée | Source | Verdict |
|---|---|---|---|---|
| Aube (10), homicides 2025 | 0,003 ‰ | Non publié dans une source indépendante lue | Atlas départemental 2025 (non ouvert) | **Non trouvé** |
| Aube (10), violences physiques intrafamiliales 2025 | 4,384 ‰ | idem | idem | **Non trouvé** |
| Aude (11), violences physiques intrafamiliales 2025 | 3,619 ‰ | idem | idem | **Non trouvé** |
| Aveyron (12), violences physiques intrafamiliales 2025 | 2,21 ‰ | idem | idem | **Non trouvé** |

Recherches faites : presse locale, Banque des Territoires, résumés du moteur de recherche : aucune source publie ces taux pour ces trois départements. Le bilan lui-même ne cite ni l'Aube, ni l'Aude, ni l'Aveyron comme taux (cartes seulement, sans valeurs par département pour ces trois).

Contrôles de plausibilité (calculs, pas des vérifications) :
- Population municipale 2023 Insee (https://www.insee.fr/fr/statistiques/8680659, lue) : Aube 310 447 ; Aude 379 648 ; Aveyron 279 609 (base indiquée par le bilan, p.73).
- Les taux du fichier correspondent à des nombres entiers de victimes avec ces populations : Aube 1 361 victimes → 4,384 ‰ ; Aude 1 374 → 3,619 ‰ ; Aveyron 618 (ou 617) → 2,21 ‰ ; Aube homicides : 1 victime → 0,0032 ‰ (affiché 0,003). Le fichier utilise donc bien le recensement 2023 comme le bilan.
- Ordre de grandeur : la moyenne France est 3,8 ‰ pour les violences intrafamiliales (Figure 9, p.21) ; l'Aube (4,4) est au-dessus, l'Aude (3,6) un peu en dessous, l'Aveyron (2,2) nettement en dessous. Les départements les plus touchés cités par la presse : Pas-de-Calais 6,2 ‰, Guyane et La Réunion 6,1 ‰, Nord et Somme 4,9 ‰ (Banque des Territoires, source secondaire, valeurs d'une autre année possible). Rien de contradictoire.
- Point de vigilance : le bilan applique le secret statistique à ses propres affichages (« ne jamais afficher des données de 1 à 4 effectifs issues des bases administratives », p.66). Le taux de 0,003 ‰ de l'Aube équivaut à une seule victime. La page data.gouv.fr ne mentionne la règle « plus de 5 faits pendant 3 années successives » que pour les communes. À vérifier avec le producteur du fichier avant d'afficher ce chiffre. Le bilan exprime d'ailleurs les homicides pour 100 000 habitants, pas pour 1 000.

### 5. Limites expliquées par le SSMSI (point 4, récapitulatif)

| Sujet | Ce que dit le SSMSI | Où |
|---|---|---|
| Délinquance enregistrée, pas totale | « de nombreuses personnes ne portent pas plainte, ce qui tend à sous-estimer l'ampleur de la délinquance » ; le bilan suit 87 % des crimes et 74 % des délits non routiers ; hors champ : polices municipales, transporteurs, infractions relevées par d'autres administrations | [Bilan] p.3, 6, 65-67 |
| Taux de plainte (enquête VRS, 2023) | violences physiques 21 %, violences sexuelles physiques 6 %, non physiques 2 %, violences conjugales 16 %, cambriolage avec effraction 41 %, vol de voiture 33 %, arnaques 14 % ; taux de plainte pas directement comparables à l'ancienne enquête CVS | [Bilan] p.8-9 |
| Libération de la parole | tendance de fond depuis 2018, contexte #MeToo 2017-2018, meilleur accueil, lois ; mais aussi hausse des violences physiques déclarées depuis 2021 dans l'enquête VRS | [Bilan] p.11-12, 24, 103 |
| Activité des services (stupéfiants) | « reflètent l'activité des services de sécurité intérieure et sont donc sensibles aux orientations des politiques publiques et à l'intensité de l'activité opérationnelle » ; effet des Jeux olympiques 2024 sur 2024 | [Bilan] p.10, 13, 152 |
| AFD usage de stupéfiants | « à partir de septembre 2020 » ; généralisation au 1er septembre 2020 (ministère de la Justice) ; 70 % des mis en cause pour usage en 2025 ; mineurs inéligibles | [Bilan] p.13, 24, 151, 155, 169 ; https://www.justice.gouv.fr/node/4109 |
| Lieu pris en compte pour les départements | lieu de commission (sauf escroqueries : lieu de résidence de la victime) ; habitants (logements pour les cambriolages) ; Insee RP 2023 | [Bilan] p.21, 73, 167 ; page data.gouv.fr |
| Données définitives | « définitives et ne seront plus révisées » sauf évolution de périmètre ; consolidées jusqu'en mai 2026 | [Bilan] p.6, 71 |
| Homicides | série « retraitée », non comparable à la base victime brute ; 2 homicides liés à des attentats en 2025 | [Bilan] p.63, 75-76 |
| Dédoublonnage | une victime associée à plusieurs infractions est comptée autant de fois que d'infractions (sauf stupéfiants : un auteur compté une fois) | [Bilan] p.68 |

### 6. Conclusion

#### Écarts, par ordre d'importance

1. **Chiffre clé des homicides, « 975 en 2025, en baisse » : à corriger.** Le SSMSI écrit « stable » (0 %, 976 en 2024), « mettant fin à l'évolution observée entre 2020 et 2023 ». Seuls -1 victime (-0,1 %). À reformuler : « 975 en 2025, stable par rapport à 2024 (976) ».
2. **Note 3 (AFD) : « depuis sa généralisation en septembre 2020 ... en représente la majorité » est inexact dans le « depuis ».** Les AFD étaient minoritaires en 2020 et 2021 ; elles dépassent la moitié à partir de 2022 (57 %) et font 70 % en 2025. La généralisation au 1er septembre 2020 est elle exacte (ministère de la Justice).
3. **Escroqueries et fraudes aux moyens de paiement : le fichier est inférieur de 0,6 % au bilan** chaque année (-1 423 en 2016, -2 647 en 2024, -2 837 en 2025), évolution 2024-2025 identique (+7,4 %). Cause non documentée dans les sources lues. Le bilan décline les escroqueries par lieu de résidence de la victime, ce qui peut jouer, mais ce n'est pas une explication sourcée.
4. **Mis en cause pour stupéfiants (trafic, usage) : le fichier est légèrement au-dessus du bilan** (trafic +0,26 à +0,33 %, usage +0,02 % en 2024-2025 et +0,08 % en 2016). Cause non documentée (piste : dédoublonnage national des personnes, non confirmée).
5. **Note 4 : omission des escroqueries** (départementalisées par résidence de la victime) et homicides exprimés pour 100 000 habitants par le SSMSI.
6. **Taux départementaux (Aube, Aude, Aveyron) : non trouvés** dans une source indépendante (seul l'Atlas départemental, non ouvert, peut les confirmer). Le taux d'homicides de l'Aube (0,003 ‰) repose sur une victime : à manier avec prudence.
7. **Métadonnée data.gouv.fr incohérente** : couverture spatiale « France métropolitaine » alors que l'historique parle d'extension aux DROM. Aucun impact sur les totaux.
8. Pas d'écart lié à l'outre-mer : le bilan (métropole + DROM, sans COM) et la somme des régions coïncident pour 14 séries sur 16.

#### Notes à corriger ou nuancer
- Note 1 : confirmée ; ajouter l'idée de périmètre (police et gendarmerie nationales, « essentiellement » crimes et délits) ou un taux de plainte ; préciser que la question de la plainte ne vaut pas pour les stupéfiants.
- Note 2 : confirmée en nuançant (« en partie » juste mais incomplet : meilleur accueil, évolutions législatives ; la hausse des violences physiques est aussi visible dans l'enquête de victimation) ; séparer « plaintes » (violences) et « activité des services » (stupéfiants).
- Note 3 : à corriger (voir écart 2).
- Note 4 : confirmée pour la commission ; signaler l'exception des escroqueries.

#### Conforme
- 14 des 16 séries (homicides, tentatives, violences physiques intrafamiliales et hors cadre familial, violences sexuelles, vols avec armes, vols violents sans arme, vols sans violence, cambriolages, vols de véhicule, vols dans les véhicules, vols d'accessoires, destructions et dégradations) : toutes les valeurs 2016, 2023, 2024, 2025 égales aux valeurs du bilan (Annexe 1) à l'arrondi près ; homicides et tentatives exactes.
- AFD (2016 = 0, 2024 = 196 601, 2025 = 217 651) et hors AFD (94 155 ; 92 203) conformes à la Figure 5 du bilan.
- Unités de compte (victimes, infractions, victimes entendues, véhicules, mis en cause) conformes à l'Annexe 1.
- Évolutions 2024-2025 calculées sur le fichier concordent avec celles du SSMSI (tableau 1.3).
- Date d'édition (09/07/2026) et licence (Licence Ouverte 2.0) conformes. Pas de version anglaise des bases ni du bilan trouvée.

### 7. URL consultées

Lues en entier ou en partie (contenu obtenu) :
- https://statistiques.interieur.gouv.fr/ssmsi/files/ssmsi/2026-07/Ins%C3%A9curit%C3%A9%20et%20d%C3%A9linquance%20en%202025%20-%20Bilan%20statistique%20-%20%C3%A9dition%202026%20-%20SSMSI.pdf (bilan, source primaire)
- https://www.data.gouv.fr/datasets/bases-statistiques-communale-departementale-et-regionale-de-la-delinquance-enregistree-par-la-police-et-la-gendarmerie-nationales (page du jeu, métadonnées)
- https://www.data.gouv.fr/api/1/datasets/621df2954fa5a3b5a023e23c/ (métadonnées JSON : licence, dates, ressources ; aucun fichier téléchargé)
- https://www.justice.gouv.fr/node/4109 (AFD : expérimentation 16/06/2020, généralisation 01/09/2020)
- https://www.insee.fr/fr/statistiques/8680659 (population municipale 2023)
- https://www.banquedesterritoires.fr/violences-physiques-et-sexuelles-toujours-de-fortes-disparites-departementales
- https://www.banquedesterritoires.fr/les-atteintes-aux-personnes-la-hausse-celles-aux-biens-en-baisse-en-2025
- https://www.connexionfrance.com/news/crime-in-france-in-2025-burglaries-and-car-thefts-fall-but-fraud-rises/767821
- https://france-statistiques.fr/evolution-homicides-france-2017-2025/ (secondaire)
- https://actu17.fr/societe/violences-physiques-sexuelles-homicides-la-delinquance-poursuit-sa-hausse-en-france-en-2025.html (29/01/2026, première photographie)
- https://rci.fm/deuxiles/infos/Societe/Bilan-de-linsecurite-et-de-la-delinquance-en-2025-que-retenir-pour-la-Guadeloupe-et (pas de chiffres nationaux)
- https://www.bien-dans-ma-ville.fr/blog/les-nouveaux-chiffres-de-la-securite-2026-region-par-region.html (secondaire, pourcentages régionaux sans base explicite ; non utilisé pour un verdict)

Refusées (HTTP 403, Cloudflare) : non lues, mentionnées via résumés du moteur de recherche seulement :
- https://www.interieur.gouv.fr/Interstats/Actualites/Insecurite-et-delinquance-en-2025-bilan-statistique-et-atlas-departemental
- https://www.interieur.gouv.fr/actualites/communiques-de-presse/insecurite-et-delinquance-en-2025-bilan-statistique-et-atlas-departemental
- https://www.interieur.gouv.fr/actualites/communiques-de-presse/insecurite-et-delinquance-en-2025-premiere-photographie
- https://statistiques.interieur.gouv.fr/ssmsi/publications/insecurite-et-delinquance-en-2025-bilan-statistique-et-atlas-departemental
- https://statistiques.interieur.gouv.fr/ssmsi/en/node/1488
- https://www.cnews.fr/france/2026-07-09/insecurite-viols-violences-physiques-tentatives-dhomicide-plusieurs-indicateurs (résumé du moteur : 9 juillet, 975, tentatives +4 %, escroqueries +7 %)
- https://www.actu-juridique.fr/justice/statistiques-de-la-delinquance-2025-vers-une-brutalisation-de-la-societe-francaise/
- https://www.lagazettedescommunes.com/club-prevention-securite/prevention-de-la-delinquance/delinquance-ce-quil-faut-retenir-du-bilan-statistique-annuel.KWOZXEFOR5H5JDYLMF3QCP76UM.html
- https://www.gendarmerie.interieur.gouv.fr/gendinfo/actualites/2020/usage-de-stupefiants-l-amende-forfaitaire-generalisee-a-l-ensemble-du-territoire
- https://mobile.interieur.gouv.fr/Interstats/Datavisualisation/ENGLISH-Welcome-to-the-SSMSI-Data-Visualisation-Space
- https://www.interieur.gouv.fr/Interstats/Sources-et-methodes-statistiques/La-mesure-de-la-delinquance/Measuring-Criminal-Behaviour

Vues seulement dans des résultats de recherche (non ouvertes) : https://www.interieur.gouv.fr/fr/content/download/139762/1102438/file/... (miroir du bilan) ; https://ofdt.fr/sites/ofdt/files/2025-02/00052-interpellations-et-condamnations-pour-infraction-a-la-legislation-sur-les-stupefiants-evolution-depuis-1996.doc (AFD environ 29 400 en 2020, d'après le résumé du moteur, cohérent avec le graphique p.155) ; Atlas départemental 2025 (ressource data.gouv.fr, non ouvert).

## Mises à jour

- **03/11/2026, relecture du PO** : l'Atlas départemental 2025 (juillet 2026, figure 1 de chaque fiche), lu par le PO, confirme les quatre taux : Aube, homicides, 1 victime pour 310 447 habitants (0,0032 ‰, p. 164) ; violences physiques intrafamiliales de l'Aube, 1 361 (4,384 ‰), de l'Aude, 1 374 pour 379 648 (3,619 ‰, p. 264), de l'Aveyron, 618 pour 279 609 (2,210 ‰, p. 266). L'Atlas repose sur la même base que le fichier et n'affiche qu'une décimale : il confirme l'extraction, pas une source indépendante.
- **03/11/2026, décision du PO** : sur la carte, un taux fondé sur 1 à 4 faits est masqué (« secret statistique », sans couleur), comme le SSMSI le fait dans son bilan. Le fichier devra garder les effectifs par département pour appliquer la règle.
- **03/11/2026, effectifs par département** : `yarn briefings crime` relancé ; chaque série départementale garde désormais, pour chaque département, le nombre de faits (victimes, infractions, véhicules ou mis en cause, selon l'indicateur) sur lequel repose son taux : la colonne `nombre` de la même ligne du fichier « DEP » que `taux_pour_mille` (champ `counts`). Le script échoue si un effectif n'est pas un entier, ou si un taux nul ne va pas avec un effectif nul. Comparé au fichier du 02/11, aucun autre chiffre ne change (séries, taux, chiffre clé, date de publication) ; seule la date de récupération passe au 2026-11-03. Contrôles : les effectifs redonnent ceux de l'Atlas lus par le PO (Aube : 1 homicide, 1 361 victimes de violences physiques intrafamiliales ; Aude : 1 374 ; Aveyron : 618), et leur somme par indicateur est le total France de la somme des régions (975 homicides, 4 477 tentatives, 7 913 vols avec armes, 211 596 cambriolages en 2025). En 2025, des taux fondés sur 1 à 4 faits : 35 départements pour les homicides, 7 pour les tentatives d'homicide, 10 pour les vols avec armes, aucun pour les 15 autres indicateurs ; aucun homicide enregistré en Ardèche, en Haute-Loire et en Lozère (taux et effectif nuls).

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
