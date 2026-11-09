# `nonTakeUp` · Les aides non réclamées (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; réserves de lecture reprises dans « À savoir », dans les notes des blocs et dans « Ce qu'on entend ». L'étude de la DREES de mai 2026 sur le RSA n'est pas saisie : elle attend que l'original soit ouvert sur le site de la DREES (voir « En attente »). La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `nonTakeUp`, dossier « Économie et fiscalité » (`economy`), aussi dans « Pouvoir d'achat » (`alsoIn: ['purchasingPower']`), page de type comparaison |
| Données | `briefings/manual/nonTakeUp.json`, saisi à la main le 2026-11-09 depuis une présentation de la DREES au Conseil d'orientation des retraites, le rapport annuel 2025 de la complémentaire santé solidaire, deux rapports d'information parlementaires et un rapport du Défenseur des droits |
| Sources | 1. DREES, « Estimer le non-recours au minimum vieillesse » (présentation au COR, 20/10/2022, diapositives 8 et 11), https://www.cor-retraites.fr/sites/default/files/2022-10/4%20Pr%C3%A9sentation%20DREES%20Estimer%20le%20non-recours%20aux%20prestations%20vieillesse.pdf ; 2. Direction de la sécurité sociale, « La complémentaire santé solidaire, rapport annuel 2025 » (p. 33, tableau 2), https://complementaire-sante-solidaire.gouv.fr/sites/default/files/2026-01/Rapport%20annuel%20C2S%202025.pdf ; 3. Sénat, rapport d'information n° 836 (2022-2023) sur la mise en œuvre de la solidarité à la source (5 juillet 2023, p. 32), https://www.senat.fr/rap/r22-836/r22-8361.pdf ; 4. Assemblée nationale, rapport d'information n° 4158 sur l'évaluation des politiques publiques en faveur de l'accès aux droits sociaux (26 octobre 2016, p. 59 et 172), https://www.assemblee-nationale.fr/14/pdf/rap-info/i4158.pdf ; 5. Défenseur des droits, « La lutte contre la fraude aux prestations sociales à l'ère de son industrialisation » (avril 2026, p. 6 et note 21), https://www.defenseurdesdroits.fr/sites/default/files/2026-04/ddd_rapport_fraude-prestations-sociales-2026_20260410.pdf. Licence « citation seule » pour les cinq, en français seulement |
| Dates de publication | 2022-10-20 (DREES, date de la présentation) ; 2025-12-09 (rapport de la C2S : date de création du PDF, mis en ligne en janvier 2026 d'après le chemin du fichier, date exacte de mise en ligne non trouvée) ; 2023-07-05 (Sénat) ; 2016-10-26 (Assemblée nationale) ; 2026-04-10 (Défenseur des droits, date du nom du fichier) |
| Séries | `aspaNonTakeUp` : taux de non-recours au minimum vieillesse des personnes seules, %, fin 2016, 1 point (49,6), diapositive 8 ; `rsaNonTakeUp` : taux de non-recours au RSA, % des foyers éligibles en moyenne par trimestre, 2018, 1 point (34), DREES (Dossiers n° 92) citée par le Sénat, seconde main ; `c2sTakeUp`, `c2sFreeTakeUp`, `c2sParticipativeTakeUp` : taux de **recours** à la C2S, ensemble, gratuite et avec participation, % des personnes éligibles, 2019 à 2021, 3 points chacun (54, 55, 56 ; 67, 69, 69 ; 28, 29, 34), tableau 2 |
| Chiffre clé | 49,6 % de non-recours au minimum vieillesse parmi les personnes seules éligibles, fin 2016, sans tendance (un seul point) |
| Règles | Saisie à la main. Chaque prestation est une série à part, avec son année : les blocs groupent par année (`periods`), jamais deux années côte à côte sans le dire. La C2S est publiée en taux de recours : le non-recours (44, 31 et 66 % en 2021) est **calculé** (100 moins le recours) et n'apparaît que dans la note du bloc, avec le mot « calculé ». Les montants (790 M€ pour le minimum vieillesse, 750 M€ par trimestre pour le RSA) et la fourchette de l'assurance chômage (25 à 42 %) sont dans les notes, pas dans des barres. La comparaison avec la fraude est seulement celle du rapport n° 4158, comme l'estimation de ses deux rapporteurs, dans une note ; jamais face aux 14 Md€ de fraude évaluée par le HCFiPS, qu'aucune source officielle ne met en regard du non-recours. Aucun montant de presse n'est saisi |
| Première édition | À remplir à la publication |

## « À savoir »

1. Selon la DREES, les montants liés au non-recours au minimum vieillesse des personnes seules s'élèvent à 790 M€ fin 2016, soit 59 % de ce qui leur est effectivement versé ; la source ne dit pas sur quelle durée. Pour le RSA, les sommes non versées atteindraient 750 M€ par trimestre en 2018 (DREES, citée par le Sénat). Sources : DREES, présentation au COR, diapositive 11 (« Fin 2016, les montants estimés liés au non-recours à l'Aspa […] s'élèvent à 790 millions d'euros, soit 59 % des montants effectivement versés aux personnes seules au titre du MV. » ; la diapositive n'écrit pas « par an », la note ne le dit donc pas) ; Sénat n° 836, p. 32 (« les sommes non versées du fait du non-recours au RSA atteindraient 750 millions d'euros par trimestre, soit 3 milliards d'euros par an » ; seule la valeur trimestrielle est reprise : on ne sait pas si l'annualisation vient de la DREES ou du Sénat).
2. En 2016, les deux rapporteurs d'un rapport de l'Assemblée nationale estimaient le non-recours entre 2 et 3 Md€ par an, en « ordres de grandeur », face à 425 M€ de fraude sociale détectée en 2014. Une estimation de droits non demandés face à un montant détecté : les deux ne mesurent pas la même chose. Source : rapport n° 4158, p. 172 (« Faute de chiffres précis, nous nous sommes bornés à établir des ordres de grandeur. Le montant du non-recours peut être estimé entre 2 et 3 milliards d'euros par an ; cette donnée est à comparer avec le montant de la fraude sociale détectée, estimée à 425 millions d'euros. ») et p. 59 (« la fraude sociale détectée qui a atteint 425 millions d'euros en 2014 »). La p. 172 écrit « estimée » pour la fraude, la p. 59 « détectée » : la note retient « détectée ».
3. Selon la Dares, citée par le Défenseur des droits (avril 2026), le non-recours à l'assurance chômage varie entre 25 et 42 % des salariés éligibles. Ni la période ni les effectifs ne sont précisés. Source : Défenseur des droits, p. 6 (« celui de non recours à l'assurance chômage, qui varie entre 25 et 42 % des salariés éligibles » ; note 21 : « DARES, Quantifier le non recours à l'assurance chômage, document d'études, 2022, n°263 »). Seconde main : le document de la Dares n'a pas pu être ouvert.

