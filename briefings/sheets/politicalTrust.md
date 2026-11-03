# `politicalTrust` · Baromètre de la confiance politique (sondage saisi à la main)

**Vérifiée le 02/11/2026** : toutes les valeurs saisies sont conformes. Chacune a été lue dans le rapport de sa vague, puis recoupée par l'écart publié dans la vague suivante. Notes corrigées : le plus bas (les partis, 15 %), le plus haut (le maire, parmi les élus seulement), la marge d'incertitude telle qu'OpinionWay l'écrit, « la seule mesure » limitée au rapport publié.

**À décider (PO)** : le baromètre n'a ni licence ni règle de citation propre. Seules s'appliquent la clause générale des Termes légaux de Sciences Po (« toute utilisation ou reproduction […] strictement interdite […] sauf accord préalable et écrit ») et la mention « © 2026 SCIENCES PO » en pied de site. Le kit cite des chiffres publiés, jamais les fichiers ni les graphiques. La vérification conseille d'écrire au CEVIPOF pour lever le doute avant de redistribuer ces séries.

| Champ | Valeur |
| --- | --- |
| Indicateur | `politicalTrust`, seconde partie du ticket #144, dossier « Institutions » (statut `planned`), nature `survey` : marqué « sondage » avec l'institut, l'échantillon et les dates (PO, 02/11/2026) |
| Données | `briefings/manual/politicalTrust.json`, saisi à la main le 2026-11-02 depuis les rapports des vagues 1 à 17 |
| Source | Sciences Po CEVIPOF, Baromètre de la confiance politique, vague 17, publiée le 09/02/2026 ; OpinionWay, 3 166 inscrits sur les listes électorales (sur 3 445 personnes de 18 ans et plus), en ligne, méthode des quotas, terrain du 12 au 28 janvier 2026 ; citation seulement ; en français seulement |
| Séries | `politicsTrust` : confiance dans la politique, 2025 et 2026 ; `mayorTrust` : confiance dans le maire de sa commune (Q14), 2009 à 2026 ; `presidentTrust` : dans le président de la République en exercice (Q14), 2013 à 2026 (question non posée en décembre 2012, valeurs de 2009 à 2011 non saisies) ; `assemblyTrust` : dans l'Assemblée nationale (Q13), 2009 à 2026 (question non posée en 2010 et 2011) ; `positionFarLeft` à `positionNoAnswer` : auto-positionnement de 0 à 10 regroupé en blocs (0-1, 2-4, 5, 6-8, 9-10) et sans réponse, 2016 à 2026 |
| Valeurs par catégorie | 2026 : `institutions` (Q13, 12 institutions, de 58 % pour le conseil municipal à 17 % pour le gouvernement) et `personalities` (Q14, 7 élus, de 60 % pour le maire à 18 % pour le président de la République) |
| Chiffre clé | 22 % des inscrits ont confiance dans la politique en 2026, en baisse (26 % en 2025) |
| Première édition | À remplir à la publication |

Chaque point porte l'année du libellé de sa vague dans le rapport de la vague 17. Le terrain a eu lieu en fin d'année jusqu'en décembre 2018, puis en janvier ou février (« Fév. 2020 » : du 28 janvier au 4 février 2020). Il n'y a pas de vague de 2019.

À actualiser : à chaque vague (une par an, publiée en février). Le PDF de la vague 17 a été remplacé le 13/03/2026 pour y ajouter la Roumanie ; les chiffres de la France n'ont pas changé.

Source secondaire à écarter : la page du CESE du 24/02/2014 donne 65 % pour le maire en décembre 2013 ; le rapport de la vague 5 donne 61 %, la valeur saisie.

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web. Il a téléchargé les 17 rapports et lu les courbes de la vague 17 point par point. Son rapport, tel quel :

Date de la vérification : 2026-11-02. Aucun fichier sous `/home/user` n'a été lu ni modifié ; tout vient du web.

### Résultat en une phrase

Les 4 séries de chiffres saisies à la main (confiance dans le maire, le président, l'Assemblée, positionnement gauche-droite) et les chiffres de la vague 17 sont tous conformes : aucune valeur saisie n'est erronée. Les écarts trouvés sont ailleurs : une source secondaire fausse (CESE, 2014), la formulation de deux notes « À savoir » (3 et 4), et l'absence de marge d'erreur chiffrée pour 3 166 répondants dans le rapport. Détail dans la conclusion.

### Méthode et niveau de fiabilité des sources

Trois voies indépendantes ont été croisées pour chaque valeur.

1. **Le rapport de la vague d'origine** (chaque vague a son propre PDF sur sciencespo.fr). Les 17 PDF ont été téléchargés et le texte extrait (`pdftotext`). Quand un tableau chiffré existe (« % Confiance »), c'est lui qui fait foi, pas la courbe.
2. **Le delta de la vague suivante.** Chaque rapport donne « Comparatif par rapport à la vague N−1 » (`+4`, `-13`…). Le delta ramené à la valeur de la vague N−1 doit redonner la valeur saisie. Ce contrôle est fait pour chaque ligne ci-dessous (colonne Source, « Δ »).
3. **Des articles de presse ou institutionnels**, quand j'en ai trouvé pour la vague concernée.

Les graphiques en courbes de la vague 17 (p. 29, 32 et 77) portent une étiquette chiffrée sur chaque point. Je les ai rendus en image à 130 puis 300 dpi et lus visuellement, couleur par couleur. Les points voisins qui se chevauchent (p. 29, déc. 2018 par exemple) sont tranchés par les tableaux des rapports d'origine, donc la lecture des courbes n'est plus un risque.

Marquage des sources dans les tableaux :

- **[PDF]** : lu directement dans le PDF téléchargé (texte extrait, image vérifiée si nécessaire).
- **[HTML]** : page web téléchargée et lue en brut (`curl`).
- **[WebFetch]** : page web lue par l'outil WebFetch, qui renvoie un résumé produit par un petit modèle (les citations n'ont pas été revérifiées dans le HTML).
- **[Moteur]** : information vue seulement dans un résumé de moteur de recherche. **Aucune valeur n'a été validée sur cette seule base** ; les rares cas sont signalés.

Les numéros de page sont ceux du PDF (ils coïncident avec le pied de page « page N »).

Légende des sources (URL complètes en fin de document) : `V1` à `V17` = rapport de la vague 1 à 17 ; `A17` = article Sciences Po du 9 février 2026 ; `INF17` = infographie CEVIPOF du 6-9 février 2026 ; `DEC17` = « Décryptages » du 9 février 2026 ; les autres codes sont explicités dans la liste finale.

---

### 1. Vague 17 : date, terrain, échantillon, confiance dans la politique

| Élément | Valeur saisie | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Date de publication | 9 février 2026 | « Le CEVIPOF publie le 9 février 2026 son Baromètre de la confiance politique, vague 17, réalisé par OpinionWay » ; article daté « 9 février 2026 » | [A17][A17] [HTML] ; franceinfo publié le 9 février 2026 à 19:38 [FI17][FI17] [WebFetch] ; présentation au CESE le 10 février 2026 (séance plénière) [CESE17][CESE17] [PDF] ; Public Sénat daté du 10/02/2026 [PS17][PS17] [WebFetch] | Conforme |
| URL de l'article | `…/barometre-de-la-confiance-politique-cevipof-2026-la-confiance-s-effondre-en-politique-la-proximite-fait-figure-de-refuge/` | Répond (HTTP 200) ; titre : « Baromètre de la confiance politique CEVIPOF 2026 : la confiance s'effondre en politique, la proximité fait figure de refuge » | [A17][A17] [HTML] | Conforme |
| Dates de terrain | 12 au 28 janvier 2026 | « Du 12 au 28 janvier 2026 » (France). L'article lui-même ne donne ni terrain ni effectif | [V17 p.3][V17] [PDF] ; [INF17][INF17] [PDF] ; [FI17][FI17] et [PS17][PS17] [WebFetch] | Conforme |
| Échantillon | 3 166 inscrits sur les listes électorales | « 3 166 personnes inscrites sur les listes électorales issu d'un échantillon de 3 445 personnes représentatif de la population française âgée de 18 ans et plus ». Quotas (sexe, âge, CSP, région de résidence, taille d'agglomération ; le critère de revenus ne s'applique pas à la France), en ligne (CAWI), norme ISO 20252 | [V17 p.3][V17] [PDF] ; [FI17][FI17], [PS17][PS17] [WebFetch] | Conforme |
| Confiance dans la politique (q0v15) | 22 %, −4 points | 22 % (4 % « oui, tout à fait » + 18 % « oui, plutôt »), 78 % pas confiance (50 % « plutôt pas », 28 % « pas du tout »), « 22 % −4 » | [V17 p.26][V17] [PDF] ; « 22 % (−4pt/2025) » [A17][A17] [HTML] ; Cautrès : « On est à 22 % de confiance cette année […] Nous avons chuté de 4 points » [CESE17][CESE17] [PDF] ; [FI17][FI17] ; [PS17][PS17] (78 % de défiance, donc 22 %) | Conforme |
| Même question, vague 16 (2025) | 26 % | 26 %, −4 points sur la vague 15 (30 %). Libellé « Février 2025 », terrain du 17 au 29 janvier 2025, 3 561 inscrits | [V16 p.27][V16] [PDF] ; « Seuls 26 % des Français déclarent avoir confiance dans la politique » [A16][A16] [HTML] ; [FI25][FI25] [WebFetch] | Conforme |
| Post officiel CEVIPOF du 9 février | (non saisi) | « la confiance dans la politique tombe à 22 % (−4 pts). Les partis au plus bas (15 %), Président à 18 %… maires 60 % » | [X CEVIPOF][TWEET] **[Moteur] seulement**, page non lue ; non utilisé pour le verdict | (information, non vérifiée) |

