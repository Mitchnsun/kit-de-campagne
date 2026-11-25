# `classSize` · Les élèves par classe

**Vérifiée le 25/11/2026** : double vérification sur le web, sans écart non expliqué (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `classSize`, volet de « PISA, sortants précoces, budget et salaires » (`schools`), dossier « Éducation » (`education`), page de type série, ticket #540 de l'app |
| Données | `briefings/manual/classSize.json`, saisi à la main le 2026-11-25 depuis le chapitre 2 des RERS 2026 (PDF) |
| Sources | DEPP, « Repères et références statistiques 2026 », https://www.education.gouv.fr/depp/reperes-et-references-statistiques-2026-505320 ; chapitre 2 « Les établissements », https://www.education.gouv.fr/sites/default/files/document/2-les-etablissementspdf-519279.pdf (PDF créé le 27/07/2026, la date retenue : la page n'en donne pas) ; licence etalab-2.0, comme les autres sources de la DEPP du kit (pied de page du site du ministère) |
| Séries | Public et privé sous contrat, France, nombre moyen d'élèves par classe à la rentrée : `elementary` et `preElementary`, fiche 2.02, tableau « Évolution du nombre moyen d'élèves par classe selon le secteur et le niveau de formation », colonnes « Public + privé sous contrat » 2015, 2020, 2025 (hors ULIS ; le tableau ne donne pas d'autres années, la courbe annuelle 2013-2025 n'est qu'en graphique) ; `lowerSecondary` (« Formations de niveau collège, hors Segpa »), `generalUpperSecondary` (« Formations générales et technologiques en lycée »), `vocationalUpperSecondary` (« Formations professionnelles en lycée »), fiche 2.05, tableau « Évolution du nombre moyen d'élèves par classe (ou division) selon le niveau de formation », bloc « Public + privé sous contrat », 2005, 2010, 2015, 2019 à 2025 (France, Mayotte à partir de 2011) |
| Chiffre clé | 21,1 élèves par classe en élémentaire à la rentrée 2025, en baisse (21,9 en 2020) ; la maternelle à côté, 21,7 |
| Règles | La fiche 2.05 (par niveau de formation, l'indicateur de « L'éducation nationale en chiffres »), jamais la 2.04 (par type d'établissement, post-bac compris), qui donne d'autres valeurs : le RERS le dit lui-même |
| Première édition | La prochaine édition du kit |

## « À savoir »

1. Fiche 2.02 : public + privé sous contrat 2015 et 2025 ; privé sous contrat 2025 : 24,2 et 24,8.
2. Fiche 2.02 : tableau REP+ 2025, CP 12,8, CE1 12,9 ; texte de la fiche : « 14 % des classes préélémentaires et 9 % des classes élémentaires accueillent 30 élèves ou plus », à propos du secteur privé.
3. Fiche 2.05 : texte (« en collège et en lycée général et technologique, le nombre moyen d'élèves par classe augmente depuis 2008 » ; « une diminution de 3,5 élèves par classe entre 1994 et 2025 » en formations professionnelles) et tableau.
4. Eurostat, `educ_uoe_perp04`, `isced11=ED1`, 2024 : France 17,9 (drapeau `d`), UE à 27 13,3, mise à jour du 05/08/2026, https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/educ_uoe_perp04?format=JSON&lang=fr&geo=FR&geo=EU27_2020&isced11=ED1 ; « L'éducation nationale en chiffres 2026 » prévient de ne pas confondre ce ratio avec le nombre d'élèves par classe.

## Double vérification

Faite le 25/11/2026 par un agent Claude (modèle Sonnet), sur une autre publication de la DEPP que le RERS (rapport `dossiers2/A-series.md` de la session).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Élémentaire 2025 | 21,1 | 21,1 | DEPP, « L'éducation nationale en chiffres 2026 », https://www.education.gouv.fr/sites/default/files/document/enc-2026pdf-519886.pdf | Conforme |
| Maternelle 2025 | 21,7 | 21,7 | Idem | Conforme |
| Collège 2025, hors Segpa | 25,7 | 25,7 | Idem | Conforme |
| Lycée général et technologique 2025 | 30,2 | 30,2 | Idem | Conforme |
| Lycée professionnel 2025 | 18,4 | 18,4 | Idem | Conforme |

**Conclusion.** Les valeurs de 2025 du RERS sont celles de « L'éducation nationale en chiffres 2026 » ; les années antérieures ne sont lues que dans le RERS.

**Pages consultées** le 25/11/2026 : celles du tableau.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande : celle des autres sources de la DEPP du kit, non relue pour ce PDF.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
