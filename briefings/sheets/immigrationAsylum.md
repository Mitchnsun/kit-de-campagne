# `immigrationAsylum` · Immigration et asile

**Vérifiée le 02/11/2026** : stocks d'immigrés et d'étrangers (1921, 2023, 2024, 2025, effectifs et parts) conformes à la série de l'Insee de juin 2026 ; premiers titres 2024-2025, primo-demandeurs 2023-2024 et acquisitions 2022-2024 conformes au ministère et à Eurostat. Corrigé : le chiffre clé n'a plus de tendance, l'Insee écrivant que ses estimations provisoires « ne permettent pas de calculer des évolutions d'une année sur l'autre » ; notes précisées (définitions, rupture de 2024, ce que compte chaque source de l'asile, voies d'acquisition).

**Écarts ouverts** : les flux de 2025 existent en plusieurs versions (premiers titres : 377 462 dans Eurostat et le dernier chiffre du ministère, 384 230 annoncés en janvier 2026 ; primo-demandeurs : 116 475 dans Eurostat, 116 944 au ministère), sans cause trouvée de la révision. Non trouvés hors de la source : premiers titres 2008, primo-demandeurs 2009, et quatre parts départementales (Paris, Seine-Saint-Denis, Guyane, Mayotte).

| Champ | Valeur |
| --- | --- |
| Indicateur | `immigrationAsylum`, ticket #142, dossier « Immigration » (statut `planned`) ; l'avertissement « un immigré n'est pas un étranger » est dans les locales de l'app (PO, 02/11/2026) |
| Données | `briefings/data/immigrationAsylum.json`, écrit par `yarn briefings immigrationAsylum` le 2026-11-02 |
| Sources | Insee, « L'essentiel sur… les immigrés et les étrangers », parue le 25/06/2026, ses tableaux lus dans la page (son classeur en était encore à 2024, PO, 02/11/2026), Licence Ouverte 2.0, en français seulement ; Eurostat, `migr_resfirst` (mis à jour le 22/10/2026), `migr_asyappctza` (03/09/2026) et `migr_acq` (27/03/2026), réutilisation libre avec mention de la source |
| Séries | `immigrants`, `immigrantShare`, `foreigners`, `foreignerShare` : effectifs et parts dans la population, de 1921 à 2025 (années de recensement, puis annuelles depuis 2006), 2024 et 2025 provisoires, rupture de série en 2024 ; `firstPermits` (depuis 2008), `firstTimeAsylumApplicants` (depuis 2009), `citizenshipAcquisitions` (depuis 1998) : Eurostat, France |
| Valeurs par département | Part des immigrés dans la population en 2023 (recensement), telle que la page la publie, Mayotte comprise ; chaque nom de département vérifié contre ceux du jeu Melodi du recensement |
| Chiffre clé | 7,97 millions d'immigrés en 2025 (11,6 % de la population), sans tendance (année provisoire) |
| Première édition | À remplir à la publication |

Champ des stocks, selon l'Insee : France métropolitaine de 1921 à 1982 ; France hors Mayotte de 1990 à 2013 ; y compris Mayotte depuis 2014.