Deux précisions sur le PDF de la vague 17 :

- Le PDF actuellement en ligne a été généré le **13 mars 2026** (métadonnées) et contient déjà la Roumanie (terrain du 2 au 23 février 2026). L'infographie du 6-9 février indique encore « Roumanie : terrain en cours ». Le PDF a donc été remplacé après la publication du 9 février. Les chiffres France que j'ai pu comparer à des documents du 6-10 février sont identiques à ceux du PDF : 22 % (article, CESE, franceinfo, Public Sénat), maire 60, président 18, Assemblée 20 et partis 15 (article et infographie), Sénat 26 et gouvernement 17 (Public Sénat). Si le kit cite l'URL du PDF, mieux vaut citer « vague 17, février 2026 » sans prétendre que le fichier date du 9 février.
- Le libellé « vague 17 – Février 2026 » désigne la publication ; le terrain est en janvier 2026.

---

### 2. Confiance dans le maire de la commune (Q14)

Question Q14 : « Avez-vous très confiance, plutôt confiance… dans les personnalités politiques suivantes : le maire de votre commune ». La valeur est « très confiance + plutôt confiance ». Le chiffre d'origine est lu dans le tableau « % Confiance » de la vague indiquée ; « Δ » = delta de la vague suivante ramené à la valeur de cette vague.

| Élément | Valeur saisie | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Déc. 2009 (V1, terrain 22-30 déc. 2009) | 65 | 65 (14 + 51) | [V1 p.19][V1] [PDF] ; Δ : V2 donne −13 sur 52, soit 65 [V2 p.16][V2] ; courbe [V17 p.32][V17] ; infographie « 15 ans » : 2009 = 65 [BILAN15][BILAN15] [PDF image lue] | Conforme |
| Déc. 2010 (V2, 7-22 déc.) | 52 | 52 (9 + 43), −13 | [V2 p.16][V2] ; Δ : V3 donne +2, soit 52 [V3 p.20][V3] ; courbe [V17 p.32][V17] | Conforme |
| Oct. 2011 (V3, 27 sept.-13 oct.) | 54 | 54 (10 + 44), +2 | [V3 p.20][V3] ; Δ : V4 donne +3 sur 57, soit 54 [V4 p.23][V4] ; courbe V17 p.32 | Conforme |
| Déc. 2012 (V4, 5-20 déc.) | 57 | 57 (8 + 49), +3 | [V4 p.23][V4] ; Δ : V5 donne +4 sur 61, soit 57 [V5 p.29][V5] ; courbe d'évolution de V5 [V5 p.30][V5] | Conforme |
| Déc. 2013 (V5, 25 nov.-12 déc.) | 61 | 61 (11 + 50), +4 | [V5 p.29][V5] et courbe p.30 [PDF] ; Δ : V6 donne +5 sur 66, soit 61 [V6 p.21][V6]. **La page CESE du 24/02/2014 donne 65 %** (voir note sous le tableau) [CESE14][CESE14] [WebFetch] | Conforme (la source secondaire CESE est en écart) |
| Déc. 2014 (V6, 5-15 déc.) | 66 | 66 (14 + 52), +5 | [V6 p.21][V6] ; Δ : V7 donne −3 sur 63, soit 66 [V7 p.23][V7] ; CESE : « 66 % des sondés disent avoir très confiance ou plutôt confiance dans le maire », 5-15 décembre 2014, 1 864 personnes [CESE15][CESE15] [WebFetch] | Conforme |
| Déc. 2015 (V7, 17-28 déc.) | 63 | 63 (11 + 52), −3 | [V7 p.23][V7] ; Δ : V8 donne +1 sur 64, soit 63 [V8 p.22][V8] | Conforme |
| Déc. 2016 (V8, 16-30 déc.) | 64 | 64 (12 + 52), +1 | [V8 p.22][V8] ; Δ : V9 donne −9 sur 55, soit 64 [V9 p.22][V9] ; Public Sénat 30/01/2018 : « passe de 64 % à 55 % » [PS18][PS18] [WebFetch] | Conforme |
| Déc. 2017 (V9, 13-26 déc.) | 55 | 55 (10 + 45), −9 | [V9 p.22][V9] ; Δ : V10 donne +3 sur 58, soit 55 [V10 p.29][V10] ; [PS18][PS18] [WebFetch] | Conforme |
| Déc. 2018 (V10, 13-24 déc.) | 58 | 58 (10 + 48), +3 | [V10 p.29][V10] ; Δ : V11 donne +5 sur 63, soit 58 [V11 p.32][V11] ; Acteurs publics 11/01/2019 : « 58 %, en hausse de 3 points » [AP19][AP19] [WebFetch] | Conforme |
| Fév. 2020 (V11, 28 janv.-4 fév.) | 63 | 63 (13 + 50), +5 | [V11 p.32][V11] ; Δ : V12 donne +2 sur 65, soit 63 [V12 p.33][V12] ; franceinfo 05/03/2020 : « les maires (63 %, en hausse de 5 points) » [FI20][FI20] [WebFetch] | Conforme |
| Fév. 2021 (V12, 20-31 janv. 2021) | 65 | 65 (15 + 50), +2 | [V12 p.33][V12] ; Public Sénat 22/02/2021 : 65 % [PS21][PS21] [WebFetch] ; Maire-info 24/02/2021 : « 65 % (+ 2 points) » [MI21][MI21] [WebFetch] | Conforme |
| Jan. 2022 (V13, 23 déc. 2021-10 janv. 2022) | 65 | 65 (16 + 49) ; « +1 » par rapport à la vague 12 bis de mai 2021 (64) | [V13 p.23][V13] ; Δ : V14 donne −8 sur 57, soit 65 [V14 p.28][V14]. Aucun article de presse avec le chiffre trouvé | Conforme |
| Fév. 2023 (V14, 27 janv.-9 fév.) | 57 | 57 (12 + 45), −8 | [V14 p.28][V14] (même chiffre dans la version « vFR » [V14FR][V14FR] [PDF]) ; Δ : V15 donne +3 sur 60, soit 57 [V15 p.24][V15] ; Acteurs publics 15/02/2024 : « +3 points » (57 en creux, chiffre dérivé) [AP24][AP24] | Conforme |
| Jan. 2024 (V15, 8-18 janv.) | 60 | 60 (13 + 47), +3 | [V15 p.24][V15] ; Acteurs publics 15/02/2024 : 60 % [AP24][AP24] [WebFetch] ; Localtis 14/02/2024 : 60 % [LT24][LT24] [WebFetch] ; infographie « 15 ans » : 2024 = 60 [BILAN15][BILAN15] | Conforme |
| Jan. 2025 (V16, 17-29 janv.) | 61 | 61 (14 + 47), +1 | [V16 p.32][V16] ; Δ : V17 donne −1 sur 60, soit 61 ; « 61 % des Français font confiance à leur maire » [A16][A16] [HTML] ; Maire-info 12/02/2025 : 61 % [MI25][MI25] ; Localtis 11/02/2025 : 61 % [LT25][LT25] [WebFetch] | Conforme |
| Jan. 2026 (V17, 12-28 janv.) | 60 | 60 (14 + 46), −1 | [V17 p.31][V17] (courbe p.32) [PDF] ; « les maires recueillent 60 % de confiance » [A17][A17] [HTML] ; [INF17][INF17] (2025 : 61 / 2026 : 60) ; [DEC17][DEC17] ; [FI17][FI17] ; [PS17][PS17] | Conforme |