Les trois points en anglais disent la même chose que le français.

Notes des blocs (dans l'app) : le bloc du RSA et du minimum vieillesse dit qu'il s'agit d'estimations de la DREES (citée par le Sénat pour le RSA), en foyers par trimestre pour le RSA (20 % trois trimestres de suite, Sénat n° 836, p. 32 : « 20 % de façon pérenne (trois trimestre consécutifs) ») et en personnes seules pour le minimum vieillesse, et que les deux taux ne se comparent pas ; le bloc de la C2S dit le non-recours calculé de 2021 et que 2022 et 2023 ne sont pas encore estimés (rapport de la C2S, p. 33 : « Le taux de recours estimé pour l'ensemble du dispositif n'a pas pu être calculé pour les années 2022 et 2023, les travaux sont toutefois en cours. »).

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/nonTakeUp.json` (clé `claims`, français et anglais). Ne restent que les fausses vérités que les chiffres de la page démentent (décision du PO du 09/11/2026). Source de chaque chiffre de la réponse :

1. « On entend que tous ceux qui ont droit au RSA le touchent. » 34 % des foyers éligibles en moyenne par trimestre en 2018, 20 % trois trimestres de suite : DREES (Dossiers n° 92, février 2022), citée par le Sénat, rapport n° 836, p. 32. Seconde main. La réponse du rapport de recherche citait l'étude de la DREES de mai 2026 (33 à 37 %, 560 000 foyers) : remplacée par le chiffre de 2018, l'étude de 2026 étant en attente.
2. « On entend que le non-recours ne représente presque rien en euros. » 790 M€ fin 2016 et 59 % des montants versés aux personnes seules : DREES, présentation au COR, diapositive 11. 750 M€ par trimestre en 2018 : Sénat n° 836, p. 32, d'après la DREES. La réponse du rapport de recherche citait 630 M€ par trimestre et 29 à 32 % en masse financière (étude de mai 2026) : non repris, en attente.
3. « On entend que les personnes âgées modestes touchent toutes le minimum vieillesse. » 49,6 % des personnes seules éligibles fin 2016 : DREES, présentation au COR, diapositive 8 (« Le taux de non-recours des personnes seules au MV est estimé à 49,6 % fin 2016. »). Les couples ne sont pas couverts (champ de l'estimation : personnes seules).

Affirmation du rapport de recherche non retenue : « On entend que la solidarité à la source a déjà réglé le non-recours. » La Cour des comptes écrit qu'il est « trop tôt » pour en faire le bilan, et la Cnaf donne les résultats d'une campagne (près de 100 000 personnes informées, 10 500 bénéficiaires) : ces chiffres disent qu'aucune mesure n'existe encore, ils ne démentent pas l'affirmation.

## En attente

- **DREES, Études et résultats n° 1370, « Non-recours au RSA : plus d'un tiers des foyers éligibles ne le percevaient pas fin 2021 » (mai 2026)** : 33 à 37 % des foyers éligibles fin 2021, 560 000 foyers (environ un million de personnes), une dépense supplémentaire d'environ 630 M€ par trimestre (626 M€ au tableau 1), 29 à 32 % en masse financière. Lu seulement dans une copie publiée par Le Media social et repris par Localtis ; le site de la DREES n'a pas pu être ouvert (réponse vide, erreur 503). À confirmer par l'utilisateur sur https://drees.solidarites-sante.gouv.fr/publications-communique-de-presse/etudes-et-resultats/260506-non-recours-au-rsa-fin-2021 (PDF identique à la copie, date de publication) avant d'entrer dans les fichiers de données, les notes ou les affirmations. Une fois confirmé, il serait une série à part (fin 2021), jamais raccordée aux 34 % de 2018 ni aux 750 M€ par trimestre (autre méthode).
- **DREES, Études et résultats n° 1379 (juillet 2026), non-recours à la prime d'activité** : aucun chiffre retenu (vu seulement dans la presse), https://www.drees.solidarites-sante.gouv.fr/sites/default/files/2026-07/ER1379_Non-recours_PA.pdf.
- **DREES, Dossier n° 97 (mai 2022)** : dire si les 790 M€ du minimum vieillesse sont annuels, https://drees.solidarites-sante.gouv.fr/sites/default/files/2022-05/Dossier%20de%20la%20DREES%20-%20Non%20recours%20au%20MV.pdf.
- **DREES, Dossier n° 92 (février 2022)** : la source première des 34 % et des 750 M€ par trimestre de 2018, https://drees.solidarites-sante.gouv.fr/sites/default/files/2022-02/DD92.pdf.
- **Dares, Document d'études n° 263 (2022)** : période, champ et éventuel montant du non-recours à l'assurance chômage, sur https://dares.travail-emploi.gouv.fr/.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web (rapport `verify-nonrecours-arrets.md`) : chaque document rouvert et relu au texte (`pdftotext`). Aucun écart de valeur ; les verdicts sont ceux du rapport.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, minimum vieillesse | 49,6 % (fin 2016) | 49,6 %, diapositive 8 ; le Défenseur des droits (2026) reprend « 50 % » d'après la DREES | présentation de la DREES au COR (URL ci-dessus) | Conforme avec réserve : estimation ancienne, personnes seules seulement, présentation et non publication écrite |
| Montants, minimum vieillesse | 790 M€, 59 % (note) | 790 M€ et 59 % (fin 2016), 1 090 M€ en extrapolant, 830 M€ fin 2012 (69 %) | diapositive 11 (URL ci-dessus) | Conforme avec réserve : « par an » non écrit ; 1 090 M€ et 2012 non saisis (méthode peut-être différente, aucune tendance tirée) |
| RSA 2018 | 34 % ; 20 % pérenne ; 750 M€ par trimestre (notes) | phrases relues dans le rapport du Sénat | https://www.senat.fr/rap/r22-836/r22-8361.pdf | Conforme avec réserve : seconde main ; « soit 3 milliards par an » d'origine inconnue, non repris ; page 32 lue au repère « - 32 - » du texte, non confirmée par le vérificateur |
| C2S, recours | 54/55/56 ; 67/69/69 ; 28/29/34 % | tableau 2, p. 33, relu | rapport annuel 2025 de la C2S (URL ci-dessus) | Conforme ; non-recours = 100 − recours, calculé |
| Assurance chômage | 25 à 42 % (note) | phrase de la p. 6 et note 21 relues | rapport du Défenseur des droits (URL ci-dessus) | Conforme avec réserve : seconde main, Dares inaccessible, période inconnue |
| Comparaison avec la fraude | 2 à 3 Md€ par an ; 425 M€ détectés en 2014 (note) | phrases exactes p. 59 et p. 172 relues | rapport n° 4158 (URL ci-dessus) | Conforme avec réserve : « ordres de grandeur », estimation de deux rapporteurs ; non-recours estimé, fraude détectée ; année du non-recours non donnée p. 172 |
| RSA fin 2021 (DREES n° 1370) | non saisi | 33 à 37 %, 560 000 foyers, 630 M€ par trimestre, dans une copie de presse | copie Le Media social ; site de la DREES inaccessible | Non trouvé chez le producteur : en attente |

**Conclusion.** Aucun chiffre du fichier n'est faux ; trois lectures sont à garder : chaque taux a son année et sa méthode, le non-recours de la C2S est calculé, et la comparaison avec la fraude met en regard une estimation et un montant détecté.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus. Le site de la DREES et celui de la Dares étaient inaccessibles (réponse vide, erreur 503).

## Réserves

- Le taux du minimum vieillesse (fin 2016) est la dernière estimation trouvée ; il ne couvre pas les couples.
- Le RSA de 2018 est de seconde main (DREES citée par le Sénat) ; sa méthode diffère de celle de l'étude de 2026.
- Les taux de deux prestations ne se comparent pas (méthodes, années, champs différents) ; le bloc les groupe par année et le dit.
- Le rapport de la C2S note que les résultats antérieurs à 2021 ne sont pas disponibles pour la version 2021 du modèle Ines : 2019 et 2020 viennent de versions antérieures du modèle.
- Aucun chiffre officiel de non-recours toutes prestations confondues n'a été trouvé ; les « 10 milliards » qui circulent n'ont pas de producteur officiel (rapport de recherche). Rien de tel n'est saisi.
- Prime d'activité et aides au logement : aucun taux ni montant officiel confirmé.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert les documents eux-mêmes.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée : le registre dit « citation seule » (chiffres cités, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