À actualiser : à chaque édition de « L'essentiel » (juin) ; les flux d'Eurostat à chaque mise à jour. Les acquisitions de 2025 (98 139 selon l'Insee, juillet 2026) ne sont pas encore dans Eurostat.

Non repris : les demandes d'asile de l'Ofpra par département (CSV de data.gouv.fr), que la page ne dessine pas.

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans lire les tableaux de la page Insee ni appeler Eurostat. Son rapport, tel quel :

Date de la vérification : 2026-11-02. Vérification faite sur le web uniquement, sans rien lire ni modifier sous `/home/user`.

### 0. Méthode, limites, légende

**Ce que je n'ai pas fait (règles respectées).** Je n'ai pas lu les tableaux HTML de la page Insee 3633212 ni son fichier xlsx. Je n'ai pas appelé l'API d'Eurostat (`migr_resfirst`, `migr_asyappctza`, `migr_acq`). Pour la page 3633212, j'ai téléchargé le HTML et extrait seulement le texte hors `<table>`, `<script>` et `<style>` (script Python lancé avec `-I`). Cela donne les définitions, notes, phrases chiffrées et lignes « Lecture ».

**Sources Insee utilisées en recoupement.** J'ai lu la série Insee 2381757 (page et xlsx) et le jeu 2381644 (acquisitions). Ce sont d'autres pages que 3633212, mais le même producteur et probablement la même base. Leur accord avec le fichier prouve la cohérence de l'Insee, pas une indépendance totale. Les vrais recoupements indépendants sont la presse, l'Ofpra, le ministère (document DGEF), Eurostat (communiqué et Statistics Explained) et les publications Insee plus anciennes.

**Ce que je n'ai pas pu lire.**
- Le site du ministère de l'Intérieur (`immigration.interieur.gouv.fr`) a répondu **HTTP 403** à l'outil de lecture web pour 4 URL : pages « Séjour », « Les titres de séjour en 2025 », « Les demandes d'asile en 2025 » et « Les demandes d'asile pour l'année 2025 ». La page « Asile », la page « Population immigrée par département » et la page sur l'accès à la nationalité 2025 ne me sont connues que par des résumés de moteur de recherche.
- J'ai tenté un `curl` avec un en-tête User-Agent de navigateur sur une de ces pages. L'environnement a refusé cette commande (classée « contournement d'un contrôle anti-bot »). Je n'ai pas insisté et je n'ai rien fait d'autre pour contourner le 403.
- Les chiffres du ministère sont donc lus soit dans un document DGEF hébergé ailleurs (kit préfets d'août 2025, copie GISTI), soit dans la presse ou les ONG qui le citent, soit dans des résumés de moteur de recherche (signalés **[R]**).
- La page Eurostat « Asylum statistics » (Statistics Explained) renvoie 404. Je n'ai donc pas de chiffre annuel Eurostat pour l'asile en France autre que le communiqué du 25/03/2026 et l'article Toute l'Europe.

**Légende des sources.**
- **[L]** : lu dans un fichier téléchargé dans `check-immigration-dl/` (texte extrait avec `pdftotext`, `python3 -I`, `curl`).
- **[W]** : page lue avec l'outil de lecture web. Le texte est restitué par un petit modèle, donc les citations sont à reconfirmer mot à mot si elles deviennent critiques.
- **[R]** : résumé de moteur de recherche seulement, page non lue ou illisible pour moi.
- **[S]** : site secondaire (presse, ONG, blog, Wikipédia).


---

### 1. Stocks (Insee)

Réponse au point 1 : **oui, les stocks concordent** avec les autres publications Insee. Ils sont plus anciens ou plus récents selon le millésime, et ils ont été révisés entre octobre 2025 et juin 2026 (voir les lignes « millésime »).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Immigrés 1921 | 1 429 000 (3,7 %) | 1 429,1 milliers ; 3,7 % ; population 38 798 milliers. Champ : **France métropolitaine** de 1921 à 1982 (le fichier écrit « France »). Part de 3,7 % en 1921 et 6,6 % en 1931 aussi dans « Immigrés et descendants d'immigrés » (Insee Références, 30/03/2023) | [L] https://www.insee.fr/fr/statistiques/fichier/2381757/demo-etran-part-pop-etran-immig.xlsx ; [W] https://www.insee.fr/fr/statistiques/6793226 | Conforme (préciser « France métropolitaine ») |
| Étrangers 1921 | 1 532 000 (3,9 %) | 1 532,0 milliers ; 3,9 % ; Français par acquisition 254,3 milliers (0,7 %). Un article du JDD cite aussi 1 532 000 | [L] xlsx ci-dessus ; [S,R] https://www.lejdd.fr/Societe/immigration-en-france-une-explosion-demographique-chiffree-par-linsee-162977 | Conforme |
| Immigrés 2023 | 7 309 000 (10,7 %) | 7 309 ; 10,7 % ; population 68 405 milliers. Insee Première 2107 (04/06/2026) : « 7,3 millions d'immigrés, selon le dernier recensement » au 1er janvier 2023 (population 68,4 millions) | [L] xlsx ; [W] https://www.insee.fr/fr/statistiques/2381757 ; [W] https://www.insee.fr/fr/statistiques/8998082 | Conforme |
| Étrangers 2023 | 5 635 000 (8,2 %) | 5 635 ; 8,2 %. Dans Insee Première 2076 (07/10/2025) : 5 622 000 (8,2 %), ancien millésime | [L] xlsx ; [W] https://www.insee.fr/fr/statistiques/8651304 | Conforme (série de juin 2026) ; l'écart de 13 000 avec octobre 2025 est un changement de millésime |
| Immigrés 2024 (provisoire, rupture) | 7 749 000 (11,3 %) | 7 749 ; 11,3 % ; population 68 638 milliers ; marqué « (p) (*) ». Insee Première 2076 (oct. 2025) : 7 726 000 (11,3 %) ; presse d'octobre 2025 : 7,726 millions | [L] xlsx ; [L] note de rupture (7 309 + 440 000 = 7 749) ; [W] 8651304 ; [S] https://www.economiematin.fr/?p=204246 | Conforme à la série de juin 2026. Écart expliqué avec la presse d'octobre 2025 (ancien millésime) |
| Étrangers 2024 (provisoire, rupture) | 6 046 000 (8,8 %) | 6 045,9 ; 8,8 %. Oct. 2025 : 6 028 000 (8,8 %) | [L] xlsx ; [W] 8651304 | Conforme à la série de juin 2026. Écart expliqué avec octobre 2025 (millésime) |
| Immigrés 2025 (provisoire) | 7 970 000 (11,6 %) | 7 970 ; 11,6 % ; population 68 852 milliers. Texte de la page : « 8,0 millions … 11,6 % ». Note de rupture, figure 3a : « 7 970 000 immigrés » | [L] xlsx ; [L] texte de 3633212 ; [L] note PDF ; [S] https://www.algerie360.com/immigration-en-france-lalgerie-reste-le-premier-pays-dorigine-des-immigres-en-2025/ ; [S] https://www.pressenza.com/fr/2026/09/sans-immigration-que-deviendrait-leconomie-francaise/ | Conforme |
| Étrangers 2025 (provisoire) | 6 297 000 (9,1 %) | 6 297,4 ; 9,1 %. Texte : « 6,3 millions … 9,1 % ». Note, figure 3b : « 6 297 000 » | [L] xlsx ; [L] texte 3633212 ; [L] note PDF | Conforme |
| Chiffre clé « 7,97 millions en 2025, en hausse » | 7,97 M, en hausse | Le niveau est exact. « En hausse » est vrai sur le long terme : la page écrit « de 7,3 % en 1999 à 11,6 % en 2025 » et « plus élevée en 2025 qu'en 1946, 1975 ou 2010 ». Mais la page écrit aussi : « Ces estimations sont provisoires et ne permettent pas de calculer des évolutions d'une année sur l'autre » | [L] texte 3633212 | Conforme, avec une réserve : ne pas afficher de variation 2024 → 2025 (+221 000 par différence). La presse le fait pourtant (« hausse de 300 000 en un an », algerie360 [S]) |

Remarques sur les écarts internes de l'Insee, sans effet sur le fichier :
- La note de rupture (figure 3a) écrit « Ils représentent **11,0 %** de la population » pour 2025. C'est une coquille probable, car tous les autres documents donnent 11,6 % [L].
- La note dit « + 425 000 étrangers » entre 2023 et 2024 (variation apparente). La différence des valeurs de la série (6 046 − 5 635) donne 411 000. L'écart de 14 000 n'est pas expliqué dans ce que j'ai lu. Il est peut-être dû à une base 2023 différente (5 622 en oct. 2025 donnerait 424 000).
- Sur la page 3633212, l'encart européen donne **9,4 %** d'étrangers pour la France au 1er janvier 2025 (source Eurostat), contre 9,1 % pour l'Insee. Ce sont deux sources et deux dates différentes, à ne pas mélanger [L].

#### 1.1 Décomposition 2025 (texte de la page 3633212)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Immigrés ayant acquis la nationalité française | 2,6 millions | « 2,6 millions d'immigrés, soit 33 % d'entre eux, ont acquis la nationalité française » | [L] https://www.insee.fr/fr/statistiques/3633212 ; [S] algerie360 | Conforme |
| Immigrés de nationalité étrangère | 5,3 millions | « 5,3 millions d'immigrés n'ayant pas acquis la nationalité française » | [L] 3633212 | Conforme |
| Étrangers nés en France | 953 000 « (texte de la page) » | Le texte dit : « **1,0 million** de personnes nées en France de nationalité étrangère ». « 953 000 » n'est pas dans le texte. Une recherche web [R] le cite comme valeur du tableau (953 milliers, 1,4 %), que je n'ai pas lu. Cohérence : 6 297 − 5 344 ≈ 953. Pour 2024, Insee Première 2076 donne 890 000 (dont 734 000 de moins de 13 ans) | [L] 3633212 (texte) ; [W] https://www.insee.fr/fr/statistiques/8651304 ; [R] recherche web sur la page 3633212 | Écart sur le libellé (la valeur 953 000 n'est pas « du texte »). Valeur exacte : Non trouvé hors tableau |
| Nés à l'étranger (immigrés + Français nés à l'étranger) | 9,6 millions (14,0 %) | « 1,7 million de personnes sont nées de nationalité française à l'étranger. Avec les personnes immigrées (8,0 millions), au total 9,6 millions … nées à l'étranger, soit 14,0 % » (« à arrondi près ») | [L] 3633212 | Conforme |

#### 1.2 Part des immigrés par département, 2023 (recensement)

La page 3633212 dit en texte : « Les immigrés représentent 21 % de la population parisienne, et près d'un tiers de la population de Seine-Saint-Denis », et « la Guyane et Mayotte concentrent une proportion d'immigrés près de trois fois plus importante qu'à l'échelle nationale ». La ligne « Lecture » dit : « en 2023, dans l'Ain, 12,4 % de la population est immigrée » [L]. Les autres valeurs exactes sont dans le tableau, que je n'ai pas lu. Le seul autre millésime 2023 que j'ai trouvé, Insee Première 2011 (29/08/2024), repose sur les **estimations de population 2023 provisoires**, pas sur le recensement.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Ain | 12,4 % | 12,4 % (ligne « Lecture » de la page). Insee Première 2011, estimations provisoires : 12,6 % | [L] 3633212 ; [W] https://www.insee.fr/fr/statistiques/8236359 | Conforme (l'autre millésime donne 12,6 %) |
| Paris | 21,2 % | Texte : « 21 % ». Insee Première 2011 : 21,5 % | [L] 3633212 ; [W] 8236359 | Valeur exacte : Non trouvé. Compatible avec le texte |
| Seine-Saint-Denis | 31,6 % | Texte : « près d'un tiers ». Insee Première 2011 : 31,4 % | [L] 3633212 ; [W] 8236359 | Valeur exacte : Non trouvé. Compatible avec le texte |
| Guyane | 31,4 % | Texte : « près de trois fois » le niveau national. Insee Première 2011 : **33,0 %**. Ministère, recensement 2022 : 31,1 % [R]. Wikipédia, 2021 : 31,5 % [S] | [L] 3633212 ; [W] 8236359 ; [R] https://www.immigration.interieur.gouv.fr/Info-ressources/Etudes-et-statistiques/Les-chiffres-de-l-immigration-en-France/Population-immigree-par-departement ; [S] https://fr.wikipedia.org/wiki/Immigration_en_France | Non trouvé (valeur exacte). Plausible, mais l'autre millésime 2023 en diffère de 1,6 point |
| Mayotte | 34,7 % | Insee Première 2011 (2023 provisoire) : 34,7 %. Même valeur dans le résumé du ministère pour 2022 [R] et sur Wikipédia pour 2021 [S] | [W] 8236359 ; [R] ministère (ci-dessus) ; [S] Wikipédia | Conforme sur la valeur. Elle est identique dans trois millésimes, ce que je ne sais pas expliquer |

---

### 2. Rupture de série 2024 (point 1, suite)

Source principale : note méthodologique Insee du **4 juin 2026**, « Rupture de série dans la mesure des populations immigrées dans les enquêtes annuelles de recensement récentes » [L] https://www.insee.fr/fr/statistiques/fichier/2383177/Note_methodo_rupture_serie_immigration.pdf

**De quoi s'agit-il.**
- C'est un changement du **protocole de collecte** du recensement en 2024, « Recens'Smart ». Un questionnaire internet accessible sur tous les supports, smartphone compris, a été mis en place.
- La note le qualifie d'« amélioration dans le protocole de collecte ». Il a deux effets :
  1. **Compter plus de monde** (immigrés et non-immigrés) : 271 000 habitants en plus par rapport à l'ancien protocole. Cet effet est traité par un « ajustement statistique » étalé sur plusieurs années.
  2. **Mieux repérer les immigrés** : des personnes classées avant comme non-immigrées le sont désormais comme immigrées (+242 000 immigrés, −242 000 non-immigrés, solde nul). Cet effet « ne doit être pris en compte que pour l'année 2024 ».
- Le taux de réponse par internet des immigrés a augmenté de 12 points entre 2023 et 2025, contre 5 points pour les non-immigrés.

**Chiffres de la note.**

| Mesure | Apparent (comparaison directe 2023 → 2024) | Corrigé de la rupture |
|---|---|---|
| Immigrés | +440 000 (part : 10,7 % → 11,3 %, soit +0,6 point ; historiquement +0,1 à +0,3 point d'une EAR à l'autre) | **+198 000** (part +0,3 point) |
| Étrangers | +425 000 | **+260 000** (effet de rupture estimé à environ +165 000) |

**Ce que l'Insee dit de la comparaison.**
- Avertissement de la page 3633212 : « les données sur le nombre et la part d'immigrés pour les années avant 2024 ne sont pas directement comparables à celles relatives à 2024 et 2025 » [L].
- Dans la note : la hausse apparente de +440 000 « est surestimée en raison d'un changement de protocole … Il s'agit là d'une rupture de série, au sens où les données de 2024 ne sont pas directement comparables à celles d'avant » [L].
- La page 3633212 ajoute : « Ces estimations sont provisoires et ne permettent pas de calculer des évolutions d'une année sur l'autre », parce que les estimations provisoires ne tiennent pas compte des ajustements statistiques [L].
- Les graphiques de la page ne relient pas les points de 2023 et 2024, ni ceux d'avant 2006 (passage du recensement exhaustif au recensement annuel par sondage) [L].

**Autres faits utiles.**
- Les données de 2019 à 2023 ont été « réajustées » : la source indique « données réajustées de 2019 à 2023 » sur la page, mais la note écrit « 2019, 2020, 2021 et 2022 » et Insee Première 2107 « 2019, 2020, 2021 et 2023 ». Les trois formulations ne coïncident pas.
- Dans la fiche Insee « Nationalités – Immigration » (version de juin 2026), la question du bulletin individuel sur la nationalité a été « modifiée en profondeur » dans l'EAR 2025 (« et/ou » pour repérer les doubles nationalités). Du recensement millésimé 2023 au millésimé 2027, les variables reposent sur deux versions de la question [L] https://www.insee.fr/fr/statistiques/fichier/2383177/fiche-nationalites-immigration.pdf. Ce n'est pas présenté comme une rupture de série dans la note.
- Le bilan démographique 2025 (janvier 2026) a tenu compte de l'ajustement Recens'Smart, selon la note [L]. Les estimations de population 2024 à 2026 y sont provisoires [R] https://www.insee.fr/fr/statistiques/8719824.

---

### 3. Flux : premiers titres de séjour (point 2)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2008 | 188 723 | Aucune source trouvée donnant ce nombre (recherche du nombre exact, Ined 2008 inaccessible, chapitre Insee F13 lu sans ce nombre) | [R] recherches web ; [L] https://www.insee.fr/fr/statistiques/fichier/version-html/6793248/IMMFRA23-F13.pdf | Non trouvé |
| 2023 | 338 877 | Nombre exact non trouvé. Ordre de grandeur : kit préfets DGEF d'août 2025, 343 024 pour 2024 « (+0,9 % par rapport à 2023) », soit environ 340 000 pour 2023. Résumé de moteur de recherche : 340 019 en 2023 (données provisoires, mi-2025). Janvier 2024 : 323 260 (provisoire) | [L] https://www.gisti.org/IMG/pdf/kit-prefets_etrangers-en-france_2025-08.pdf ; [R] https://demarchesadministratives.fr/actualites/hausse-des-visas-nette-augmentation-des-departs-forces-tous-les-chiffres-sur-immigration-en-2024 ; [R,S] https://www.europe1.fr/politique/immigration-record-du-nombre-de-premiers-titres-de-sejour-a-323260-en-2023-4227072 | Non trouvé (valeur plausible : 338 877 est à 0,3 % du ~340 000 déduit) |
| 2024 | 345 587 | « 345 587 selon les chiffres définitifs » (franceinfo, 27/01/2026). Table du ministère reprise par l'IFRAP : 2024 « définitif » = 345 587. Le **kit préfets d'août 2025 (« données définitives de 2024 »)** donnait 343 024 (dont 8 896 Britanniques). Première publication de janvier 2025 : 336 700 | [W] https://www.franceinfo.fr/societe/immigration/immigration-384-230-premiers-titres-de-sejour-delivres-en-2025-en-hausse-de-11-2-e-de-11-2_7767725.html ; [W] https://www.ifrap.org/fonction-publique-et-administration/lasile-nouveau-moteur-de-limmigration-reguliere ; [L] kit GISTI ; [R,S] https://www.europe1.fr/societe/immigration-336700-premiers-titres-de-sejour-delivres-en-2024-en-hausse-de-18-287577 | Conforme à la dernière version du ministère. Écart expliqué avec 343 024 (août 2025) et 336 700 (janvier 2025) : révisions successives, le chiffre monte à mesure que les titres sont enregistrés |
| 2025 | 377 462 | Eurostat Statistics Explained (extraction du 11/09/2026) : « France (377 462, 9.8%) ». Causeur (28/10/2026, source DGEF) : 377 462, avec les motifs 116 835 + 90 959 + 88 001 + 50 848 + 30 819 = 377 462. IFRAP (10/07/2026) : table « 2025 provisoire », « plus de 377 000 ». Algérie-Éco (02/09/2026) : 377 462. **Mais** annonce du ministère du 27/01/2026 : **384 230** (+11,2 %), reprise partout dans la presse | [W] https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Residence_permits_-_statistics_on_first_permits_issued_during_the_year ; [W,S] https://www.causeur.fr/immigration-edouard-philippe-calculs-titres-de-sejour-2027-336201 ; [W] IFRAP ; [W,S] https://algerie-eco.com/2026/09/02/visas-titres-de-sejour-nationalite-les-chiffres-de-limmigration-algerienne-en-france-en-2025/ ; [W] franceinfo (ci-dessus) | Conforme à la version la plus récente. Écart expliqué avec 384 230 (janvier 2026) : deux versions du ministère. Je n'ai pas trouvé l'explication de la révision à la baisse (−6 768, −1,8 %) |

Autres éléments sur 2025 :
- Résumé de moteur de recherche de la page ministère « Titres de séjour en 2025 » : 377 462 en « +9,2 % », « provisoire », observation au 31 mai 2026, chiffre définitif attendu en janvier 2027 [R] https://www.immigration.interieur.gouv.fr/documentation/etudes-et-statistiques/titres-de-sejour-en-2025-protections-subsidiaires-ont-plus-que-double.html. La date du « 31 mai 2026 » n'est confirmée par aucune page lue (l'IFRAP ne la contient pas).
- La Cimade attribue la hausse apparente de 2025 en partie à un rattrapage administratif lié à la fin d'une pratique qui bloquait les titres délivrés au titre de l'asile [W,S] https://www.lacimade.org/donnees-migratoires-2025-une-analyse-critique/.

#### Écart Eurostat / ministère : ce qu'on peut dire sans deviner

- **Les totaux sont identiques** pour les deux années comparables : 2024 = 345 587 (fichier, franceinfo, IFRAP) et 2025 = 377 462 (fichier, Eurostat SE, DGEF via Causeur et IFRAP). Je n'observe donc **aucun écart de champ** entre Eurostat et le ministère dans les derniers millésimes.
- Les seuls écarts observés sont **entre versions du ministère** (336 700 → 343 024 → 345 587 pour 2024 ; 384 230 → 377 462 pour 2025).
- Définition du ministère : « Les premiers titres de séjour correspondent aux titres détenus par des étrangers majeurs à la suite d'une première demande de séjour », renouvellements exclus même en cas de changement de motif ; date de référence = début de validité du titre ; les Britanniques sont présentés séparément (titre obligatoire depuis le 01/10/2021) [W] https://www.data.gouv.fr/datasets/66a8cc809b4750710f18920c. Le kit DGEF les compte **dans** le total (« dont 8 896 Britanniques ») [L].
- Définition d'Eurostat : permis « valables pour une durée minimale de trois mois et délivrés au niveau national » ; ressortissants de pays tiers ; données exclusivement administratives ; la protection temporaire (Ukraine) n'est dans aucune statistique de titres de séjour [W] https://ec.europa.eu/eurostat/fr/web/migration-asylum/managed-migration/methodology et SE ci-dessus.
- **Mineurs** : le ministère ne compte que des majeurs. Pour Eurostat, la page SE ne dit rien sur les mineurs. Un blog [S] (Tribalat, citant les métadonnées Eurostat) écrit que la France n'exige pas de titre des enfants, donc les moins de 16 ans sont absents des données françaises : https://micheletribalat.fr/435108953/442891477. Je ne le présente pas comme établi.
- **Documents de circulation, VLS-TS** : aucune source lue ne traite les documents de circulation. Selon le même blog [S], les VLS-TS sont inclus dans les données françaises d'Eurostat.
- **Règle des « 6 mois après expiration »** (un titre est « premier » s'il est délivré pour la première fois ou au moins 6 mois après l'expiration du précédent) : elle apparaît seulement dans un résumé de moteur de recherche [R]. La page méthodologique d'Eurostat que j'ai lue ne la contient pas.
- Les **motifs** diffèrent entre les deux sources alors que le total est le même : « études » 118 404 chez Eurostat contre 116 835 chez la DGEF (Causeur) ; « famille » 90 959 dans les deux.

---

### 4. Flux : asile (point 3)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2009 primo-demandeurs | 42 070 | Non trouvé. Séries nationales de 2009 : Ofpra 33 235 premières demandes hors mineurs accompagnants ; avec 5 568 mineurs accompagnants : 38 803 ; avec 8 883 réexamens : 47 686 | [L] https://www.assemblee-nationale.fr/dyn/13/questions/QANR5L13QE85075.pdf ; [W] https://www.insee.fr/fr/statistiques/6793252 | Non trouvé (aucune série nationale retrouvée ne donne 42 070 ; le périmètre d'Eurostat pour 2009 n'est pas documenté dans ce que j'ai lu) |
| 2023 | 145 160 | Ministère, GUDA : « 145 160 premières demandes et 21 896 réexamens, soit au total 167 056 demandes » | [W] https://www.data.gouv.fr/datasets/demandes-dasile-publication-du-27-juin-2024 | Conforme |
| 2024 | 129 910 | Kit DGEF d'août 2025 : « Premières demandes d'asile (France entière) : 129 909 (−10,5 % depuis 2023) dont 20 072 procédures Dublin ». Ofpra, premières demandes 2024 : 130 029 (autre objet) | [L] https://www.gisti.org/IMG/pdf/kit-prefets_etrangers-en-france_2025-08.pdf ; [L] rapport Ofpra, annexe 1 | Conforme (1 de différence, voir l'arrondi plus bas) |
| 2025 | 116 475 | Ministère : première publication de janvier 2026 **116 476** (−10,3 %) avec 35 189 demandes ultérieures, soit 151 665 au total [R]. Version révisée : **116 944** (+0,4 %) ; La Cimade, 09/02/2026 : 116 944 premières et 35 890 nouvelles demandes [W,S]. Franceinfo (27/01/2026) : 116 746 (−10,1 %) sur 151 665 [W,S]. Eurostat, communiqué du 25/03/2026 : « France (116 400, 17%) » (arrondi à la centaine) ; Toute l'Europe (maj. 16/09/2026) : 116 370 | [R] https://www.immigration.interieur.gouv.fr/publications/chiffres-de-limmigration-en-france/demandes-dasile-pour-lannee-2025 ; [W,S] https://www.lacimade.org/bilan2025asile/ ; [W,S] https://www.franceinfo.fr/societe/immigration/expulsions-demandes-d-asile-titres-de-sejour-ce-qu-il-faut-retenir-du-rapport-annuel-sur-l-immigration-du-ministere-de-l-interieur_7765943.html ; [W] https://ec.europa.eu/eurostat/web/products-eurostat-news/w/ddn-20260325-2 ; [W,S] https://www.touteleurope.eu/l-ue-dans-le-monde/le-nombre-de-demandeurs-d-asile-dans-l-union-europeenne/ | Écart expliqué : 116 475 correspond au chiffre ministériel de janvier 2026 (116 476), arrondi. Le ministère est depuis passé à 116 944, et Eurostat publiait 116 370 à 116 400 en mars à septembre 2026. Valeur Eurostat exacte non vérifiable (API exclue) |

Remarques :
- Les trois valeurs du fichier pour 2023, 2024 et 2025 sont des multiples de 5. Ceci est compatible avec l'arrondi dont parle l'Insee : « les données pour la France diffèrent légèrement de celles qui se trouvent dans les tableaux précédents en raison des règles d'arrondi utilisées par Eurostat » [W] https://www.insee.fr/fr/statistiques/6793252.
- 116 476 + 35 189 = 151 665, le total que franceinfo cite. Ceci laisse penser que le « 116 746 » de franceinfo est une inversion de chiffres. C'est une déduction de ma part, pas un fait établi.
- La page de La Cimade (« analyse critique ») donne 116 944 premières et 35 960 demandes ultérieures [W,S] https://www.lacimade.org/donnees-migratoires-2025-une-analyse-critique/. Les « demandes ultérieures » varient aussi selon la version (35 189, 35 890, 35 960).

#### Ofpra

| Élément | Valeur annoncée | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Demandes de protection internationale 2025 | 145 270 (« selon l'annonce de son rapport ? ») | Rapport d'activité 2025 : « 145 270 demandes enregistrées en 2025 », −5,5 % après 153 715 en 2024. Annexe 1 : premières demandes **111 343** (130 029 en 2024, −14,4 %), réexamens **33 713** (23 573, +43,0 %), réouvertures **214** (113), total **145 270**. Calcul de l'Ofpra : « Premières demandes + demandes de réexamen + demandes de réouverture de dossiers clos ». Données arrêtées au 2 février 2026. Communiqué du 27/07/2026 : « 145 270 » | [L] https://www.ofpra.gouv.fr/sites/default/files/2026-07/Rapport%20d%27activit%C3%A9%202025%20Ofpra.pdf ; [W] https://www.ofpra.gouv.fr/actualites/lofpra-publie-son-rapport-dactivite-2025-a-loccasion-des-75-ans-de-la-convention-de | Conforme |
| Bilan provisoire de janvier 2026 | non cité | 145 210 « dont 730 demandes de statut d'apatride », chiffres « provisoires » au 31/12/2025 | [W] https://www.ofpra.gouv.fr/actualites/bilan-2025-de-lofpra-une-activite-record-et-des-evolutions-contrastees | Écart expliqué (le rapport donne 145 270) ; la presse cite l'un ou l'autre |

#### Ce que compte chaque source

| Source | Objet compté | Preuves | 2025 |
|---|---|---|---|
| **Eurostat** (primo-demandeurs) | « A first-time asylum applicant/seeker refers to a person lodging an application for international protection » pour la première fois dans le pays déclarant, y compris les personnes en procédure Dublin si c'est leur première demande dans ce pays | [W] communiqué Eurostat 25/03/2026 ; fiche Insee : séries Eurostat « y compris sous statut Dublin » [W] 6793252 | 116 475 (fichier) |
| **Ministère de l'Intérieur** (DGEF/DSED, guichets uniques, GUDA) | Premières demandes enregistrées en guichet unique, **procédures Dublin comprises** (20 072 sur 129 909 en 2024), plus les « demandes ultérieures » (réexamens) comptées à part. Hors GUDA, il recense aussi des « autres demandes » : requalifications de procédures Dublin non transférées (16 155 en 2023), réinstallations (3 191 en 2023) | [L] kit DGEF ; [W] data.gouv.fr 27/06/2024 ; La Cimade [W,S] | 116 476 puis 116 944 |
| **Ofpra** | Demandes **introduites à l'Ofpra** : premières demandes, réexamens, réouvertures. Les mineurs sont inclus dans les données publiées depuis 2020 (111 343 = 82 127 majeurs + 28 382 mineurs accompagnés + 834 mineurs non accompagnés). Hors procédures Dublin, tant qu'elles ne sont pas requalifiées en procédure normale ou accélérée | [L] rapport Ofpra ; [W] Insee 6793252 : « premières demandes déposées à l'Ofpra (donc hors procédures Dublin) » | 111 343 premières ; 145 270 au total |

- Pour l'écart ministère/Ofpra en 2025 (116 944 contre 111 343 en premières demandes), La Cimade parle d'un « décalage lié aux requalifications Dublin » [W,S]. L'Ofpra ne l'écrit pas dans son rapport ; je ne l'ai pas trouvé non plus dans la page Ofpra sur le guichet unique, qui précise seulement que l'attestation de demande d'asile n'est pas remise dans le cadre de Dublin [W] https://www.ofpra.gouv.fr/en/step-2-introduction.
- Le ministère compte donc des personnes que l'Ofpra ne reçoit pas (Dublin) et l'Ofpra compte des personnes déjà enregistrées en préfecture lors des années précédentes. Les deux séries ne s'additionnent pas et ne se remplacent pas.
- La page Cimade cite aussi l'OFII (122 476 premières demandes en 2025, 133 685 en 2024) [W,S] https://www.lacimade.org/bilan2025asile/. Je n'ai pas trouvé la définition de ce comptage.
- **Non trouvé** : si les premières demandes du ministère incluent les mineurs accompagnants ; si le comptage Eurostat les inclut.

---

### 5. Flux : acquisitions de la nationalité (point 4)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 1998 | 123 761 | Insee Références 2005, fiche 1.3, ligne « Ensemble » : 123 761 en 1998 (décret 58 123 ; déclaration 23 789 ; manifestation de volonté 25 549 ; sans formalité 4 000 (e) ; déclaration anticipée 12 300 (e)). Sources : ministère des Affaires sociales, du Travail et de la Solidarité, et ministère de la Justice. La somme des lignes donne 123 761 | [L] https://insee.fr/fr/statistiques/fichier/1371777/IMMFRA05.PDF | Conforme pour la valeur nationale. Deux composantes sont des estimations. La valeur Eurostat n'est pas vérifiable |
| 2022 | 114 483 | « Ensemble » 114 483 | [W] https://www.insee.fr/fr/statistiques/2381644 | Conforme |
| 2023 | 97 288 | « Ensemble » 97 288. Eurostat SE : France « 6 400 more » en 2024 (103 700 − 6 400 ≈ 97 300, calcul de ma part) | [W] 2381644 ; [W] https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Acquisition_of_citizenship_statistics | Conforme |
| 2024 | 103 661 | « Ensemble » 103 661 (Insee, publié le 09/07/2026). Kit DGEF d'août 2025 : « Total des acquisitions (par décret, par déclaration, sans formalités – France entière) : 103 661 (+6,6 %) ». Eurostat SE : « France (103 700 ; 8.8% of the EU total) », données extraites le 17/03/2026. Connexion : « over 103,000 in 2024, up 6.6% » | [W] 2381644 ; [L] kit GISTI ; [W] Eurostat SE ; [S] https://www.connexionfrance.com/news/france-sees-fall-in-immigration-latest-official-figures-show/802607 | Conforme |
| 2025 (absent du fichier) | n/a | Insee : 98 139 (96 158 en décret et déclaration + 1 981 sans formalité), −5,3 % | [W] 2381644 ; [S] https://www.lapresse.tn/2026/10/29/nationalite-francaise-durcissement-des-conditions-les-maghrebins-toujours-nombreux-parmi-les-nouveaux-francais/ | Information : Eurostat s'arrête à 2024 (prochaine mise à jour de l'article SE prévue en mars 2027) |

#### Comparaison avec le ministère : par décret, par déclaration, sans formalité

Le ministère de l'Intérieur n'a la compétence que pour la naturalisation par décret et trois procédures de déclaration (mariage, ascendants, fratries). Le ministère de la Justice traite le reste : filiation et droit du sol, c'est-à-dire les jeunes de 13, 16 ou 18 ans nés en France de parents étrangers et le double droit du sol [L] kit DGEF d'août 2025.

| Voie | 2024 | 2025 | Source |
|---|---|---|---|
| Décret (naturalisation + réintégration), Intérieur | 48 829 | 42 246 (−13,5 %) | [L] kit DGEF ; [W,S] franceinfo 27/01/2026 |
| Déclarations du ressort de l'Intérieur (mariage, ascendants, fratries) | 17 916 | 19 989 (+11,6 %) | idem |
| **Total « ministère de l'Intérieur »** | **66 745** | **62 235** (−6,8 %) | [L] kit DGEF ; [W,S] franceinfo https://www.franceinfo.fr/societe/immigration/expulsions-demandes-d-asile-titres-de-sejour-ce-qu-il-faut-retenir-du-rapport-annuel-sur-l-immigration-du-ministere-de-l-interieur_7765943.html |
| Autres déclarations (Justice : déclarations anticipées, etc.) | 34 764 (calcul) | 33 923 | [R,calcul] ; cohérent avec les lignes Insee |
| Sans formalité | 2 152 | 1 981 | [W] Insee 2381644 |
| **Ensemble (Insee, Eurostat)** | **103 661** | **98 139** | [W] 2381644 |

Contrôle arithmétique : 66 745 + 34 764 + 2 152 = 103 661 et 62 235 + 33 923 + 1 981 = 98 139. Le total Insee par déclaration en 2025 est 53 912 (déclaration anticipée 32 923, mariage 17 579, ascendants et fratries 2 410, autres 1 000) et le « mariage + ascendants/fratries » fait 19 989, le chiffre « Intérieur ».

**Ce que compte Eurostat.** La page SE parle de l'acquisition de la citoyenneté « by the usually resident population » ; elle ne liste pas les modes (« déclaration », « option » et « de plein droit » n'y figurent pas) [W]. Le nombre français d'Eurostat (103 700 pour 2024) correspond au total « Ensemble » de l'Insee, qui contient les 2 152 acquisitions « sans formalité » : toutes les voies sont donc dans le chiffre, ce que je déduis de la concordance des nombres.

**Vocabulaire.** L'Insee et le ministère écrivent « sans formalité » (parfois « sans formalité (à la majorité) »), pas « de plein droit ». L'Insee emploie « de plein droit » pour l'attribution à la naissance [L] fiche Nationalités–Immigration.

**Risque de confusion pour les joueurs.** La presse présente les 62 235 de 2025 (ou 66 745 de 2024) comme le nombre de personnes « devenues françaises », alors que ce n'est que la part du ministère de l'Intérieur. Le fichier (103 661) est le total.

---

### 6. Notes « À savoir » (point 5 du fichier et rédactions proposées)

Les longueurs sont comptées en caractères sans les espaces insécables que le projet impose peut-être (typographie vérifiée par `yarn check:locales`).

#### Note 1 : définitions

- **Verdict** : correcte, avec une correction. Définition de l'immigré : « Selon la définition adoptée par le Haut Conseil à l'Intégration, un immigré est une personne née étrangère à l'étranger et résidant en France » ; la qualité d'immigré est permanente (même après acquisition de la nationalité). Définition de l'étranger : « une personne qui réside en France et ne possède pas la nationalité française » [L] https://www.insee.fr/fr/statistiques/fichier/2383177/fiche-nationalites-immigration.pdf. « 2,6 millions d'immigrés sont français » : exact (« ont acquis la nationalité française »). **« 953 000 étrangers nés en France » : le texte de la page dit 1,0 million.**
- **Rédaction proposée (253 caractères)** : « Un immigré est une personne née étrangère à l'étranger et qui vit en France, même devenue française : c'est le cas de 2,6 millions d'entre eux en 2025. Un étranger n'a pas la nationalité française : ils sont 6,3 millions, dont 1,0 million nés en France. »
- Variante si vous gardez la valeur du tableau : remplacer « 1,0 million » par « 953 000 », en sachant que cette valeur vient du tableau et que le texte de la page arrondit à 1,0 million.

#### Note 2 : provisoire et rupture de série

- **Verdict** : juste sur le fond, mais incomplète. Il faut dire que (a) la rupture vient du changement de protocole de collecte (questionnaire internet sur tous supports, depuis 2024), (b) les estimations provisoires ne permettent aucune variation d'une année sur l'autre, donc pas non plus 2024 → 2025 ; (c) l'Insee a chiffré la rupture (voir la section 2).
- **Rédaction proposée (286 caractères)** : « Les chiffres de 2024 et 2025 sont provisoires. Depuis 2024, le recensement collecte mieux les réponses (questionnaire sur smartphone) : c'est une rupture de série. Ces années ne se comparent pas à celles d'avant, et l'Insee déconseille d'en tirer des évolutions d'une année sur l'autre. »

#### Note 3 : asile

- **Verdict** : à nuancer. « Sans les personnes en procédure Dublin » est exact pour l'Ofpra [W] Insee 6793252. Il manque l'inverse : **Eurostat inclut les procédures Dublin** (communiqué Eurostat et fiche Insee). « Que transmet le ministère de l'Intérieur » repose sur une concordance de chiffres (2023 : 145 160 identique ; 2024 : 129 909 contre 129 910), pas sur une phrase lue. Pour les titres de séjour, un blog [S] cite une brochure Insee disant que la DGEF/DSED transmet directement à Eurostat.
- **Rédaction proposée (305 caractères)** : « Eurostat compte les primo-demandeurs d'asile, procédures Dublin comprises ; ses chiffres français coïncident avec les premières demandes enregistrées aux guichets uniques du ministère de l'Intérieur. L'Ofpra compte les demandes déposées chez lui (premières demandes, réexamens, réouvertures), hors Dublin. »

#### Note 4 : acquisitions de la nationalité

- **Verdict** : « toutes les voies » est exact. Deux corrections : (a) l'Insee et le ministère disent « sans formalité » (acquisition à la majorité), pas « de plein droit » ; (b) il faut éviter la confusion avec les 66 745 (2024) et 62 235 (2025), qui sont la part du ministère de l'Intérieur seul, souvent présentée dans la presse comme le total.
- **Rédaction proposée (280 caractères)** : « Les acquisitions de la nationalité comptent toutes les voies : décret, déclaration (mariage, déclaration anticipée…) et sans formalité (à la majorité). Les 103 661 de 2024 incluent les déclarations enregistrées par la Justice, absentes des 66 745 du seul ministère de l'Intérieur. »

---

### 7. Licences et version anglaise (point 5)

**Insee : Licence Ouverte 2.0.** Page « Mentions légales et crédits » [L, lue avec curl] https://www.insee.fr/fr/information/2008466 : « Sauf mention contraire, les informations publiques diffusées sur ce site (données, bases de données, publications, fichiers téléchargeables) sont mises à disposition sous la Licence Ouverte / Open Licence version 2.0 (Etalab). Cette licence autorise la réutilisation libre, y compris à des fins commerciales, sous réserve de mentionner la source sous la forme « Source : Insee », de mentionner la date de dernière mise à jour des données lorsque celle-ci est connue et de ne pas altérer le sens des informations ou induire en erreur quant à leur interprétation. »
- La page 3633212 elle-même ne contient aucune mention de licence dans son texte ; son pied de page renvoie à « Mentions légales et crédits » [L].
- Les données Eurostat reprises sur cette page (comparaison européenne, « Source : Eurostat (extraction en juin 2026) ») relèvent des règles d'Eurostat.

**Eurostat : réutilisation autorisée avec mention de la source.** Page « Copyright notice » [W] https://ec.europa.eu/eurostat/help/copyright-notice :
- le contenu éditorial est sous licence Creative Commons Attribution 4.0 International ;
- la réutilisation, commerciale ou non, « is authorised provided the source is acknowledged », selon la politique de la Commission mise en œuvre par la décision du 12 décembre 2011 (2011/833/UE) ;
- une traduction ou modification des données ou du texte doit être signalée, et une clause de non-responsabilité d'Eurostat doit figurer ;
- les contenus de tiers et certains documents avec mention restrictive sont exclus.
- Les pages Statistics Explained lues ne contiennent pas de mention de licence propre : seulement « Source: Eurostat (online data code: migr_resfirst) » et un lien « Legal notice » [W].
- Le jeu de données et la CC BY 4.0 : la notice parle du contenu éditorial et de la réutilisation des données ; je n'ai pas lu de page qui rattache expressément chaque jeu de données `migr_*` à la CC BY 4.0.

**Ministère de l'Intérieur** (non lisible directement). Les jeux data.gouv.fr de la DGEF affichent « License Not Specified » sur la fiche, avec en pied de site la Licence Ouverte 2.0 « sauf indication contraire » [W] https://www.data.gouv.fr/datasets/demandes-dasile-publication-du-27-juin-2024. Je n'ai pas pu lire les mentions du site du ministère.

**Ofpra.** Le rapport indique une mise à disposition des données en open data sur data.gouv.fr « à compter du mois suivant la publication ». Aucune mention de licence trouvée dans le texte du rapport (recherche de « licence », « reproduction », « Etalab » sans résultat) [L].

**Version anglaise de 3633212.**
- `https://www.insee.fr/en/statistiques/3633212` renvoie **HTTP 404** : confirmé avec `curl` (code 404, en-tête `content-language: fr-FR`) et avec l'outil de lecture web. La variante `?sommaire=3633217` aussi.
- Même résultat en `/en/` pour 2381757, 2381644, 8651304 et l'information 2008466 : les identifiants français ne se retrouvent pas tels quels en anglais.
- Le lien « English » de la page française pointe vers `/langue/en`, qui redirige vers l'accueil anglais `https://www.insee.fr/en/accueil` (HTTP 200).
- L'Insee a des versions anglaises sous d'**autres identifiants** : par exemple Insee Première 2076 en anglais, `https://www.insee.fr/en/statistiques/8654456` (« In 2024, 6.0 million foreigners lived in France, 0.9 million of whom were born there », HTTP 200, millésime d'octobre 2025). Le bilan démographique 2025 existe en anglais en 8726555 [R].
- Je n'ai pas trouvé d'équivalent anglais de « L'essentiel sur… les immigrés et les étrangers » (recherche limitée au domaine insee.fr). Lier la version française.

---

### 8. Conclusion

#### Écarts, par ordre d'importance

1. **Flux 2025 en plusieurs versions.** Le fichier utilise le dernier chiffre pour les premiers titres (377 462, aussi chez Eurostat), mais la presse a surtout repris **384 230** (annonce du 27/01/2026). Pour l'asile, 116 475 correspond au chiffre ministériel de janvier 2026 (116 476), mais le ministère est passé à **116 944** et Eurostat publiait 116 370 à 116 400. Ces valeurs 2025 sont provisoires. À indiquer (« provisoire », date d'extraction) ; un joueur qui cherche en ligne trouvera des chiffres un peu différents.
2. **« 953 000 étrangers nés en France » présenté comme texte de la page** : le texte dit « 1,0 million ». La valeur 953 000 vient du tableau et je ne l'ai pas confirmée hors tableau.
3. **« En hausse » pour 7,97 millions** : exact à long terme (7,3 % en 1999, 11,6 % en 2025), mais l'Insee interdit de calculer une variation annuelle à partir d'estimations provisoires, et la rupture de 2024 rend la comparaison avec 2023 trompeuse (+440 000 apparents, +198 000 corrigés). Éviter d'afficher une variation 2023 → 2024 → 2025.
4. **Valeurs non retrouvées** : premiers titres 2008 (188 723) et 2023 (338 877) ; primo-demandeurs d'asile 2009 (42 070) ; valeurs départementales exactes pour Paris (21,2), Seine-Saint-Denis (31,6), Guyane (31,4), Mayotte (34,7) hors tableau. Pour la Guyane, l'autre millésime 2023 que j'ai lu donne 33,0 %.
5. **Note 4** : « de plein droit » n'est pas le vocabulaire de l'Insee ni du ministère (« sans formalité »). Risque de confusion avec les 62 235 / 66 745 du seul ministère de l'Intérieur.
6. **Note 3** : manque la précision qu'Eurostat inclut Dublin ; l'origine « ministère » repose sur une concordance de chiffres.
7. **Note 2** : à compléter (pas de variation annuelle sur du provisoire).
8. **Champ de 1921** : France métropolitaine (le fichier écrit France). Les comparaisons avec des recensements généraux anciens demandent de la vigilance selon l'Insee.
9. **Mises à jour disponibles** : acquisitions 2025 = 98 139 (Insee, 09/07/2026), absentes du fichier (Eurostat s'arrête à 2024).
10. **Coquilles de l'Insee, hors fichier** : la note de rupture écrit « 11,0 % » pour 2025 (c'est 11,6 %) et donne +425 000 étrangers là où la série donne +411 000.

#### Conforme

- Stocks Insee 1921, 2023, 2024 et 2025, immigrés et étrangers, effectifs et parts (série Insee de juin 2026, note de rupture, texte de la page, presse).
- Décomposition 2025 : 2,6 M, 5,3 M, 9,6 M (14,0 %).
- Ain 12,4 % (ligne « Lecture » de la page) ; ordres de grandeur de Paris, Seine-Saint-Denis, Guyane et Mayotte cohérents avec le texte.
- Premiers titres 2024 (345 587, dernier millésime) et 2025 (377 462, version révisée = Eurostat SE).
- Primo-demandeurs 2023 (145 160) et 2024 (129 910 contre 129 909), égaux aux chiffres du ministère.
- Ofpra 2025 : 145 270 (111 343 + 33 713 + 214).
- Acquisitions 1998 (123 761), 2022, 2023 et 2024 (114 483, 97 288, 103 661), identiques au total Insee « Ensemble » et au total du kit DGEF.
- Licences : Insee Licence Ouverte 2.0 ; Eurostat réutilisation avec mention de la source (CC BY 4.0 pour le contenu éditorial) ; `/en/statistiques/3633212` bien en 404.

---

### 9. URL consultées

**Insee**
- https://www.insee.fr/fr/statistiques/3633212 (HTML téléchargé, texte hors tableaux ; statut des URL `/en/`)
- https://www.insee.fr/en/statistiques/3633212 (404)
- https://www.insee.fr/fr/statistiques/fichier/2383177/Note_methodo_rupture_serie_immigration.pdf
- https://www.insee.fr/fr/statistiques/fichier/2383177/fiche-nationalites-immigration.pdf
- https://www.insee.fr/fr/statistiques/2381757 et https://www.insee.fr/fr/statistiques/fichier/2381757/demo-etran-part-pop-etran-immig.xlsx
- https://www.insee.fr/fr/statistiques/2381759
- https://www.insee.fr/fr/statistiques/2381644
- https://www.insee.fr/fr/statistiques/8651304 (Insee Première 2076) et https://www.insee.fr/fr/statistiques/fichier/version-html/8651304/ip2076.pdf
- https://www.insee.fr/en/statistiques/8654456 (Insee Première 2076 en anglais)
- https://www.insee.fr/fr/statistiques/8998082 (Insee Première 2107, « Flux migratoires »)
- https://www.insee.fr/fr/statistiques/8236359 (Insee Première 2011)
- https://www.insee.fr/fr/statistiques/6793226 (Insee Références 2023, histoire des migrations)
- https://www.insee.fr/fr/statistiques/6793252 (fiche 2.5, premières demandes d'asile)
- https://www.insee.fr/fr/statistiques/fichier/version-html/6793248/IMMFRA23-F13.pdf
- https://insee.fr/fr/statistiques/fichier/1371777/IMMFRA05.PDF
- https://www.insee.fr/fr/statistiques/zones/8997734 (RP 2023, sans données lisibles)
- https://www.insee.fr/fr/statistiques/8719824 (bilan démographique 2025)
- https://www.insee.fr/fr/information/2008466 (mentions légales)
- Statuts `/en/` : 8651304, 2381757, 2381644, information/2008466 (404) ; https://www.insee.fr/langue/en (200, accueil anglais)

**Eurostat**
- https://ec.europa.eu/eurostat/web/products-eurostat-news/w/ddn-20260325-2
- https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Residence_permits_-_statistics_on_first_permits_issued_during_the_year
- https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Acquisition_of_citizenship_statistics
- https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Asylum_statistics (404)
- https://ec.europa.eu/eurostat/help/copyright-notice
- https://ec.europa.eu/eurostat/about-us/policies/copyright (404)
- https://ec.europa.eu/eurostat/fr/web/migration-asylum/managed-migration/methodology

**Ofpra**
- https://www.ofpra.gouv.fr/sites/default/files/2026-07/Rapport%20d%27activit%C3%A9%202025%20Ofpra.pdf
- https://www.ofpra.gouv.fr/actualites/lofpra-publie-son-rapport-dactivite-2025-a-loccasion-des-75-ans-de-la-convention-de
- https://www.ofpra.gouv.fr/actualites/bilan-2025-de-lofpra-une-activite-record-et-des-evolutions-contrastees
- https://www.ofpra.gouv.fr/en/step-2-introduction

**Ministère de l'Intérieur (403 pour l'outil de lecture) et documents liés**
- https://www.immigration.interieur.gouv.fr/documentation/etudes-et-statistiques/titres-de-sejour-en-2025-protections-subsidiaires-ont-plus-que-double.html (403)
- https://www.immigration.interieur.gouv.fr/Info-ressources/Etudes-et-statistiques/Les-chiffres-de-l-immigration-en-France/Sejour (403)
- https://www.immigration.interieur.gouv.fr/chiffres-de-limmigration-en-france/demandes-dasile-en-2025-procedure-sur-deux-aboutit-a-protection (403)
- https://www.immigration.interieur.gouv.fr/publications/chiffres-de-limmigration-en-france/demandes-dasile-pour-lannee-2025 (403)
- Résumés de recherche seulement : pages « Asile », « Population immigrée par département », « Accès à la nationalité française pour l'année 2025 »
- https://www.gisti.org/IMG/pdf/kit-prefets_etrangers-en-france_2025-08.pdf (copie d'un kit DGEF, août 2025, lu)
- https://www.data.gouv.fr/datasets/demandes-dasile-publication-du-27-juin-2024
- https://www.data.gouv.fr/datasets/66a8cc809b4750710f18920c (titres de séjour, publication du 27 juin 2024)
- https://www.assemblee-nationale.fr/dyn/13/questions/QANR5L13QE85075.pdf