Note sur l'écart CESE 2014. La page du CESE (24/02/2014, vague 5) écrit : « maire (65 %), conseiller général (45 %), conseillers régionaux (44 %), député (27 %) ». Dans le rapport V5, p.29, le maire est à 61 %, le conseiller général à 45 %, les régionaux à 44 %, le député à 41 % et les députés européens à 27 %. Le CESE a donc repris 65 (valeur de 2009) pour le maire et 27 (députés européens) pour le député. Cette page est erronée ; 61 est confirmé par V5, V6 (+5), la courbe de V5 et la courbe de V17. Ne pas utiliser cette page.

Hors périmètre demandé : la vague 6 bis (février 2015) n'est pas dans la liste ; la courbe de V17 p.32 la place à 67 %.

---

### 3. Confiance dans le président de la République en exercice (Q14)

| Élément | Valeur saisie | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Déc. 2013 | 26 | 26 (4 + 22), « Nouvel item » | [V5 p.29][V5] ; Δ : V6 donne −3 sur 23, soit 26 [V6 p.21][V6] ; courbe [V17 p.32][V17] | Conforme |
| Déc. 2014 | 23 | 23 (3 + 20), −3 | [V6 p.21][V6] ; Δ : V7 donne +6 sur 29, soit 23 [V7 p.23][V7] | Conforme |
| Déc. 2015 | 29 | 29 (4 + 25), +6 | [V7 p.23][V7] ; Δ : V8 donne −4 sur 25, soit 29 [V8 p.22][V8] | Conforme |
| Déc. 2016 | 25 | 25 (3 + 22), −4 | [V8 p.22][V8] ; Δ : V9 donne +11 sur 36, soit 25 [V9 p.22][V9] | Conforme |
| Déc. 2017 | 36 | 36 (7 + 29), +11 | [V9 p.22][V9] ; Δ : V10 donne −13 sur 23, soit 36 [V10 p.29][V10] ; Public Sénat 30/01/2018 : « +11 points » sans niveau absolu [PS18][PS18] [WebFetch] | Conforme |
| Déc. 2018 | 23 | 23 (5 + 18), −13 | [V10 p.29][V10] ; Acteurs publics 11/01/2019 : « 23 % », « −13 points » [AP19][AP19] [WebFetch] ; Δ : V11 donne +7 sur 30, soit 23 ; franceinfo 05/03/2020 : « 30 %, contre 23 % en 2018 » [FI20][FI20] [WebFetch] | Conforme |
| Fév. 2020 | 30 | 30 (6 + 24), +7 | [V11 p.32][V11] ; [FI20][FI20] [WebFetch] ; Δ : V12 donne +7 sur 37, soit 30 [V12 p.33][V12] | Conforme |
| Fév. 2021 | 37 | 37 (8 + 29), +7 | [V12 p.33][V12] ; Public Sénat 22/02/2021 : 37 % [PS21][PS21] ; Maire-info 24/02/2021 : 37 %, « +7 » [MI21][MI21] [WebFetch] | Conforme |
| Jan. 2022 | 38 | 38 (8 + 30), « +2 » sur la vague 12 bis (36) | [V13 p.23][V13] ; Δ : V14 donne −9 sur 29, soit 38 [V14 p.28][V14]. Pas de presse avec le chiffre trouvée | Conforme |
| Fév. 2023 | 29 | 29 (6 + 23), −9 | [V14 p.28][V14] ; Δ : V15 donne « = » sur 29 [V15 p.24][V15] | Conforme |
| Jan. 2024 | 29 | 29 (6 + 23), « = » | [V15 p.24][V15] ; Localtis 14/02/2024 : « 29 % des sondés déclarent ainsi avoir confiance dans le président de la République actuel » [LT24][LT24] [WebFetch] ; infographie « 15 ans » : 2024 = 29 [BILAN15][BILAN15] | Conforme |
| Jan. 2025 | 23 | 23 (4 + 19), −6 | [V16 p.32][V16] ; « seulement 23 % au président de la République » [A16][A16] [HTML] ; Maire-info 12/02/2025 : 23 % [MI25][MI25] [WebFetch] | Conforme |
| Jan. 2026 | 18 | 18 (4 + 14), −5 | [V17 p.31][V17] (courbe p.32) ; « tombe à 18 % (vs 23 % en 2025) » [A17][A17] [HTML] ; [INF17][INF17] (23 → 18) ; « la confiance dans le Président de la République est au plus bas » [INF17][INF17] | Conforme |

Remarques :

- La série mélange trois personnes : Sarkozy (jusqu'en 2011), Hollande (2013-2016), Macron (depuis déc. 2017). La question est « le président de la République actuel ».
- Valeurs plus anciennes non saisies mais existantes : déc. 2009 = 32 [V1 p.19][V1], déc. 2010 = 29 [V2 p.16][V2], oct. 2011 = 27 [V3 p.20][V3]. Déc. 2012 : **question non posée** (absente de [V4 p.23][V4], puis « Nouvel item » dans V5 ; la note « 2009-2019 » dit « Non proposé en 2012 » [DIX19][DIX19] p.9). C'est pourquoi la série saisie commence en déc. 2013.
- À ne pas confondre avec « l'institution présidentielle » (Q13) : 22 % en janvier 2026.

---

### 4. Confiance dans l'Assemblée nationale (Q13)

Q13 n'a pas été posée dans les vagues 2 et 3 (déc. 2010, oct. 2011 : aucune page « institutions » dans [V2][V2] et [V3][V3]), d'où les années manquantes.

| Élément | Valeur saisie | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Déc. 2009 | 38 | 38 (1 + 37) | [V1 p.18][V1] [PDF] ; Δ : V4 donne −10 sur 28 (comparatif « vague 1, décembre 2009 »), soit 38 [V4 p.21][V4] ; courbe [V17 p.29][V17] | Conforme |
| Déc. 2012 | 28 | 28 (1 + 27), −10 | [V4 p.21][V4] ; Δ : V5 donne +8 sur 36, soit 28 [V5 p.27][V5] | Conforme |
| Déc. 2013 | 36 | 36 (3 + 33), +8 | [V5 p.27][V5] ; Δ : V6 donne +3 sur 39, soit 36 [V6 p.19][V6] | Conforme |
| Déc. 2014 | 39 | 39 (2 + 37), +3 | [V6 p.19][V6] ; Δ : V7 donne +2 sur 41, soit 39 [V7 p.21][V7] | Conforme |
| Déc. 2015 | 41 | 41 (3 + 38), +2 | [V7 p.21][V7] ; Δ : V8 donne +1 sur 42, soit 41 [V8 p.20][V8] | Conforme |
| Déc. 2016 | 42 | 42 (2 + 40), +1 | [V8 p.20][V8] ; Δ : V9 donne −13 sur 29, soit 42 [V9 p.20][V9] | Conforme |
| Déc. 2017 | 29 | 29 (2 + 27), −13 | [V9 p.20][V9] ; Δ : V10 donne −6 sur 23, soit 29 [V10 p.27][V10] | Conforme |
| Déc. 2018 | 23 | 23 (1 + 22), −6 | [V10 p.27][V10] ; Δ : V11 donne +8 sur 31, soit 23 [V11 p.29][V11] ; Acteurs publics 11/01/2019 ne donne pas le chiffre (« entre 28 et 23 % ») [AP19][AP19] | Conforme |
| Fév. 2020 | 31 | 31 (3 + 28), +8 | [V11 p.29][V11] ; Δ : V12 donne +7 sur 38, soit 31 [V12 p.30][V12] | Conforme |
| Fév. 2021 | 38 | 38 (5 + 33), +7 | [V12 p.30][V12] ; Public Sénat 22/02/2021 : « 38 % » (« en nette hausse », +7) [PS21][PS21] [WebFetch] ; Δ : V13 donne « = » [V13 p.21][V13] | Conforme |
| Jan. 2022 | 38 | 38 (5 + 33), « = » | [V13 p.21][V13] ; Δ : V14 donne −10 sur 28, soit 38 [V14 p.25][V14] | Conforme |
| Fév. 2023 | 28 | 28 (2 + 26), −10 | [V14 p.25][V14] (idem version vFR [V14FR][V14FR]) ; Δ : V15 donne +1 sur 29, soit 28 [V15 p.21][V15] | Conforme |
| Jan. 2024 | 29 | 29 (4 + 25), +1 | [V15 p.21][V15] ; Δ : V16 donne −5 sur 24, soit 29 [V16 p.29][V16] | Conforme |
| Jan. 2025 | 24 | 24 (3 + 21), −5 | [V16 p.29][V16] ; « 24 % […] niveau historiquement bas, soit un retour à son niveau de décembre 2018 » [A16][A16] [HTML] ; Localtis 11/02/2025 : « 24 % » [LT25][LT25] [WebFetch] | Conforme |
| Jan. 2026 | 20 | 20 (2 + 18), −4 | [V17 p.28][V17] (aussi p.30 et courbe p.29) ; « 20 % (−4 pts / 2025) » [A17][A17] [HTML] ; « le pourcentage le plus bas constaté depuis la création du Baromètre en 2009 » [DEC17][DEC17] [PDF] ; [PS17][PS17] et [FI17][FI17] | Conforme |

Détail : « un retour à son niveau de décembre 2018 » (A16) : la valeur de décembre 2018 est 23, pas 24 ; approximation de rédaction sans conséquence sur la valeur saisie.

---

### 5. Auto-positionnement gauche-droite (NOU1)

Question NOU1 : « Sur une échelle de 0 à 10, où 0 correspond à la gauche et 10 correspond à la droite, où diriez-vous que vous vous situez ? ». Colonnes de valeurs : extrême gauche / gauche / centre / droite / extrême droite / ne se prononce pas.

#### 5a. Regroupement des points d'échelle en blocs

Le rapport fournit l'histogramme point par point (V17 p.76, vérifié sur l'image) et colore les barres par bloc :

