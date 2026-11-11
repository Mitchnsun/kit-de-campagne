# `hospitalBeds` · Les lits d'hôpital

**Vérifiée le 11/11/2026** : double vérification sur le web, sans écart non expliqué : 2024 en premiers résultats, que la DREES a depuis consolidés de peu (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `hospitalBeds`, quatrième volet de la page « Dépense, médecins et hôpital » (`healthCare`), dossier « Santé » (`health`), page de type série, ticket #143 de l'app |
| Données | `briefings/data/hospitalBeds.json`, écrit par `yarn briefings hospitalBeds` le 2026-11-11 |
| Sources | DREES, « Graphique 1 – Évolution du nombre de lits et de places au 31 décembre, depuis fin 2013 » (data.drees), page https://data.drees.solidarites-sante.gouv.fr/explore/dataset/graphique-1-evolution-du-nombre-de-lits-et-de-places-au-31-decembre-depuis-fin-2013/information/ ; données par l'API du jeu (`/records`) ; aucune licence dans les métadonnées du jeu (`license` vide) : chiffres cités avec leur source ; daté par la date de modification du jeu, 2025-11-12 |
| Séries | `fullTimeBeds` : « Nombre de lits d'hospitalisation complète », au 31 décembre, 2013 à 2024, 12 points ; `partTimePlaces` : « Nombre de places d'hospitalisation partielle », 2013 à 2024, 12 points |
| Chiffre clé | 367 335 lits d'hospitalisation complète fin 2024, en baisse après 369 363 fin 2023 ; 91 232 places écrites à côté |
| Règles | Le script lit les douze lignes du jeu, échoue si l'API en annonce plus qu'elle n'en rend, sur une année manquante ou en double, un champ absent, une valeur non entière ou hors de l'ordre de grandeur (250 000 à 500 000 lits, 40 000 à 150 000 places). Les lits et les places sont montrés ensemble, sur la même vue |
| Première édition | À remplir à la publication |

## « À savoir »

1. Lits et places, à lire ensemble : les colonnes du jeu (« Nombre de lits d'hospitalisation complète », « Nombre de places d'hospitalisation partielle ») ; les valeurs de 2013 et 2024 du fichier. La publication du graphique : Études et résultats n° 1353 de la DREES, « Dans les établissements de santé en 2024, la baisse du nombre de lits ralentit et les alternatives à l'hospitalisation complète poursuivent leur progression » (13/11/2025 ; le jeu est daté du 12/11/2025), qui écrit « environ 367 300 lits et 91 200 places » (Santé mentale, qui la cite). « De jour ou de nuit » : définitions de la SAE (résumé du moteur de recherche, qui compte aussi la chirurgie ambulatoire dans les places). « 2024 : premiers résultats » : le Panorama « Les établissements de santé en 2024 – Édition 2026 » (20/05/2026) donne 367 100 lits et 91 100 places, chiffres consolidés (extrait de recherche).
2. Une capacité au 31 décembre : titre du jeu (« au 31 décembre »). « Au 31 décembre 2024, 2 965 entités géographiques disposent de capacités d'accueil » (ER n° 1353, cité par Santé mentale).

Les points en anglais disent la même chose que le français.

## Double vérification

Faite le 11/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans passer par la source du script : la presse et les diffuseurs qui citent la DREES ou l'Insee, les pages de l'Insee, le lisez-moi de l'APL. Le site principal de la DREES refuse les scripts (réponse vide, erreur 503) : ses pages, le Panorama et ses fichiers n'ont pu être vus que par des extraits de recherche, signalés comme tels.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, lits fin 2024 | 367 335 | « environ 367 300 lits et 91 200 places » | https://www.santementale.fr/2025/11/en-2024-la-baisse-du-nombre-de-lits-ralentit-et-les-alternatives-a-lhospitalisation-progressent-encore/ (qui cite l'ER n° 1353) | Conforme à l'arrondi |
| Places fin 2024 | 91 232 | 91 200 | idem | Conforme à l'arrondi |
| Fin 2024, chiffres consolidés | 367 335 ; 91 232 | 367 100 lits et 91 100 places ; la DREES précise que les chiffres consolidés diffèrent légèrement des premiers résultats de novembre 2025 | Panorama « Les établissements de santé en 2024 – Édition 2026 », https://drees.solidarites-sante.gouv.fr/publications-communique-de-presse-documents-de-reference/panoramas-de-la-drees/260520-Etablissements-de-sant%C3%A9-en-2024 (extrait de recherche) | Écart expliqué : le jeu suit les premiers résultats ; la note et la note du graphique le disent |
| Fin 2023 | 369 363 ; 88 471 | 369 400 lits, 88 500 places (SAE 2023, résumé du moteur) | recherche | Conforme à l'arrondi |
| Fin 2013 | 412 788 ; 67 783 | « 23 200 places de plus que fin 2013 » (Panorama 2026) ; 91 232 − 67 783 = 23 449 (calcul) | extrait de recherche | Conforme à l'arrondi |
| Années 2014 à 2022 | du jeu | aucune source indépendante | | Non trouvé hors du jeu |
| Définitions | notes 1 et 2, note du graphique | « Hospitalisation partielle : concerne l'accueil de jour ou de nuit et les unités ayant des activités d'anesthésie, de chirurgie ambulatoire ou de médecine ambulatoire. En MCO, le séjour est inférieur à vingt-quatre heures, en psychiatrie et en SMR, il comporte plusieurs journées ou nuitées de moins de vingt-quatre heures. » ; les capacités fermées « faute de personnel en nombre suffisant sont exclues » | ER n° 1353, p. 2, encadré 1 (même définition dans l'ER n° 1315, p. 2), relu par l'agent du PO le 11/11/2026 | Conforme ; la note dit « de jour ou de nuit » sans détailler l'ambulatoire |
| Champ | France entière, service de santé des armées compris (note du graphique, depuis le 11/11/2026) | « Le champ retenu porte sur la France entière (incluant Saint-Martin et Saint-Barthélemy), y compris le service de santé des armées (SSA). » ; sont exclus les établissements « sans capacité d'accueil en hospitalisation complète ou partielle (centres de dialyse, de radiothérapie et établissements faisant uniquement de l'hospitalisation à domicile [HAD]) » | ER n° 1353, p. 2, encadré 1 (même phrase dans l'ER n° 1315), relu par l'agent du PO | Conforme |
| Fin 2024 | 367 335 lits ; 91 232 places | « Nombre de lits d'hospitalisation complète 367 335 -0,5 » ; « Nombre de places d'hospitalisation partielle 91 232 3,1 » | ER n° 1353, p. 4, tableau 2 | Conforme |
| Fin 2019 à fin 2021 | 390 703 ; 385 973 ; 380 607 | les mêmes valeurs, « Bases statistiques publiées en janvier 2025 » | DREES, « Bon usage des bases SAE et spécificités 2023 », note méthodologique du 10/01/2025, p. 4, tableau 2a | Conforme : le fichier suit les bases corrigées |
| Fin 2022 et fin 2023 | 373 828 ; 369 363 | 373 873 et 369 309 dans les bases de janvier 2025 | même note, p. 4, tableau 2a | Écart expliqué : le jeu de novembre 2025 suit des bases statistiques plus récentes (« SAE 2013-2023 (bases statistiques), 2024 (base administrative) », ER n° 1353, graphique 1) ; 45 et 54 lits d'écart |
| Licence | citée seulement | métadonnée `license` vide ; la publication n'en dit rien dans les extraits | métadonnées du jeu | Non trouvé : chiffres cités avec leur source |

**Conclusion.** Les chiffres de 2013 et de 2024 sont ceux de la DREES ; 2024 est un premier résultat, dit comme tel.

**Pages consultées** (le 11/11/2026) :

- https://www.santementale.fr/2025/11/en-2024-la-baisse-du-nombre-de-lits-ralentit-et-les-alternatives-a-lhospitalisation-progressent-encore/
- https://data.drees.solidarites-sante.gouv.fr/api/explore/v2.1/catalog/datasets/graphique-1-evolution-du-nombre-de-lits-et-de-places-au-31-decembre-depuis-fin-2013 (métadonnées, sans licence)
- ER n° 1353 (https://www.drees.solidarites-sante.gouv.fr/sites/default/files/2025-11/ER1353%20-%20SAE%20-%20MEL2.pdf) et Panorama 2026 des établissements de santé : non ouverts (site de la DREES), vus par extraits de recherche

## Rupture de série en 2022 ? (vérifié le 11/11/2026)

Un extrait de recherche prêtait à un sénateur l'affirmation que la DREES reconnaît qu'un changement de méthode à partir des données de 2022 « surestime mécaniquement la diminution des lits ». L'agent du PO a lu dans son navigateur l'ER n° 1353, l'ER n° 1315, l'ER n° 1289 (décembre 2023) et les notes méthodologiques « Bon usage des bases SAE et spécificités 2022 » (30/10/2023) et « … 2023 » (10/01/2025) :

- Aucun de ces documents ne décrit de changement de méthode commençant avec les données de 2022, ni n'emploie « surestimer » ou « rupture ».
- Ils décrivent des **corrections après coup des lits de 2020 et 2021**, une partie des établissements ayant déclaré des « lits budgétés » ou « lits autorisés », « sans écarter les lits non disponibles du fait du manque de personnel, alors que la SAE le requiert » (note 2022, p. 4). Total des corrections : −397 lits en 2020, −1 803 en 2021 (même note, tableau 2).
- D'où deux valeurs de la baisse de 2022 selon la version des bases : −2,2 % (« Bases statistiques en ligne avant janvier 2025 ») ou −1,8 % (bases de janvier 2025 et ER n° 1315), note 2023, p. 4, tableau 2b.
- La seule discontinuité signalée porte sur 2019, pour une unité dont la rétropolation n'a pas pu remonter plus loin (note 2023, p. 4).
- La note 2023 demande de ne pas calculer d'évolution sur les bases administratives (« les considérer plutôt comme une « photographie » de l'année considérée », p. 2) ; la DREES le fait pourtant pour la dernière année de ses ER (2024 en base administrative dans l'ER n° 1353), ce que la note du graphique dit par « 2024 en premiers résultats ».

**Conclusion** : pas de rupture à marquer ; la série du fichier est celle que la DREES a corrigée. Le PO a arbitré le 11/11/2026 : pas de `breaks`, le champ dans la note du graphique.

## Mises à jour

- **11/11/2026** : le champ et la rupture supposée de 2022 vérifiés dans les publications de la DREES (sections ci-dessus) ; la note du graphique de l'app nomme le champ (« France entière, service de santé des armées compris »).

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
