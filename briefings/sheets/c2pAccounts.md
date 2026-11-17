# `c2pAccounts` · Les comptes de pénibilité (partie de la page « Retraites », saisie à la main)

**Vérifiée le 17/11/2026** : les valeurs saisies sont celles du rapport, relues dans le PDF ; aucune autre publication récente ne donne ces cumuls (section « Double vérification »). Le rapport se contredit sur le cumul : son schéma 1 écrit « 2,3 million de salariés depuis 2015 », son texte et son graphique 1 « près de 2,7 millions fin 2024 » ; le fichier suit le texte et le graphique, et une note le dit.

| Champ | Valeur |
| --- | --- |
| Indicateur | `c2pAccounts`, sixième volet de la page « Retraites » (`pensions`), dossier « Travail et retraites » (`work`), page de type série, recherche du 17/11/2026 (#21) |
| Données | `briefings/manual/c2pAccounts.json`, saisi le 2026-11-17 depuis le PDF |
| Source | Cnam (« Source : CNAM, SIPP décembre 2024 »), « Rapport d'évaluation des politiques de sécurité sociale - AT-MP », annexe 1 au projet de loi d'approbation des comptes de la sécurité sociale de l'année 2025 (n° 2843, déposé à l'Assemblée nationale le 27/05/2026, https://www.assemblee-nationale.fr/dyn/17/dossiers/DLR5L17N54373), PDF https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1112994/file/PLACSS%202025%20Annexe%201%20-%20REPSS%20AT-MP%202026.pdf, fiche 1.10 « Bénéficiaires d'un compte professionnel de prévention », pages 61 et 62 ; chiffres cités (`citation-only`) |
| Séries | `openAccounts` : personnes avec au moins une exposition validée depuis 2015, cumul en fin d'année, graphique 1 (étiquettes en millions, à une décimale), 2015 à 2024, 10 points ; `exposedEmployees` : « environ 886 000 salariés » déclarés exposés en 2024 ; `earlyRetirement` (25 700), `partTime` (4 800), `training` (2 400), `retraining` (260) : salariés dont une demande de conversion de points a abouti, en cumul à fin 2024, un point chacun (période 2024) |
| Chiffre clé | 2,7 millions fin 2024, en hausse après 2,4 millions fin 2023 |
| Règles | Les valeurs du graphique sont arrondies à 100 000 près par la Cnam : jamais plus précises dans le fichier |
| Première édition | À remplir à la publication |

À actualiser : à chaque rapport AT-MP annexé au projet de loi d'approbation des comptes (fin mai) ou au PLFSS (octobre).

## « À savoir »

1. Les six facteurs, les régimes et les usages des points : fiche 1.10, p. 61 (« salariés du régime général et du régime agricole, exposés à des facteurs de risques professionnels, au-delà de seuils fixés par décret » ; « travail de nuit, répétitif, en équipes successives alternantes, en milieu hyperbare, températures extrêmes et bruit » ; formation, temps partiel, majoration de durée d'assurance « dans la limite de deux ans avant l'âge légal », reconversion) ; schéma 1 (« Réduction de 50% du temps de travail pendant 4 mois sans perte de salaire »).
2. Le cumul, son arrondi et la contradiction du schéma : p. 61-62 (« passé d'environ 0,6 million fin 2015 à près de 2,7 millions fin 2024 », « 86 % des comptes professionnels de prévention ouverts sont crédités d'un point au moins ») ; schéma 1 (« 2,3 million de salariés depuis 2015 »).
3. 2024 : p. 62 (« environ 886 000 salariés ont été déclarés exposés », « 40 % [...] au titre du travail de nuit et 32 % au titre du travail en équipes successives alternantes », « 33 900 salariés ont eu une demande de conversion de points qui a abouti. Pour 25 700 salariés, il s'agissait d'une demande de majoration de durée d'assurance »).
4. Les facteurs retirés en 2017 : p. 61 et « Précisions juridiques » p. 62 (les dix critères de la loi du 20 janvier 2014, « recentré sur 6 facteurs » depuis le 1er octobre 2017).

## Double vérification

Faite le 17/11/2026 par un agent Claude (modèle Opus) par la recherche web.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, 2,7 millions fin 2024 | 2 700 000 | Aucune autre publication trouvée | Recherches « compte professionnel de prévention 2,7 millions », « 886 000 exposés » | Non trouvé |
| Exposés dans l'année | 886 000 (2024) | 898 000 en 2016, l'année la plus haute de 2015 à 2021 | Assurance retraite, « C2P 2015-2021 » (https://statistiques-recherche.lassuranceretraite.fr/app/uploads/2023/04/C2P-2015-2021-portraits_dispositifs-retraite.pdf), d'après un résumé de moteur | Ordre de grandeur cohérent |
| Départs au titre du C2P | — | 2 864 départs en 2024 à la CNAV | DREES, EACR, feuille `H-Conditions_liq` (voir `retirementConditions.md`) | Cohérent avec 25 700 conversions en trimestres depuis 2015 |

**Conclusion.** Pas d'écart, mais pas de recoupement direct du cumul : à refaire avec le rapport AT-MP suivant ou une publication de la DARES.

**Pages consultées** le 17/11/2026 : celles du tableau.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source : non trouvé pour le cumul.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande (chiffres cités avec leur source).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
