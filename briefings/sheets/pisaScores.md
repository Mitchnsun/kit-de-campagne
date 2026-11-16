# `pisaScores` · PISA (partie de la page « Éducation »)

**Vérifiée le 02/11/2026** : toutes les valeurs conformes à l'annexe Excel de l'OCDE (`https://stat.link/mrq53f`) ; notes corrigées (résultats du prochain cycle en 2030, sciences non significatif). Double vérification commune aux trois parties de la page « Éducation » : voir `schools.md`.

| Champ | Valeur |
| --- | --- |
| Indicateur | `pisaScores`, partie de la page composite `schools`, dossier « Éducation », ticket #32 (statut `planned`) |
| Données | `briefings/data/pisaScores.json`, écrit par `yarn briefings pisaScores` le 2026-11-02, réécrit le 2026-11-03 pour la date de publication (mêmes chiffres) |
| Sources | DEPP, Notes d'Information n° 26.40 (compréhension de l'écrit, culture mathématique) et n° 26.39 (culture scientifique), septembre 2026, PDF et XLSX ; publiées le 08/09/2026 avec les résultats de l'OCDE, fichiers datés du 04/09/2026 par leur serveur (les pages du ministère refusent les scripts) ; Licence Ouverte |
| Séries | `readingFrance`, `readingOecd`, `mathematicsFrance`, `mathematicsOecd`, `scienceFrance`, `scienceOecd` : scores moyens depuis le premier cycle de chaque domaine, France et moyenne des 24 pays de l'OCDE présents à tous les cycles |
| Valeurs par catégorie | 2025 : `franceScores` 456,33 / 457,66 / 483,42, `franceStandardErrors` 3,24 / 3,00 / 3,21, `oecdScores` (38 pays) 460,94 / 463,02 / 481,91, `oecdStandardErrors` 0,45 / 0,42 / 0,44 (écrit, maths, sciences) |
| Chiffre clé | 458 points en culture mathématique en 2025, en baisse (474 en 2022) |
| Première édition | À remplir à la publication |

À actualiser : le cycle PISA 2029, résultats en 2030.

## Mises à jour

- **16/11/2026** (#448 de l'app, décision du PO de placer la note sur les réseaux sociaux dans une page d'éducation) : les anciens points 3 (la moyenne de l'OCDE, 38 pays ou 24 pays) et 4 (le cycle de quatre ans) sont réunis en un point 3, sans changer leurs mots ; nouveau point 4, la loi sur les réseaux sociaux avant 15 ans. Sources : dossier législatif de l'Assemblée nationale, https://www.assemblee-nationale.fr/dyn/17/dossiers/proteger_mineurs_reseaux_sociaux_17e (texte de la commission mixte paritaire adopté le 21 juillet 2026 ; « Loi n°2026-813 du lundi 24 août 2026 visant à protéger les mineurs des risques auxquels les expose l'utilisation des réseaux sociaux », publiée au Journal officiel du 25 août 2026) ; Conseil constitutionnel, décision n° 2026-911 DC du 14 août 2026, https://www.conseil-constitutionnel.fr/decision/2026/2026911DC.htm (§ 2 : l'article 1er instituait « une interdiction d'accès des mineurs de quinze ans aux services de réseaux sociaux en ligne » ; dispositif : « L'article 1er de la loi visant à protéger les mineurs des risques auxquels les expose l'utilisation des réseaux sociaux est contraire à la Constitution. »). Faits confirmés par la recherche du 15/11/2026 (`research-gap-g2.md`, § 3.8 et 3.9) et sa double vérification sur le web par un agent Claude (modèle Sonnet), 15/11/2026 (`check-gap-g2.md`, § 3). La note n'a pas de lien avec les scores de PISA : aucune page de l'éducation n'en a, le PO l'a placée ici.
- **03/11/2026, relecture du PO** : les pages HTML des deux notes (NI 26.40 : https://www.education.gouv.fr/depp/pisa-2025-les-acquis-des-eleves-de-15-ans-en-comprehension-de-l-ecrit-et-en-culture-mathematique-en-505645 ; NI 26.39 : https://www.education.gouv.fr/depp/pisa-2025-en-culture-scientifique-le-score-baisse-par-rapport-2015-en-france-comme-dans-l-ocde-et-505639), lues par le PO, affichent le **08/09/2026**, le jour des résultats de l'OCDE. Le 04/09/2026 était la date des fichiers chez leur serveur. Le script écrit désormais la date des pages ; les chiffres ne changent pas.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
