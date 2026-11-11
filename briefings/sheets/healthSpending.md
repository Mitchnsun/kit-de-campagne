# `healthSpending` · La dépense de santé

**Vérifiée le 11/11/2026** : double vérification sur le web, sans écart sur 2025 ; la série de l'édition 2026 diffère de celle des éditions précédentes (écart expliqué en partie, section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `healthSpending`, premier volet de la page « Dépense, médecins et hôpital » (`healthCare`, page à volets), dossier « Santé » (`health`), page de type comparaison, ticket #143 de l'app |
| Données | `briefings/data/healthSpending.json`, écrit par `yarn briefings healthSpending` le 2026-11-11 |
| Sources | DREES, « Les comptes de la santé - Répartition par financeur » (data.drees, jeu `cns_financement`), page https://data.drees.solidarites-sante.gouv.fr/explore/dataset/cns_financement/information/ ; données https://data.drees.solidarites-sante.gouv.fr/api/explore/v2.1/catalog/datasets/cns_financement/exports/json ; Licence Ouverte v2.0 (Etalab), que les métadonnées du jeu citent, avec l'obligation de mentionner la source ; daté par la date de modification du jeu, 2026-10-01 |
| Séries | `dcsi` : dépense courante de santé au sens international (DCSi), tous financeurs, en milliards d'euros courants, poste `d00000`, 2010 à 2025, 16 points ; `csbm` : consommation de soins et de biens médicaux (CSBM), poste `p00000`, 2010 à 2025, 16 points. Répartitions de 2025 : `dcsiByFunder` (Sécurité sociale `f110`, administrations publiques centrales et locales `f120`, organismes complémentaires `f210`, ménages `f220`, entreprises `f300`) et `csbmByFunder` (les mêmes sans les entreprises) |
| Chiffre clé | 353,2 Md€ de DCSi en 2025 (353,185), en hausse après 342,0 Md€ en 2024 ; CSBM 256,5 Md€ |
| Règles | Le script lit tout le jeu (3 504 lignes), garde les postes `d00000` et `p00000`, vérifie leurs libellés et ceux des financeurs, et échoue sur une année manquante ou en double, des années différentes entre les deux postes, un montant hors de l'ordre de grandeur (DCSi entre 150 et 600 Md€, CSBM entre 100 et 450 Md€, CSBM sous la DCSi chaque année), et des financeurs dont la somme s'écarte du total de plus de 0,01 Md€. Montants arrondis au million d'euros. Le jeu ne marque aucune année provisoire : aucun statut. La DCSi et la CSBM ne sont jamais additionnées : chacune a sa vue, et la note de lecture le dit |
| Première édition | À remplir à la publication |

## « À savoir »

1. La DCSi sert aux comparaisons entre pays ; la CSBM en est la principale partie, 256,5 Md€ sur 353,2 Md€ en 2025 ; les deux ne s'additionnent pas. Sources : le jeu `cns_financement` lui-même (poste `p00000` de niveau 1 sous `d00000` de niveau 0 ; `q00000` « DCSi hors CSBM ») ; page de présentation des comptes de la santé, édition 2026 (01/10/2026), relevée par l'agent du PO le 11/11/2026 : « Principal agrégat de la DCSi, la consommation de soins et de biens médicaux (CSBM) atteint 256,5 milliards d'euros en 2025. » et « En 2025, la dépense courante de santé au sens international (DCSi) s'élève à 353,2 milliards d'euros. »
2. 9,7 % de la DCSi financés par les ménages en 2025, après 9,8 % en 2024, et 495 € de reste à charge par habitant, sur toute la DCSi : même page (« La part des dépenses financée par les ménages recule un peu en 2025, à 9,7 %, après 9,8 % en 2024. » ; « Au total, le reste à charge des ménages s'établit en 2025 à 495 euros par habitant. » ; « L'opposition entre la DCSi et la CSBM, structurante dans les éditions précédentes, disparaît, la CSBM apparaissant comme une composante de la DCSi. »). Recoupement par calcul sur le fichier : 34,097 / 353,185 = 9,65 %, arrondi à 9,7 % ; 33,41 / 342,04 = 9,77 %, arrondi à 9,8 % (calculs, non écrits dans les notes).
3. Euros courants, et la série de 2010 à 2025 de l'édition 2026, qui diffère des précédentes : le jeu ne donne que des montants en euros (champ `montant`), de 2010 à 2025, modifié le 01/10/2026 ; « L'édition 2026 se distingue par un changement de focale par rapport aux éditions précédentes » (Hospitalia, qui cite la DREES) ; pour 2024, l'édition 2025 donnait 332,6 Md€ de DCSi et 254,8 Md€ de CSBM (vie-publique.fr, résumé du moteur de recherche), l'édition 2026 342,0 et 249,7 (voir « Double vérification »).

Les points en anglais disent la même chose que le français.

## Double vérification