| Point | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | NSP |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Jan. 2026 (%) | 2 | 3 | 6 | 8 | 8 | 13 | 7 | 9 | 9 | 6 | 6 | 23 |

Somme des blocs : 2 + 3 = **5** ; 6 + 8 + 8 = **22** ; **13** ; 7 + 9 + 9 = **25** ; 6 + 6 = **12** ; NSP **23** ; total 100.

Les blocs sont donc : **extrême gauche = 0-1, gauche = 2-4, centre = 5, droite = 6-8, extrême droite = 9-10**, NSP à part. Source : [V17 p.76][V17] [PDF + image]. Le même regroupement redonne exactement les blocs publiés dans toutes les vagues 8 à 17 (somme des histogrammes de [V8 p.53][V8], [V9 p.58][V9], [V10 p.58][V10], [V11 p.61][V11], [V12 p.61][V12], [V13 p.43][V13], [V14 p.64][V14], [V15 p.54][V15], [V16 p.77][V16]). Verdict : **Conforme** (hypothèse « extrême gauche = 0-1 » confirmée ; les libellés de 0 et 10 sont « Très à gauche / Très à droite » dans V8-V14, « Extrême gauche / Extrême droite » dans V15-V17).

#### 5b. Valeurs par vague

« Δ » = comparatif publié dans la vague suivante, ramené à cette vague, sur les 6 colonnes.

| Élément | Valeur saisie | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Déc. 2016 (V8) | 9 / 18 / 19 / 24 / 13 / 17 | 9 / 18 / 19 / 24 / 13 / 17 (somme 100) | [V8 p.53][V8] [PDF] ; Δ : V9 (−3, +1, +1, +2, −6, +5) redonne les 6 valeurs [V9 p.58][V9] ; courbe [V17 p.77][V17] | Conforme |
| Déc. 2017 (V9) | 6 / 19 / 20 / 26 / 7 / 22 | 6 / 19 / 20 / 26 / 7 / 22 | [V9 p.58][V9] ; Δ : V10 (−1, =, −3, +1, +1, +2) redonne les 6 valeurs [V10 p.58][V10] | Conforme |
| Déc. 2018 (V10) | 5 / 19 / 17 / 27 / 8 / 24 | 5 / 19 / 17 / 27 / 8 / 24 | [V10 p.58][V10] ; Δ : V11 (−1, −1, +2, +1, +1, −2) redonne les 6 valeurs [V11 p.61][V11] | Conforme |
| Fév. 2020 (V11) | 4 / 18 / 19 / 28 / 9 / 22 | 4 / 18 / 19 / 28 / 9 / 22 | [V11 p.61][V11] ; Δ : V12 (+1, +1, −2, +3, −2) redonne les 5 blocs [V12 p.61][V12] | Conforme |
| Fév. 2021 (V12) | 5 / 19 / 17 / 31 / 7 / 21 | 5 / 19 / 17 / 31 / 7 / 21 | [V12 p.61][V12] ; Δ : V13 (+1, −2, −3, +1, +4) redonne les 5 blocs [V13 p.43][V13] | Conforme |
| Jan. 2022 (V13) | 6 / 17 / 14 / 32 / 11 / 20 | 6 / 17 / 14 / 32 / 11 / 20 (échantillon exceptionnel de 10 566 inscrits) | [V13 p.43][V13] ; Δ : V14 (−1, +5, +2, −4, −2) redonne les 5 blocs [V14 p.64][V14] | Conforme |
| Fév. 2023 (V14) | 5 / 22 / 16 / 28 / 9 / 20 | 5 / 22 / 16 / 28 / 9 / 20 | [V14 p.64][V14] ; Δ : V15 (−1, =, −1, −1, =, +3) redonne les 6 valeurs [V15 p.54][V15] | Conforme |
| Jan. 2024 (V15) | 4 / 22 / 15 / 27 / 9 / 23 | 4 / 22 / 15 / 27 / 9 / 23 | [V15 p.54][V15] ; Δ : V16 (=, =, =, +1, +1, −2) redonne les 6 valeurs [V16 p.77][V16] | Conforme |
| Jan. 2025 (V16) | 4 / 22 / 15 / 28 / 10 / 21 | 4 / 22 / 15 / 28 / 10 / 21 | [V16 p.77][V16] ; Δ : V17 (+1, =, −2, −3, +2, +2) redonne les 6 valeurs [V17 p.76 et p.78][V17] | Conforme |
| Jan. 2026 (V17) | 5 / 22 / 13 / 25 / 12 / 23 | 5 / 22 / 13 / 25 / 12 / 23 ; NSP libellé « Ne se prononce pas : 23 % +2 » | [V17 p.76-78][V17] [PDF + image] | Conforme |

Remarques :

- Aucune presse trouvée avec la distribution complète ; la voie indépendante est donc le rapport de chaque vague et les deltas de la vague suivante. Les deltas couvrent les 6 colonnes de V8 à V11 et de V15 à V17, et les 5 blocs (sans NSP) pour V12, V13 et V14 ; pour ces trois vagues, le NSP (21, 20, 20) est contrôlé par la somme à 100 avec les 5 blocs.
- L'article de The Conversation du 8 mars 2022 sur « gauche et droite » utilise une **autre enquête** (Enquête électorale française, ENEF) et ne sert pas de contrôle ; il y est noté 7 % de non-réponse, contre 20 % dans le baromètre pour la même période [CONV22][CONV22] [WebFetch].
- Rupture possible dans la série : la vague 13 (jan. 2022) repose sur 10 566 inscrits, les autres sur environ 2 000 à 3 500.

---

### 6. Vague 17 : institutions (Q13), personnalités (Q14), partis (Q25)

Source du chiffre absolu : [V17][V17] (p.28 pour Q13, p.31 pour Q14, p.40 pour Q25) [PDF]. Contrôle indépendant : la valeur de la vague 16, dans [V16][V16] (p.29, p.32, p.41), plus le delta publié dans V17 redonne exactement la valeur 2025.

#### 6a. Institutions (Q13, V17 p.28)

