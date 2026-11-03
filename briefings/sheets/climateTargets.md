# `climateTargets` · Objectifs climatiques (saisie à la main)

**Vérifiée le 02/11/2026** : les trois budgets carbone sont conformes au décret n° 2026-636 (art. 2), à la SNBC 3 de juillet 2026 et à la page SNBC du ministère. Les valeurs 261 et 193 sont celles du projet de juin 2026. Notes alignées sur le texte du décret (« hors puits de carbone »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `climateTargets`, troisième page du ticket #29, dossier « Écologie et énergie » (statut `planned`), graphique de comparaison avec les émissions (`emissions`) |
| Données | `briefings/manual/climateTargets.json`, saisi à la main le 2026-11-02 depuis le décret (PO, 02/11/2026 : saisies à la main dans `manual/`) |
| Source | Légifrance, décret n° 2026-636 du 16 juillet 2026 relatif aux budgets carbone nationaux et à la stratégie nationale bas-carbone, JORF n° 0166 du 18 juillet 2026, article 2 (`https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907`) ; Licence Ouverte (données de Légifrance) ; en français seulement |
| Série | `carbonBudget` : budget carbone annuel moyen, en MtCO₂e par an, hors puits de carbone, pour 2024-2028 (342), 2029-2033 (262) et 2034-2038 (194) ; chaque point porte l'année où commence sa période |
| Chiffre clé | 342 MtCO₂e par an pour 2024-2028, sans tendance |
| Première édition | À remplir à la publication |

À actualiser : à la prochaine révision de la stratégie nationale bas-carbone, ou si un décret modifie les budgets. Les budgets indicatifs du puits (décret, art. 10 : -46, -33, -31) et les tranches annuelles (art. 6) ne sont pas saisis.

## Double vérification

La vérification de ces valeurs a été faite avec celle des émissions (`emissions.md`), le 02/11/2026, par un agent Claude (modèle Sonnet) qui cherche sur le web. Il a lu le décret dans l'archive du Journal officiel (DILA). Extrait de son rapport, tel quel :

### 5. Budgets carbone de la SNBC 3

**Le bon jeu est 342 / 262 / 194 MtCO2e par an** (2024-2028 / 2029-2033 / 2034-2038, hors puits de carbone). Il est fixé par le **décret n° 2026-636 du 16 juillet 2026** relatif aux budgets carbone nationaux et à la stratégie nationale bas-carbone, JORF n° 0166 du 18 juillet 2026, NOR TECR2618516D (id Légifrance JORFTEXT000054440907). Article 2 : « Les budgets carbone des périodes 2024-2028, 2029-2033 sont révisés et fixés respectivement à 342 et 262 Mt de CO2e par an et le budget carbone pour la période 2034-2038 est fixé à 194 Mt CO2e par an, hors « puits de carbone » ».

| Élément | Valeur à vérifier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Budget 2024-2028 | 342 | 342 Mt CO2e/an | [décret art. 2](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907), [SNBC 3 juillet 2026 p.66-67](https://www.ecologie.gouv.fr/sites/default/files/documents/SNBC3-Partie1-Juillet2026.pdf), [ministère](https://www.ecologie.gouv.fr/politiques-publiques/strategie-nationale-bas-carbone-snbc) | Conforme |
| Budget 2029-2033 | 262 ou 261 | **262** (décret ; SNBC 3 de juillet 2026 : « fixé à 262 Mt CO2e/an » ; page SNBC du ministère). **261** = valeur du projet de juin 2026, encore citée par le Citepa (Rapport p.90 ; Synthèse parle du « projet »), par le HCC (p.136 : « passe de 265 à 261 Mt ») et par la page « Suivi des émissions » du ministère, mise à jour le 22/10/2026 | idem + [Rapport p.90](https://www.citepa.org/wp-content/uploads/2026/06/Citepa_Secten-2026.pdf), [HCC p.136](https://www.hautconseilclimat.fr/wp-content/uploads/2026/07/HCC_RA2026-Chapitre-3_1707.pdf), [ministère, suivi](https://ecologie.gouv.fr/strategie-nationale-bas-carbone/suivi-des-emissions-gaz-effet-serre) | **262 est juste.** 261 est périmé (projet) |
| Budget 2034-2038 | 194 ou 193 | **194** (décret, SNBC 3 juillet 2026). **193** = projet de juin 2026 (Citepa p.90, page « Suivi » du ministère) | idem | **194 est juste.** 193 est périmé |
| Tranches annuelles indicatives | – | 2024 : 367 ; 2025 : 359 ; 2026 : 348 ; 2027 : 328 ; 2028 : 308 (décret art. 6). Le projet citait 369 et 364 pour 2024 et 2025 (Synthèse p.1) ; le décret reprend les valeurs de l'inventaire 2026 (déduit de l'égalité avec Secten 2026) | [décret art. 6](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907), [Synthèse p.1](https://www.citepa.org/wp-content/uploads/2026/06/Synthese-et-messages-cles-Secten-2026.pdf) | Information |
| Années de référence du décret | – | 1990 : 547 ; 2005 : 556 ; 2024 : 367, « issues de l'inventaire … du Citepa au format Secten de 2026 » ; secteurs 2024 : transports 125, bâtiments 56, agriculture 78, industrie 62, énergie 31, déchets 15 | [décret art. 3](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000054440907) | Conforme au fichier (arrondis) |

Points d'attention :
- La page « Suivi des émissions » du ministère est **incohérente avec sa propre page SNBC** (261/193 contre 262/194). Elle n'a manifestement pas été remise à jour après le décret. Ne pas s'y fier pour ces deux budgets.
- Les budgets de puits UTCATF ont aussi changé : décret art. 10, budgets indicatifs -46 / -33 / -31 MtCO2e par an (2024-2028 / 2029-2033 / 2034-2038). Le Citepa (Rapport p.524) cite le projet de juin avec « -33 » pour 2024-2028. Si la page parle du puits, utiliser le décret.
- Avant le décret, les versions antérieures du projet donnaient d'autres valeurs (HCC p.136 : 265 pour 2029-2033 ; Wikipédia, résumé d'outil : 265 et 192, non retenu comme preuve) : la valeur dépend donc de la version citée.
- Non vérifié : le texte consolidé sur la page Légifrance elle-même (lu via l'archive DILA).

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
