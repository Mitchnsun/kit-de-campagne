# `retirementAge` · L'âge de départ à la retraite (partie de la page « Retraites », saisie à la main)

**Vérifiée le 17/11/2026** : les valeurs saisies sont celles du fichier du COR et de la feuille de la DREES, relues par un script de lecture ; le texte du rapport du COR et le Panorama 2024 de la DREES les recoupent (section « Double vérification »). L'accord écrit du COR du 03/11/2026 couvre tout son fichier de données, donc cette série (déclaration du PO du 17/11/2026) ; la mention est « COR, rapport annuel de juin 2026 » (voir `contributorsPerRetiree.md`).

| Champ | Valeur |
| --- | --- |
| Indicateur | `retirementAge`, troisième volet de la page « Retraites » (`pensions`), dossier « Travail et retraites » (`work`), page de type série, recherche du 17/11/2026 (#21) |
| Données | `briefings/manual/retirementAge.json`, saisi le 2026-11-17 (projections : saisie à la main, guide 8 de l'app) |
| Sources | 1. COR, rapport annuel de juin 2026, publié le 11/06/2026, « Données juin 2026 – partie 2 » (https://www.cor-retraites.fr/sites/default/files/2026-06/Donn%C3%A9es_RA2026_P2.xlsx), onglet « Fig 2.5 » ; chiffres cités, mention « COR, rapport annuel de juin 2026 ». 2. DREES, EACR, « 62 EACR diffusée Part 1 - version du 26 mai 2026.xlsx », feuille `A-Age_conjoncturel` ; Licence Ouverte 2.0 |
| Séries | `retirementAge` : âge conjoncturel de départ, tous régimes, retraités de droit direct résidant en France et à l'étranger (ligne « Obs » de 2000 à 2025, ligne « Tous scénarios » de 2026 à 2070), arrondi au centième, 71 points ; 2025 `provisional` (estimé : « Les chiffres 2025 sont estimés », note 62 du rapport, modèle Ancêtre de la DREES), 2026 à 2070 `projection`. `cnav` (code 0015), `stateCivilServants` (0012), `cnracl` (0032), `cnieg` (0100), `sncf` (0060), `ratp` (0300), `enim` (0070), `canssm` (0080) : âge conjoncturel de 2024, deux sexes (`Sexe` « Ensemble »), un point chacun |
| Chiffre clé | 63,13 ans en 2025 (estimé), en hausse après 62,95 en 2024 : la dernière année de la série, même provisoire (PO, 17/11/2026) |
| Règles | Les valeurs « Obs » et « Tous scénarios » de 2025 sont égales (vérifié) ; la feuille de la DREES n'a pas de ligne tous régimes et ses âges par régime ne se moyennent pas ; huit grands régimes retenus sur les treize de 2024 (non repris : Agirc-Arrco, complémentaire du régime général, ERAFP, additionnel, Banque de France, CRPCEN, FSPOEIE) |
| Première édition | À remplir à la publication |

À actualiser : à chaque rapport annuel du COR (juin) et à chaque version de l'EACR (mai).

## « À savoir »

1. Définition et champ : note de la figure 2.5 du fichier, « Champ : retraités de droit direct résidents en France et à l'étranger de l'ensemble des régimes de retraite français légalement obligatoires. Source : Drees, modèles Ancêtre et Trajectoire, projections COR - juin 2026 » ; la définition (génération fictive aux taux de départ de l'année) est celle de l'annexe méthodologique du COR (https://www.cor-retraites.fr/sites/default/files/2026-06/Annexe_m%C3%A9thodo_en_ligne_2026.pdf).
2. Évolution et projection : onglet « Fig 2.5 » (60,49 en 2010, 62,95 en 2024, 63,13 en 2025, 64,08 en 2031, 64,51 en 2040, 64,63 en 2070), une seule ligne pour tous les scénarios ; rapport, partie 2, chapitre 2, § 3.2 : « passerait de 63,1 ans en 2025 à 64,6 ans environ à partir des années 2040 ».
3. Par régime : feuille `A-Age_conjoncturel`, 2024, « Ensemble » : CANSSM 54,76, RATP 56,89, ENIM 57,69, SNCF 59,22, CNIEG 60,2, CNRACL 62,46, fonction publique d'État civile 63,18, CNAV 63,6.

## Double vérification

Faite le 17/11/2026 par un agent Claude (modèle Opus), hors du fichier de données : le rapport annuel du COR en PDF (https://www.cor-retraites.fr/sites/default/files/2026-07/RA_2026_def.pdf, lu en entier par `pdftotext`) et la recherche web.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, 2025 | 63,13 | « 63,1 ans en 2025 » | Rapport du COR, synthèse et partie 2, chapitre 2 (RA_2026_def.pdf) | Conforme |
| Statut de 2025 | estimé | « Les derniers chiffres disponibles sont ceux de 2024. Les chiffres 2025 sont estimés » (note 62, sur les retraités du modèle Ancêtre) | RA_2026_def.pdf | Conforme |
| 2070 | 64,63 | « 64,6 ans en 2070 » | RA_2026_def.pdf | Conforme |
| 2022 | 62,68 | « 62 ans et 8 mois » fin 2022 (62,67) | DREES, Les retraités et les retraites, édition 2024, fiche 15 (https://drees.solidarites-sante.gouv.fr/sites/default/files/2024-10/RR24%20-%20Fiche%2015%20-%20L%E2%80%99%C3%A2ge%20moyen%20de%20d%C3%A9part%20%C3%A0%20la%20retraite%20et%20son%20%C3%A9volution.pdf), d'après un résumé de moteur de recherche (le site de la DREES répond 503) | Conforme (résumé) |
| Âges par régime, 2024 | 8 valeurs | Non trouvé hors du fichier : le Panorama 2026 de la DREES ne répond pas depuis l'environnement | — | Non trouvé |

**Conclusion.** Le chiffre clé, son statut et la projection concordent avec le texte du COR ; les âges par régime restent à recouper dans le Panorama 2026 de la DREES (fiche 15).

**Pages consultées** le 17/11/2026 : celles du tableau.

## Mises à jour

Aucune.
- **25/11/2026** (Mitchnsun/moi-president#541, PO, 25/11/2026) : point 4 ajouté, la suspension de la réforme de 2023. Loi n° 2025-1403 du 30/12/2025 de financement de la sécurité sociale pour 2026, art. 105 (JORF du 31/12/2025, lu dans une copie du Journal officiel), qui réécrit L. 161-17-2 et L. 161-17-3 du code de la sécurité sociale pour les pensions prenant effet à compter du 1er septembre 2026 ; décision n° 2025-899 DC du 30/12/2025, qui n'en censure que le VII (un rapport sur Mayotte) ; âges par génération sur Service-Public, F14043 (« Vérifié le 14 août 2026 »), https://www.service-public.gouv.fr/particuliers/vosdroits/F14043 ; trimestres sur F35063, https://www.service-public.gouv.fr/particuliers/vosdroits/F35063 (170 de 1963 à mars 1965, 171 d'avril à décembre 1965, 172 dès 1966). Lu par un agent Claude (modèle Sonnet) le 25/11/2026 (rapport `research/briefings-quiz-2026-11/verification-incoherences.md` de l'app), puis sur Légifrance le même jour : L. 161-17-2, 3° (« Soixante-deux ans et neuf mois, pour les assurés nés entre le 1er janvier 1963 et le 31 mars 1965 ») et L. 161-17-3, 4° et 6° (170 et 172 trimestres), en vigueur depuis le 31 décembre 2025, https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000053280889 et https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000053280903. Le texte ne fixe pas de date de fin : la note n'en donne pas. Cet âge légal n'est pas l'âge conjoncturel du COR des points 1 et 2.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande : l'accord du COR couvre tout le fichier (PO, 17/11/2026).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
