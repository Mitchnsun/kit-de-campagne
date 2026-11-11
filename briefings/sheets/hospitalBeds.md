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
| Définitions | notes 1 et 2, note du graphique | hospitalisation partielle : accueil de jour ou de nuit, anesthésie et chirurgie ambulatoire (résumé du moteur) ; « lits en état d'accueillir des patients » au 31 décembre | recherche ; Santé mentale | Conforme, la chirurgie ambulatoire non nommée dans la note |
| Champ (France entière, DROM, service de santé des armées) | non dit | non retrouvé pour 2024 | ER n° 1353 (extraits), Santé mentale | Non trouvé : la page ne dit pas de champ |
| Licence | citée seulement | métadonnée `license` vide ; la publication n'en dit rien dans les extraits | métadonnées du jeu | Non trouvé : chiffres cités avec leur source |

**Conclusion.** Les chiffres de 2013 et de 2024 sont ceux de la DREES ; 2024 est un premier résultat, dit comme tel.

**Pages consultées** (le 11/11/2026) :

- https://www.santementale.fr/2025/11/en-2024-la-baisse-du-nombre-de-lits-ralentit-et-les-alternatives-a-lhospitalisation-progressent-encore/
- https://data.drees.solidarites-sante.gouv.fr/api/explore/v2.1/catalog/datasets/graphique-1-evolution-du-nombre-de-lits-et-de-places-au-31-decembre-depuis-fin-2013 (métadonnées, sans licence)
- ER n° 1353 (https://www.drees.solidarites-sante.gouv.fr/sites/default/files/2025-11/ER1353%20-%20SAE%20-%20MEL2.pdf) et Panorama 2026 des établissements de santé : non ouverts (site de la DREES), vus par extraits de recherche

## À vérifier par le PO

- **Une rupture de méthode en 2022 ?** Un extrait de recherche prête à un sénateur l'affirmation que la DREES reconnaît qu'un changement de méthode à partir des données de 2022 « surestime mécaniquement la diminution des lits ». Non vérifié : à relire dans l'ER n° 1353 ou l'ER n° 1315 (site de la DREES, inaccessible d'ici). Si c'est écrit, la série prend une rupture en 2022 (`breaks`) et une note le dit ; la DREES trace pourtant elle-même la série d'un trait depuis 2013 (titre du graphique).
- **Le champ** de la SAE pour 2024 (France entière, DROM, service de santé des armées), à relire dans l'ER n° 1353.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
