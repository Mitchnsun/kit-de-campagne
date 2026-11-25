# `unemploymentRules` · Les règles de l'assurance chômage

**Vérifiée le 25/11/2026** : chaque citation relue par script, caractère pour caractère, dans une copie ouverte du texte (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `unemploymentRules`, dossier « Travail et retraites » (`work`), page de règles (`chart: 'rules'`, nature `law`), ticket #541 de l'app |
| Données | `briefings/manual/unemploymentRules.json`, saisi à la main le 2026-11-25 |
| Sources | Unédic, « Texte consolidé du règlement général annexé à la convention du 15 novembre 2024 relative à l'Assurance chômage », version consolidée « intégrant l'avenant n°1 du 7 juillet 2025 et l'avenant n°2 du 10 avril 2026 », datée du 1er septembre 2026, https://www.unedic.org/la-reglementation/conventions-d-assurance-chomage/texte-consolide-du-reglement-general-annexe-a-la-convention-du-15-novembre-2024-4 ; Unédic, « Texte consolidé de la convention du 15 novembre 2024 relative à l'Assurance chômage », même version, https://www.unedic.org/la-reglementation/conventions-d-assurance-chomage/texte-consolide-de-la-convention-du-15-novembre-2024-relative-a-lassurance-chomage-3 ; ministère du Travail, Code du travail numérique, art. L5422-2-2, « Mis à jour le : 26/10/2025 », https://code.travail.gouv.fr/code-du-travail/l5422-2-2 (licence etalab-2.0) ; Légifrance, « Décret n° 2023-33 du 26 janvier 2023 relatif au régime d'assurance chômage », JORF n° 0023 du 27 janvier 2023, NOR MTRD2235569D, https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000047061815 (Licence Ouverte 2.0). Les textes de l'Unédic : citation seule |
| Règles | Les jours des textes, jamais les mois de l'Unédic (dits dans les libellés de l'app, d'après sa fiche) ; métropole (l'outre-mer a ses durées) |
| Chiffre clé | 548 jours au plus avant 55 ans (règlement général, art. 9, § 4, 2°) |
| Première édition | La prochaine édition du kit |

## Les règles et leurs textes

| Règle | Article | Chiffre |
| --- | --- | --- |
| `maxUnder55`, `max55to56`, `max57AndOver` | Règlement général, art. 9, § 4, 2° (le texte écrit « âgés de moins 55 ans », sans « de ») | 548, 685, 822 jours |
| `coefficient` | Règlement général, art. 9, § 1er, 1°, al. 2 | 0,75 |
| `floor` | Règlement général, art. 9, § 4, 1°, al. 1 | 182 jours |
| `breakUnder55`, `break55AndOver` | Règlement général, art. 9, § 8, 2°, a) (avenant n° 2 du 10 avril 2026, art. 2, 2°, d) : même texte) | 456, 624 jours ; pas de palier à 57 ans |
| `breakExtension` | Convention, art. 2, § 14, al. 2 | sans chiffre |
| `breakStart` et la date `conventionalBreakRule` | Convention, art. 11, § 7 | 1er septembre 2026 |
| `supplement` | Règlement général, art. 9, § 1er, 2° | sans chiffre |
| `supplementTrigger` | Règlement général, art. 9 bis, § 1er : « l'une ou l'autre » des conditions, + 0,8 point en un trimestre ou 9,0 % | 9 % |
| `modulation` | Code du travail, art. L. 5422-2-2, 1re phrase | sans chiffre |
| Date `coefficientStart` | Décret n° 2023-33, art. 1 (art. 5 bis inséré dans le décret n° 2019-797) : les articles modifiés « sont applicables aux travailleurs privés d'emploi dont la fin de contrat de travail est intervenue à compter du 1er février 2023 » ; le décret, lui, entre en vigueur le lendemain de sa publication | 1er février 2023 |
| Date `ageThresholds` | Convention, art. 11, § 1er, al. 3 : l'article 9 entre en vigueur « au plus tard au 1er avril 2025 » ; avant, 53 et 55 ans (circulaire Unédic n° 2023-08) | au plus tard le 1er avril 2025 |

## « À savoir »

1. Fiche Unédic : « 18 mois, soit 548 jours calendaires » ; la durée dépend des jours travaillés (règlement, art. 9, § 1er, 1°).
2. Règlement, art. 9, § 1er, 1° (coefficient sans condition) et art. 9 bis, § 1er ; circulaire Unédic n° 2023-08 du 26/07/2023 : « quel que soit l'état de la conjoncture, excepté pour les allocataires résidant dans les DROM-COM ».
3. Avenant n° 2 du 10 avril 2026 (PDF de l'Unédic) ; loi n° 2026-470 du 11 juin 2026, article unique, qui complète L. 5422-2 du Code du travail (JORF n° 0136 du 12 juin 2026, NOR TRSD2606801L, https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054237287 ; elle ne fixe aucune durée). L'avenant n° 2 est agréé par l'arrêté du 19 juin 2026 (JORF n° 0145 du 23 juin 2026, NOR TRSD2614637A, https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054297458).
4. Insee, Informations rapides n° 270 : « Au troisième trimestre 2026, le taux de chômage s'établit à 8,2 % », https://insee.fr/fr/statistiques/9118603. La note ne dit pas si le complément est applicable : aucune circulaire de constat n'a été trouvée.

## Double vérification

Faite le 25/11/2026 par un agent Claude (modèle Sonnet) qui a ouvert chaque texte et vérifié chaque citation par script dans la copie enregistrée (rapport `research/briefings-quiz-2026-11/verification-textes.md` de l'app), après une première recherche sur les mêmes règles (`verification-regles.md`, § 2), avec laquelle les durées concordent. Deux points de la première recherche sont corrigés : le coefficient n'a pas de condition, et la loi n° 2026-470 ne fixe pas de durée.

## Mises à jour

- **25/11/2026** : la quatrième source, la fiche « Durée d'indemnisation » de l'Unédic, est remplacée par le décret n° 2023-33, qui fixe la date du calendrier ; les textes lus sur Légifrance dans un navigateur le 25/11/2026 (`research/briefings-quiz-2026-11/releve-navigateur-legifrance.md` de l'app).

## Relecture

- [x] Chaque citation relue dans une copie ouverte.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Le décret n° 2023-33, la loi n° 2026-470 et l'arrêté d'agrément du 19 juin 2026 lus sur Légifrance dans un navigateur le 25/11/2026 (`research/briefings-quiz-2026-11/releve-navigateur-legifrance.md` de l'app).
