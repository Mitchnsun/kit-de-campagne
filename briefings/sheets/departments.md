# `departments` · Fond de carte des départements

**Vérifié le 02/11/2026** : double vérification sur le web, sans écart (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Fichier | `briefings/basemap/departments.json`, écrit par `yarn briefings:map` le 2026-11-02 ; `departments.json` dans l'édition « Données des Dossiers » |
| Usage | Les pages en carte des Dossiers : pauvreté (#26), urbain et rural (#23), scrutins passés (#33), et les autres cartes à venir (#28, #30, #140, #142, #143), ticket #148 de l'app |
| Source | IGN, ADMIN EXPRESS COG CARTO PE (petite échelle), édition 2026, COG au 1er janvier 2026 ; couche `ADMINEXPRESS-COG-CARTO-PE.2026:departement` du WFS de la Géoplateforme (https://data.geopf.fr/wfs/ows) ; jeu de données https://www.data.gouv.fr/datasets/admin-express/ ; Licence Ouverte 2.0 |
| Projections | Projetées par le service : Lambert-93 (EPSG:2154) pour la métropole ; UTM locales pour l'outre-mer : EPSG:5490 (Guadeloupe, Martinique), 2972 (Guyane), 2975 (La Réunion), 4471 (Mayotte) |
| Traitement | Simplification par mapshaper, en une seule topologie (deux voisins gardent la même frontière, aucun département ne disparaît), jusqu'à 1,5 unité du cadre ; chemins SVG en coordonnées entières, anneaux tracés selon la règle pair-impair (l'enclave de Valréas est un trou de la Drôme) |
| Cadres | Métropole, Corse comprise : 1000 × 948 unités. Chaque département d'outre-mer dans son propre cadre, à sa propre échelle (200 unités au plus) : les cartes le disent. Pas d'encart pour Paris (aucun sur la planche `DOS-5-carte`) |
| Contenu | Les 101 départements, avec leur code du COG et leur nom officiel : 96 en métropole (Corse en `2A` et `2B`), 971 à 974 et 976 |
| Poids | 37 Ko en JSON réduit (critère de #148 : moins de 150 Ko) |
| Première édition | À remplir à la publication |

## Mention à afficher

La Licence Ouverte 2.0 demande la source et la date de dernière mise à jour, sans laisser croire à une caution de l'IGN. L'IGN ne donne pas de formule propre à ADMIN EXPRESS (non trouvée). Mention proposée, à valider par le PO : « Contours des départements : IGN, ADMIN EXPRESS COG CARTO PE, édition 2026, Licence Ouverte 2.0. Simplifiés pour le jeu. »

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans appeler la couche WFS qu'utilise le script. Le rendu du fichier (la métropole et les cinq encarts) a aussi été dessiné et relu à l'œil.

Date de la vérification : 2026-11-02.
Fichier vérifié : 101 départements (96 métropolitains avec 2A et 2B, plus 971, 972, 973, 974, 976), produits à partir de la couche WFS `ADMINEXPRESS-COG-CARTO-PE.2026:departement` de la Géoplateforme (millésime 2026, producteur IGN).
Méthode : aucun appel à la couche WFS. Les codes et noms ont été comparés par script (Python) au fichier CSV officiel de l'Insee, téléchargé directement sur insee.fr. Les produits et projections ont été vérifiés dans la documentation PDF de l'IGN, dans le flux de l'API de téléchargement de la Géoplateforme (service distinct du WFS), dans la fiche de métadonnées ISO du catalogue CSW de la Géoplateforme, dans l'API de data.gouv.fr et dans une copie du registre EPSG (epsg.io).

Réserve de méthode : pour les points 2 et 3, les sources disponibles sont presque toutes produites par l'IGN lui-même (documentation, métadonnées, flux de téléchargement), ou reprises de l'IGN par data.gouv.fr. La seule source tierce pour les projections est le registre EPSG (via epsg.io). La seule source tierce pour la licence est le texte de la Licence Ouverte 2.0 (Etalab).

### 1. Codes et noms des départements contre le COG 2026 de l'Insee

Source de référence : `v_departement_2026.csv` (COG au 1er janvier 2026, 101 lignes de données, UTF-8), téléchargé sur insee.fr. data.gouv.fr (jeu « Code officiel géographique », licence Licence Ouverte, mis à jour le 2026-10-06) référence ce même fichier (même URL insee.fr, daté du 2026-02-24).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Nombre de départements | 101 (96 métropolitains + 5 DROM) | 101 lignes dans `v_departement_2026.csv` ; la documentation IGN (descriptif de contenu v4.0, § 5.17) écrit « Depuis avril 2011, on compte 101 départements (dont 5 d'outre-mer) » | https://www.insee.fr/fr/statistiques/fichier/8740222/v_departement_2026.csv ; https://data.geopf.fr/annexes/ressources/documentation/DC_ADMIN_EXPRESS_4-0.pdf | Conforme |
| Codes (101) | 01 à 19, 21 à 95 (sans 20), 2A, 2B, 971, 972, 973, 974, 976 | Mêmes 101 codes (comparaison ensembliste par script : 0 code en plus, 0 code en moins) | https://www.insee.fr/fr/statistiques/fichier/8740222/v_departement_2026.csv | Conforme |
| Noms (101), orthographe, traits d'union, accents, apostrophes | Liste du fichier `departments-list.txt` | Colonne `LIBELLE` du COG 2026 : identique caractère par caractère pour les 101 (0 différence). `LIBELLE` = `NCCENR` pour les 101 lignes. Apostrophes : ASCII (') des deux côtés (« Côte-d'Or », « Côtes-d'Armor », « Val-d'Oise ») ; aucune apostrophe typographique dans le COG | idem | Conforme |
| 971 | Guadeloupe | Guadeloupe (région 01) | idem | Conforme |
| 972 | Martinique | Martinique (région 02) | idem | Conforme |
| 973 | Guyane | Guyane (région 03) | idem | Conforme |
| 974 | La Réunion | La Réunion (majuscule à « Réunion », accent, article « La » dans le libellé ; NCC « LA REUNION ») (région 04) | idem | Conforme |
| 976 | Mayotte | Mayotte (région 06) | idem | Conforme |
| 2A / 2B | Corse-du-Sud / Haute-Corse | 2A Corse-du-Sud, 2B Haute-Corse (région 94) | idem | Conforme |
| 67 et 68 (Collectivité européenne d'Alsace) | 67 Bas-Rhin, 68 Haut-Rhin | Les deux départements restent dans le COG 2026 : 67 « Bas-Rhin » et 68 « Haut-Rhin ». La Collectivité européenne d'Alsace est une collectivité à compétences départementales à part, code `6AE`, dans `v_ctcd_2026.csv` (chef-lieu 67482). Dans `v_commune_2026.csv`, 514 communes ont DEP = 67 et 366 ont DEP = 68, toutes rattachées à CTCD = 6AE | https://www.insee.fr/fr/statistiques/fichier/8740222/v_ctcd_2026.csv ; https://www.insee.fr/fr/statistiques/fichier/8740222/v_commune_2026.csv | Conforme |
| Fusion ou nouveau code de département en 2026 | Aucun | Aucun. Les 34 875 communes du COG 2026 (type COM) portent exactement 101 valeurs distinctes de DEP, les mêmes que le fichier. La page de l'Insee ne mentionne pas de fusion de départements (changements 2026 : 19 communes ont changé de nom, 40 communes déléguées ou associées supprimées, aucune commune nouvelle) | https://www.insee.fr/fr/information/8740222 | Conforme |
| Rhône (69) et Métropole de Lyon | 69 Rhône | Le département 69 « Rhône » reste un seul département dans le COG 2026 (266 communes) ; la Métropole de Lyon (58 communes) est une collectivité à compétences départementales (CTCD `69M`) et non un département (`69D` : 208 communes). Pas de code de département 69M | https://www.insee.fr/fr/statistiques/fichier/8740222/v_ctcd_2026.csv ; https://www.insee.fr/fr/statistiques/fichier/8740222/v_commune_2026.csv | Conforme |
| Paris (75) | 75 Paris | 75 « Paris » (1 commune) ; CTCD `75C` « Ville de Paris » | idem | Conforme |
| Mayotte : changement de nom au 1er janvier 2026 | « Mayotte » (département 976) | L'Insee écrit : « la collectivité territoriale de Mayotte, régie par l'article 73 de la Constitution, prend le nom de Département-Région de Mayotte et le code 976R au 1er janvier 2026 ». Ce changement touche la collectivité (CTCD `976R`, « Département-Région de Mayotte »), pas la ligne du département : `v_departement_2026.csv` garde DEP 976, libellé « Mayotte ». | https://www.insee.fr/fr/information/8740222 ; https://www.insee.fr/fr/statistiques/fichier/8740222/v_ctcd_2026.csv | Écart expliqué (aucun effet sur le fichier ; à retenir si l'interface devait un jour afficher le nom de la collectivité) |

### 2. ADMIN EXPRESS COG CARTO PE

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Le produit « ADMIN EXPRESS COG CARTO PE » existe | `publication: ADMIN EXPRESS COG CARTO PE` | Oui. Le descriptif de contenu v4.0 (mai 2025) liste « ADMIN EXPRESS COG CARTO Petite échelle » (abrégé PE) et « ADMIN EXPRESS COG CARTO PLUS Petite échelle ». Le flux de l'API de téléchargement de la Géoplateforme a une ressource `ADMIN-EXPRESS-COG-CARTO-PE`. data.gouv.fr titre le jeu « ADMIN EXPRESS, ADMIN EXPRESS COG, ADMIN EXPRESS COG CARTO, ADMIN EXPRESS COG CARTO PE, ADMIN EXPRESS COG CARTO PLUS PE » | https://data.geopf.fr/annexes/ressources/documentation/DC_ADMIN_EXPRESS_4-0.pdf ; https://data.geopf.fr/telechargement/resource/ADMIN-EXPRESS-COG-CARTO-PE ; https://www.data.gouv.fr/fr/datasets/admin-express/ | Conforme |
| PE = édition « petite échelle » | Petite échelle | Le flux de téléchargement décrit le produit ainsi : « ADMIN EXPRESS COG CARTO PE est une édition millésimée d'ADMIN EXPRESS pour un usage cartographique petite échelle (édition annuelle) ». Le descriptif de contenu : « Édition millésimée généralisée d'ADMIN EXPRESS COG pour un usage cartographique et/ou statistique à petite échelle ». La métadonnée ISO : COG CARTO est « un produit généralisé moyenne échelle », COG CARTO PE et CARTOPLUS PE sont « des produits généralisés petite échelle » | https://data.geopf.fr/telechargement/resource/ADMIN-EXPRESS-COG-CARTO-PE ; DC v4.0 § 1.1 et 2.1 ; https://data.geopf.fr/csw?SERVICE=CSW&VERSION=2.0.2&REQUEST=GetRecordById&ID=IGNF_ADMIN-EXPRESS&elementSetName=full&OUTPUTSCHEMA=http://www.isotc211.org/2005/gmd | Conforme |
| Lien avec « COG CARTO » | « petite échelle de COG CARTO » (énoncé de la demande) | Nuance : l'IGN présente COG CARTO PE comme un produit frère de COG CARTO, tous deux dérivés d'ADMIN EXPRESS COG, et non comme une version « dérivée de COG CARTO ». Mêmes traitements que COG CARTO (défonce sur l'estuaire de la Gironde, sélection des îlots rocheux de moins de 500 m²), seule la généralisation diffère : algorithme Sherbend (FME) avec un rayon de 1 000 m, « pour proposer une donnée moins lourde avec des géométries plus simplifiées ». Précision en erreur moyenne quadratique : 15 à 50 m pour COG CARTO, 60 à 600 m pour PE | DC v4.0 §§ 3.3 et 3.4.2 : https://data.geopf.fr/annexes/ressources/documentation/DC_ADMIN_EXPRESS_4-0.pdf | Écart expliqué (nuance de formulation, pas d'effet sur le fichier) |
| Existence de l'édition 2026 | `vintage: 2026` | Oui. Le flux de téléchargement liste les paquets `ADMIN-EXPRESS-COG-CARTO-PE_4-0__GPKG_…_2026-01-01` (France métropolitaine, chaque DROM, WGS84), mis à jour le 2026-07-02 et le 2026-07-03 ; `editionDateEnd` = 2026-01-01. Les éditions 2025-01-01 sont aussi listées. data.gouv.fr liste la ressource WFS `ADMINEXPRESS-COG-CARTO-PE.2026:departement` (« ADMIN EXPRESS COG CARTO PE 2026 département », mise à jour le 2026-05-13) et les services WMS/WMTS `ADMINEXPRESS-COG-CARTO-PE.2026` | https://data.geopf.fr/telechargement/resource/ADMIN-EXPRESS-COG-CARTO-PE?page=1 (pages 1 à 3) ; https://www.data.gouv.fr/api/1/datasets/5808de39c751df1e0679df72/ | Conforme |
| Sens du millésime | COG 2026 | Produits « COG » : édition annuelle « au 1er janvier de l'année en cours (les modifications mises en œuvre à partir du 2 janvier ne sont pas prises en compte) » (DC v4.0 § 1.3) ; le millésime 2026 suit donc le COG de l'Insee au 1er janvier 2026, cohérent avec les 101 départements du point 1 | DC v4.0 § 1.3 | Conforme |
| Version du produit en 2026 | non indiquée dans le fichier | Version 4.0 (nom des paquets `…_4-0__…_2026-01-01`). Le suivi des évolutions depuis la v4.0 (août 2025) ne décrit pas de changement de version | https://data.geopf.fr/annexes/ressources/documentation/SE_ADMIN_EXPRESS_depuis_v4-0.pdf | Conforme (information) |
| Produit « PLUS PE » (rapprochement fictif des DROM-COM) | Le fichier utilise PE, pas PLUS PE | `ADMIN EXPRESS COG CARTO PLUS Petite échelle` existe aussi : même généralisation que PE, avec « rapprochement fictif des DROM-COM autour de la métropole » et géoréférencement fictif en Lambert 93. Les cadres des DROM du fichier (971 à 976, plus grande dimension de 200 unités) ne viennent donc pas de ce produit mais de la mise en page du script | DC v4.0 §§ 1.1, 3.4.2 | Écart expliqué (le fichier utilise bien PE) |
| Licence | non indiquée dans l'extrait fourni | Licence Ouverte / Open Licence version 2.0 (Etalab). data.gouv.fr : `license = lov2`, producteur « Institut national de l'information géographique et forestière ». Métadonnée ISO de l'IGN : « Licence Ouverte / Open License (compatible ODC-BY, CC-BY 2.0) » avec renvoi vers le PDF Etalab ; « Pas de restriction d'accès public » | https://www.data.gouv.fr/fr/datasets/admin-express/ ; https://www.data.gouv.fr/api/1/datasets/5808de39c751df1e0679df72/ ; ISO CSW (URL ci-dessus) | Conforme |
| Dernière mise à jour du jeu sur data.gouv.fr | non applicable | 2026-10-19 (`last_update`). Métadonnée ISO : `modified` = 2026-10-19 ; « API de diffusion … Edition Septembre 2026 », « API de téléchargement : ADMIN EXPRESS - Edition Octobre 2026 ». Fréquence déclarée : mensuelle pour ADMIN EXPRESS ; annuelle pour les produits COG | idem | Conforme (information) |
| Obligation d'attribution (texte de la licence) | non indiquée | Licence Ouverte 2.0 : le réutilisateur doit « mentionner la paternité de l'Information : sa source (a minima le nom du Concédant) et la date de la dernière mise à jour de l'Information réutilisée ». Il peut le faire en indiquant l'URL de l'information. La mention ne doit ni conférer un caractère officiel à la réutilisation, ni suggérer une caution du Concédant. Les modifications et l'usage commercial sont permis (« l'adapter, la modifier, l'extraire et la transformer ») | https://raw.githubusercontent.com/etalab/licence-ouverte/master/LO.md (dépôt officiel Etalab) | Conforme (obligation à respecter dans le jeu) |
| Formule de mention propre à l'IGN pour ADMIN EXPRESS | non indiquée | Non trouvé. Ni la page data.gouv.fr, ni la métadonnée ISO, ni les trois PDF de documentation (DC, DL, SE v4.0) ne donnent de formule imposée. Les conditions d'utilisation de cartes.gouv.fr renvoient à la licence attachée au jeu (« Vous vous engagez à respecter les termes de la licence attachée à ces données ») et ne précisent pas de formule. La page de la FAQ de l'IGN (professionnels.ign.fr/faq) est en erreur 404. Je n'ai donc pas de texte officiel de l'IGN à citer, seulement la règle de la Licence Ouverte 2.0. | https://cartes.gouv.fr/cgu ; ISO CSW ; PDF DC/DL/SE | Non trouvé |

Mention minimale proposée (construite à partir de la règle de la licence, pas citée de l'IGN) : « Contours des départements : IGN, ADMIN EXPRESS COG CARTO PE, édition 2026 (COG au 1er janvier 2026), Licence Ouverte 2.0, mis à jour le 2026-10-19 (fiche data.gouv.fr). Données simplifiées par l'éditeur du jeu. » Ce texte est à valider par le propriétaire du projet. La licence autorise la simplification ; la mention ne doit pas laisser croire que l'IGN cautionne le jeu.

### 3. Projections des départements d'outre-mer dans les produits de l'IGN

Source principale : descriptif de contenu ADMIN EXPRESS v4.0, § 2.3 « Références géodésiques » (« Les données sont proposées de façon standard dans les systèmes légaux de référence suivants »). Confirmée par les catégories et les paquets du flux de téléchargement de `ADMIN-EXPRESS-COG-CARTO-PE` (une livraison par territoire) et par le registre EPSG (via epsg.io).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| France métropolitaine | EPSG:2154 (Lambert-93) | RGF93 / Lambert 93, EPSG 2154. Paquet PE `…_GPKG_LAMB93_FXX_2026-01-01`. EPSG : « ETRS89-FRA [RGF93 v1] / Lambert-93 - France » | DC v4.0 § 2.3 ; https://data.geopf.fr/telechargement/resource/ADMIN-EXPRESS-COG-CARTO-PE?page=1 ; https://epsg.io/2154 | Conforme |
| Guadeloupe (971) | EPSG:5490 (RGAF09 / UTM 20N) | RGAF09, UTM Nord fuseau 20, EPSG 5490. Paquet PE `…_GPKG_RGAF09UTM20_GLP_2026-01-01`. EPSG : « RGAF09 / UTM zone 20N » | DC v4.0 § 2.3 ; flux PE page 2 ; https://epsg.io/5490 | Conforme |
| Martinique (972) | EPSG:5490 | RGAF09, UTM Nord fuseau 20, EPSG 5490. Paquet PE `…_RGAF09UTM20_MTQ_2026-01-01` | idem | Conforme |
| Guyane (973) | EPSG:2972 (RGFG95 / UTM 22N) | RGFG95, UTM Nord fuseau 22, EPSG 2972. Paquet PE `…_UTM22RGFG95_GUF_2026-01-01`. EPSG : « RGFG95 / UTM zone 22N » | DC v4.0 § 2.3 ; flux PE page 3 ; https://epsg.io/2972 | Conforme |
| La Réunion (974) | EPSG:2975 (RGR92 / UTM 40S) | RGR92, UTM Sud fuseau 40, EPSG 2975. Paquet PE `…_RGR92UTM40S_REU_2026-01-01`. EPSG : « RGR92 / UTM zone 40S » | DC v4.0 § 2.3 ; flux PE page 3 ; https://epsg.io/2975 | Conforme |
| Mayotte (976) | EPSG:4471 (RGM04 / UTM 38S) | RGM04, UTM Sud fuseau 38, EPSG 4471. Paquet PE `…_RGM04UTM38S_MYT_2026-01-01`. EPSG : « RGM04 / UTM zone 38S ». Nuance : le registre EPSG indique que ce CRS est « replaced by RGM23 / UTM zone 38S (CRS code 10674) with effect from 2023-01-01 » ; l'IGN continue d'utiliser RGM04 / EPSG 4471 dans ADMIN EXPRESS v4.0 et dans l'édition 2026 | DC v4.0 § 2.3 ; flux PE page 2 ; https://epsg.io/4471 | Écart expliqué (conforme à l'IGN ; le CRS EPSG est en cours de remplacement par RGM23 dans le registre) |
| Autres territoires livrés (hors fichier) | non utilisés | Saint-Martin et Saint-Barthélemy : EPSG 5490. Saint-Pierre-et-Miquelon : RGSPM06 / UTM 21N, EPSG 4467. Livraison « France entière » en coordonnées géographiques WGS84G (EPSG 4326) | DC v4.0 § 2.3 ; flux PE | Conforme (information) |
| Un seul CRS pour toute la France dans le produit PE | non applicable | Non : les contours PE sont livrés par territoire dans leur projection légale, et en WGS84 pour la France entière. Le rapprochement fictif des DROM en Lambert 93 n'existe que dans le produit PLUS PE | DC v4.0 §§ 1.1, 2.3, 3.4.2 | Conforme (information) |

### Conclusion

- Codes et noms : aucun écart. Les 101 codes et les 101 noms du fichier sont identiques au fichier officiel `v_departement_2026.csv` de l'Insee (COG au 1er janvier 2026). Le COG 2026 compte exactement ces 101 départements : pas de fusion, pas de nouveau code, 67 et 68 maintenus (la Collectivité européenne d'Alsace est la collectivité `6AE`, pas un département), la Métropole de Lyon n'est pas un département (69 reste « Rhône »).
- Ce qui a changé au 1er janvier 2026 dans le COG ne touche pas la liste des départements : la collectivité de Mayotte devient « Département-Région de Mayotte » (code de collectivité 976R) ; le département garde le code 976 et le libellé « Mayotte ».
- ADMIN EXPRESS COG CARTO PE existe, est le produit généralisé « petite échelle » de l'offre ADMIN EXPRESS (version 4.0), avec une édition 2026 (au 1er janvier 2026, paquets publiés en juillet 2026). Nuance : l'IGN le présente comme un produit frère de COG CARTO (moyenne échelle), pas comme sa version dérivée.
- Licence : Licence Ouverte 2.0 (Etalab), jeu mis à jour le 2026-10-19 sur data.gouv.fr. L'obligation est de citer la source (au moins l'IGN) et la date de dernière mise à jour. L'IGN ne donne pas de formule propre pour ADMIN EXPRESS (non trouvé).
- Projections : les cinq projections attendues sont toutes confirmées par le descriptif de contenu de l'IGN et par les paquets de téléchargement du produit PE. Seule nuance : le registre EPSG signale que RGM04 / UTM 38S (4471) est remplacé par RGM23 (10674) depuis 2023, mais l'IGN utilise toujours 4471.
- Limites : les PDF de `geoservices.ign.fr` redirigent désormais vers cartes.gouv.fr ; je les ai lus dans leur copie `data.geopf.fr/annexes/…`. La seule source tierce pour les projections est epsg.io ; je n'ai pas consulté le registre EPSG officiel (epsg.org).

### URL consultées (2026-11-02)

Consultées avec succès :

- https://www.insee.fr/fr/information/8740222 (page COG 2026, téléchargement des fichiers)
- https://www.insee.fr/fr/statistiques/fichier/8740222/v_departement_2026.csv
- https://www.insee.fr/fr/statistiques/fichier/8740222/v_ctcd_2026.csv
- https://www.insee.fr/fr/statistiques/fichier/8740222/v_region_2026.csv
- https://www.insee.fr/fr/statistiques/fichier/8740222/v_comer_2026.csv
- https://www.insee.fr/fr/statistiques/fichier/8740222/v_commune_2026.csv
- https://www.data.gouv.fr/api/1/datasets/code-officiel-geographique-cog/ (jeu « Code officiel géographique », licence fr-lo, mis à jour le 2026-10-06)
- https://www.data.gouv.fr/fr/datasets/admin-express/ et https://data.gouv.fr/en/datasets/admin-express-admin-express-cog-admin-express-cog-carto-admin-express-cog-carto-pe (fiche du jeu ADMIN EXPRESS)
- https://www.data.gouv.fr/api/1/datasets/5808de39c751df1e0679df72/ (métadonnées et liste des 255 ressources du jeu ADMIN EXPRESS)
- https://data.geopf.fr/telechargement/resource/ADMIN-EXPRESS-COG-CARTO-PE (pages 1 à 3 : 28 paquets, projections, éditions 2024, 2025 et 2026)
- https://data.geopf.fr/csw?SERVICE=CSW&VERSION=2.0.2&REQUEST=GetRecordById&ID=IGNF_ADMIN-EXPRESS&elementSetName=full&OUTPUTSCHEMA=http://www.isotc211.org/2005/gmd (fiche ISO du catalogue : licence, échelles, mise à jour)
- https://data.geopf.fr/annexes/ressources/documentation/DC_ADMIN_EXPRESS_4-0.pdf (descriptif de contenu v4.0, mai 2025)
- https://data.geopf.fr/annexes/ressources/documentation/DL_ADMIN_EXPRESS_4-0.pdf (descriptif de livraison v4.0)
- https://data.geopf.fr/annexes/ressources/documentation/SE_ADMIN_EXPRESS_depuis_v4-0.pdf (suivi des évolutions depuis la v4.0, août 2025)
- https://raw.githubusercontent.com/etalab/licence-ouverte/master/LO.md (texte de la Licence Ouverte 2.0)
- https://cartes.gouv.fr/cgu (conditions d'utilisation de la Géoplateforme)
- https://epsg.io/2154, https://epsg.io/5490, https://epsg.io/2972, https://epsg.io/2975, https://epsg.io/4471, https://epsg.io/4467

Recherches web qui ont orienté les sources (résultats secondaires, non cités comme preuves) : « Insee code officiel géographique 2026 liste des départements », « IGN ADMIN EXPRESS COG CARTO PE petite échelle », deux recherches sur l'attribution des données IGN sous Licence Ouverte.

Échecs ou sources non exploitables :

- https://geoservices.ign.fr/sites/default/files/2025-06/SE_ADMIN_EXPRESS_depuis_v4-0.pdf, https://geoservices.ign.fr/adminexpress et https://geoservices.ign.fr/documentation/donnees/vecteur/adminexpress : redirection 301 vers cartes.gouv.fr (page d'application sans contenu lisible). Les PDF ont été obtenus sur data.geopf.fr (ci-dessus).
- https://cartes.gouv.fr/rechercher-une-donnee/dataset/IGNF_ADMIN-EXPRESS : application web, aucun contenu lisible.
- https://web.archive.org/… : accès refusé par l'outil.
- https://www.etalab.gouv.fr/wp-content/uploads/2018/11/open-licence.pdf : connexion coupée ; texte de la licence lu sur le dépôt GitHub d'Etalab.
- https://www.etalab.gouv.fr/licence-ouverte-open-licence/ : redirige vers data.gouv.fr.
- http://professionnels.ign.fr/faq : erreur 404.

## Mises à jour

- **03/11/2026, relecture du PO** : mention validée telle quelle, à afficher sous chaque carte : « Contours des départements : IGN, ADMIN EXPRESS COG CARTO PE, édition 2026, Licence Ouverte 2.0. Simplifiés pour le jeu. »

## Relecture

- [x] Les 101 codes et noms comparés au COG 2026 de l'Insee.
- [x] La licence vérifiée, et la mention qu'elle demande.
- [x] Le rendu relu : aucun trou entre départements voisins, les encarts lisibles.
- [ ] Relue par le PO, mention comprise.
