# `genderPayGap` · L'égalité salariale

**Vérifiée le 15/11/2026** : double vérification sur le web par un agent Claude (modèle Sonnet), 15/11/2026, sans écart non expliqué (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `genderPayGap`, dossier « Travail et retraites » (`work`), page de type série, ticket #441 de l'app |
| Données | `briefings/data/genderPayGap.json`, écrit par `yarn briefings genderPayGap` le 2026-11-16 |
| Sources | Insee, « Écart de salaire entre femmes et hommes en 2024 – La réduction des écarts de salaires se poursuit à un rythme proche de sa tendance sur longue période », Insee Focus n° 377 (Mathilde Gerardin, paru le 26/02/2026), https://www.insee.fr/fr/statistiques/8743657, en français seulement (https://www.insee.fr/en/statistiques/8743657 répond 404) ; fichier https://www.insee.fr/fr/statistiques/fichier/8743657/if377.xlsx, feuille « Figure 1a » ; Licence Ouverte 2.0 (Etalab), mention « Source : Insee » (https://www.insee.fr/fr/information/2008466) ; daté par le « Paru le » de la page |
| Séries | Écarts entre femmes et hommes dans le secteur privé, en %, annuels. `fullTimeEquivalentGap` : salaire net en équivalent temps plein (EQTP), 1995 à 2024, 30 points (1995 : 22,1 ; 2012 : 19,8 ; 2023 : 14,2 ; 2024 : 14,0), ruptures 2002 et 2012. `salaryIncomeGap` : revenu salarial, 30 points (33,7 ; 29,7 ; 22,2 ; 21,8), ruptures 2002 et 2012. `workVolumeGap` : volume de travail annuel, 30 points (14,9 ; 12,4 ; 9,3 ; 9,1), rupture 2002. `comparableJobGap` : écart « à emploi comparable », 2024 seulement, 3,6 (texte de la page, pas une série) |
| Chiffre clé | 14,0 % en 2024, en baisse (14,2 % en 2023) ; à côté, chacun avec sa définition et son champ : 21,8 % (revenu salarial) et 3,6 % (à emploi comparable) |
| Règles | Ancienne série jusqu'en 2011, nouvelle série dès 2012, comme les colonnes « Ancienne série » et « Nouvelle série » de la feuille ; les deux valeurs de 2012 sont exigées (EQTP 19,7 et 19,8, revenu salarial 29,5 et 29,7), l'ancienne n'est dite que dans « À savoir ». Ruptures : 2002 (France métropolitaine, puis France hors Mayotte) et 2012 (complémentaire santé obligatoire dans les salaires). Le script échoue si le titre A1, les en-têtes A3 à F4 ou les notes (champ, lissage de 2002 à 2006, complémentaire santé, effet faible sur les écarts) changent, si une année manque depuis 1995, si une valeur n'est pas un nombre ou sort de sa série, si la ligne de lecture (A36) ne dit pas les chiffres de la dernière année, ou si le texte de la page ne donne plus l'écart « à emploi comparable » de cette année, estimé sur 25 % des établissements, avec la mise en garde de l'Insee sur la discrimination. Chaque édition a une nouvelle page et un nouveau fichier (`8381248/if349.xlsx`, puis `8743657/if377.xlsx`) : constante `FOCUS` du script, à changer à la prochaine édition, vers février ou mars 2027 |
| Première édition | À remplir à la publication |

## « À savoir »

1. Le salaire en EQTP n'est pas celui des seuls temps pleins ; le revenu salarial compte le temps travaillé (9,1 %). Source : « Définitions » de la page (« un salaire converti à un temps plein pendant toute l'année, quel que soit le volume de travail effectif […] tous les postes y compris les postes à temps partiel sont pris en compte au prorata de leur volume de travail effectivement rémunéré ») ; texte (« le volume de travail annuel des femmes est inférieur de 9,1 % à celui des hommes en 2024 ») ; feuille « Figure 1a », F34.
2. Le piège du 3,6 %. Source : texte de la page (« l'écart de salaire net en EQTP « à emploi comparable » est estimé à 3,6 % en 2024. Ce chiffre résulte d'une estimation sur une partie seulement du secteur privé (25 % des établissements représentant 40 % des EQTP) » ; « ne peut pas être interprété au sens strict comme une mesure de la discrimination salariale […] comme l'expérience, l'ancienneté dans l'entreprise ou le niveau de diplôme ») ; 13,0 % : feuille « Figure 2 », D33, et texte (« Sur un champ légèrement différent […] 13,0 % en 2024 »).
3. Les ruptures et les deux valeurs de 2012. Source : notes A35 et A37 de la feuille « Figure 1a » ; ligne 22 (2012), colonnes B à E.
4. Le secteur privé seulement. Source : champ A37 de la feuille « Figure 1a » ; l'analyse étendue au public, annoncée par la page « Inégalités femmes-hommes − 2027 : la statistique publique au service des débats », Insee, 15/10/2026, https://www.insee.fr/fr/statistiques/8996936?sommaire=8996963 (« sera étendue aux secteurs privés et publics début décembre 2026 lors de la parution de l'Insee Références France, Portrait Social »). À relire avant l'édition suivante.