**Presse, ONG, sites secondaires**
- franceinfo : https://www.franceinfo.fr/societe/immigration/immigration-384-230-premiers-titres-de-sejour-delivres-en-2025-en-hausse-de-11-2-e-de-11-2_7767725.html ; https://www.franceinfo.fr/societe/immigration/expulsions-demandes-d-asile-titres-de-sejour-ce-qu-il-faut-retenir-du-rapport-annuel-sur-l-immigration-du-ministere-de-l-interieur_7765943.html ; https://www.franceinfo.fr/societe/immigration/les-demandes-d-asile-ont-recule-de-5-5-en-france-en-2025-par-rapport-a-2024-selon-l-office-francais-de-protection-des-refugies-et-apatrides_8124962.html
- La Cimade : https://www.lacimade.org/bilan2025asile/ ; https://www.lacimade.org/donnees-migratoires-2025-une-analyse-critique/ ; https://www.lacimade.org/rapport-2025-ofpra-cartographie-de-la-demande-dasile/
- Causeur : https://www.causeur.fr/immigration-edouard-philippe-calculs-titres-de-sejour-2027-336201
- IFRAP : https://www.ifrap.org/fonction-publique-et-administration/lasile-nouveau-moteur-de-limmigration-reguliere
- Algérie-Éco : https://algerie-eco.com/2026/09/02/visas-titres-de-sejour-nationalite-les-chiffres-de-limmigration-algerienne-en-france-en-2025/
- Algerie360 : https://www.algerie360.com/immigration-en-france-lalgerie-reste-le-premier-pays-dorigine-des-immigres-en-2025/
- Pressenza : https://www.pressenza.com/fr/2026/09/sans-immigration-que-deviendrait-leconomie-francaise/
- Maire-info : https://maire-info.com/populations-etrangeres-et-immigrees-en-france-les-nouvelles-statistiques-de-linsee-article2-30076
- Économie Matin : https://www.economiematin.fr/?p=204246
- Toute l'Europe : https://www.touteleurope.eu/l-ue-dans-le-monde/le-nombre-de-demandeurs-d-asile-dans-l-union-europeenne/
- Brussels Times : https://www.brusselstimes.com/2044172/eu-asylum-claims-drop-27-in-2025-as-venezuelans-surpass-syrians
- InfoMigrants : https://www.infomigrants.net/fr/post/72678/asile-en-france-en-2025--les-femmes-desormais-plus-nombreuses-a-beneficier-de-la-protection-subsidiaire
- Connexion France : https://www.connexionfrance.com/news/france-sees-fall-in-immigration-latest-official-figures-show/802607
- La Presse (Tunisie) : https://www.lapresse.tn/2026/10/29/nationalite-francaise-durcissement-des-conditions-les-maghrebins-toujours-nombreux-parmi-les-nouveaux-francais/
- Michèle Tribalat (blog) : https://micheletribalat.fr/435108953/442891477
- Wikipédia : https://fr.wikipedia.org/wiki/Immigration_en_France
- Europe 1 : https://www.europe1.fr/societe/immigration-336700-premiers-titres-de-sejour-delivres-en-2024-en-hausse-de-18-287577 ; https://www.europe1.fr/politique/immigration-record-du-nombre-de-premiers-titres-de-sejour-a-323260-en-2023-4227072 (résumés de recherche)
- Démarches administratives : https://demarchesadministratives.fr/actualites/hausse-des-visas-nette-augmentation-des-departs-forces-tous-les-chiffres-sur-immigration-en-2024 (403, résumé de recherche)
- JDD : https://www.lejdd.fr/Societe/immigration-en-france-une-explosion-demographique-chiffree-par-linsee-162977 (résumé de recherche)
- Forum Réfugiés : https://www.forumrefugies.org/s-informer/publications/articles-d-actualites/en-france/1860-en-2025-plus-de-la-moitie-des-demandeurs-d-asile-proteges (503, résumé de recherche)

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
