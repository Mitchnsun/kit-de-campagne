# `electricityProduction` · Électricité (partie du mix électrique)

**Vérifiée le 02/11/2026** : double vérification sur le web, valeurs de 2025 conformes (section « Double vérification ») ; avant d'entrer dans le kit, la source scindée en deux (le rapport cité, ses données sous Licence Ouverte) et la note sur la part bas-carbone précisée (conventions de RTE). Complétée le 09/11/2026 : la part du nucléaire, conforme au Bilan 2025 (section 8).

| Champ | Valeur |
| --- | --- |
| Indicateur | `electricityProduction`, partie « Électricité » de la page composite `electricityMix`, dossier « Écologie et énergie » (`ecology`), ticket #29 de l'app (statut `planned`) ; l'autre partie, `energyMix` (SDES), viendra plus tard |
| Données | `briefings/data/electricityProduction.json`, écrit par `yarn briefings electricityProduction` le 2026-11-02, puis le 2026-11-09 (part du nucléaire, #307) |
| Sources | RTE, « Bilan électrique 2025 », https://analysesetdonnees.rte-france.com/bilan-electrique-2025/synthese (anglais : « Annual Electricity Review 2025 », https://analysesetdonnees.rte-france.com/en/annual-review-2025/keyfindings), cité (mentions légales de RTE : réutilisation « sous réserve de mentionner la source ») ; RTE (ODRÉ), « Production nationale annuelle par filière (2012 à 2025) », Licence Ouverte v2.0, modifié le 25/02/2026, le jour de la publication du Bilan |
| Séries | `lowCarbonShare` : part bas-carbone de la production, 95,2 % en 2025, lue dans le texte du Bilan (« Cela représente 95,2 % de l'électricité produite sur le territoire métropolitain ») ; `total`, `nuclear`, `hydro`, `wind`, `solar`, `bioenergy`, `fossil` : production par filière en TWh, 2012 à 2025 ; `nuclearShare` : part du nucléaire dans la production, en %, 2012 à 2025 (68,1 % en 2025), calculée par le script (#307) |
| Chiffre clé | 95,2 % d'électricité bas-carbone en 2025, la part de RTE citée telle quelle (#29) ; une seule année, pas de tendance |
| Règles | Le script s'arrête si le texte du Bilan ne dit plus la part, ou si le Bilan et les données ne sont pas de la même année. Recalculée depuis ODRÉ, la part vaudrait 96,6 % hors fossiles ou 94,6 % sans les bioénergies : l'écart tient aux conventions de RTE (la moitié des déchets ménagers comptée renouvelable, 70 % du pompage des STEP retranché de l'hydraulique). La part du nucléaire, elle, est calculée : `production_nucleaire` / `production_totale` × 100, au dixième, chaque année ; le script échoue sur une année sans total |
| Première édition | À remplir à la publication |

## « À savoir »

1. Part de l'électricité, pas de l'énergie : la part du nucléaire, 68,1 % de la production en 2025, se lit dans la série `nuclearShare` (373,0 / 547,5) et dans le Bilan électrique 2025 de RTE (page Production : « 68,1 % en 2025 ») ; mix énergétique : SDES, Chiffres clés de l'énergie, édition 2026 (30/09/2026, données 2025 provisoires), pétrole 38 %, électricité 27 %, gaz 18 % de la consommation finale.
2. Le piège du débat de 2007 : transcription du débat du 2 mai 2007 (Vie publique), Nicolas Sarkozy : « La moitié de notre électricité est d'origine nucléaire », Ségolène Royal : « Non, 17 % seulement de l'électricité » (mots relevés dans la transcription par une vérification sur les sources primaires, le 09/11/2026, que l'agent de cette mise à jour n'a pas relue ; l'échange, 50 % contre 17 %, est aussi rapporté par World Nuclear News, « French candidates slip up on nuclear facts »). La part réelle : Annales des Mines, « Faits et chiffres pour 2007 », électricité (Réalités industrielles, août 2008) : « La production totale nette d'électricité s'élève à 544,4 TWh […]. Elle se répartit en 418,6 TWh nucléaires (76,9 %) ». La note donne la production nette, celle de la source ; elle ne dit pas ce que chacun pensait mesurer.
3. Les conventions de RTE : note du graphique de la part bas-carbone et glossaire du Bilan (« par convention, 50 % des déchets ménagers sont considérés comme renouvelables »).
4. Consommation 2025 : 451,2 TWh corrigés ; solde exportateur 92,3 TWh, record pour la deuxième année ; périmètre « France métropolitaine et Corse ».

Non repris : les écarts de 0,1 à 0,2 TWh entre le fichier et les Bilans d'origine pour 2012 et 2024 (révision de la série par RTE, probablement) ; le fioul 2025 à 1,7 TWh dans le texte de RTE, 1,6 dans sa figure et dans ODRÉ (somme cohérente avec 18,7). Retiré le 09/11/2026, pour garder quatre points : « la production d'origine fossile (18,7 TWh en 2025) la plus faible depuis le début des années 1950, selon RTE » (sa vérification reste en section 5, note 4).

À actualiser : le Bilan électrique 2026, vers février 2027.

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans relire la source du script. Son rapport, tel quel :

Date de la vérification : 2026-11-02. Méthode : sources web uniquement, API ODRÉ non appelée, aucun fichier de `/home/user` lu ou modifié.

Comment lire les sources. Les pages HTML ont été lues avec un outil qui en renvoie un résumé automatique. Pour les valeurs importantes, j'ai donc recoupé avec le **texte brut des PDF** de RTE (rapport complet anglais, « Key findings » anglais, « Principaux résultats » français, extraits avec `pdftotext`) : ces lignes sont marquées « PDF ». Une valeur « résumé de moteur de recherche » n'a été retenue nulle part comme preuve unique, sauf mention explicite.

Abréviations des sources (URL complètes en fin de document) :
- **[Syn]** page de synthèse du Bilan 2025 ; **[Prod]** page « Production » du Bilan 2025 ; **[EN-Gen]** page anglaise « Generation ».
- **[PR-fr]** PDF « Principaux résultats » (français) ; **[KF-en]** PDF « Key findings » (anglais) ; **[RC-en]** PDF « Full report » (anglais, 146 pages).
- **[CP]** actualité/communiqué RTE du 25/02/2026 ; **[Pub]** page « Bilans électriques nationaux et régionaux » de rte-france.com.
- **[ML]** mentions légales de analysesetdonnees.rte-france.com ; **[eCO2]** page éCO2mix « La production d'électricité par filière ».
- **[B24]** page « Production » du Bilan 2024 ; **[B12]** Bilan électrique 2012 (PDF, copie hébergée par pole-medee.com, métadonnées : créé le 18/01/2013).
- **[DG]** fiche data.gouv.fr du jeu de données (métadonnées, pas les données) ; **[CdE]** Connaissance des énergies.
- **[SDES-CC]** SDES, Chiffres clés de l'énergie, édition 2026 ; **[SDES-Bilan]** SDES, bilan énergétique 2025 provisoire.

---

### 1. Production 2025, 2024 et 2012 (France métropolitaine, TWh)

#### 1.a Année 2025

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Total 2025 | 547,5 | 547,5 (« a atteint 547,5 TWh en 2025 », +8,2 TWh, +1,5 %) | [Syn], [PR-fr] (PDF), [RC-en] fig. 2.1 et 2.2 (PDF), [CP] | Conforme |
| Nucléaire 2025 | 373,0 | 373,0 (+11,3 TWh ; 68,1 % du mix) | [Prod], [PR-fr] (PDF), [RC-en] fig. 2.2 (PDF) | Conforme |
| Hydraulique 2025 | 62,4 | 62,4 (−12,9 TWh ; 11,4 %) | [Prod], [RC-en] fig. 2.2 (PDF) | Conforme |
| Éolien 2025 | 49,6 | 49,6 = 43,9 terrestre + 5,7 en mer (9,1 %) | [RC-en] fig. 2.2 (PDF) ; [Prod] pour 43,9 et 5,7 ; [CdE] pour 49,6 | Conforme |
| Solaire 2025 | 32,9 | 32,9 (+8,1 TWh, +32,7 % ; 6,0 %) | [Prod], [RC-en] (PDF) | Conforme |
| Bioénergies 2025 | 10,9 | 10,9 (« Thermique renouvelable et déchets », 2,0 %) | [RC-en] fig. 2.2 (PDF) ; [CdE] (« thermiques renouvelables et déchets : 10,9 TWh ») | Conforme (RTE n'emploie pas le mot « bioénergies » dans le rapport ; c'est le nom de la filière ODRÉ et d'éCO2mix) |
| Thermique fossile 2025 | 18,7 | 18,7 (gaz + fioul + charbon) | [Prod], [RC-en] p. 46 (PDF) | Conforme |
| Gaz 2025 | 16,4 | 16,4 (3,0 %) | [Prod], [RC-en] fig. 2.2 (PDF) | Conforme |
| Fioul 2025 | 1,6 | **1,6** dans la figure 2.2 du rapport ; **1,7** dans le texte du rapport (p. 46) et sur la page [Prod] | [RC-en] fig. 2.2 et p. 46 (PDF) ; [Prod] | Écart expliqué : RTE donne deux valeurs ; le fichier suit la figure (16,4 + 1,6 + 0,7 = 18,7 ; avec 1,7 la somme ferait 18,8). Arrondi interne à RTE |
| Charbon 2025 | 0,7 | 0,7 (0,1 %) | [Prod], [RC-en] (PDF) | Conforme |
| Cohérence de la somme | 373,0 + 62,4 + 49,6 + 32,9 + 10,9 + 18,7 = 547,5 | La figure 2.2 de RTE ajoute une ligne « Autres : 0,1 TWh » (somme des lignes de la figure : 547,6) | [RC-en] fig. 2.2 (PDF) | Conforme à l'arrondi près ; la catégorie « Autres » n'est pas dans le fichier |

#### 1.b Année 2024

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Total 2024 | 539,3 | 539,3 (fig. 2.1 ; 547,5 − 8,2 = 539,3) | [RC-en] fig. 2.1 (PDF) ; [B24] affiche « 539 » | Conforme |
| Nucléaire 2024 | 361,7 | 361,7 (373,0 − 11,3) ; [B24] : 361,7 | [RC-en] (PDF), [B24] | Conforme |
| Hydraulique 2024 | 75,3 | 75,3 déduit (62,4 + 12,9). [B24] affiche 75,1 | [RC-en] (PDF), [B24] | Écart expliqué : 0,2 TWh entre deux éditions de RTE (révision ou définition) ; le fichier suit la série du Bilan 2025. Valeur 75,1 lue via résumé automatique, à ne pas considérer comme recoupée |
| Éolien 2024 | 46,8 | 46,8 = 42,8 terrestre + 4,0 en mer ; cohérent avec 49,6 − 2,8 (« +2,8 TWh » de RTE) | [B24], [RC-en] (PDF), [Prod] | Conforme |
| Solaire 2024 | 24,8 | 24,8 (32,9 − 8,1) ; [B24] : 24,8. La fiche [DG] précise que le solaire 2022-2024 a été relevé après un recalcul de l'autoconsommation | [RC-en] (PDF), [B24], [DG] | Conforme (valeur révisée ; ne pas comparer avec d'anciennes publications) |
| Bioénergies 2024 | 10,6 | [B24] affiche 10,5. Le Bilan 2025 ne donne pas de valeur 2024 pour cette filière dans le texte | [B24] | Écart expliqué probable (0,1 TWh, arrondi ou révision) ; valeur exacte du Bilan 2025 non trouvée |
| Thermique fossile 2024 | 20,0 | 20,0 dans [B24] et par différence (18,7 + 1,3) ; mais le texte du rapport 2025 écrit « 19,9 TWh » en 2024 (p. 46) | [B24], [RC-en] p. 46 (PDF) | Écart expliqué : arrondi interne à RTE (−1,3 TWh et 19,9 ne sont compatibles avec 18,7 qu'à ±0,1) |

#### 1.c Année 2012

Source primaire : Bilan électrique 2012 de RTE, tableau « Bilan énergétique France 2012 » [B12]. Je n'ai pas trouvé de source RTE récente donnant la série 2012 révisée par filière (ni le rapport 2025 ni les pages consultées ne la donnent en valeurs ; l'API ODRÉ est exclue).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Total 2012 | 542 | 541,4 (« production nette », −0,3 % vs 2011) ; le texte écrit aussi « 541 TWh ». À noter : la somme des filières du fichier (405 + 63,8 + 14,9 + 4,1 + 5,8 + 48,1) fait 541,7, arrondi à 542 | [B12] p. 3 | Écart (0,3 à 0,6 TWh) : cause probable, une révision de la série par RTE depuis 2013, non confirmée par une source |
| Nucléaire 2012 | 405 | 404,9 | [B12] | Conforme (arrondi) |
| Hydraulique 2012 | 63,8 | 63,8 | [B12] | Conforme |
| Éolien 2012 | 14,9 | 14,9 | [B12] | Conforme |
| Solaire 2012 | 4,1 | 4,0 (« La production photovoltaïque s'élève à 4,0 TWh ») | [B12] | Écart (0,1 TWh), probable révision/arrondi, non confirmé |
| Bioénergies 2012 | 5,8 | 5,9 (« autres sources d'énergies renouvelables » : déchets ménagers, déchets de papeterie, biomasse, biogaz) | [B12] | Écart (0,1 TWh), probable révision/arrondi, non confirmé |
| Thermique fossile 2012 | 48,1 | 47,9 (charbon 18,1 + fioul 6,6 + gaz 23,2) | [B12] | Écart (0,2 TWh), probable révision/arrondi, non confirmé |

Remarque de forme : le fichier arrondit 2012 à l'entier pour le total et le nucléaire (542 et 405) mais pas pour les autres lignes (une décimale). Si le fichier garde ces deux valeurs entières, le dire (« arrondi ») ou passer à 541,7 et 405,0 pour rester homogène avec le reste.

---

### 2. Part bas-carbone telle qu'écrite par RTE

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Phrase citée | « Le volume de production d'électricité bas-carbone (nucléaire et renouvelable) en France a atteint en 2025 un maximum historique, soit 521,1 TWh. Cela représente 95,2 % de l'électricité produite sur le territoire métropolitain » | Phrase identique dans le PDF français, qui continue par « , une part similaire à celle de 2024. » (95,0 % en 2024). La même phrase existe en anglais : « The volume of low-carbon (nuclear and renewable) electricity generated in France reached an all-time high of 521.1 TWh in 2025. This represents 95.2% of the electricity generated in mainland France » | [PR-fr] (PDF), [Syn], [KF-en] (PDF) | Conforme (citation tronquée avant « une part similaire à celle de 2024 » : fermer par un point ou une ellipse) |
| Volume bas-carbone 2025 | 521,1 TWh | 521,1 TWh | [PR-fr], [Syn], [CP], [KF-en] | Conforme |
| Part bas-carbone 2025 | 95,2 % | 95,2 % (521,1 / 547,5 = 95,18 %) ; 95,0 % en 2024 ; part renouvelable 27,0 % en 2025 contre 27,9 % en 2024 | [PR-fr], [RC-en] fig. 2.1 (PDF) | Conforme |
| Part sans fossile (note #29) | 96,6 % | (547,5 − 18,7) / 547,5 = 96,58 % (calcul de ma part) | calcul sur 1.a | Conforme (arithmétique) |
| Part sans bioénergies (note #29) | 94,6 % | (547,5 − 18,7 − 10,9) / 547,5 = 94,59 % (calcul de ma part) | calcul sur 1.a | Conforme (arithmétique) |
| Comptage des bioénergies par RTE | « part renouvelable ? » | Oui, en partie. Définition RTE de « Thermique renouvelable et déchets » : production des centrales thermiques à partir de bioénergies (biomasse solide et biogaz), de déchets papetiers ou de déchets ménagers (« par convention, 50 % des déchets ménagers sont considérés comme renouvelables »). Note de bas de graphique sous la part bas-carbone : « La production à partir de déchets ménagers est considérée renouvelable à 50 %. La production hydraulique est retranchée de 70 % de la consommation de pompage des STEP selon la Directive européenne 2009/28/CE. » Les déchets industriels et la part non renouvelable des déchets ménagers sont comptés comme émetteurs (988 gCO2e/kWh), biogaz et biomasse à 70, bois à 66, déchets renouvelables à 0. éCO2mix confirme que la filière Bioénergies « inclut également la production à partir de déchets, qui est en partie non renouvelable » | [PR-fr] (PDF), [RC-en] glossaire et annexe p. 145 (PDF), [eCO2] | Conforme, avec un point qui change la note (voir ci-dessous) |

#### Vérification des 521,1 TWh (reconstitution de ma part, RTE ne publie pas le détail)

Le rapport définit le bas-carbone comme nucléaire + renouvelable. Je l'ai reconstitué ainsi :

| Terme | TWh | Origine |
|---|---|---|
| Nucléaire | 373,0 | RTE |
| Hydraulique brute | 62,4 | RTE |
| − 70 % du pompage des STEP (0,7 × 8,1) | −5,7 | pompage 8,1 TWh en 2025 : [RC-en] p. 12 (PDF) ; règle 70 % : note de bas de graphique |
| Éolien | 49,6 | RTE |
| Solaire | 32,9 | RTE |
| Bioénergies comptées bas-carbone | ≈ 8,9 | **déduit** : 521,1 − (373,0 + 56,7 + 49,6 + 32,9) |
| Total | 521,1 | RTE |

Contrôles : (521,1 − 373,0) / 547,5 = 27,05 %, soit les « 27 % » de part renouvelable de RTE, donc le nucléaire est bien la seule source bas-carbone non renouvelable. Les ≈ 2,0 TWh de bioénergies non comptées (10,9 − 8,9) correspondent à l'ordre de grandeur des 2,3 MtCO2e que RTE attribue à l'incinération de déchets non renouvelables (≈ 2,3 TWh au facteur 988 gCO2e/kWh). Écart de 0,3 TWh : au-delà de l'arrondi, donc la déduction reste une estimation.

**Conséquence pour la note #29 et pour la note (2).** Le passage de 96,6 % (somme brute hors fossile) à 95,2 % (RTE) se décompose à peu près ainsi : 528,8 − 521,1 = 7,7 TWh, dont environ 5,7 TWh pour la déduction du pompage des STEP (≈ 1,0 point) et environ 2,0 TWh pour la part non renouvelable des déchets (≈ 0,4 point). Le traitement des bioénergies n'explique donc qu'une partie de l'écart ; la déduction du pompage hydraulique pèse davantage, et elle est invisible dans les valeurs par filière du fichier. Le même constat est fait, sans explication, par [CdE] (« environ 7,7 TWh de plus que les 521,1 TWh annoncés »).

---

### 3. Dates et licences

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Publication du Bilan électrique 2025 | « février 2026 ? » | 25/02/2026 : date de l'actualité/communiqué RTE et du PDF « Principaux résultats ». Le « Rapport complet » est daté du 03/03/2026 sur rte-france.com. Presse : « RTE, en publiant son bilan électrique annuel » le 25 février ; [CdE] « Mis à jour le 26 février 2026 » (le texte dit « ce 25 février ») ; NucNet 06/03/2026. Les pages du portail analysesetdonnees ne portent pas de date | [CP], [Pub], [CdE], [NucNet] | Conforme (février 2026, le 25) |
| Dernière mise à jour du jeu ODRÉ | 25/02/2026 | Fiche data.gouv.fr du jeu « Production nationale annuelle par filière (2012 à 2025) » : « Dernière mise à jour 25 février 2026 », CSV et JSON « mis à jour le 25 février 2026 ». Diffuseur « Open Data Réseaux Énergies », créateur et éditeur : RTE | [DG] | Conforme (source : la fiche data.gouv.fr, pas la page ODRÉ, que je n'ai pas consultée) |
| Licence des données ODRÉ | Licence Ouverte v2.0 | « Licence Ouverte / Open Licence version 2.0 » sur la fiche data.gouv.fr | [DG] | Conforme (même réserve : métadonnées data.gouv.fr, pas la page ODRÉ) |
| Note sur le jeu ODRÉ | non mentionnée | « Suite à un recalcul de l'autoconsommation photovoltaïque, la production photovoltaïque sur les années 2022 à 2024 a augmenté. » | [DG] | À reprendre dans la note de source : un solaire 2022-2024 lu dans une ancienne publication RTE sera plus bas |
| Licence du texte et des chiffres du rapport (portail analysesetdonnees) | « Licence Ouverte ? » | **Aucune licence n'est indiquée** sur les pages du Bilan ni sur le communiqué. Les mentions légales du portail disent : « Les données publiées sur le site … sont publiques et leur réutilisation est permise sous réserve de mentionner la source. » ; les éléments du site sont « soumis à la législation protégeant le droit d'auteur » et « aucune licence, ni aucun autre droit sauf celui de consulter les informations, n'est conféré à quiconque » ; toute autre utilisation du contenu (texte, images) suppose une autorisation écrite préalable de RTE, avec citation de la source. Les mentions ne sont pas datées | [ML], [Syn], [CP], [Pub] | Écart : le texte du rapport n'est pas sous Licence Ouverte. Seule la réutilisation des données publiées, avec mention de la source, est permise |
| Licence éCO2mix | non demandée | Aucune licence indiquée sur la page éCO2mix consultée | [eCO2] | Non trouvé |

Conséquence pratique : citer le chiffre « 95,2 % / 521,1 TWh » avec sa source (« RTE, Bilan électrique 2025 », 25/02/2026) et la mention « réutilisation permise sous réserve de citer la source (mentions légales de RTE) », sans écrire « Licence Ouverte » pour ce chiffre. Garder la Licence Ouverte v2.0 pour les valeurs tirées d'ODRÉ. Je ne donne pas d'avis juridique : si le kit reprend plus qu'une phrase courte du texte, demander l'autorisation prévue par les mentions légales.

---

### 4. Version anglaise

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Existence d'une version anglaise | « Electricity report ? » | Oui. Titre anglais de RTE : **« Annual Electricity Review 2025 »** (titre de page : « 2025 Review – Key findings | Analysis and Data » ; couverture des PDF : « 2025 Electricity Review »). Ce n'est pas « Electricity report » | [KF-en] (PDF), [EN-Key], [EN-Gen] | Écart de libellé : à corriger si le kit écrit « Electricity report » |
| URL des pages anglaises | à fournir | Pages : `https://analysesetdonnees.rte-france.com/en/annual-review-2025/keyfindings` ; `.../generation` ; `.../consumption`, `.../prices`, `.../trade`, `.../ghg-emissions`, `.../europe`, `.../electrification-of-energy-uses` (menu lu sur la page [EN-Gen]). La page française [Syn] renvoie vers `/en/annual-review-2025/generation` | [EN-Key], [EN-Gen] | Conforme |
| PDF anglais | à fournir | « Key findings » (22 pages) et « Full report » (146 pages), hébergés sous `/analyse-et-donnees/2026-04/`. Métadonnées du PDF « Key findings » : créé le 01/04/2026. Les pages rte-france.com [CP] et [Pub] ne listent **aucune version anglaise**, seulement les PDF français | [KF-en], [RC-en], [EN-Gen], [CP], [Pub] | Conforme |
| Date de publication de la version anglaise | non demandée | Pas de date affichée sur les pages ; seul indice : dossier `2026-04` et date de création du PDF (01/04/2026), soit environ un mois après le français | [EN-Key] | Non trouvé (date exacte) |

---

### 5. Les quatre notes « À savoir »

#### Note (1) : le mix électrique (RTE, surtout nucléaire) n'est pas le mix énergétique (SDES), où le pétrole domine la consommation finale

- **Vérifié.** SDES, Chiffres clés de l'énergie, édition 2026 (publiée le 30/09/2026, données 2025 provisoires), consommation finale par énergie : pétrole 38 %, électricité 27 %, gaz naturel 18 %. Le pétrole « demeure toutefois prépondérant dans le secteur des transports » ([SDES-CC], lu directement ; l'infographie SDES vue dans un résumé de moteur de recherche donne en plus 14 % pour les renouvelables thermiques et déchets et 3 % pour la chaleur commercialisée, non vérifié sur la page).
- Côté RTE : le nucléaire est 68,1 % de la production 2025 ; RTE écrit aussi (en anglais, ma traduction) que les énergies fossiles représentent encore près de 60 % de la consommation totale d'énergie de la France, et que la part de l'électricité dans la consommation finale « reste globalement stable depuis de nombreuses années » ([KF-en] et [PR-fr], PDF).
- **Piège de périmètre.** SDES donne une production d'électricité de 559 TWh en 2025 (+2,1 %) ([SDES-Bilan]), contre 547,5 TWh chez RTE. Je n'ai pas trouvé la page qui explique la différence de périmètre : ne pas mélanger les deux séries dans une même phrase.
- **Proposition :** « L'électricité (RTE) n'est pas toute l'énergie (SDES) : en 2025, le pétrole reste la première énergie consommée en France (38 % de la consommation finale, contre 27 % pour l'électricité ; données provisoires). Le nucléaire fournit 68 % de l'électricité produite, pas de l'énergie consommée. » Citer l'édition et l'année du SDES ; les parts passent à jour à chaque édition.

#### Note (2) : la part bas-carbone est le chiffre de RTE (95,2 % en 2025), cité tel quel ; le comptage des bioénergies la modifie

- **Chiffre vérifié** (voir section 2). La note est juste, mais incomplète : le comptage des bioénergies n'est pas le seul facteur, et pas le principal.
- **Proposition :** « La part bas-carbone est le chiffre de RTE : 95,2 % en 2025 (521,1 TWh). RTE compte comme renouvelable la moitié de l'électricité tirée des déchets ménagers et retranche de la production hydraulique 70 % de l'électricité consommée par le pompage des stations de transfert d'énergie. En additionnant simplement les filières du fichier hors fossile, on obtient 96,6 % ; hors bioénergies, 94,6 %. » (Ordre de grandeur de l'écart entre 96,6 % et 95,2 % : environ 5,7 TWh de pompage et 2 TWh de déchets non renouvelables, estimation de ma part.)
- Si la note doit rester courte : supprimer « le comptage des bioénergies la modifie » au profit de « selon les conventions de RTE (déchets, pompage) ».

#### Note (3) : France métropolitaine seulement, production (pas consommation) ; consommation 2025 d'environ 451 TWh corrigée de la météo ; exportations

- **451 TWh vérifié** : « En 2025, la consommation électrique en France métropolitaine (corrigée des aléas météorologiques et des effets calendaires) est restée stable … atteignant 451 TWh (+0,4 % par rapport à 2024) » ; valeur précise 451,2 TWh ([PR-fr] et [KF-en], PDF). La consommation **brute** est de 446,2 TWh dans le résumé, 446,1 TWh dans le tableau de reconstitution du rapport complet (deux valeurs chez RTE). Dire « corrigée des aléas météorologiques et des effets calendaires », pas seulement « de la météo ».
- **Périmètre** : le rapport indique que le périmètre géographique du Bilan est « la France métropolitaine et la Corse » (« mainland France and Corsica », encadré « Definitions » de [RC-en], PDF). « Métropolitaine » est donc correct, et inclut la Corse. Je n'ai pas de source pour décrire le périmètre exact des autres territoires.
- **Exportations** : solde net de 92,3 TWh à l'export en 2025, un record pour la deuxième année consécutive (89 TWh en 2024, 89,0 dans le rapport complet), soit 17 % de la production ([KF-en], [RC-en] PDF, [CP]). Exports bruts 103,6 TWh, imports 11,3 TWh ([KF-en], PDF). Italie 26,2 TWh en tête : valeur lue uniquement dans un résumé de moteur de recherche, non vérifiée.
- **Pourquoi la production dépasse la consommation** (reconstitution du rapport) : 547,5 − 8,1 (pompage STEP) − 92,3 (solde commercial) − 1,0 (écart entre flux physiques et commerciaux) = 446,1 TWh de consommation brute.
- **Proposition :** « Ces chiffres concernent la production d'électricité de la France métropolitaine, pas la consommation. En 2025, la consommation s'élève à environ 451 TWh (corrigée des aléas météorologiques et des effets calendaires ; 446 TWh avant correction), et la France exporte 92,3 TWh nets, un record. »

#### Note (4) : la production fossile au plus bas depuis des décennies (à quel secteur se rapporte « le plus faible observé depuis près de 75 ans » ?)

- **Vérifié : la phrase vise la production d'origine fossile** (gaz, charbon, fioul), pas les émissions ni la production totale. Texte du PDF français, point 4 : « La production d'origine fossile a poursuivi en 2025 son recul (−1,3 TWh par rapport à 2024). Le niveau de production de cette filière a été le plus faible observé depuis près de 75 ans. » ([PR-fr], [Syn]). Le communiqué : « la production thermique fossile a atteint son plus bas niveau depuis 75 ans » ([CP]). La page détaillée est plus précise : 18,7 TWh, « le niveau le plus bas depuis le début des années 1950 », et « pour la deuxième année consécutive » (2024 : 19,9 TWh, déjà un minimum) ([Prod], [RC-en] p. 46).
- **Ne pas confondre** avec les émissions du secteur électrique : 10,9 MtCO2e en 2025, « plus bas niveau depuis 1945 » ([RC-en], chapitre Émissions, PDF) ; intensité 19,6 gCO2e/kWh. Ce sont deux repères différents (volume produit, depuis ≈ 1950 ; émissions, depuis 1945).
- **Périmètre de « fossile » chez RTE** : gaz, charbon et fioul uniquement (note 28 du rapport). L'incinération de déchets non renouvelables est rangée dans « thermique renouvelable et déchets », pas dans « fossile ».
- **Le fichier ne peut pas démontrer ce record** : la série ODRÉ commence en 2012. La phrase doit donc être attribuée à RTE.
- **Proposition :** « La production d'électricité à partir de gaz, de charbon et de fioul (18,7 TWh) a atteint en 2025 son niveau le plus bas depuis le début des années 1950, selon RTE. » (Éviter « depuis des décennies » : trop vague, et RTE donne une date. Éviter « 75 ans » seul si le kit veut rester précis : RTE écrit « près de 75 ans ».) Un résumé de moteur de recherche cite « depuis environ 1950 » : cohérent avec « début des années 1950 ».

---

### 6. Conclusion

#### Écarts, du plus important au moins important

1. **Licence du rapport (écart avec l'hypothèse « Licence Ouverte »).** Aucune licence n'est indiquée sur les pages du Bilan 2025. Les mentions légales de RTE permettent de réutiliser les données publiées en citant la source, et réservent le droit d'auteur sur le reste. La Licence Ouverte v2.0 n'est établie que pour le jeu ODRÉ (fiche data.gouv.fr). Écrire la source du 95,2 % comme « RTE, Bilan électrique 2025 », sans mention de licence ouverte.
2. **Note (2) : le comptage des bioénergies n'est pas le facteur principal.** RTE retranche aussi 70 % du pompage des STEP de la production hydraulique (8,1 TWh de pompage en 2025, soit environ 5,7 TWh retirés) et ne compte que 50 % des déchets ménagers comme renouvelables ; la déduction du pompage explique environ trois quarts de l'écart entre 96,6 % et 95,2 % (estimation de ma part). À reformuler (voir proposition).
3. **Libellé anglais** : RTE écrit « Annual Electricity Review 2025 » (couverture : « 2025 Electricity Review »), pas « Electricity report ».
4. **Données 2012** : le fichier diffère légèrement du Bilan 2012 d'origine (total 542 contre 541,4 ; fossile 48,1 contre 47,9 ; solaire 4,1 contre 4,0 ; bioénergies 5,8 contre 5,9 ; nucléaire 405 contre 404,9). Probable révision de la série par RTE, **non confirmée** (je n'ai pas trouvé la série révisée sur une source RTE et n'ai pas appelé ODRÉ). À signaler dans la note de source, ou à accepter comme tolérance de ±0,3 TWh.
5. **Fioul 2025** : 1,6 dans la figure du rapport (valeur du fichier), 1,7 dans le texte du rapport et sur la page Production. Le fichier est cohérent avec la somme 18,7 ; ne pas « corriger » vers 1,7.
6. **2024** : fossile 20,0 (fichier) contre 19,9 (texte du rapport 2025) ; hydraulique 75,3 contre 75,1 et bioénergies 10,6 contre 10,5 sur la page du Bilan 2024 (valeurs lues par résumé automatique). Écarts de 0,1 à 0,2 TWh, du niveau de l'arrondi ou d'une révision.
7. **Citation du 95,2 %** : la phrase du fichier s'arrête avant « une part similaire à celle de 2024 » ; fermer proprement la citation.

#### Valeurs conformes

Toutes les valeurs 2025 du fichier (total 547,5 ; nucléaire 373,0 ; hydraulique 62,4 ; éolien 49,6 ; solaire 32,9 ; bioénergies 10,9 ; fossile 18,7 ; gaz 16,4 ; charbon 0,7), la phrase RTE sur le bas-carbone (521,1 TWh, 95,2 %), les 96,6 % et 94,6 % de la note #29 (calcul), la date de publication (25/02/2026), la mise à jour ODRÉ (25/02/2026, via data.gouv.fr) et la Licence Ouverte v2.0 du jeu ODRÉ (via data.gouv.fr). Les valeurs 2024 de total, nucléaire, éolien et solaire sont conformes.

#### Non trouvé

- La page ODRÉ elle-même (non consultée, comme demandé) : dates et licence ne reposent que sur la fiche data.gouv.fr.
- La série 2012 révisée par RTE ; la valeur 2024 des bioénergies dans le Bilan 2025.
- La date de publication précise de la version anglaise et la licence d'éCO2mix.
- Le communiqué RTE au format PDF, et le rapport complet français (plus de 10 Mo, non lisible par l'outil) : les valeurs ont été lues dans la page d'actualité, le PDF « Principaux résultats » et le rapport complet anglais.
- Le périmètre exact de l'écart entre les 559 TWh du SDES et les 547,5 TWh de RTE.

---

### 7. URLs consultées (date de consultation : 2026-11-02)

Pages et PDF de RTE
- [Syn] https://analysesetdonnees.rte-france.com/bilan-electrique-2025/synthese
- [Prod] https://analysesetdonnees.rte-france.com/bilan-electrique-2025/production
- [EN-Gen] https://analysesetdonnees.rte-france.com/en/annual-review-2025/generation
- [EN-Key] https://analysesetdonnees.rte-france.com/en/annual-review-2025/keyfindings
- [B24] https://analysesetdonnees.rte-france.com/bilan-electrique-2024/production
- https://analysesetdonnees.rte-france.com/production/synthese (page multi-années, sans valeurs par filière)
- [ML] https://analysesetdonnees.rte-france.com/mentions-legales
- [CP] https://www.rte-france.com/actualites/bilan-electrique-2025-conditions-sont-reunies-permettre-france-accelerer-electrification
- [Pub] https://www.rte-france.com/donnees-publications/publications/bilans-electriques-nationaux-regionaux
- [eCO2] https://www.rte-france.com/eco2mix/la-production-delectricite-par-filiere
- [KF-en] https://assets.rte-france.com/analyse-et-donnees/2026-04/RTE%20-%20Annual%20electricity%20review%202025%20-%20Key%20findings.pdf (texte extrait avec pdftotext)
- [RC-en] https://assets.rte-france.com/analyse-et-donnees/2026-04/RTE%20-%20Annual%20electricity%20review%202025%20-%20Full%20report_0.pdf (texte extrait avec pdftotext)
- [PR-fr] https://assets.rte-france.com/prod/public/2026-03/Bilan-electrique-2025-principaux-resultats.pdf (texte extrait avec pdftotext)
- https://assets.rte-france.com/analyse-et-donnees/2026-01/2026-01-02-bilan-electrique-2025-premieres-tendances.pdf (ouvert, illisible par l'outil, non utilisé)
- https://assets.rte-france.com/analyse-et-donnees/2026-03/BE2025%20-%20Rapport%20Complet.pdf (refusé : plus de 10 Mo, non lu)
- [B12] https://pole-medee.com/wp-content/uploads/2013/02/RTE_bilan_electrique_2012.pdf (copie du Bilan électrique 2012, hébergée par un tiers, texte extrait avec pdftotext)

Autres sources
- [DG] https://www.data.gouv.fr/datasets/production-nationale-annuelle-par-filiere-2012-a-2021/ (fiche du jeu ; les ressources liées n'ont pas été ouvertes)
- [CdE] https://www.connaissancedesenergies.org/la-production-electrique-bas-carbone-de-la-france-atteint-un-maximum-historique-en-2025
- [NucNet] https://www.nucnet.org/news/france-s-electricity-mix-reaches-95-low-carbon-with-higher-nuclear-generation-3-5-2026
- [SDES-CC] https://www.statistiques.developpement-durable.gouv.fr/chiffres-cles-de-lenergie-edition-2026
- https://www.statistiques.developpement-durable.gouv.fr/edition-numerique/chiffres-cles-energie/fr/donnees-cles
- https://www.statistiques.developpement-durable.gouv.fr/edition-numerique/chiffres-cles-energie/fr/livre
- [SDES-Bilan] https://www.statistiques.developpement-durable.gouv.fr/bilan-energetique-de-la-france-en-2025-donnees-provisoires

Vues uniquement dans des résultats de moteur de recherche (non ouvertes, pas utilisées comme preuve unique)
- https://www.enerdata.net/publications/daily-energy-news/rte-reports-annual-2025-balance-frances-fossil-output-hits-75-year-low.html
- https://www.statistiques.developpement-durable.gouv.fr/infographies/9286 (infographie SDES « Données sur l'énergie en 2025 »)
- Résultats de recherche Banque des Territoires, Selectra, Opera Énergie : source des 26,2 TWh vers l'Italie (non vérifié) et de la date du 25 février.

### 8. Part du nucléaire (ajoutée le 09/11/2026)

Faite le 09/11/2026 par un agent Claude (modèle Opus), sur les pages du Bilan électrique de RTE, pas sur l'API ODRÉ que lit le script.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Part du nucléaire 2025 | 68,1 % (373,0 / 547,5) | « la forte part de la production nucléaire dans le mix électrique français (entre 63 et 77 % sur les dix dernières années, 68,1 % en 2025) » | Bilan électrique 2025, page Production | Conforme |
| Fourchette des dernières années | de 62,5 % (2022) à 76,5 % (2015) sur 2015-2025 ; 72,4 % au plus sur 2016-2025 | « entre 63 et 77 % sur les dix dernières années » | Bilan électrique 2025, page Production | Conforme à l'arrondi (RTE compte onze ans, 2015 compris) |
| Part du nucléaire 2024 | 67,1 % (361,7 / 539,3) | « En 2024, la filière nucléaire a représenté 65 % du mix de production français » | Bilan électrique 2024, page Production | Écart : 361,7 TWh rapportés au total de ce même Bilan (539 TWh) font 67,1 % ; le chiffre de 65 % n'a pas d'explication sur la page. Le kit ne le reprend pas : la note et le chiffre clé portent sur 2025 |
| Part du nucléaire 2007 (« À savoir » 2) | hors fichier (la série commence en 2012) | 418,6 TWh sur 544,4 TWh nets, 76,9 % | Annales des Mines, « Faits et chiffres pour 2007 », électricité (PDF, lu avec `pdftotext`) | Conforme |
| Mots du débat de 2007 (« À savoir » 2) | cités | Relevés dans la transcription de Vie publique par une vérification sur les sources primaires ; l'échange (50 % contre 17 %) rapporté par World Nuclear News | Vie publique (non relue par l'agent) ; World Nuclear News | Conforme (citation relevée, non relue ici) |

Pages consultées le 09/11/2026 : https://analysesetdonnees.rte-france.com/bilan-electrique-2025/production ; https://analysesetdonnees.rte-france.com/bilan-electrique-2024/production ; https://annales.org/ri/2008/ri-aout-2008/Electricite.pdf ; https://www.world-nuclear-news.org/articles/french-candidates-slip-up-on-nuclear-facts (vu dans un moteur de recherche).

## Mises à jour

- **09/11/2026** (#307) : série `nuclearShare` ajoutée par le script, l'instantané récrit par `yarn briefings electricityProduction` (les autres séries et les dates des sources ne changent pas, seule la date de récupération) ; la page la montre dans une vue « Part du nucléaire » et à côté du chiffre clé. « À savoir » 1 récrit (la part du nucléaire, de l'électricité et non de l'énergie consommée), 2 ajouté (le débat de 2007), l'ancien 4 retiré (voir « À savoir »). Vérification : section 8.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