| Élément | Valeur saisie | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Conseil municipal | 58 | 58, « = » (8 + 50) | [V17 p.28][V17] ; V16 : 58, −1 vs 59 (cohérent) [V16 p.29][V16] ; la courbe de V17 p.29 redonne 58 | Conforme |
| Conseil départemental | 49 | 49, −1 (4 + 45) | [V17 p.28][V17] ; V16 : 50 (49 + 1) [V16 p.29][V16] | Conforme |
| Conseil régional | 46 | 46, −3 (4 + 42) | [V17 p.28][V17] ; V16 : 49 (46 + 3) | Conforme |
| Cour des comptes | 44 (nouvel item) | 44, « Nouvel item » (7 + 37) | [V17 p.28][V17] ; absente de V16 p.29, ce qui confirme le nouvel item | Conforme |
| Conseil constitutionnel | 36 | 36, −3 (6 + 30) | [V17 p.28][V17] ; V16 : 39 (36 + 3) | Conforme |
| CESE | 33 | 33, −3 (4 + 29) | [V17 p.28][V17] ; V16 : 36 (33 + 3) | Conforme |
| Union européenne | 29 | 29, −3 (3 + 26) ; idem p.30 (tableau international) | [V17 p.28 et p.30][V17] ; V16 : 32 (29 + 3) | Conforme |
| Sénat | 26 | 26, −6 (2 + 24) ; idem p.30 | [V17 p.28 et p.30][V17] ; V16 : 32 (26 + 6) ; Public Sénat : « Sénat : 26 % » [PS17][PS17] [WebFetch] | Conforme |
| Parlement européen | 25 | 25, −4 (3 + 22) ; idem p.30 | [V17 p.28 et p.30][V17] ; V16 : 29 (25 + 4) | Conforme |
| Institution présidentielle | 22 | 22, −4 (3 + 19) | [V17 p.28][V17] ; V16 : 26 (22 + 4) | Conforme |
| Assemblée nationale | 20 | 20, −4 (2 + 18) | [V17 p.28 et p.30][V17] ; [A17][A17] [HTML] ; [PS17][PS17] ; [FI17][FI17] | Conforme |
| Gouvernement | 17 | 17, −6 (2 + 15) ; idem p.30 | [V17 p.28 et p.30][V17] ; V16 : 23 (17 + 6) ; [PS17][PS17] [WebFetch] : « Gouvernement : 17 % » | Conforme |

Seuls les chiffres de l'Assemblée, du Sénat, du gouvernement et du maire figurent dans la presse consultée. Les 8 autres chiffres de Q13 reposent sur le rapport V17 (lu en direct) et sur la cohérence avec V16. Un résumé de moteur de recherche cite aussi « 58 % conseil municipal, 49 % départemental, 46 % régional, 17 % gouvernement » (**[Moteur] seulement**, non utilisé) ; il concorde.

#### 6b. Personnalités (Q14, V17 p.31)

| Élément | Valeur saisie | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Maire | 60 | 60, −1 (14 + 46) | [V17 p.31][V17] ; [INF17][INF17] ; [A17][A17] | Conforme |
| Conseiller départemental | 44 | 44, −4 (4 + 40) | [V17 p.31][V17] ; [INF17][INF17] (2025 : 48 / 2026 : 44) ; V16 : 48 [V16 p.32][V16] | Conforme |
| Conseillers régionaux | 42 | 42, −4 (3 + 39) | [V17 p.31][V17] ; [INF17][INF17] (46 → 42) ; V16 : 46 | Conforme |
| Député | 34 | 34, −6 (4 + 30) | [V17 p.31][V17] ; [INF17][INF17] (40 → 34) ; V16 : 40 | Conforme |
| Députés européens | 27 | 27, −5 (3 + 24) | [V17 p.31][V17] ; [INF17][INF17] (32 → 27) ; V16 : 32 | Conforme |
| Premier ministre | 27 | 27, « = » (3 + 24) | [V17 p.31][V17] ; [INF17][INF17] (27 → 27) ; V16 : 27 | Conforme |
| Président de la République | 18 | 18, −5 (4 + 14) | [V17 p.31][V17] ; [INF17][INF17] (23 → 18) ; [A17][A17] | Conforme |

#### 6c. Partis politiques (Q25, V17 p.40)

| Élément | Valeur saisie | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Partis politiques | 15 | 15, −1 (2 + 13) ; 16 en 2025 et 20 en 2024 | [V17 p.40][V17] ; « seuls 15 % des Français déclarent leur faire confiance » [A17][A17] [HTML] ; « 15 % (16 % en 2025, 20 % en 2024) » [INF17][INF17] ; V16 p.41 = 16 (2 + 14) [V16][V16] ; V15 p.33 = 20 [V15][V15] ; [DEC17][DEC17] | Conforme |

À noter : un résumé de moteur de recherche citait « partis 16 % » pour 2026. C'est la valeur de 2025 ; le rapport et l'article donnent bien 15 % pour 2026.

---

### 7. Conditions de réutilisation et version anglaise

| Élément | Valeur saisie | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Mention de droits dans le rapport vague 17 | « © Sciences Po ? » | Aucune mention « © », « droits », « reproduction », « licence » ou « citer » dans les 169 pages du PDF. Seule marque : « pour Sciences Po CEVIPOF » et « OpinionWay » en pied de page (recherche dans le texte extrait) | [V17][V17] [PDF] | Non trouvé |
| Mention de droits sur le site | « © Sciences Po ? » | Pied de page : « © 2026 SCIENCES PO ». Les « Termes légaux » (Mentions légales, Conditions générales) s'appliquent à tout le domaine sciencespo.fr : « Toute utilisation ou reproduction, totale ou partielle, de la Plateforme, des éléments qui le composent et/ou des informations qui y figurent, par quelque procédé que ce soit, est strictement interdite […] sauf accord préalable et écrit de Sciences Po » | [TERMES][TERMES] [HTML] ; [A17][A17] (pied de page) | Écart expliqué (clause générale, pas de licence propre au baromètre) |
| Licence ou règle de citation propre au baromètre | (à trouver) | Aucune licence (Creative Commons, Etalab…) ni format de citation sur la page du baromètre, la page « Le Baromètre, c'est quoi ? », la page OpinionWay, la page de l'Institut de l'Entreprise, ni dans le rapport. Aucune mention de dépôt ouvert des données (Quetelet/Progedo) : la page du baromètre parle d'une « base de données constituée depuis 2011 » sans lien d'accès | [PAGEBARO][PAGEBARO] [HTML] ; [SPCEST][SPCEST] [WebFetch] ; [OW17][OW17] [WebFetch] ; [IE17][IE17] [WebFetch] | Non trouvé |
| Version anglaise | (à trouver) | Pas de version anglaise du rapport de la vague 17. Le site anglais `/cevipof/en/` n'a pas de page baromètre ; sa seule page sur la vague 16 est un résumé de 4 points de vue qui renvoie vers un PDF étiqueté « (french) ». La page OpinionWay est en français seulement (le lien « EN » mène à l'accueil). Seule trace d'anglais : 4 pages dans le rapport de la vague 14 (méthodologie et pages internationales), et le nom anglais « Political Trust Barometer » | [EN16][EN16] [WebFetch] ; [OW17][OW17] ; [V14 p.4][V14] ; sitemap anglais `https://www.sciencespo.fr/cevipof/en/sitemap-0.xml` [HTML] | Non trouvé |

Lecture pratique (sans valeur de conseil juridique) :

- Les chiffres isolés (« 22 % des Français déclarent avoir confiance dans la politique ») sont des résultats publiés ; la clause du site vise la reproduction du contenu de la plateforme. Pour un kit qui copie quelques chiffres, une citation exacte de la source et de la vague suffit en pratique ; pour reproduire des graphiques, des tableaux ou le PDF, il faut l'accord écrit du CEVIPOF.
- Citation proposée : « Baromètre de la confiance politique du CEVIPOF, vague 17 (janvier 2026), OpinionWay pour Sciences Po CEVIPOF, 3 166 inscrits sur les listes électorales, terrain du 12 au 28 janvier 2026 ».
- Si le jeu affiche des résultats de sondage, la loi du 19 juillet 1977 impose des mentions pour les sondages d'opinion liés aux élections. D'après un résumé de moteur de recherche (**[Moteur] seulement**, texte de loi non vérifié), la liste inclut l'organisme, le commanditaire, les dates, les questions et la marge d'erreur. Le baromètre mesure la confiance, pas des intentions de vote : à faire valider ; hors périmètre de cette vérification.
- Le plus sûr pour lever le doute : écrire au CEVIPOF ou passer par l'adresse de contact de la page du baromètre.

