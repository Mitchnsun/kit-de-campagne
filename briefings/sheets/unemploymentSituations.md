# `unemploymentSituations` · Chômeurs, halo, sous-emploi et inscrits (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart de valeur ; réserves de lecture reprises dans les notes des blocs, dans « À savoir » et dans le « À savoir » lu en premier. Les valeurs du 2e trimestre 2026 sont celles que l'Insee publie au 09/11/2026 ; il publie le 3e trimestre 2026 le 10/11/2026 à 7 h 30, et la prochaine édition les remplacera. La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `unemploymentSituations`, dossier « Travail et retraites » (`work`), volet « Situations » de la page composite `unemploymentBeyond` (voir `unemploymentBeyond.md`), page de type comparaison, recherche du 09/11/2026 |
| Données | `briefings/manual/unemploymentSituations.json`, saisi à la main le 2026-11-09 depuis l'IR n° 192 de l'Insee (texte et tableau ; identifiants de la BDM relus par la recherche et la contre-vérification), la note Dares Indicateurs n° 47 (page STMT de France Travail), le dossier D1 et la fiche F9 de l'ECRT 2026 de l'Insee |
| Sources | 1. Insee, « Au deuxième trimestre 2026, le taux de chômage augmente de 0,2 point et atteint 8,3 %, Informations rapides n° 192 », https://www.insee.fr/fr/statistiques/9032359, données https://www.insee.fr/fr/statistiques/serie/011818555 ; 2. Insee, « Une photographie du marché du travail en 2025, Insee Première n° 2096 », encadré « Définitions », https://www.insee.fr/fr/statistiques/8901327 ; 3. France Travail, Dares, « Les inscrits à France Travail au 3e trimestre 2026, Dares Indicateurs n° 47 », https://statistiques.francetravail.org/stmt/publication ; 4. Insee, « Le nombre de chômeurs au sens du BIT et des inscrits à France Travail en catégorie A : l'écart s'est réduit entre 2021 et 2024 mais demeure élevé », dossier de l'ECRT 2026, https://www.insee.fr/fr/statistiques/8733119 (PDF https://www.insee.fr/fr/statistiques/fichier/8733119/ECRT2026-D1.pdf) ; 5. Insee, « Inégalités face au chômage », fiche de l'ECRT 2026, figure 3, https://www.insee.fr/fr/statistiques/8733055. Licence `etalab-2.0` pour l'Insee (1, 2, 4, 5 ; Insee Première 2096 porte « Reproduction partielle autorisée sous réserve de la mention de la source et de l'auteur »), « citation seule » pour France Travail et la Dares (3 : aucune licence lue). Toutes en français seulement |
| Dates de publication | 2026-08-07 (IR n° 192, « Paru le 07/08/2026 ») ; 2026-03-25 (Insee Première n° 2096) ; 2026-10-28 (publication STMT du 3e trimestre 2026, la date de la même source dans le fichier de la page « Chômage », et mise à jour de la BDM ; la recherche écrit « octobre 2026 ») ; 2026-07-02 (ECRT 2026, dossier D1 et fiche F9) |
| Séries | Toutes trimestrielles, CVS, un seul point, 2026-T2, France (Mayotte comprise, séries rétropolées par l'Insee), personnes de 15 ans ou plus en logement ordinaire, IR n° 192 : `unemployed` chômeurs au sens du BIT, 2 677 000 (BDM `011818555`) ; `halo` halo autour du chômage, 1 865 000, 15 ans ou plus (`011818564`) ; `underemployed` sous-emploi, 1 296 000 (`011818739`) ; `longTermUnemployed` chômeurs de longue durée, 671 000 (`011818577`) ; `unemploymentRate` taux de chômage, 8,3 % des actifs (`011818543`) ; `haloShare` part du halo, 4,4 % de la population des 15-64 ans (`011818623`) ; `underemploymentShare` part du sous-emploi, 4,4 % des personnes en emploi (`011818670`) ; `longTermRate` taux de chômage de longue durée, 2,1 % des actifs (`011818581`) |
| Ventilations | `registeredByCategory` : moyenne du 3e trimestre 2026, France hors Mayotte (A à E CVS-CJO, F et G bruts), Dares Indicateurs n° 47 : catégorie A 3 353 400 ; A, B, C 5 847 500 ; A à E 6 587 600 ; F 597 000 ; G 386 100. `categoryABitStatus` : moyenne 2024, France hors Mayotte, 15-64 ans, dossier D1 : parmi les inscrits en catégorie A, chômeurs au sens du BIT 49 %, inactifs dans le halo 25 %, inactifs hors du halo 17 %, en emploi 8 %. `lastJobEnd` : moyenne 2025, France, chômeurs de tous âges, fiche F9 : fin d'un emploi à durée limitée 47,0 %, licenciement 9,5 %, rupture conventionnelle 8,4 %, démission 6,7 %, jamais travaillé 11,5 % |
| Chiffre clé | 2 677 000 chômeurs au sens du BIT au 2e trimestre 2026, sans tendance (un seul point dans le fichier ; l'Insee écrit + 62 000 sur le trimestre, non saisi) ; à côté, le halo, 1 865 000 |
| Règles | Saisie à la main. Trois vues : les quatre situations en nombre puis en part, chaque part nommée avec sa population, sans tableau ; les inscrits par catégorie (avec un tableau), puis les inscrits en A selon le BIT ; la fin du dernier emploi (avec un tableau). Les définitions de l'Insee sont dans la note du bloc des nombres ; celles des catégories dans la note des inscrits, d'après la note de la Dares : A, B, C « tenus de rechercher un emploi », A « sans emploi », B et C « en activité réduite », A à E « ni en attente d'orientation ni en parcours social » (D et E sont donc inscrits sans être tenus de rechercher un emploi), F « parcours social », G « attente d'une orientation par le réseau pour l'emploi ». Les catégories D et E ne sont pas détaillées davantage (formation, maladie… : lus par la recherche dans la fiche F10 de l'ECRT, non retenue comme source). La part de 25,1 % (671 000 / 2 677 000) et les sommes de 99 % (49 + 25 + 17 + 8) et 83,1 % (les cinq circonstances) sont des calculs, dans les notes avec « calculé ». Les 17,2 % de personnes contraintes dans leur offre de travail (autre dénominateur : actifs ou dans le halo, 15-64 ans) sont dans la note du bloc des parts, pas en barre. Non saisis : les chômeurs par âge (740 000 de 15-24 ans : page des jeunes), la moyenne 2025 (2 451 000 chômeurs, fiche F8, non retenue), les 23,1 % de chômeurs de longue durée en 2025 (fiche F8), le temps partiel (17,8 %) et la durée du travail (31,1 heures, IR n° 192 : hors des vues demandées) |
| Première édition | À remplir à la publication |

## « À savoir »

1. Les chômeurs au sens du BIT (Insee, 2e trimestre 2026, France entière) et les inscrits à France Travail (Dares, 3e trimestre 2026, hors Mayotte) n'ont ni la même définition, ni la même période, ni le même champ : on ne retranche pas les uns des autres, et un inscrit n'est pas forcément chômeur au sens du BIT. Sources : IR n° 192 (champ « France ») ; Dares Indicateurs n° 47 (« en France hors Mayotte ») ; dossier D1 (« Un individu inscrit en catégorie A peut ne pas être chômeur au sens du BIT, par exemple lorsqu'il n'a pas recherché d'emploi au cours d'un mois donné »). Précaution du rapport final (`inscritsFranceTravail` : « ne pas les soustraire »).
2. Le nombre du halo compte les personnes de 15 ans ou plus, sa part les 15-64 ans : ils n'ont pas la même base. Le sous-emploi se rapporte aux personnes en emploi, le chômage et le chômage de longue durée aux actifs : ces parts ne s'additionnent pas et ne se comparent pas. Sources : IR n° 192 (« Parmi les personnes inactives au sens du BIT, 1,9 million souhaitent un emploi » ; « La part du halo dans la population des 15-64 ans [...] à 4,4 % » ; « 4,4 % des personnes en emploi sont en situation de sous-emploi » ; « 2,1 % de la population active ») ; Insee Première n° 2096 (« Le taux de chômage est le rapport entre le nombre de chômeurs et le nombre d'actifs »).
3. Les 671 000 chômeurs de longue durée sont comptés parmi les 2 677 000 chômeurs, dont ils font un quart (25,1 %, calculé). Le halo, des inactifs qui souhaitent travailler, et le sous-emploi, des personnes en emploi, sont hors des chômeurs. Sources : IR n° 192 (« Parmi les chômeurs, 671 000 personnes [...] ») ; calcul du rapport final (671 000 / 2 677 000 = 25,1 %) ; Insee Première n° 2096 (définitions du halo, « personnes sans emploi », et du sous-emploi, « personnes ayant un emploi à temps partiel »).
4. En 2024, selon l'Insee, 65 % des moins de 25 ans au chômage ou dans le halo ne sont pas inscrits à France Travail, contre un peu plus de 20 % de leurs aînés. Source : dossier D1, encadré 3 (« 65 % des jeunes de moins de 25 ans au chômage ou dans le halo ne sont pas inscrits à France Travail, contre un peu plus de 20 % de leurs aînés »).

Les quatre points en anglais disent la même chose que le français.

**Le « À savoir » lu en premier** (`readFirst` du volet, dans l'app) : un chômeur au sens du BIT et un inscrit à France Travail ne sont pas la même chose, comptés l'un par l'enquête Emploi, l'autre sur les listes de France Travail, et les deux ne se recouvrent qu'en partie (dossier D1 : « A contrario, un chômeur au sens du BIT peut ne pas être inscrit en catégorie A ») ; le taux de chômage ne compte ni le halo ni le sous-emploi (définitions de l'Insee Première n° 2096 : le halo est fait d'inactifs, le sous-emploi de personnes en emploi).

**Notes des blocs** (dans l'app) : les définitions de l'Insee (Insee Première n° 2096 : « Un chômeur au sens du Bureau international du travail (BIT) est une personne âgée de 15 ans ou plus qui répond simultanément à trois conditions [...] » ; halo, sous-emploi, chômage de longue durée) ; les 17,2 % de l'IR n° 192 (« 17,2 % des participants au marché du travail (personnes actives ou dans le halo autour du chômage) se trouvent contraints dans leur offre de travail ») ; les catégories et l'inscription automatique depuis janvier 2025 (page STMT : « les demandeurs et bénéficiaires du RSA, les jeunes en recherche d'emploi suivis par les missions locales, les personnes en situation de handicap suivies par Cap emploi sont systématiquement inscrits à France Travail à compter de janvier 2025 », relue le 09/11/2026 ; la page « Chômage » le dit aussi) ; les phrases de l'Insee sur l'écart (dossier D1 : « Le seul fait d'être inscrit sur les listes de France Travail n'est en effet pas considéré en soi comme une démarche active de recherche d'emploi au regard des critères du BIT » ; « Parmi les chômeurs au sens du BIT, en 2024, 62 % sont inscrits dans la catégorie A quand 23 % ne sont pas inscrits à France Travail ») ; les licenciements « dont un peu moins de la moitié pour motif économique » (fiche F9).

## Ce qu'on entend

Aucune affirmation : voir `unemploymentBeyond.md`.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-jeunes.md` : séries de la BDM retéléchargées par l'API SDMX, PDF lus avec `pdftotext`, pages de l'Insee et de France Travail en texte brut.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 2 677 000 (2026-T2) | BDM `011818555` : 2677 (milliers) ; IR n° 192 : « Personnes au chômage [...] 2 677 » | IR n° 192 (URL ci-dessus) | Conforme |
| Halo, sous-emploi, chômage de longue durée | 1 865 000 ; 1 296 000 ; 671 000 | BDM `011818564` 1865, `011818739` 1296, `011818577` 671 ; phrases de l'IR recopiées | idem | Conforme ; le halo (15 ans ou plus) et sa part (15-64 ans) n'ont pas la même base |
| Parts | 8,3 ; 4,4 ; 4,4 ; 2,1 % | BDM `011818543` (relue pour la page « Chômage »), `011818623` 4.4, `011818670`, `011818581` 2.1 | idem | Conforme |
| Inscrits par catégorie | 3 353 400 ; 5 847 500 ; 6 587 600 ; 597 000 ; 386 100 | Dares Indicateurs n° 47 et BDM `010597456`, `010597571` (mise à jour 28/10/2026) ; F et G relus sur la page STMT à la saisie | Dares Indicateurs n° 47 (URL ci-dessus) | Conforme |
| Inscrits en A selon le BIT | 49 ; 25 ; 17 ; 8 % | « En moyenne en 2024, parmi les inscrits en catégorie A, 49 % sont au chômage au sens du BIT, 25 % sont inactifs dans le halo autour du chômage, 17 % sont inactifs hors du halo et 8 % sont en emploi. » | dossier D1 (PDF ci-dessus) | Conforme ; catégorie A seule, année 2024, France hors Mayotte |
| Fin du dernier emploi | 47,0 ; 9,5 ; 8,4 ; 6,7 ; 11,5 % | phrase de la fiche recopiée ; relue sur la page à la saisie | fiche F9 (URL ci-dessus) | Conforme ; parts des chômeurs, pas des salariés |
| 65 % des moins de 25 ans (note) | 65 % | phrase de l'encadré 3 | dossier D1 | Conforme ; « chômage ou halo », pas les seuls chômeurs |
| 17,2 % (note) | 17,2 % | phrase de l'IR, BDM `011818634` | IR n° 192 | Conforme ; autre dénominateur |
| 25,1 % (note) | 25,1 % | 671 000 / 2 677 000 = 0,2507 | — | Calculé, dit « calculé » |

**Conclusion.** Aucun chiffre du fichier n'est faux ; chômeurs et inscrits ne sont jamais soustraits, et chaque part garde son dénominateur.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus ; à la saisie, la page de l'IR n° 192, la fiche F9 et la page STMT, relues.

## Réserves

- Valeurs du 2e trimestre 2026 publiées au 09/11/2026 : l'Insee publie le 3e trimestre le 10/11/2026 et peut réviser les trimestres passés (coefficients de correction saisonnière). La prochaine édition les remplacera.
- Trois champs : chômeurs, halo, sous-emploi et chômage de longue durée en France entière (2e trimestre 2026) ; inscrits en France hors Mayotte (3e trimestre 2026) ; recouvrement BIT-inscrits en France hors Mayotte, 15-64 ans (2024).
- Les catégories A à E sont corrigées des variations saisonnières, F et G sont des données brutes.
- Les 49 % portent sur la catégorie A seule et sur 2024, pas sur les catégories A, B, C ni sur 2026.
- La labellisation des séries d'inscrits est suspendue depuis le 01/01/2025 (description du jeu de données de la Dares, citée par la recherche).

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a relu la BDM, les PDF et les pages.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Insee : Licence Ouverte 2.0, mention « Source : Insee » et date de dernière mise à jour (https://www.insee.fr/fr/information/2008466) ;
  - citation seule : France Travail, Dares (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
