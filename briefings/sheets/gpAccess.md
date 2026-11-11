# `gpAccess` · L'accès aux médecins généralistes

**Vérifiée le 11/11/2026** : double vérification sur le web et sur le lisez-moi de la DREES, sans écart (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `gpAccess`, deuxième volet de la page « Dépense, médecins et hôpital » (`healthCare`), dossier « Santé » (`health`), page de type comparaison, ticket #143 de l'app |
| Données | `briefings/data/gpAccess.json`, écrit par `yarn briefings gpAccess` le 2026-11-11 |
| Sources | DREES, « Accessibilité potentielle localisée (APL) aux professionnels de santé » (data.drees, jeu `530_l-accessibilite-potentielle-localisee-apl`), page https://data.drees.solidarites-sante.gouv.fr/explore/dataset/530_l-accessibilite-potentielle-localisee-apl/information/ ; fichier « Indicateurs d'APL moyens par dixièmes de population.xlsx » (pièce jointe `indicateurs_d_apl_moyens_par_dixiemes_de_population_xlsx`), feuille « Médecins généralistes » ; Licence Ouverte v2.0 (Etalab), citée par les métadonnées du jeu ; daté par la date de modification du jeu, 2026-07-22 |
| Séries | `aplMean` : APL moyenne aux médecins généralistes de 65 ans ou moins, consultations, visites et téléconsultations par an et par habitant standardisé, France hors Mayotte, ligne « France entière hors Mayotte », 2022 à 2024, 3 points ; `aplGap` : « Rapport entre l'accessibilité des 10 % de la population les mieux dotés et les 10 % de la population les moins bien dotés », 2022 à 2024, 3 points. Répartition `aplTenths` : les dix dixièmes de population en 2024 (`d1` le moins bien doté à `d10` le mieux doté) |
| Chiffre clé | 3,26 consultations par an et par habitant en 2024, en baisse après 3,29 en 2023 ; rapport 4,28 écrit à côté |
| Règles | Le script lit la seule feuille « Médecins généralistes », vérifie son titre (« APL moyen aux médecins généralistes », « par habitant standardisé »), son champ (« hors Mayotte »), la ligne des années et les onze libellés, et échoue sur une année manquante, une valeur hors de l'ordre de grandeur (moyenne 1,5 à 6, dixième 0,3 à 12, rapport 1 à 15) ou des dixièmes qui ne croissent pas. Valeurs telles que le fichier les écrit. Aucune commune, aucune carte (PO, 11/11/2026) : les moyennes nationales seulement |
| Première édition | À remplir à la publication |

## « À savoir »

1. Ce que compte l'APL, calculée commune par commune : « APL_Lisez-moi.pdf », pièce jointe du même jeu (« L'APL est un indicateur local, disponible au niveau de chaque commune, qui tient compte de l'offre et de la demande issues des communes environnantes. […] L'APL tient également compte du niveau d'activité des professionnels en exercice ainsi que de la structure par âge de la population de chaque commune qui influence les besoins de soins. ») ; l'unité : titre de la feuille (« consultations, visites et téléconsultations par habitant standardisé ») et lisez-moi (« il s'exprime dorénavant en nombre de consultations (ou visites) accessibles par an et par habitant »).
2. Méthode révisée, prudence sur l'évolution, champ : lisez-moi (« Plusieurs changements dans le calcul de ces indicateurs ont été introduits depuis la publication des données présentes dans le dossier « Méthode concertée V2 – 2015-2022 » » ; « La standardisation ainsi effectuée ne permet en revanche pas de comparer l'accessibilité entre deux millésimes en tenant compte de l'évolution des besoins en soins due au vieillissement global de la population. En conséquence, il faut être vigilant sur l'interprétation de l'évolution de l'accessibilité, en particulier sur de longues périodes ») ; champ de la feuille : « Médecins généralistes libéraux âgés de 65 ans ou moins et médecins généralistes salariés en centre de santé ; France hors Mayotte. »
3. Aucune part de la population en « désert médical » pour cette méthode ; « près de 6 % » en 2018 : lisez-moi, qui cite Blandine Legendre (DREES), « En 2018, les territoires sous-dotés en médecins généralistes concernent près de 6 % de la population », Études et Résultats n° 1144, février 2020, publication de la méthode « concertée V2 ». Le lisez-moi précise que « la population non standardisée doit être utilisée pour comptabiliser la population sous un seuil d'APL » : un tel calcul sur les communes n'est pas fait (PO, 11/11/2026).
4. « 4,1 fois » contre 4,28 : la note de lecture de la feuille écrit « Celle des 10 % les mieux dotés est de 5,65 consultations, visites ou téléconsultations par habitant, soit 4,1 fois plus que l'accessibilité moyenne des 10 % les moins dotés. », la dernière ligne du tableau 4,28 (5,65 / 1,32 = 4,28, calcul). La page de la DREES du 22/07/2026, relevée par l'agent du PO, écrit « 5,7, soit 4,3 fois supérieure ».

Les points en anglais disent la même chose que le français.

## Double vérification

Faite le 11/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans passer par la source du script : la presse et les diffuseurs qui citent la DREES ou l'Insee, les pages de l'Insee, le lisez-moi de l'APL. Le site principal de la DREES refuse les scripts (réponse vide, erreur 503) : ses pages, le Panorama et ses fichiers n'ont pu être vus que par des extraits de recherche, signalés comme tels.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, moyenne 2024 | 3,26 | « En 2024, l'accessibilité moyenne aux médecins généralistes en ville est de 3,3 consultations, téléconsultations ou visites à domicile par an et par habitant » ; « diminue de 1,1 % par rapport à 2023 » | https://www.infirmiers.com/profession-ide/infirmiers-medecins-generalistes-laccessibilite-recule-legerement-en-2024 ; page de la DREES du 22/07/2026 (extrait de recherche, et relevée par l'agent du PO) | Conforme à l'arrondi ; 3,26 / 3,29 = −0,9 % (calcul) quand la DREES écrit −1,1 %, sans doute sur des valeurs non arrondies |
| Moyennes 2022 et 2023 | 3,34 ; 3,29 | 2022 : « 3,3 consultations » (page de la DREES de novembre 2023, résumé du moteur) | recherche | Conforme à l'arrondi pour 2022 ; 2023 non trouvé hors du fichier |
| 10 % les mieux dotés, 2024 | 5,65 | « 5,7 consultations par an et par habitant » | infirmiers.com | Conforme à l'arrondi |
| 10 % les moins bien dotés, 2024 | 1,32 | « 1,3 » (page de la DREES du 22/07/2026, relevée par l'agent du PO) | compte rendu du PO | Conforme à l'arrondi |
| Rapport, 2024 | 4,28 | « 4,3 fois supérieure » ; « augmente de 5,3 % par rapport à 2023 » (4,28 / 4,07 = +5,2 %, calcul) | infirmiers.com | Conforme. La note de lecture du fichier écrit « 4,1 fois » (lue par Claude dans le fichier) : la note 4 le dit |
| Définition de l'APL | note 1 | « L'APL […] tient compte de l'offre et de la demande issues des communes environnantes » ; « du niveau d'activité des professionnels en exercice ainsi que de la structure par âge de la population de chaque commune » | APL_Lisez-moi.pdf (pièce jointe du jeu) | Conforme |
| Méthode révisée, prudence | note 2 | Les quatre changements du lisez-moi ; « il n'est pas recommandé d'analyser l'évolution de l'indicateur d'APL (…) en particulier sur de longues périodes » (page de la DREES, citée par infirmiers.com) | lisez-moi ; infirmiers.com | Conforme. La note disait « d'une année à l'autre » : corrigée en « surtout sur de longues périodes » |
| Champ | note 2 | « Médecins généralistes libéraux âgés de 65 ans ou moins et médecins généralistes salariés en centre de santé ; France hors Mayotte. » (feuille du fichier) ; « excluant les cabinets localisés à Mayotte » (lisez-moi) | fichier ; lisez-moi | Conforme |
| « Près de 6 % » en 2018 | note 3 | « En 2018, les territoires sous-dotés en médecins généralistes concernent près de 6 % de la population » (ER n° 1144, février 2020), méthode « concertée V2 » | lisez-moi ; https://drees.solidarites-sante.gouv.fr/sites/default/files/er1144.pdf (titre vu) | Conforme |
| Aucune part en « désert médical » pour la méthode actuelle | note 3 | Ni confirmé ni contredit : aucune publication de 2026 trouvée | recherche ; page de la DREES du 22/07/2026 relevée par l'agent du PO (3,3, −1,1 %, 1,3, 5,7, 4,3 : pas de part de population) | Non trouvé, cohérent |
| Licence | Licence Ouverte 2.0 | « Licence Ouverte v2.0 (Etalab) », modifié le 2026-07-22 | métadonnées du jeu | Conforme |

**Conclusion.** Les chiffres de 2024 sont ceux que la DREES écrit, arrondis ; la note sur l'évolution suit maintenant les mots de la DREES.

**Pages consultées** (le 11/11/2026) :

- https://www.infirmiers.com/profession-ide/infirmiers-medecins-generalistes-laccessibilite-recule-legerement-en-2024
- https://data.drees.solidarites-sante.gouv.fr/api/datasets/1.0/530_l-accessibilite-potentielle-localisee-apl/attachments/apl_lisez_moi_pdf (APL_Lisez-moi.pdf)
- https://data.drees.solidarites-sante.gouv.fr/api/explore/v2.1/catalog/datasets/530_l-accessibilite-potentielle-localisee-apl/ (métadonnées, licence)
- https://drees.solidarites-sante.gouv.fr/communique-de-presse-jeux-de-donnees/jeux-de-donnees/260722-accessibilite-aux-soins-de-premier-recours-en-2024 : non ouverte ici (extrait de recherche) ; relevée par l'agent du PO le 11/11/2026

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
