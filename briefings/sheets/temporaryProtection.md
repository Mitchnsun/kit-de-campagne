# `temporaryProtection` · Protection temporaire (Ukrainiens)

**Vérifiée le 11/11/2026** : double vérification sur le web, sans écart non expliqué (section « Double vérification »). Le recoupement des chiffres de la France n'a pas pu se faire avec le ministère de l'Intérieur (page fermée aux scripts).

| Champ | Valeur |
| --- | --- |
| Indicateur | `temporaryProtection`, dossier « Défense et Europe » (`defence`), volet de la page `ukrainianRefugees` (page de type volets), première série de la page, ticket #349 de l'app |
| Données | `briefings/data/temporaryProtection.json`, écrit par `yarn briefings temporaryProtection` le 2026-11-11 |
| Sources | Eurostat, « Personnes bénéficiant d'une protection temporaire à la fin du mois par nationalité, âge et sexe - données mensuelles » (`migr_asytpsm`), page https://ec.europa.eu/eurostat/databrowser/view/migr_asytpsm/default/table?lang=fr, API https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/migr_asytpsm?format=JSON&geo=FR&geo=EU27_2020&citizen=UA&sex=T&age=TOTAL&lang=en, mise à jour du 2026-11-10, licence d'Eurostat (« Source : Eurostat ») |
| Séries | `france` : citoyens ukrainiens (`citizen=UA`), femmes et hommes (`sex=T`), tous âges (`age=TOTAL`), en France (`geo=FR`), `migr_asytpsm`, de 2022-03 à 2026-09, 55 points (26 315 puis 45 525) ; `europeanUnion` : les mêmes dans l'Union (`geo=EU27_2020`), de 2022-08 à 2026-09, 50 points (3 608 165 puis 4 302 850), cinq ruptures de série (2024-02, 2024-07, 2024-10, 2025-06, 2025-09, drapeau `b`) |
| Chiffre clé | France, septembre 2026 : 45 525, en hausse sur août (45 185) |
| Règles | Chiffres de fin de mois, jamais intitulés « réfugiés ». Chaque mois de chaque territoire doit avoir son chiffre, sinon le script échoue (le mois d'octobre 2026, sans chiffre, est écarté). Le drapeau `d` (définition différente) marque tous les mois de la France et n'est pas gardé dans le fichier : la page le dit dans sa note. Le drapeau `b` devient les `breaks` de la série de l'Union. L'Union n'a aucun chiffre avant 2022-08 |
| Première édition | À remplir à la publication |

## « À savoir »

1. Eurostat compte les personnes sous protection temporaire le dernier jour du mois ; ce n'est pas le statut de réfugié et ce décompte ne s'additionne pas avec celui du HCR. Source : titre du jeu de données (« à la fin du mois »), métadonnées d'Eurostat https://ec.europa.eu/eurostat/cache/metadata/en/migr_asytp_esms.htm (définition de la protection temporaire, décision d'exécution (UE) 2022/382 du Conseil du 4 mars 2022).
2. Drapeau `d` sur tous les chiffres de la France ; mineurs généralement non comptés. Source : les données de l'API (`status`) ; métadonnées d'Eurostat, section « Accuracy » : « France: In most cases, minors can stay in France without a permit. Therefore, minors are generally not included in statistics on temporary protection. » Les métadonnées ne rattachent pas le drapeau `d` à cette raison : la note les met côte à côte sans le dire.
3. L'Union commence en août 2022 et compte cinq ruptures de série. Source : les données de l'API (`status` `b`, `value` vide avant 2022-08).

Les trois points en anglais disent la même chose que le français.

## Double vérification

Faite le 11/11/2026 par un agent Claude qui cherche sur le web, sans passer par le script : les métadonnées d'Eurostat, la brève d'Eurostat du 10/03/2026, la presse relayant Eurostat.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, France 2026-09 | 45 525 | 45 525 (réponse de l'API le 11/11/2026, la valeur donnée par le PO) | API ci-dessus | Conforme (même source) |
| Union 2026-01 | 4 307 325 | « About 4.38 million » non-EU citizens who fled Ukraine, au 31/01/2026 | https://ec.europa.eu/eurostat/web/products-eurostat-news/w/ddn-20260310-1 | Écart expliqué : la brève compte tous les ressortissants de pays tiers fuyant l'Ukraine, le fichier les seuls citoyens ukrainiens (`citizen=UA`) ; le rapport exact des deux n'a pas été retrouvé |
| France, mineurs | note de la page | « France: data do not generally include minors. » | même brève | Conforme |
| France, variation d'avril 2026 | 48 550 en mars, 48 165 en avril, soit −385 (−0,8 %) | −440 (−0,9 %) d'après un résumé de recherche de la brève d'avril 2026, non ouverte | recherche web, brève d'Eurostat d'avril 2026 | Non trouvé en source ouverte : même ordre de grandeur, champ probablement différent (toutes nationalités) |
| Autre décompte français | — | 118 800 Ukrainiens adultes bénéficiaires de la protection temporaire en France depuis 2022 (ministère de l'Intérieur, résumé de recherche) | https://www.immigration.interieur.gouv.fr/documentation/etudes-et-statistiques/presence-des-ukrainiens-adultes-ayant-autorisation-de-sejour-en-france.html | Non vérifié : la page répond 403 aux scripts ; c'est un cumul d'adultes depuis 2022, non un stock de fin de mois, donc non comparable |

**Conclusion.** Les chiffres du fichier sont ceux d'Eurostat ; aucun recoupement indépendant exact n'a été possible, les autres décomptes (brèves d'Eurostat, ministère de l'Intérieur) ayant un champ différent.

**Pages consultées** le 11/11/2026 : l'API et les métadonnées d'Eurostat, la brève du 10/03/2026, des résumés de recherche web.

## Mises à jour

Aucune.

## Relecture

- [ ] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Partiel (voir ci-dessus).
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande (« Source : Eurostat », modifications signalées).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