Les points en anglais disent la même chose que le français.

## « Ce qu'on entend »

Proposées par la recherche du 15/11/2026, qui les marque « à valider » : aucune source consultée ne montre qui les dit, ce sont des formules qui circulent. À confirmer par le PO.

1. « À travail égal, les femmes sont payées 22 % de moins. » Réponse par les trois écarts de la page, chacun avec sa définition : 21,8 % de revenu salarial (temps de travail compris), 14,0 % en EQTP, 3,6 % à emploi comparable, sur un quart des établissements et un autre champ. Source : chapeau et texte de la page.
2. « À poste égal, il n'y a plus d'écart de salaire. » Réponse : 3,6 % à emploi comparable en 2024, 14,0 % en EQTP tous emplois confondus. Source : chapeau et texte de la page.

## Double vérification

Faite le 15/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, fichiers retéléchargés et relus (openpyxl, HTML nettoyé) : la page et le fichier du Focus n° 377, l'édition précédente (Focus n° 349), Eurostat, la presse.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Les trois séries, 1995 à 2024 | 30 années × 5 colonnes (revenu salarial et EQTP en ancienne et nouvelle série, volume de travail) | comparées cellule par cellule : aucune différence (1995 : 33,7 / 22,1 / 14,9 ; 2012 : 29,5 et 29,7 / 19,7 et 19,8 / 12,4 ; 2024 : 21,8 / 14,0 / 9,1) | https://www.insee.fr/fr/statistiques/fichier/8743657/if377.xlsx, feuille « Figure 1a », A5:F34 | Conforme |
| Chiffre clé, 2024 | 14,0 | chapeau : « même à temps de travail identique, le salaire moyen des femmes est inférieur à celui des hommes, de 14,0 % » | https://www.insee.fr/fr/statistiques/8743657 | Conforme |
| Revenu salarial et volume de travail, 2024 | 21,8 ; 9,1 | 21,8 % (22 060 € contre 28 220 €, figure 1b) ; 9,1 % (0,71 contre 0,78 EQTP, figure 1d) | if377.xlsx, figures 1b et 1d | Conforme |
| Années 1995 à 2023 | séries du fichier | Focus n° 349 (paru le 04/03/2025) : identiques cellule par cellule ; 2023 : 22,2 / 14,2 / 9,3 | https://www.insee.fr/fr/statistiques/fichier/8381248/if349.xlsx ; https://www.insee.fr/fr/statistiques/8381248 | Conforme |
| Ruptures et lissage | 2002, 2012 ; lissage de 2002 à 2006 dans « À savoir » | notes A35 (lissage, complémentaire santé obligatoire, « faible sur les écarts ») et A37 (champ) | if377.xlsx, feuille « Figure 1a » | Conforme |
| Écart à emploi comparable | 3,6 (2024) | « estimé à 3,6 % en 2024 », « 25 % des établissements représentant 40 % des EQTP », « ne peut pas être interprété […] comme une mesure de la discrimination salariale » | page du Focus n° 377 | Conforme |
| Écart en EQTP du champ de la figure 2 | 13,0 (« À savoir ») | ligne « Ensemble » : 2 514 €, 2 891 €, 13,0 | if377.xlsx, feuille « Figure 2 », D33 | Conforme |
| L'écart à emploi comparable n'est pas une série | 2024 seulement | 3,8 % en 2023 (Focus n° 349), sur des champs que l'Insee dit « pas complètement comparables » (« Méthodes » du n° 377) | pages des Focus n° 349 et n° 377 | Conforme (le fichier n'en garde que la dernière année) |
| Ordre de grandeur, autre définition | 14,0 (2024) | Eurostat, écart de rémunération non ajusté (`earn_gr_gpgr2`), France : 11,8 en 2024 (provisoire), 12,3 en 2023 (provisoire) ; UE à 27 : 11,1 en 2024 (provisoire) ; mise à jour du 27/10/2026 | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/earn_gr_gpgr2?format=JSON&geo=FR&geo=EU27_2020&nace_r2=B-S_X_O&sinceTimePeriod=2018&lang=en | Écart expliqué : une autre mesure (salaire horaire brut, entreprises de 10 salariés ou plus, administration publique exclue), ni montrée sur la page ni comparée dans une note |
| Reprise par la presse | 14,0 | Carenews, 04/03/2026 : « Les femmes gagnent en moyenne 14 % de moins que les hommes pour le même temps de travail, selon l'Insee » | https://www.carenews.com/carenews-info/news/les-femmes-gagnent-en-moyenne-14-de-moins-que-les-hommes-pour-le-meme-temps-de | Conforme |
| Reprise par l'Insee pour la campagne | chapeau | « Paru le 15/10/2026 », chapeau du n° 377 repris, analyse public et privé annoncée pour début décembre 2026 | https://www.insee.fr/fr/statistiques/8996936?sommaire=8996963 | Conforme |
| Page en anglais | aucune | 404 | https://www.insee.fr/en/statistiques/8743657 | Conforme (`frenchOnly`) |
| Licence | Licence Ouverte 2.0 | « Licence Ouverte / Open Licence version 2.0 (Etalab) […] mentionner la source sous la forme « Source : Insee » » | https://www.insee.fr/fr/information/2008466 | Conforme |

