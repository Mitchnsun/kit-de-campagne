# `conventionalBreaks` · Les ruptures conventionnelles

**Vérifiée le 25/11/2026** : relevé dans un navigateur par un agent, puis chaque cellule relue par l'agent principal dans les trois fichiers XLSX téléchargés (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `conventionalBreaks`, volet de « Le chômage au-delà du taux » (`unemploymentBeyond`), dossier « Travail et retraites » (`work`), page de type série, ticket #541 de l'app |
| Données | `briefings/manual/conventionalBreaks.json`, saisi à la main le 2026-11-25 : le site de la Dares refuse les scripts, ses fichiers ont été téléchargés dans un navigateur |
| Sources | Dares, « Les ruptures conventionnelles en 2024 » (Dares Résultats n° 15, Ayoub Berami, 8 avril 2026), https://dares.travail-emploi.gouv.fr/publication/les-ruptures-conventionnelles-en-2024, fichier `Données_ DR_ruptures co_2024_actualisé.xlsx`, feuille « Graphique 1 » ; Dares, « Les mouvements de main-d'œuvre », page de données mise à jour le 22 octobre 2026, https://dares.travail-emploi.gouv.fr/donnees/les-mouvements-de-main-doeuvre, fichiers `Dares_Données annuelles_Mouvements de main-doeuvre_DI2026T2_corrige.xlsx` (feuille « MMO_annuels ») et `Dares_Données trimestrielles-Mouvements de main-doeuvre_DI2026T2_corrige.xlsx` (feuille « MMO_trimestriels »). Mentions légales de la Dares : contenus « librement et gratuitement réutilisables dans les conditions fixées par la loi n°78-753 du 17 juillet 1978 » ; les liens pointent vers les pages, pas vers les fichiers, comme elle le demande (sauf le fichier de l'étude, dont l'adresse est dans la page). Citation seule dans le registre |
| Séries | `homologatedFrance` : « Nombre de ruptures en France » (col. D), 2021 à 2024 ; `homologatedMetro` : « Nombre de ruptures en France métropolitaine » (col. B), 2008 à 2024, arrondies à l'unité (2013 à 2020 ont des décimales dans le fichier) ; champ « France, secteur privé » (A24) ; `declaredAnnual` : « Ruptures conventionnelles...11 » (col. K), « Ensemble des établissements / Ensemble des secteurs », 2008 à 2025 ; `declaredQuarterly` : même colonne, trimestriel, 2008-T3 à 2026-T2 (2008-T1 et T2 à 0, écartés) ; champ des MMO : « France métropolitaine du champ privé hors agriculture, hors contrats intérimaires et hors particuliers employeurs » |
| Chiffre clé | 538 433 homologuées en France en 2024 (la publication écrit 538 400), en baisse (544 038 en 2023) ; le dernier trimestre déclaré à côté, 118 128 au 2e trimestre 2026 |
| Règles | Deux comptes jamais additionnés ni comparés comme un seul : les homologations à la date de la demande, les déclarations sociales à la date de fin du contrat. Le total des homologations de 2025 n'est pas encore publié |
| Première édition | La prochaine édition du kit |

## « À savoir »

1. Page de l'étude : « En 2024, 538 400 ruptures conventionnelles individuelles sont homologuées dans le secteur privé, en légère baisse après deux années de nette hausse (-1,0 % en 2024, après +4,9 % en 2023 et +10,9 % en 2022). »
2. MMO_annuels, K2231 : 514 768 en 2024 ; page de données : les homologations sont mesurées « à date d'homologation (contrairement aux mouvements de main-d'œuvre, qui sont enregistrés à la date de rupture de contrat) ».
3. Page « Les mouvements de main-d'œuvre » : « Au 2e trimestre 2026, 118 100 ruptures conventionnelles ont lieu en France métropolitaine sur le champ privé hors agriculture et particuliers employeurs (-2,7 % par rapport au trimestre précédent). »
4. Le dispositif existe depuis 2008 (série trimestrielle à 0 avant 2008-T3) ; le droit au chômage : Code du travail, art. L. 5422-1, I, 2° ; la durée depuis le 1er septembre 2026 : `unemploymentRules`.

## Double vérification

Le relevé du navigateur (rapport `research/briefings-quiz-2026-11/releve-navigateur-dares.md` de l'app) et la relecture par l'agent principal des cellules B3 à B20, D17 à D20 et A24 de « Graphique 1 », de K1, K711, K806, K2231 et K2326 de « MMO_annuels » et de toute la colonne K de « MMO_trimestriels » (lignes « Ensemble des établissements / Ensemble des secteurs ») concordent. Les écarts que la première recherche n'avait pas tranchés le sont : 538 400 (homologations, France) et 514 768 (déclarations, métropole) en 2024 ; 190 789 (homologations, métropole) et 192 278 (déclarations) en 2009. « 515 000 » n'est écrit nulle part.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