---

### 8. Notes « À savoir » prévues

#### Note 1 : sondage, pas statistique publique, marge d'erreur

- **Faits : confirmés.** OpinionWay pour le CEVIPOF ; 3 166 inscrits sur les listes électorales (sur 3 445 personnes interrogées, représentatives des 18 ans et plus) ; terrain du 12 au 28 janvier 2026 ; en ligne ; méthode des quotas [V17 p.3][V17].
- **Marge d'erreur : le rapport ne la donne pas pour 3 166.** La page 3 écrit : « les résultats de ce sondage doivent être lus en tenant compte des marges d'incertitude : 0,7 à 1,7 point au plus pour un échantillon de 3 500 répondants et 1 à 2,3 points pour un échantillon de 1 800 répondants ». La vague 14, avec 3 072 inscrits, écrivait « 0,8 à 1,8 point au plus pour un échantillon de 3 100 répondants » [V14 p.4][V14].
- **Calcul personnel (non publié par OpinionWay) :** pour n = 3 166, à 95 % de confiance, ±1,74 point pour un résultat à 50 % et ±0,76 point pour un résultat à 5 % ou 95 %. Cela retombe sur la fourchette d'OpinionWay (0,7 à 1,7 pour 3 500 ; 0,8 à 1,8 pour 3 100).
- **Rédaction proposée :** « Ce sont les résultats d'un sondage en ligne (OpinionWay pour le CEVIPOF, 3 166 inscrits sur les listes électorales, du 12 au 28 janvier 2026), pas une statistique publique. La marge d'incertitude est d'environ 1 à 2 points (0,7 à 1,7 point pour 3 500 répondants selon OpinionWay) ; elle est plus large pour un sous-groupe. » On peut ajouter que l'échantillon est construit par quotas, donc la marge est indicative.

#### Note 2 : mesure la confiance, jamais une intention de vote

- **Confirmée.** Aucune question d'intention de vote dans le rapport V17 (169 pages), l'infographie, les Décryptages et l'article. Aucune occurrence de « 2027 » dans ces quatre documents. La seule mention de « la prochaine présidentielle » est dans une question sur le fonctionnement du Parlement (q6v17 : revenir ou non à « une majorité nette à l'Assemblée nationale après la prochaine présidentielle », p.69), pas une intention de vote.
- Aucun changement nécessaire.

#### Note 3 : confiance maximale dans les élus locaux (maire 60 %), minimale dans le gouvernement et le président (17 et 18 %)

- **Chiffres corrects** (maire 60, gouvernement 17, président 18), mais **la formulation est inexacte à deux endroits**.
  1. « Les plus bas » : les **partis politiques sont à 15 %** et les réseaux sociaux à 15 % [V17 p.40][V17], donc plus bas que le gouvernement (17) et le président (18). Le gouvernement (17) est bien le plus bas des **institutions** de Q13, et le président (18) le plus bas des **personnalités** de Q14, mais la phrase doit le dire.
  2. « La plus haute » : le maire (60) est le plus haut des **élus et institutions politiques**, mais d'autres acteurs sont nettement au-dessus : artisans 84, science 82, PME 80, hôpitaux 79, gendarmerie 77 [V17 p.40][V17].
- 17 vient de Q13 (le gouvernement, institution) et 18 de Q14 (le président en exercice, personnalité) : l'« institution présidentielle » (Q13) est à 22 %.
- **Rédaction proposée :** « Parmi les élus et les institutions politiques, la confiance est la plus forte pour le maire (60 %) et la plus faible pour le gouvernement (17 %) et le président de la République (18 %) ; les partis politiques sont encore plus bas (15 %). » Le CEVIPOF dit lui-même « une confiance dans les partis et le chef de l'État au plus bas depuis 2009 » [A17][A17].

#### Note 4 : l'auto-positionnement est la seule mesure des courants chez les inscrits ; 23 % ne répondent pas

- **23 % : confirmé** (« Ne se prononce pas : 23 % », +2 sur 2025) [V17 p.76 et p.78][V17].
- **« La seule mesure » : vrai pour le rapport publié, pas pour l'enquête.** Le rapport V17 ne publie aucune autre distribution partisane (aucune proximité à un parti, aucun vote passé). Mais les Décryptages ([DEC17][DEC17] [PDF], pp. 2-3) croisent des résultats par proximité partisane (« sympathisants Renaissance », « sympathisants de La France insoumise », « Rassemblement national »…) : la proximité à un parti est donc mesurée dans les microdonnées, simplement pas publiée en distribution.
- **Rédaction proposée :** « Dans le rapport publié, l'auto-positionnement sur une échelle de 0 à 10 est la seule mesure des orientations politiques des inscrits ; 23 % ne se positionnent pas (« ne se prononce pas »). » Préciser « inscrits sur les listes électorales » : ce n'est pas toute la population (V17 p.3).

---

### 9. Autres points d'attention pour le kit

