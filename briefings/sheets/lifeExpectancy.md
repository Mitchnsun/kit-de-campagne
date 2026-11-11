# `lifeExpectancy` · L'espérance de vie

**Vérifiée le 11/11/2026** : double vérification sur les pages de l'Insee, sans écart non expliqué (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `lifeExpectancy`, troisième volet de la page « Dépense, médecins et hôpital » (`healthCare`), dossier « Santé » (`health`), page de type série, ticket #143 de l'app |
| Données | `briefings/data/lifeExpectancy.json`, écrit par `yarn briefings lifeExpectancy` le 2026-11-11 |
| Sources | Insee, « Bilan démographique 2025 » (Insee Première n° 2087, paru le 13/01/2026), https://www.insee.fr/fr/statistiques/8719824, en anglais « Demographic report 2025 », https://www.insee.fr/en/statistiques/8726555 ; séries BDM 001686961 (https://www.insee.fr/fr/statistiques/serie/001686961) et 001686956 ; Licence Ouverte 2.0 (Etalab), celle de l'Insee ; daté par la dernière mise à jour des séries, 2026-01-13 |
| Séries | `womenLifeExpectancy` : « Espérance de vie à la naissance - Femmes - France (inclus Mayotte à partir de 2014) », BDM 001686961, en années, 1994 à 2025, 32 points ; `menLifeExpectancy` : la même pour les hommes, 001686956, 32 points. 2023, 2024 et 2025 provisoires (`OBS_STATUS` P) |
| Chiffre clé | 85,9 ans pour les femmes en 2025 (provisoire), en hausse après 85,8 ; 80,3 ans pour les hommes écrit à côté |
| Règles | Le script vérifie les titres des deux séries, échoue sur une année manquante, une valeur hors de 60 à 100 ans ou des années différentes entre femmes et hommes, et garde les années provisoires avec leur statut |
| Première édition | À remplir à la publication |

## « À savoir »

1. La définition : page de l'Insee Première n° 2087, section des définitions (« L'espérance de vie à la naissance représente la durée de vie moyenne d'une génération fictive qui serait soumise à chaque âge aux conditions de mortalité de l'année considérée. »).
2. Années provisoires, Mayotte : statut `P` des observations 2023 à 2025 dans la BDM (les années antérieures `DEF`), titre des séries (« inclus Mayotte à partir de 2014 »).

Les points en anglais disent la même chose que le français.

## Double vérification

Faite le 11/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans passer par la source du script : la presse et les diffuseurs qui citent la DREES ou l'Insee, les pages de l'Insee, le lisez-moi de l'APL. Le site principal de la DREES refuse les scripts (réponse vide, erreur 503) : ses pages, le Panorama et ses fichiers n'ont pu être vus que par des extraits de recherche, signalés comme tels.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, 2025 | 85,9 (femmes) ; 80,3 (hommes) | « elle s'établit à 85,9 ans pour les femmes et à 80,3 ans pour les hommes » ; « it stood at 85.9 years for women and 80.3 years for men » | https://www.insee.fr/fr/statistiques/8719824 ; https://www.insee.fr/en/statistiques/8726555 | Conforme |
| 2024 | 85,8 ; 80,2 | « 85,8 ans pour les femmes (contre 84,4 ans dans l'UE) et 80,2 ans pour les hommes » | page de 2025 (ci-dessus) | Conforme (révisés depuis le bilan de 2024) |
| 2020 | 85,1 ; 79,1 | « 2020p 85,1 79,1 » (tableau de l'Insee, résumé du moteur) | https://www.insee.fr/fr/statistiques/7666863 | Conforme |
| 2022 | 85,1 ; 79,3 | Bilan 2022, provisoire : 85,2 ; 79,3 (résumé du moteur) | recherche | Écart expliqué : le fichier lit la valeur définitive de la BDM (`DEF`), le bilan 2022 la valeur provisoire |
| Années provisoires | 2023 à 2025 | « p : provisoire » pour 2024 et 2025 sur la page ; `OBS_STATUS` P de 2023 à 2025 dans la BDM | page de 2025 ; API de la BDM | Conforme |
| Champ | Mayotte comprise depuis 2014 | « Champ : France hors Mayotte jusqu'en 2013 et France à partir de 2014 » | page de 2025 | Conforme |
| Définition | note 1 | « L'espérance de vie à la naissance représente la durée de vie moyenne d'une génération fictive qui serait soumise à chaque âge aux conditions de mortalité de l'année considérée. » (définitions de l'Insee Première, relues par Claude) | page de 2025 | Conforme |
| Licence | Licence Ouverte 2.0 | celle de l'Insee, comme les autres séries de la BDM des Dossiers | | Conforme |
| Version anglaise | « Demographic report 2025 » | trouvée : la source passe de « français seulement » à une page en anglais | https://www.insee.fr/en/statistiques/8726555 | Corrigé dans le registre de l'app |

**Conclusion.** Les chiffres de 2025 sont ceux du bilan démographique ; l'écart de 2022 tient à la valeur définitive de la BDM.

**Pages consultées** (le 11/11/2026) :

- https://www.insee.fr/fr/statistiques/8719824
- https://www.insee.fr/en/statistiques/8726555
- https://api.insee.fr/series/BDM/V1/data/SERIES_BDM/001686961+001686956 (réponse lue par Claude)
- pages de l'Insee de 2022 et 2023 : vues seulement dans les résultats de recherche

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