Relu le 16/11/2026 à la construction de la page : la page et le fichier retéléchargés, le fichier du kit comparé cellule par cellule à la feuille « Figure 1a » (aucune différence), « Paru le 26/02/2026 » sur la page. Aucun chiffre hors de la recherche et de sa vérification.

**Conclusion.** Les trois séries sont celles du Focus n° 377, sans révision depuis le n° 349 ; le chiffre d'Eurostat, plus bas, mesure autre chose.

**Pages consultées** (le 15/11/2026, et le 16/11/2026 pour la page et le fichier du n° 377) :

- https://www.insee.fr/fr/statistiques/8743657 et son fichier `if377.xlsx`
- https://www.insee.fr/en/statistiques/8743657 (404)
- https://www.insee.fr/fr/statistiques/8381248 et son fichier `if349.xlsx`
- https://www.insee.fr/fr/statistiques/8996936?sommaire=8996963
- https://www.insee.fr/fr/information/2008466
- l'API d'Eurostat, `earn_gr_gpgr2` (adresse ci-dessus)
- l'article de Carenews du 04/03/2026 (adresse ci-dessus)

## Mises à jour

- **16/11/2026** (Mitchnsun/moi-president#457) : notes « À savoir » relues (revue d'un joueur, réécriture, recherches et contre-vérification par des agents Claude, modèle Sonnet, validées par le PO) ; notes (← ancien numéro) : 1 ← 2, 2 ← 1 réécrite, 3 ← 4 réécrite, 4 ← 3.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO (dont les deux affirmations de « Ce qu'on entend »).