1. **Libellés de date.** Les libellés des courbes (déc. 2009, févr. 2020, févr. 2021…) sont ceux du rapport V17 ; le terrain réel est parfois un autre mois : oct. 2011 = 27 sept.-13 oct. ; déc. 2013 = 25 nov.-12 déc. ; « Fév. 2020 » = 28 janv.-4 fév. 2020 ; « Fév. 2021 » = 20-31 janv. 2021 (la mise en page à deux colonnes de la page méthodologie de V11 et V12 rend l'attribution des dates à la France très probable, pas certaine) ; « Jan. 2022 » = 23 déc. 2021-10 janv. 2022 ; « Fév. 2023 » = 27 janv.-9 fév. 2023 ; « Fév. 2025 » dans V16 = 17-29 janv. 2025. Aucun de ces écarts ne rend une valeur fausse ; ils comptent pour les phrases « en 2020 ».
2. **Taille et base des échantillons.** Déc. 2009 : 1 475 personnes, « représentatif de la population française âgée de 18 ans et plus » (sans la mention « inscrite sur les listes ») [V1 p.3][V1] ; vagues 2 à 8 : 1 500 à 2 064, « 18 ans et plus et inscrite sur les listes électorales » ; vague 9 à 12 : environ 2 000 à 2 100 ; vague 13 : 10 566 ; vagues 14 à 17 : 3 072 à 3 561. Marges d'incertitude annoncées : 1 à 2,5 points (vagues 2 à 6), 1 à 2,2 (vagues 7 à 12), 0,7 à 1,7 (vagues 15 à 17, calculées pour 3 500 répondants).
3. **Sources secondaires à écarter.** La page CESE du 24/02/2014 (voir §2). La presse écrit parfois « par rapport à 2019 » pour une hausse de la vague 11 de février 2020 (Public Sénat 2021) : le rapport V12 compare bien à février 2020.
4. **Pages non lisibles.** Le Monde (9 février 2026) et Le Figaro (2021) sont bloqués pour l'outil ; la page RCF a répondu HTTP 403 ; la tentative de lire la loi de 1977 sur Légifrance est tombée sur un autre texte. Aucune de ces pages n'est utilisée dans les verdicts.

---

### Conclusion

**Écarts et points à corriger (par ordre d'importance)**

1. **Note « À savoir » 3 : formulation à corriger.** Le gouvernement (17) et le président (18) ne sont pas les plus bas : les partis politiques et les réseaux sociaux sont à 15 %. Le maire n'est le plus haut que parmi les élus ; les artisans (84), la science (82), les hôpitaux (79) etc. sont au-dessus. Rédaction proposée au §8.
2. **Note « À savoir » 4 : nuance à ajouter.** « La seule mesure » vaut pour le rapport publié, pas pour l'enquête (la proximité partisane existe dans les microdonnées et dans les Décryptages). Les 23 % sont confirmés.
3. **Note « À savoir » 1 : la marge d'erreur n'est pas donnée pour 3 166** dans le rapport (0,7 à 1,7 pour 3 500 ; 1 à 2,3 pour 1 800). Calcul propre : environ 0,8 à 1,7 point à 95 %. À présenter comme un ordre de grandeur, la méthode étant par quotas.
4. **Source secondaire fausse :** CESE, 24/02/2014, donne 65 % pour le maire (vague 5) ; la valeur correcte et saisie est 61 %. À ne pas utiliser.
5. **Conditions de réutilisation : introuvables.** Pas de licence ni de règle de citation propre au baromètre ; seule la clause générale de Sciences Po (reproduction interdite sans accord écrit) et « © 2026 SCIENCES PO » en pied de site. Pas de version anglaise du rapport.
6. **PDF vague 17 remplacé après le 9 février** (généré le 13 mars 2026, Roumanie incluse). Les chiffres France sont les mêmes que dans l'infographie et la presse du 9-10 février.

**Aucun écart de valeur : toutes les valeurs saisies sont conformes.**

- Vague 17 : date de publication (9 février 2026), terrain (12-28 janvier 2026), 3 166 inscrits, 22 % (−4) et 26 % en 2025.
- Maire : 17 valeurs sur 17.
- Président : 13 sur 13.
- Assemblée nationale : 15 sur 15.
- Auto-positionnement : 10 vagues sur 10, soit 60 chiffres ; blocs 0-1 / 2-4 / 5 / 6-8 / 9-10.
- Vague 17, institutions : 12 sur 12 ; personnalités : 7 sur 7 ; partis : 15 %.
- Chaque valeur a été lue dans le rapport de sa propre vague puis recoupée par le delta de la vague suivante. Aucune n'a été validée sur un seul résumé de moteur de recherche.

**Ce qui repose sur une seule source forte** (le rapport d'origine plus le delta suivant, sans presse) : maire et président Jan. 2022 ; Assemblée 2009-2018 hors 2012 ; toute la distribution gauche-droite ; les huit chiffres Q13 non repris par la presse (conseils municipal, départemental, régional, Cour des comptes, Conseil constitutionnel, CESE, Union européenne, Parlement européen, institution présidentielle).

---

### URL consultées (consultation du 2026-11-02)

**Site CEVIPOF / Sciences Po**

- [A17]: https://www.sciencespo.fr/cevipof/fr/actualites/barometre-de-la-confiance-politique-cevipof-2026-la-confiance-s-effondre-en-politique-la-proximite-fait-figure-de-refuge/ (HTML)
- [A16]: https://www.sciencespo.fr/cevipof/fr/actualites/barometre-de-la-confiance-politique-du-cevipof-2025-le-grand-desarroi-democratique.html (HTML)
- [PAGEBARO]: https://www.sciencespo.fr/cevipof/fr/etudes-enquetes/barometre-confiance-politique/ (HTML)
- Liste des vagues : https://www.sciencespo.fr/cevipof/fr/content/le-barometre-de-la-confiance-politique (WebFetch)
- [SPCEST]: https://www.sciencespo.fr/fr/actualites/barometre-de-la-confiance-politique/ (WebFetch)
- [TERMES]: https://www.sciencespo.fr/fr/termes-legaux/ (HTML)
- [EN16]: https://www.sciencespo.fr/cevipof/en/news/4-points-of-view-on-the-cevipof-s-political-trust-barometer/ (WebFetch) ; https://www.sciencespo.fr/cevipof/en/ (HTML) ; https://www.sciencespo.fr/cevipof/en/sitemap-0.xml (HTML)
- [INF17]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BaroConf2026_infographieFChanvril_V17_PremiersResultats.pdf
- [DEC17]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BCP2026_Decryptages_fev2026.pdf
- [BILAN15]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/Bilan%2015ans%20Baro_FC_BD.pdf (PDF sans couche texte, lu en image)
- [DIX19]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/CEVIPOF_confiance_10ans_CHEURFA_CHANVRIL_2019.pdf

**Rapports par vague (PDF, téléchargés et extraits)**

- [V17]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/Barometre_confiance_CEVIPOFVague17_fev2026_vd1.pdf
- [V16]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/Barometre%20confiance%20CEVIPOF%20Vague%2016%20fev%202025-v2_0.pdf
- [V15]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BConf_V15_Extraction1_modif.pdf
- [V14]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/OpinionWay%20pour%20le%20CEVIPOF%20-%20Barom%c3%a8tre%20de%20la%20confiance%20en%20politique%20-%20vague%2014%20-%20F%c3%a9vrier%202023.pdf
- [V14FR]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/Barometre%20de%20la%20confiance%20en%20politique%20-%20vague%2014%20-%20Fevrier%202023%20-%20vFR.pdf%20(1).pdf
- [V13]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/OpinionWay%20pour%20le%20CEVIPOF-Barome%cc%80tre%20de%20la%20confiance%20en%20politique%20-%20vague%2013%20-%20janvier%202022.pdf
- [V12]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/OpinionWay%20pour%20le%20CEVIPOF-Barome%cc%80tre%20de%20la%20confiance%20en%20politique%20-%20vague12%20-%20Rapport%20international%20(1).pdf
- [V11]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/OpinionWay%20pour%20le%20CEVIPOF-Barome%cc%80tre%20de%20la%20confiance%20en%20politique%20-%20vague11%20-%20Comparaison-1.pdf
- [V10]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/CEVIPOF_confiance_vague10-1.pdf
- [V9]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/Barometre_confiance_vague9.pdf
- [V8]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ15515-CEVIPOF-Barometre_confiance_en_politique_vague8-1.pdf
- [V7]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ15515-CEVIPOF-Barometre_confiance_en_politique_vague7-vdef.pdf
- [V6]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ10890-CEVIPOF-Barometre_confiance_en_politique_vague6_VF.pdf
- [V5]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ9724%20-%20CEVIPOF%20-%20Barome%cc%80tre%20confiance%20en%20politique%20vag5%20VF.pdf
- [V4]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ8950%20-%20CEVIPOF%20-%20Barome%cc%80tre%20confiance%20en%20politique%20vag4%20VF.pdf
- [V3]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ6992%20-%20CEVIPOF%20-%20Barome%cc%80tre%20confiance%20en%20politique%20vag3_V2.pdf
- [V2]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ6992%20-%20CEVIPOF%20-%20Barome%cc%80tre%20confiance%20en%20politique%20vag2_PREZVF.pdf
- [V1]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ6127-CEVIPOF-Confiance%20en%20politique%20V1-1.pdf

**Presse et sources institutionnelles**

- [CESE17]: https://www.lecese.fr/print/pdf/node/20420 (PDF, lu ; publié le 03/02/2026, séance plénière du 10 février 2026)
- [CESE14]: https://www.lecese.fr/content/le-cese-partenaire-du-5e-sondage-cevipof (WebFetch ; erreur sur le maire)
- [CESE15]: https://www.lecese.fr/content/le-cese-soutient-le-barometre-cevipof-de-la-confiance-politique-pour-la-3eme-annee-consecutive (WebFetch)
- [PS17]: https://www.publicsenat.fr/actualites/politique/78-des-francais-nont-pas-confiance-en-la-politique-selon-le-barometre-de-cevipof (WebFetch)
- [PS21]: https://www.publicsenat.fr/actualites/politique/barometre-du-cevipof-les-francais-font-davantage-confiance-a-leurs-elus-187710 (WebFetch)
- [PS18]: https://www.publicsenat.fr/actualites/politique/barometre-de-confiance-politique-un-leger-effet-macron-mais-toujours-une-forte (WebFetch)
- [FI17]: https://www.franceinfo.fr/politique/seuls-22-des-francais-ont-confiance-en-la-politique-en-recul-de-quatre-points-en-un-an-selon-l-enquete-annuelle-du-cevipof_7794830.html (WebFetch)
- [FI25]: https://www.franceinfo.fr/politique/confiance-dans-la-politique-la-defiance-des-francais-est-a-un-niveau-jamais-mesure-selon-le-cevipof-qui-publie-son-barometre-annuel_7068434.html (WebFetch)
- [FI20]: https://www.franceinfo.fr/politique/politiques-soignants-policiers-trois-enseignements-a-retenir-du-barometre-de-la-confiance-politique-du-cevipof_3853057.html (WebFetch)
- [MI21]: https://www.maire-info.com/elus/confiance-les-maires-toujours-plebiscites-les-elus-nationaux-progressent-un-peu-art26-25049 (WebFetch)
- [MI25]: https://www.maire-info.com/elus/dans-un-climat-de-defiance-generalisee-la-confiance-envers-les-maires-ne-se-dement-pas-art26-29390 (WebFetch)
- [AP19]: https://acteurspublics.fr/articles/la-confiance-des-francais-dans-leurs-institutions-est-au-plus-bas/ (WebFetch)
- [AP24]: https://acteurspublics.fr/articles/60-des-francais-ont-confiance-en-leur-maire/ (WebFetch)
- [LT24]: https://www.banquedesterritoires.fr/les-francais-font-toujours-davantage-confiance-leur-maire (WebFetch)
- [LT25]: https://www.banquedesterritoires.fr/barometre-cevipof-lelu-local-rare-rescape-dune-vaste-crise-de-confiance (WebFetch)
- [OW17]: https://www.opinion-way.com/fr/publications/en-quoi-les-francais-ont-ils-confiance-aujourdhui-2-2026-22435/ (WebFetch)
- [IE17]: https://www.institut-entreprise.fr/publication/cevipof_-_le_barometre_de_la_confiance_politique_vague_17/ (WebFetch)
- [CONV22]: https://theconversation.com/la-gauche-et-la-droite-font-elles-encore-sens-en-france-178181 (WebFetch ; autre enquête, non utilisée comme contrôle)
- [TWEET]: https://x.com/CEVIPOF/status/2020937651998577042 (**résumé de moteur seulement**, page non lue)

**Consultées sans résultat exploitable** : https://www.rcf.fr/articles/actualite/confiance-politique-face-a-la-defiance-nationale-la-proximite-devient-le-dernier (HTTP 403) ; Le Monde, 9 février 2026, et Le Figaro, 2021 (bloqués pour l'outil) ; https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000699944 (mauvais texte) ; https://www.vie-publique.fr/eclairage/23927-sondages-dopinion-une-legislation-recemment-renovee (page vide).

<!-- Définitions de liens (Markdown de référence) -->

[A17]: https://www.sciencespo.fr/cevipof/fr/actualites/barometre-de-la-confiance-politique-cevipof-2026-la-confiance-s-effondre-en-politique-la-proximite-fait-figure-de-refuge/
[A16]: https://www.sciencespo.fr/cevipof/fr/actualites/barometre-de-la-confiance-politique-du-cevipof-2025-le-grand-desarroi-democratique.html
[PAGEBARO]: https://www.sciencespo.fr/cevipof/fr/etudes-enquetes/barometre-confiance-politique/
[SPCEST]: https://www.sciencespo.fr/fr/actualites/barometre-de-la-confiance-politique/
[TERMES]: https://www.sciencespo.fr/fr/termes-legaux/
[EN16]: https://www.sciencespo.fr/cevipof/en/news/4-points-of-view-on-the-cevipof-s-political-trust-barometer/
[INF17]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BaroConf2026_infographieFChanvril_V17_PremiersResultats.pdf
[DEC17]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BCP2026_Decryptages_fev2026.pdf
[BILAN15]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/Bilan%2015ans%20Baro_FC_BD.pdf
[DIX19]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/CEVIPOF_confiance_10ans_CHEURFA_CHANVRIL_2019.pdf
[V17]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/Barometre_confiance_CEVIPOFVague17_fev2026_vd1.pdf
[V16]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/Barometre%20confiance%20CEVIPOF%20Vague%2016%20fev%202025-v2_0.pdf
[V15]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BConf_V15_Extraction1_modif.pdf
[V14]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/OpinionWay%20pour%20le%20CEVIPOF%20-%20Barom%c3%a8tre%20de%20la%20confiance%20en%20politique%20-%20vague%2014%20-%20F%c3%a9vrier%202023.pdf
[V14FR]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/Barometre%20de%20la%20confiance%20en%20politique%20-%20vague%2014%20-%20Fevrier%202023%20-%20vFR.pdf%20%281%29.pdf
[V13]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/OpinionWay%20pour%20le%20CEVIPOF-Barome%cc%80tre%20de%20la%20confiance%20en%20politique%20-%20vague%2013%20-%20janvier%202022.pdf
[V12]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/OpinionWay%20pour%20le%20CEVIPOF-Barome%cc%80tre%20de%20la%20confiance%20en%20politique%20-%20vague12%20-%20Rapport%20international%20%281%29.pdf
[V11]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/OpinionWay%20pour%20le%20CEVIPOF-Barome%cc%80tre%20de%20la%20confiance%20en%20politique%20-%20vague11%20-%20Comparaison-1.pdf
[V10]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/CEVIPOF_confiance_vague10-1.pdf
[V9]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/Barometre_confiance_vague9.pdf
[V8]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ15515-CEVIPOF-Barometre_confiance_en_politique_vague8-1.pdf
[V7]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ15515-CEVIPOF-Barometre_confiance_en_politique_vague7-vdef.pdf
[V6]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ10890-CEVIPOF-Barometre_confiance_en_politique_vague6_VF.pdf
[V5]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ9724%20-%20CEVIPOF%20-%20Barome%cc%80tre%20confiance%20en%20politique%20vag5%20VF.pdf
[V4]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ8950%20-%20CEVIPOF%20-%20Barome%cc%80tre%20confiance%20en%20politique%20vag4%20VF.pdf
[V3]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ6992%20-%20CEVIPOF%20-%20Barome%cc%80tre%20confiance%20en%20politique%20vag3_V2.pdf
[V2]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ6992%20-%20CEVIPOF%20-%20Barome%cc%80tre%20confiance%20en%20politique%20vag2_PREZVF.pdf
[V1]: https://www.sciencespo.fr/cevipof/sites/sciencespo.fr.cevipof/files/BJ6127-CEVIPOF-Confiance%20en%20politique%20V1-1.pdf
[CESE17]: https://www.lecese.fr/print/pdf/node/20420
[CESE14]: https://www.lecese.fr/content/le-cese-partenaire-du-5e-sondage-cevipof
[CESE15]: https://www.lecese.fr/content/le-cese-soutient-le-barometre-cevipof-de-la-confiance-politique-pour-la-3eme-annee-consecutive
[PS17]: https://www.publicsenat.fr/actualites/politique/78-des-francais-nont-pas-confiance-en-la-politique-selon-le-barometre-de-cevipof
[PS21]: https://www.publicsenat.fr/actualites/politique/barometre-du-cevipof-les-francais-font-davantage-confiance-a-leurs-elus-187710
[PS18]: https://www.publicsenat.fr/actualites/politique/barometre-de-confiance-politique-un-leger-effet-macron-mais-toujours-une-forte
[FI17]: https://www.franceinfo.fr/politique/seuls-22-des-francais-ont-confiance-en-la-politique-en-recul-de-quatre-points-en-un-an-selon-l-enquete-annuelle-du-cevipof_7794830.html
[FI25]: https://www.franceinfo.fr/politique/confiance-dans-la-politique-la-defiance-des-francais-est-a-un-niveau-jamais-mesure-selon-le-cevipof-qui-publie-son-barometre-annuel_7068434.html
[FI20]: https://www.franceinfo.fr/politique/politiques-soignants-policiers-trois-enseignements-a-retenir-du-barometre-de-la-confiance-politique-du-cevipof_3853057.html
[MI21]: https://www.maire-info.com/elus/confiance-les-maires-toujours-plebiscites-les-elus-nationaux-progressent-un-peu-art26-25049
[MI25]: https://www.maire-info.com/elus/dans-un-climat-de-defiance-generalisee-la-confiance-envers-les-maires-ne-se-dement-pas-art26-29390
[AP19]: https://acteurspublics.fr/articles/la-confiance-des-francais-dans-leurs-institutions-est-au-plus-bas/
[AP24]: https://acteurspublics.fr/articles/60-des-francais-ont-confiance-en-leur-maire/
[LT24]: https://www.banquedesterritoires.fr/les-francais-font-toujours-davantage-confiance-leur-maire
[LT25]: https://www.banquedesterritoires.fr/barometre-cevipof-lelu-local-rare-rescape-dune-vaste-crise-de-confiance
[OW17]: https://www.opinion-way.com/fr/publications/en-quoi-les-francais-ont-ils-confiance-aujourdhui-2-2026-22435/
[IE17]: https://www.institut-entreprise.fr/publication/cevipof_-_le_barometre_de_la_confiance_politique_vague_17/
[CONV22]: https://theconversation.com/la-gauche-et-la-droite-font-elles-encore-sens-en-france-178181
[TWEET]: https://x.com/CEVIPOF/status/2020937651998577042

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
