# `pastSponsorships` · Les parrainages de 2022

**Vérifiée le 15/11/2026** : double vérification sur le web par un agent Claude (modèle Sonnet), 15/11/2026, sans écart non expliqué hors l'écart de 10 entre le ministère et le Conseil, signalé dans « À savoir » (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `pastSponsorships`, dossier « Institutions » (`institutions`), page de type comparaison, nature « scrutin historique » (vrais noms des candidatures retenues), ticket #444 de l'app |
| Données | `briefings/data/pastSponsorships.json`, écrit par `yarn briefings pastSponsorships` le 2026-11-16 (fichiers retéléchargés, empreintes SHA-1 conformes) |
| Sources | 1. Conseil constitutionnel, data.gouv.fr, « Parrainages des candidats à l'élection présidentielle française de 2022 », https://www.data.gouv.fr/datasets/parrainages-des-candidats-a-lelection-presidentielle-francaise-de-2022 (créé le 26/01/2022, dernière mise à jour le 07/03/2022 18:34), fichier JSON « Les parrainages au 07 mars 2022 » https://static.data.gouv.fr/resources/parrainages-des-candidats-a-lelection-presidentielle-francaise-de-2022/20220307-183354/parrainagestotal.json (SHA-1 `b6d4f770c5adc1dd2b69a23271cb6dd878af2d1c`, celle que déclare data.gouv.fr) ; 2. idem pour 2017, https://www.data.gouv.fr/datasets/parrainages-des-candidats-a-lelection-presidentielle-francaise-de-2017, CSV « Les parrainages au 18 mars 2017 » https://static.data.gouv.fr/resources/parrainages/20170320-103202/parrainagestotal.csv (SHA-1 `3c2ba4ec1b41af4feda29456bc5d3562443af22c`) ; 3. Conseil constitutionnel, décision n° 2022-198 PDR du 16 juin 2022, « Observations du Conseil constitutionnel sur l'élection présidentielle des 10 et 24 avril 2022 », https://www.conseil-constitutionnel.fr/decision/2022/2022198PDR.htm (PDF : …/bank_mm/decisions/2022198pdr/2022198pdr.pdf), p. 2. Licence des deux jeux : « Other (Public Domain) » (`other-pd`) sur data.gouv.fr ; le Conseil demande de citer le site comme source avec la date, l'intitulé et l'auteur, et de respecter l'intégrité des données (mentions légales, https://www.conseil-constitutionnel.fr/mentions-legales, lien « Conditions d'utilisation » de la page). La décision est citée (`citation-only`). Pages en français seulement |
| Séries | Annuelles (2017, 2022), en nombre : `validated` (14 296 ; 13 427, les lignes des fichiers), `received` (14 586 ; 13 672, décision n° 2022-198 PDR), `peopleSponsored` (61 ; 64 personnes ayant au moins un parrainage validé), `qualified` (11 ; 12 candidatures retenues). Quotidiennes, aux 11 dates de publication de 2022 : `publishedOnDay` (313, 1 756, 3 017, 1 139, 1 851, 593, 948, 648, 1 523, 963, 676) et `publishedCumulative` (313 au 01/02 … 13 427 au 07/03) |
| Répartitions | `byMandate2022` : maires 9 207, conseils départementaux 1 594, conseils régionaux et Assemblée de Corse 1 120, parlementaires 826, Parlement européen 66, autres mandats 614 ; `byMandate2017` : 10 310, 1 727, 1 101, 666, 60, 432 ; `qualifiedAndOthers2022` : candidatures retenues 12 195, autres personnes présentées 1 232 ; `mayorsQualifiedAndOthers2022` : 8 117 et 1 090 |
| Listes (vrais noms) | Les 12 candidatures de la décision n° 2022-187 PDR, noms tels que le Conseil les écrit (« PÉCRESSE Valérie »), l'app les affiche en casse normale, prénom d'abord : `byCandidate2022` (Pécresse 2 636 … Arthaud 576), `mayorsByCandidate2022` (1 373 … 312), `departmentsByCandidate2022` (107 … 75). Les 52 autres personnes ne sont jamais nommées |
| Chiffre clé | 13 427 parrainages validés en 2022, en baisse (14 296 en 2017) |
| Règles | Le script ne garde de chaque ligne que le mandat, le département ou la collectivité, la candidature et la date : jamais le nom, le prénom, la civilité ni la circonscription d'un parrain. « Maires » : maire, maire délégué ou déléguée, maire d'arrondissement ; l'Assemblée de Corse avec les conseils régionaux ; le Conseil de Paris, la métropole de Lyon, les présidences d'EPCI, les assemblées d'outre-mer, les Français de l'étranger et trois présidences d'exécutif en « autres mandats » (29 libellés en 2022, 24 en 2017, chacun dans une table). Il s'arrête si l'empreinte SHA-1 change (après trois nouvelles tentatives), si une clé (2022) ou l'en-tête (2017) diffère, si le nombre de lignes n'est pas 13 427 ou 14 296, si un mandat manque à la table, si un département n'est pas l'une des 110 valeurs connues de l'année (ou si l'une manque), si une date n'est pas l'une des 11 décisions de 2022 (6 en 2017), ou si les candidatures qui atteignent le seuil recalculé (500 parrainages, 30 départements ou collectivités, 50 au plus comptés par département) ne sont pas exactement les 12 de la décision n° 2022-187 PDR (les 11 de la liste du 18/03/2017). Chaque fichier est daté par la dernière date de publication qu'il contient. Jamais le jeu de 2027 |
| Ce que la page ne montre pas | Aucune vue par famille, aucune couleur de parti, aucun taux de rejet calculé (des valeurs cachées du moteur, `CAMP_FRACTION` et `invalidRate`, s'appuient sur ces fichiers, #145) ; pas de part des maires par candidature ; le repère de 500 est une règle de la loi, écrite dans l'app, pas un chiffre du fichier |
| Première édition | À remplir à la publication |

## « À savoir »

1. Reçus et validés. Source : décision n° 2022-198 PDR, p. 2 (« 13 672 formulaires ont été reçus (dont 13 427 validés), au lieu de 14 586 (dont 14 296 validés) en 2017 ») ; contrôles : site 2022 du Conseil, « Quels sont les contrôles opérés par le Conseil constitutionnel sur les parrainages ? », https://presidentielle2022.conseil-constitutionnel.fr/les-parrainages/parrainages-les-regles/quels-sont-les-controles-operes-par-le-conseil-constitutionnel-sur-les-parrainages.html (« porter une signature manuscrite ; être daté ; être entièrement rempli » ; « Seul le premier parrainage sera validé »). Les motifs de rejet ne sont pas chiffrés par le Conseil ; la note n'en calcule aucun taux.
2. Dates de publication, pas d'envoi. Source : colonne `DatePublication` du fichier (11 valeurs, les dates des décisions n° 2022-175 à 2022-186 PDR citées dans les visas de la décision n° 2022-187 PDR) ; « adressés à partir du 27 janvier 2022 et qui lui sont parvenus au plus tard le 4 mars 2022 à dix-huit heures » (décision n° 2022-187 PDR, https://www.conseil-constitutionnel.fr/sites/default/files/as/root/bank_mm/decisions/2022187pdr/2022187pdr.pdf).
3. La règle des 500. Source : loi n° 62-1292 du 6 novembre 1962, art. 3 I (Légifrance) ; site 2022 du Conseil (« ne tiendra compte que de 50 d'entre elles ») ; les Français de l'étranger et le Parlement européen sont chacun une valeur de « Département » du fichier.
4. Élus habilités, et l'écart de 10. Source : ministère de l'Intérieur, réponse à la question écrite n° 5709 (Viry), JO AN du 17/06/2025, p. 5261, https://www.assemblee-nationale.fr/dyn/17/questions/QANR5L17QE5709 (« En 2022, 13 437 élus, soit environ 32 % des 42 000 élus habilités ont effectivement parrainé une candidate ou un candidat (contre 34% en 2017 et 36 % en 2012) »). Le Conseil et le fichier comptent 13 427 parrainages validés ; 13 437 et 13 427 font tous deux 32,0 % de 42 000 : l'écart n'est pas départageable, la page cite le Conseil.

Les points en anglais disent la même chose que le français.

## « Ce qu'on entend »

Proposées par la recherche du 15/11/2026 (§ 2.5), chacune réfutée par les chiffres du fichier du Conseil. Une quatrième, « la publicité des parrainages a fait fuir les élus », n'est pas retenue : le Conseil y répond par les formulaires reçus (13 672 contre 14 586), mais la part d'élus qui parrainent baisse (36 %, 34 %, 32 %, ministère) ; les chiffres nuancent plus qu'ils ne réfutent.

1. « Il faut 500 signatures de maires. » Réponse : 9 207 des 13 427 parrainages validés venaient de maires (délégués et d'arrondissement compris), les autres de cinq autres groupes de mandats. Source : fichier de 2022.
2. « Les parrainages restent secrets. » Réponse : le fichier publie le nom et le mandat de chaque parrain ; 11 dates de publication en 2022. Source : fichier de 2022 (la page n'en montre aucun nom).
3. « Une candidature peut trouver ses 500 parrainages dans une seule région. » Réponse : 30 départements ou collectivités au moins, 50 comptés au plus par département ; les 12 candidatures retenues en avaient dans 75 à 107. Source : site 2022 du Conseil ; fichier de 2022.

## Double vérification

Faite le 15/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, fichiers retéléchargés et recomptés à part (Python), sans passer par le script : les décisions du Conseil sur son miroir officiel (`webview-ccfr.sites.prod.conseilconstitutionnel.aquaray.com`, mêmes chemins que `www.conseil-constitutionnel.fr`, qui coupe la connexion), l'API de data.gouv.fr, la réponse ministérielle, la presse.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Lignes 2022 (chiffre clé) | 13 427 | 13 427 ; « 13 672 formulaires ont été reçus (dont 13 427 validés) » ; Politis et Maire-info (recherche) : 13 672 / 13 427 | JSON data.gouv.fr ; décision n° 2022-198 PDR, p. 2 | Conforme |
| Reçus / validés 2017 | 14 586 / 14 296 | « au lieu de 14 586 (dont 14 296 validés) en 2017 » ; 14 296 lignes dans le CSV de 2017 | décision n° 2022-198 PDR ; CSV 2017 | Conforme |
| Personnes présentées | 64 (2022), 61 (2017) | 64 ; 61 | JSON 2022 ; CSV 2017 | Conforme |
| Candidatures retenues | 12 ; 11 | « douze candidats contre onze candidats en 2017 » ; seuil recalculé : les 12 de la décision n° 2022-187 PDR, les 11 de 2017 (Yade, 12e nom, sous le seuil) | décisions n° 2022-198 et 2022-187 PDR ; CSV 2017 | Conforme |
| Départements ou collectivités | 110 valeurs (101 + 9) | 110 | JSON 2022 | Conforme |
| Dates de publication 2022 | 11, du 01/02 au 07/03 ; 313, 1 756, 3 017, 1 139, 1 851, 593, 948, 648, 1 523, 963, 676 | identiques ; cumul 313, 2 069, 5 086, …, 10 265 (24/02), 12 751 (03/03), 13 427 | JSON 2022 | Conforme |
| Instantanés du 24/02 et du 03/03 | cumuls 10 265 et 12 751 | égaux aux nombres de lignes des fichiers de ces dates (fichiers intermédiaires non téléchargés par la vérification) | JSON final | Conforme (indirect) |
| Totaux des 12 candidatures | Pécresse 2 636, Macron 2 098, Hidalgo 1 440, Mélenchon 906, Zemmour 741, Jadot 712, Lassalle 642, Roussel 626, Le Pen 622, Dupont-Aignan 600, Poutou 596, Arthaud 576 | identiques | JSON 2022 | Conforme |
| Maires par candidature | 1 373, 1 296, 712, 698, 671, 312, 623, 408, 313, 591, 545, 575 | identiques (maire au sens large) | JSON 2022 | Conforme |
| Départements par candidature | 107, 107, 96, 104, 95, 98, 86, 95, 101, 84, 91, 75 | identiques | JSON 2022 | Conforme |
| Maires, ensemble | 9 207 | 8 712 maires + 27 d'arrondissement + 468 délégués (345 + 123) | JSON 2022 | Conforme |
| Mandats 2022 | 1 594 ; 1 120 ; 826 ; 66 ; 614 | 740 + 854 ; 511 + 581 + 28 ; 309 + 221 + 191 + 105 ; 33 + 33 ; Paris 131, Lyon 106, EPCI 74, outre-mer 150, AFE 69, consulaires 81, exécutifs 3 | JSON 2022 | Conforme |
| Mandats distincts | 29 libellés | 29 | JSON 2022 | Conforme |
| Maires 2017 | 10 310 | 10 310 | CSV 2017 | Conforme |
| Plus de 50 dans un département | publiés et comptés dans le total | Pécresse 9 départements (Seine-et-Marne 105), Macron 5 (Polynésie 110), Hidalgo 7, Jadot 1 (Rhône 70) | JSON 2022 | Conforme |
| « Communes et intercommunalités » | non montré | 69,1 % (maires et présidences d'EPCI, 9 281) ; 70,9 % seulement avec le Conseil de Paris et la métropole de Lyon ; le ministère écrit « près des trois quarts » | JSON 2022 ; QE n° 5709 | Écart expliqué : la page et les notes n'emploient pas ce pourcentage |
| 42 000 ; 32 / 34 / 36 % | note 4 | « environ 32 % des 42 000 élus habilités … (contre 34% en 2017 et 36 % en 2012) » | QE n° 5709, PDF de l'Assemblée nationale | Conforme |
| 13 437 contre 13 427 | note 4 | le ministère écrit 13 437 ; 13 437 / 42 000 et 13 427 / 42 000 font tous deux 32,0 % ; aucune explication trouvée | QE n° 5709 | Écart (non expliqué, dit dans la note ; la page cite le Conseil) |
| Licence | « Other (Public Domain) » | API data.gouv.fr : `license: other-pd` ; dernière mise à jour 2022-03-07 18:34 | https://www.data.gouv.fr/api/1/datasets/parrainages-des-candidats-a-lelection-presidentielle-francaise-de-2022/ | Conforme |
| Empreintes | b6d4f770… ; 3c2ba4ec… | égales à l'API et aux fichiers téléchargés (et au CSV de 2022, 637d2b29…, même contenu) | API data.gouv.fr | Conforme |
| Dates de réception (27/01 au 04/03 18 h) | note 2 | non rouvertes par la vérification ; citées mot pour mot par la recherche dans la décision n° 2022-187 PDR, relue le 16/11/2026 à la construction de la page | décision n° 2022-187 PDR | Conforme (relu) |

Relu le 16/11/2026 à la construction de la page : les deux fichiers retéléchargés par le script, empreintes SHA-1 conformes, et le fichier du kit identique à celui que donnent les fichiers de la recherche ; la décision n° 2022-187 PDR (liste et visas) et la p. 2 de la décision n° 2022-198 PDR relues dans les copies de la recherche. Aucun chiffre hors de la recherche et de sa vérification.

**Conclusion.** Tous les comptes du fichier sont ceux du Conseil, recomptés deux fois ; seul l'écart de 10 entre le ministère et le Conseil reste sans explication, et la page cite le Conseil.

**Pages consultées** (le 15/11/2026, et le 16/11/2026 pour les deux fichiers) :

- https://static.data.gouv.fr/resources/parrainages-des-candidats-a-lelection-presidentielle-francaise-de-2022/20220307-183354/parrainagestotal.json et `…/20220307-183308/parrainagestotal.csv`
- https://static.data.gouv.fr/resources/parrainages/20170320-103202/parrainagestotal.csv
- https://www.data.gouv.fr/api/1/datasets/parrainages-des-candidats-a-lelection-presidentielle-francaise-de-2022/ et `…-de-2017/`
- le miroir officiel du Conseil constitutionnel : décisions n° 2022-187 PDR et n° 2022-198 PDR (PDF), `/decision/2017/2017172PDR.htm`, `/mentions-legales`
- https://presidentielle2022.conseil-constitutionnel.fr/ (« Qui peut parrainer un candidat », « Quels sont les contrôles opérés… »)
- https://www.assemblee-nationale.fr/dyn/17/questions/QANR5L17QE5709.pdf
- recherches web : Politis, Maire-info (13 672 / 13 427)

## Mises à jour

Aucune. Les jeux de 2017 et de 2022 sont figés : le script échoue si leur empreinte change. Les parrainages de 2027 n'entrent pas dans les Dossiers.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO (dont les trois affirmations de « Ce qu'on entend »).
