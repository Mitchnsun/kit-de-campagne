# `dataCentreConsumption` · La consommation d'électricité des data centers

**Vérifiée le 17/11/2026** : double vérification sur le web, sans écart non expliqué (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `dataCentreConsumption`, dossier « Écologie et énergie » (`ecology`), premier volet (« Consommation ») de la page composite `dataCentres` (voir `dataCentres.md`), page de type série |
| Données | `briefings/data/dataCentreConsumption.json`, écrit par `yarn briefings dataCentreConsumption` le 2026-11-17 |
| Sources | SDES, « La consommation d'électricité des data centers en 2024 », publiée le 02/07/2026, https://www.statistiques.developpement-durable.gouv.fr/la-consommation-delectricite-des-data-centers-en-2024 ; fichier « Données sur la consommation d'électricité des data centers en 2024 » (xlsx), https://www.statistiques.developpement-durable.gouv.fr/media/9471/download, feuille « Figure 1 ». Sources du SDES écrites sous le tableau : « SDES, Données locales de l'électricité ; ©Ademe-baseOPERAT. Traitement SDES ». Licence : mentions légales du SDES, « Les publications et données mises à disposition sur le site du service des données et études statistiques (SDES) sont consultables et téléchargeables gratuitement sous licence ouverte telle que décrite dans le décret n°2017-638 ; sauf spécification contraire, elles peuvent être réutilisées à des fins commerciales » ; mention : la source et la date de sa dernière mise à jour (Licence Ouverte 2.0, `etalab-2.0`, comme `energyMix`). Page en français seulement |
| Séries | Annuelles, 2018 à 2024, 7 points chacune, en TWh au GWh près (le fichier du SDES écrit des GWh avec décimales ; le script arrondit au GWh puis divise par 1 000) : `total` « Ensemble des centres de données » (3,311 en 2018 ; 4,052 en 2023 ; 4,339 en 2024), et les tranches de consommation annuelle du site, `under2` « Moins de 2 GWh », `from2To5`, `from5To10`, `from10To50`, `over50` « De 50 GWh à plus » (0,553 en 2018 ; 1,408 en 2024) |
| Chiffre clé | 4,339 TWh en 2024, écrit « 4,34 TWh » (la page écrit les séries au centième), en hausse (4,052 TWh en 2023) |
| Règles | Le script lit la page (date « Publié le », lien du classeur « Données sur la consommation d'électricité des data centers… »), puis la feuille « Figure 1 » : il échoue si le titre, le champ, l'en-tête, une année (consécutives depuis 2018) ou un libellé de tranche change, si une valeur manque, ou si les tranches ne font pas le total à 1 GWh près. Une nouvelle édition (nouvelle page) se met dans `PAGE` du script et dans le registre |
| Première édition | À remplir à la publication |

## « À savoir »

1. Champ et estimation de l'ensemble : 471 centres « dont la consommation dépasse 1 GWh par an au moins une année entre 2018 et 2024 » ; « au moins 200 centres de données plus modestes » ; « entre 4,3 et 6 TWh », « soit 1 à 1,5 % de l'électricité consommée en France ». Source : la page du SDES ci-dessus, section « Une consommation d'électricité en hausse de 7 % ».
2. Concentration : « 21 % de centres de données consomment à eux seuls 75 % », Île-de-France « 63 % » ; « les plus gros centres, dont la consommation a progressé de 155 % », « la consommation globale […] a progressé de 31 % » entre 2018 et 2024. Source : la même page (résumé et première section).
3. Méthode et révision : centres « dénombrés par le nombre de points de livraison d'électricité » (note de la figure 2) ; données locales d'Enedis et de RTE, à défaut OPERAT ou la base de la Commission européenne, années manquantes interpolées ou reconduites : « Méthodologie d'estimation de la consommation électrique des centres de données - Mai 2026 », https://www.statistiques.developpement-durable.gouv.fr/media/9472/download (section « Évolution par rapport à la précédente publication » : répertoire enrichi, consommation un peu augmentée pour toutes les années, puis diminuée par une méthode nouvelle). 2023 : 3 898,5 GWh dans le fichier de l'édition du 16/10/2025 (https://www.statistiques.developpement-durable.gouv.fr/media/8754/download, « Figure 1 », « Ensemble des centres de données »), 4 052,2 GWh dans celui de 2026.
4. Les estimations de RTE : « inférieur à 1 TWh en 2024 pour les seuls centres de données raccordés au réseau de transport ou de l'ordre de 4 à 5 TWh pour l'ensemble des centres de données sur sites dédiés (et entre 5 et 10 TWh en incluant les centres de données internes) ». Source : RTE, Bilan prévisionnel 2025-2035, chapitre « La consommation d'électricité » (23/12/2025), § 2.5.2, p. 27, https://assets.rte-france.com/prod/public/2025-12/2025-12-23-bilan-previsionnel-2025-consommation.pdf.

Les quatre points en anglais disent la même chose que le français.

## Double vérification

Faite le 17/11/2026 par un agent Claude (modèle Opus) : fichiers retéléchargés et relus (openpyxl, `pdftotext`, HTML nettoyé), puis recherche sur le web. Aucune reprise de presse des chiffres de l'édition 2026 n'a été trouvée : la vérification passe par d'autres publications du SDES.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé 2024 | 4,339 TWh | « 4,3 TWh », « 471 data centers » | Infographie du SDES, https://www.statistiques.developpement-durable.gouv.fr/media/9501/download | Conforme |
| Évolution 2023-2024 | 4,052 → 4,339 (+7,1 %) | « + 7 % » (infographie), « près de 7,1 % » (page) | idem ; page du SDES | Conforme |
| Évolution 2018-2024 | 3,311 → 4,339 (+31,0 %) | « + 31 % » | Infographie | Conforme |
| Tranche de plus de 50 GWh | 1,408 TWh en 2024 ; 0,553 en 2018 (+155 %) | « 1 408 GWh » (lecture de la figure 1) ; « 155 % » | Page du SDES | Conforme |
| Série 2018-2023 | 3,311 … 4,052 | Édition précédente : 3 211,7 … 3 898,5 GWh | https://www.statistiques.developpement-durable.gouv.fr/media/8754/download | Écart expliqué : révision de toute la série par le SDES (méthodologie de mai 2026), dite dans la note 3 |
| Licence | Licence Ouverte 2.0 | « licence ouverte telle que décrite dans le décret n°2017-638 » | https://www.statistiques.developpement-durable.gouv.fr/mentions-legales | Conforme |

**Conclusion.** Les valeurs sont celles du classeur du SDES de juillet 2026 ; toute la série a été révisée depuis l'édition d'octobre 2025, qui ne doit plus être citée.

**Pages consultées** le 17/11/2026 : les URL ci-dessus, et la page de l'édition précédente, https://www.statistiques.developpement-durable.gouv.fr/la-consommation-delectricite-des-centres-de-donnees-entre-2018-et-2023 (16/10/2025 ; son résumé écrit « en hausse de 21 % entre 2022 et 2023 » quand son tableur donne +1,5 % : une coquille de l'édition précédente, sans effet ici).

## Mises à jour

Aucune. À actualiser : la prochaine édition du SDES (non annoncée ; la précédente date d'octobre 2025, celle-ci de juillet 2026).

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
