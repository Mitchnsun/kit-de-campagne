# `youthEurope` · Le chômage des jeunes en Europe (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart de valeur ; tous les rangs refaits sur les 27 valeurs d'Eurostat. Réserves reprises ci-dessous (définition différente pour la France, taux mensuel qui n'est pas celui de l'Insee). La licence des sources n'a pas été vérifiée (voir « Relecture »).

**Le 2e trimestre 2026.** Ce volet n'a aucune valeur du 2e trimestre 2026 (moyennes annuelles d'Eurostat ; le taux mensuel de septembre 2026 n'est que dans une note). La prochaine édition du kit remplacera les valeurs trimestrielles de l'Insee des volets `youthUnemployment` et `youthActivity`, publiées de nouveau le 10/11/2026.

| Champ | Valeur |
| --- | --- |
| Indicateur | `youthEurope`, dossier « Travail et retraites » (`work`), volet « En Europe » de la page composite `youthEmployment` (voir `youthEmployment.md`), page de type comparaison, recherche du 09/11/2026 |
| Données | `briefings/manual/youthEurope.json`, saisi à la main le 2026-11-09 depuis l'API d'Eurostat (valeurs relues par la contre-vérification ; les 27 valeurs de 2025 et les classements refaits par programme) |
| Sources | 1. Eurostat, « Unemployment by sex and age - annual data » (`une_rt_a`), https://ec.europa.eu/eurostat/databrowser/view/une_rt_a/default/table?lang=fr, API https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/une_rt_a?format=JSON&lang=en&sex=T&unit=PC_ACT&age=Y15-24&sinceTimePeriod=2015. 2. Eurostat, « Youth unemployment ratio by NUTS 2 region » (`yth_empl_140`, valeurs nationales sous le code du pays), https://ec.europa.eu/eurostat/databrowser/view/yth_empl_140/default/table?lang=fr. 3. Eurostat, « Young persons neither in employment nor in education and training by labour status (NEET rates) » (`edat_lfse_20`), https://ec.europa.eu/eurostat/databrowser/view/edat_lfse_20/default/table?lang=fr. 4. Eurostat, « Unemployment by sex and age - monthly data » (`une_rt_m`), https://ec.europa.eu/eurostat/databrowser/view/une_rt_m/default/table?lang=fr, pour la note sur le taux mensuel. Pages anglaises `?lang=en` ; licence Eurostat (« Source : Eurostat ») |
| Dates de publication | 2026-11-06 (`une_rt_a`) ; 2026-10-30 (`yth_empl_140`, `edat_lfse_20`) ; 2026-11-05 (`une_rt_m`) : dates de mise à jour des jeux de données |
| Séries | `franceRate` et `euRate` : taux de chômage des 15-24 ans, France et UE à 27, 2015 à 2025, 11 points chacune (France 26,2 puis 19,8 ; UE 22,4 puis 15,2). La France porte le drapeau « d » de 2021 à 2025, dit dans la note du bloc |
| Ventilations | `unemployment` (2025) : les 27 États membres, dans l'ordre de leur taux (Roumanie 26,1 … France 19,8, 7e … Allemagne 7,1). `ratio` (2025) : ratio de chômage des 15-24 ans (chômeurs / population) de la France (8,5), de l'UE à 27 (6,2, hachurée) et des sept pays que donne le rapport final : Suède 13,9, Finlande 11,7, Danemark 9,6, Estonie 8,9, Espagne 8,4, Italie 4,6, Allemagne 3,9. `neet` (2025) : NEET des 15-29 ans, les 27 États membres dans l'ordre (Roumanie 19,2 … France 12,9, 5e … Pays-Bas 5,3 ; ex æquo dans l'ordre de l'API : Estonie et Finlande 11,2, Chypre et Hongrie 10,6, Tchéquie et Portugal 8,0) |
| Chiffre clé | 19,8 % des actifs de 15 à 24 ans au chômage en France en 2025 selon Eurostat, en hausse (18,8 % en 2024) ; à côté, l'UE à 27, 15,2 % |
| Règles | Saisie à la main. Quatre vues : « Chômage, UE » (classement des 27), « Depuis 2015 » (France et UE, l'UE hachurée), « Ratio de chômage » (barres), « NEET, UE » (classement des 27). Les rangs sont ceux que l'app affiche en triant les valeurs, et les notes des blocs disent « rangs calculés » ; le rang de la France est dans « À savoir », avec « calculé ». Le ratio de chômage n'est pas classé : le rapport final ne donne que neuf de ses valeurs, le rang de la France (5e, calculé) est dans une note. Non saisis : le taux d'emploi des 15-24 ans par pays, le chômage selon le niveau d'éducation, le chômage des 15-74 ans, le NEET avant 2025, la comparaison de 2023 de la Cour des comptes (17,2 % et 14,5 %, révisés depuis par Eurostat) |
| Première édition | À remplir à la publication |

## « À savoir »

1. 19,8 % en France, 15,2 % dans l'UE à 27 en 2025 : le 7e taux le plus élevé des 27 (rang calculé), derrière la Roumanie, l'Espagne, la Suède, la Finlande, l'Estonie et l'Italie ; pour 2025, le taux d'Eurostat est celui de l'Insee. Source : `une_rt_a`, cellules 2025 (FR 19.8 « d » ; EU27_2020 15.2) ; classement refait sur les 27 valeurs, sans égalité touchant la France ; Insee Première 2096 (19,8 % en 2025).
2. Ratio de chômage de 8,5 % en France et de 6,2 % dans l'UE : 5e des 27 (rang calculé) ; même mesure que la part de chômage de l'Insee (8,5 % en 2025). Source : `yth_empl_140`, cellules 2025 (FR 8.5 ; EU27_2020 6.2) ; rang refait par la contre-vérification (Suède 13,9 ; Finlande 11,7 ; Danemark 9,6 ; Estonie 8,9 devant) ; égalité Roumanie-Irlande à 6,2 sans effet sur la France.
3. NEET de 12,9 % en France et de 11,0 % dans l'UE : 5e des 27 (rang calculé) ; à ne pas comparer au NEET trimestriel de l'Insee. Source : `edat_lfse_20` (wstatus=NEMP), cellules 2025 (FR 12.9 « d » ; EU27_2020 11.0) ; classement refait sur les 27 valeurs.
4. Définition différente pour la France signalée par Eurostat ; taux mensuel des moins de 25 ans de 21,9 % en septembre 2026, une estimation d'Eurostat, pas le taux trimestriel de l'Insee. Source : drapeau « d » des valeurs françaises (« definition differs (see metadata) ») ; `une_rt_m` (FR 2026-09 : 21.9 ; la Roumanie n'a plus de valeur depuis juillet 2026).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/youthEurope.json` (clé `claims`). Source de chaque chiffre de la réponse :

1. « On entend que la France a le pire chômage des jeunes d'Europe. » 19,8 % et 15,2 % (2025) : `une_rt_a`. 7e des 27, et les six pays au-dessus avec leur taux (26,1 ; 24,9 ; 24,3 ; 21,8 ; 20,7 ; 20,6) : classement calculé sur les 27 valeurs de `une_rt_a`, dit « calculé ». 8,5 % et 6,2 %, 5e rang : `yth_empl_140`, rang calculé. Définition différente : drapeau « d ». La phrase du rapport « Le taux français est supérieur à la moyenne de l'UE sans être le plus élevé » n'est pas reprise : elle redit les chiffres.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-jeunes.md` : API d'Eurostat rouverte, classements refaits par programme (`rank.py`) ; relus de nouveau le 09/11/2026 dans les fichiers JSON téléchargés : identiques.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 19,8 % (France, 2025) | `une_rt_a` FR 2025 19.8 « d » | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/une_rt_a?format=JSON&lang=en&sex=T&unit=PC_ACT&age=Y15-24&sinceTimePeriod=2015 | Conforme, avec réserve : définition différente |
| France et UE 2015-2025 | 2 × 11 valeurs | Valeurs de l'API relues | idem | Conforme |
| Classement du chômage | 27 valeurs, France 7e | 1 RO 26,1 … 7 FR 19,8 … 27 DE 7,1 ; aucune valeur manquante | idem | Conforme (rang calculé) |
| Ratio de chômage | 9 valeurs, France 5e | `yth_empl_140` 2025 : FR 8.5, EU27_2020 6.2, SE 13.9, FI 11.7, DK 9.6, EE 8.9, ES 8.4, IT 4.6, DE 3.9 | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/yth_empl_140?format=JSON&lang=en&sex=T&age=Y15-24&unit=PC&sinceTimePeriod=2019 | Conforme, avec réserve : jeu titré « par région NUTS 2 », valeurs nationales sous le code du pays |
| Classement des NEET | 27 valeurs, France 5e | 1 RO 19,2 … 5 FR 12,9 … 27 NL 5,3 ; ex æquo sans effet sur la France ; Danemark en rupture (« b ») | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/edat_lfse_20?format=JSON&lang=en&sex=T&age=Y15-29&wstatus=NEMP&training=NO_FE_NO_NFE&unit=PC&sinceTimePeriod=2010 | Conforme (rang calculé) |
| Taux mensuel (note) | 21,9 % (septembre 2026) | `une_rt_m` FR 2026-09 21.9 ; UE 15.5 | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/une_rt_m?format=JSON&lang=en&sex=T&unit=PC_ACT&age=Y_LT25&s_adj=SA&sinceTimePeriod=2026-01 | Conforme, avec réserve : estimation d'Eurostat, pas l'Insee |

**Conclusion.** Aucun chiffre du fichier n'est faux ; chaque rang est calculé et dit tel.

**Pages consultées** le 09/11/2026 : les API des URL ci-dessus.

## Réserves

- Eurostat signale une définition différente pour la France (et l'Espagne) : les blocs et une note le disent.
- Le taux mensuel d'Eurostat (21,9 % en septembre 2026) n'est pas le taux trimestriel de l'Insee (21,6 % au 2e trimestre 2026) : la page ne les rapproche pas.
- Le NEET d'Eurostat n'est pas celui de l'Insee (volet `youthActivity`).
- Le ratio de chômage n'est montré que pour neuf lignes : les 27 valeurs ne sont pas dans le rapport final.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert l'API d'Eurostat.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Eurostat : réutilisation permise, commerciale comprise, mention « Source : Eurostat » et modifications signalées (https://ec.europa.eu/eurostat/help/copyright-notice).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