Faite le 11/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans passer par la source du script : la presse et les diffuseurs qui citent la DREES ou l'Insee, les pages de l'Insee, le lisez-moi de l'APL. Le site principal de la DREES refuse les scripts (réponse vide, erreur 503) : ses pages, le Panorama et ses fichiers n'ont pu être vus que par des extraits de recherche, signalés comme tels.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, DCSi 2025 | 353,185 Md€ | « En 2025, la dépense courante de santé au sens international (DCSi) s'élève à 353,2 milliards d'euros » | https://www.hospitalia.fr/DREES-les-depenses-de-sante-en-2025-Resultats-des-comptes-de-la-sante-Edition-2026_a5269.html ; https://www.omedit-idf.fr/veille/les-depenses-de-sante-en-2025-panorama-de-la-drees/ | Conforme |
| CSBM 2025 | 256,452 Md€ | « la consommation de soins et de biens médicaux (CSBM) atteint 256,5 milliards d'euros en 2025 » | Hospitalia ; https://www.echangesassurances.org/actualites/depenses-sante-2025-drees-complementaires | Conforme |
| Ménages, DCSi 2025 | 34,097 Md€ | « le reste à charge des ménages atteint 34,1 milliards d'euros » | https://selectra.info/assurance/actualites/marche/reste-a-charge-sante-495-euros-drees | Conforme |
| Organismes complémentaires, DCSi 2025 | 43,389 Md€ | « 43,4 milliards d'euros », soit 12,3 % ; 33,5 Md€ sur la CSBM | Selectra | Conforme |
| Ménages, CSBM 2025 | 19,691 Md€ | « le reste à charge tombe à 19,7 milliards d'euros » sur les soins et biens médicaux | Selectra | Conforme |
| Administrations publiques (Sécurité sociale et administrations centrales et locales), DCSi 2025 | 249,223 + 24,284 = 273,507 Md€ (calcul) | « se maintient à 77,4 % » ; 273,507 / 353,185 = 77,44 % (calcul) | Hospitalia ; Échanges assurances | Conforme (la part, pas les montants) |
| Sécurité sociale, autres administrations, entreprises, pris un à un | 249,2 ; 24,3 ; 2,2 Md€ (DCSi), 201,6 ; 1,7 (CSBM) | Aucune source tierce ne les donne ; les financeurs de chaque poste font son total (calcul : 353,187 et 256,452) | presse citée, OMEDIT, Meilleurtaux, MoneyVox, JeChange | Non trouvé (le script vérifie que leur somme fait le total) |
| Part des ménages et reste à charge | 9,7 % (2025), 9,8 % (2024), 495 € par habitant (notes) | « la part financée par les ménages passe à 9,7 % en 2025, contre 9,8 % en 2024 » ; « le reste à charge des ménages s'établit en 2025 à 495 euros par habitant » | Hospitalia ; https://www.meilleurtaux.com/comparateur-assurance/mutuelle-sante/actualites/2026-octobre/sante-qui-finance-les-353-2-mdeur-depenses-en-2025.html | Conforme |
| Reste à charge, non comparable aux éditions précédentes | note 2 | « Ne comparez pas ces 495 € au chiffre par habitant mis en avant dans l'édition précédente de la Drees » ; « L'opposition entre la DCSi et la CSBM, structurante dans les éditions précédentes, disparaît » | Selectra ; Hospitalia | Conforme |
| DCSi et CSBM 2024 | 342,042 et 249,698 Md€ | Édition 2025 : 332,6 Md€ de DCSi (« 333 milliards ») et 254,8 Md€ de CSBM pour 2024. Calcul : 353,185 / 342,042 = +3,3 %, comme la hausse de 2025 que la presse cite | https://www.vie-publique.fr/en-bref/300320-des-depenses-de-sante-en-augmentation-de-36-en-2024 (résumé du moteur) | Écart expliqué en partie : l'édition 2026 révise la série et change de présentation ; la cause du détail n'est pas trouvée. La note 3 dit que ses montants ne se comparent pas aux éditions précédentes |
| Composition de la DCSi | note 1 et note du bloc | Le jeu : `q00000` « DCSi hors CSBM », fait de `q10000` « Soins de longue durée », `q20000` « Prévention », `q30000` « Gestion du système de santé » ; glossaire des comptes (résumé du moteur, non ouvert) | jeu `cns_financement` | Conforme |
| Licence | Licence Ouverte 2.0 | « Licence Ouverte v2.0 (Etalab) » | métadonnées du jeu `cns_financement` | Conforme |

**Conclusion.** Les chiffres de 2025 sont ceux que la presse cite de la DREES ; la série de l'édition 2026 diffère des éditions précédentes, ce que la note 3 dit.

**Pages consultées** (le 11/11/2026) :

- https://www.hospitalia.fr/DREES-les-depenses-de-sante-en-2025-Resultats-des-comptes-de-la-sante-Edition-2026_a5269.html
- https://selectra.info/assurance/actualites/marche/reste-a-charge-sante-495-euros-drees
- https://www.echangesassurances.org/actualites/depenses-sante-2025-drees-complementaires
- https://www.omedit-idf.fr/veille/les-depenses-de-sante-en-2025-panorama-de-la-drees/
- https://www.meilleurtaux.com/comparateur-assurance/mutuelle-sante/actualites/2026-octobre/sante-qui-finance-les-353-2-mdeur-depenses-en-2025.html
- https://www.jechange.fr/assurance/mutuelle-sante/news/reste-a-charge-sante-495-euros-207-euros-soins-longue-duree-mutuelle
- https://www.moneyvox.fr/assurance/actualites/110626/depenses-de-sante-menages-mutuelles-securite-sociale-qui-paie-quoi
- vie-publique.fr (édition 2025) et la page du Panorama de la DREES du 01/10/2026 : vues seulement dans les résultats de recherche ; la page de la DREES relevée par l'agent du PO le 11/11/2026 (citations des notes 1 et 2)

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
