# `permitReasons` · Premiers titres de séjour par motif

**Vérifiée le 09/11/2026** : les valeurs de 2025 écrites par le script (et celles de 2024 que la recherche donne) égalent celles de la recherche contre-vérifiée du 09/11/2026, sans écart ; réserves de lecture (« autres motifs » et taux pour 100 000 habitants calculés, population provisoire, nomenclature différente de la DGEF), reprises dans « À savoir » et ci-dessous. La licence des sources n'a pas été vérifiée pour la DGEF (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `permitReasons`, dossier « Immigration » (`immigration`), page de type comparaison |
| Données | `briefings/data/permitReasons.json`, écrit par `yarn briefings permitReasons` le 2026-11-09 (script `scripts/briefings/permitReasons.ts` de l'app) |
| Sources | Eurostat, « Permis délivrés pour la première fois par raison, durée de validité et nationalité » (`migr_resfirst`, mis à jour le 22/10/2026) ; Eurostat, « Permis délivrés pour la première fois pour d'autres raisons par raison, durée de validité et nationalité » (`migr_resoth`, 28/09/2026) ; Eurostat, « Population au 1er janvier » (`tps00001`, 27/10/2026) ; API de diffusion d'Eurostat en JSON, sans clé, réutilisation libre avec mention de la source. Ministère de l'Intérieur (DGEF), « Les étrangers en France 2025 – Rapport au Parlement » (PDF créé le 28/09/2026, date saisie à la main dans le script : le site du ministère refuse les scripts), licence « citation seule », en français seulement : il ne fournit aucun chiffre du fichier, seulement ceux des notes et des affirmations |
| Séries | France, premiers titres délivrés à des ressortissants de pays tiers, chaque année depuis 2008, en personnes : `total` (TOTAL, 18 points), `education` (EDUC), `family` (FAM), `employment` (EMP), `otherReasons` (OTH, protection internationale comprise), toutes de `migr_resfirst` ; `protection` (RFG_SPROT, statut de réfugié et protection subsidiaire, `migr_resoth`, depuis 2009, 17 points) |
| Valeurs par catégorie | `byReason` (dernière année, 2025) : études 118 404, famille 90 959, protection internationale 84 657, emploi 50 848, autres motifs 32 594 (**calculé** : OTH 117 251 moins RFG_SPROT 84 657) ; `permitsPer100k` (2025, provisoire) : premiers titres pour 100 000 habitants au 1er janvier, France 548, UE 855 (**calculé**) |
| Chiffre clé | 377 462 premiers titres en 2025, en hausse (345 587 en 2024) ; à côté, études 118 404 et famille 90 959 |
| Règles | Le script lit cinq réponses de `migr_resfirst` (tous motifs, France et UE ; puis chaque motif, France), une de `migr_resoth` (protection internationale, France) et une de `tps00001` (France et UE), et vérifie l'intitulé de chaque jeu. Il échoue si les quatre motifs de la dernière année ne font pas le total, si la protection dépasse les autres motifs, ou si une année ou un territoire manque. Une année marquée `p` par Eurostat est provisoire ; les taux pour 100 000 habitants le sont dès qu'un de leurs chiffres l'est (population 2025 : `p` pour la France, `ep` pour l'UE). Les deux valeurs calculées vont en valeurs par catégorie, jamais en série, et la page dit « calculé ». Le regroupement familial au sens strict (DGEF) n'est pas une série : il est dans « À savoir » et « Ce qu'on entend » |
| Première édition | À remplir à la publication |

À actualiser : à chaque mise à jour de `migr_resfirst` (Eurostat, d'après le ministère) ; la date du rapport de la DGEF dans le script à chaque nouveau rapport au Parlement.

## « À savoir »

1. Les premiers titres sont délivrés pour la première fois à des ressortissants de pays tiers. Le ministère de l'Intérieur (DGEF) en compte 384 230 en 2025, chiffre provisoire d'une autre nomenclature : il ne s'additionne pas aux chiffres d'Eurostat et ne s'y mêle pas. Source : DGEF, rapport au Parlement 2025, https://www.immigration.interieur.gouv.fr/sites/dgef/files/medias/documents/2026-10/INTV2623196X_Rapport%20au_Parlement_2025_28sept2026.pdf (« Le nombre de premiers titres de séjour a atteint 384 230, en hausse de 11,2 % » ; colonne 2025 « provisoire »).
2. Le motif familial réunit plusieurs situations : familles de Français, membres de famille d'étrangers ou de ressortissants de l'UE, liens personnels et familiaux. Le regroupement familial au sens strict en est une partie : 17 812 premiers titres en 2024 selon la DGEF, dernière année détaillée. Source : même rapport (« Regroupement familial 14 448 15 181 15 288 17 812 nd » ; 2025 « nd »).
3. « Autres motifs » est calculé : les autres motifs d'Eurostat moins la protection internationale (statut de réfugié et protection subsidiaire). Les rapports pour 100 000 habitants sont calculés eux aussi, avec la population au 1er janvier, provisoire ; le total de l'UE est arrondi par Eurostat. Source : API Eurostat, `migr_resfirst` (OTH 117 251 ; UE 3 860 000), `migr_resoth` (RFG_SPROT 84 657), `tps00001` (FR 68 882 600 `p`, UE 451 284 558 `ep`).
4. Un visa n'est pas un titre de séjour : les 23 662 visas délivrés en 2025 au titre du regroupement familial (DGEF, toutes nationalités) ne s'ajoutent pas aux titres. Source : rapport de la DGEF (« Total 22 390 15 858 19 159 20 991 23 662 + 12,7 % », champ « Périmètre France, toutes nationalités »).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/permitReasons.json` (clé `claims`, français et anglais). Source de chaque chiffre de la réponse :

1. « On entend que la France distribue des titres de séjour à tour de bras, plus que ses voisins. » 377 462 : Eurostat, `migr_resfirst`. 548 et 855 pour 100 000 habitants : calculés (premiers titres et population au 1er janvier 2025, `tps00001`). 21e sur 27 par ordre décroissant : rang calculé par la recherche et la contre-vérification (non recalculé par le script, qui ne lit que la France et l'UE). 384 230 (provisoire) et +11,2 % : DGEF. Le mot « calculé » est dans la réponse.
2. « On entend que le regroupement familial est la première source d'immigration. » « Premier motif depuis 2022 » : DGEF (la recherche le lit dans le rapport). 118 404 et 90 959 : Eurostat, `migr_resfirst`. 17 812 (2024) : DGEF.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après son rapport `verify-immigration.md` : API d'Eurostat réinterrogée, rangs et ratios recalculés, PDF de la DGEF re-téléchargé. Puis, le même jour, les valeurs écrites par le script ont été comparées à celles de la recherche : toutes égales.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, total | 377 462 (2025) ; 345 587 (2024) | 377 462 ; 345 587 (même valeur que le total 2024 de la DGEF) | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/migr_resfirst?geo=FR&sinceTimePeriod=2024&citizen=TOTAL&duration=TOTAL | Conforme |
| Par motif, 2025 | études 118 404 ; famille 90 959 ; emploi 50 848 ; protection 84 657 ; autres 32 594 | Idem ; 117 251 − 84 657 = 32 594 ; somme 377 462 ; emploi 2024 58 603 ; protection 2024 52 586 | même API ; `migr_resoth?…reason=RFG_SPROT` | Conforme. « Autres » est calculé, non publié |
| Pour 100 000 habitants | 548 (FR) ; 855 (UE), provisoire | 548,0 (rang 21) ; 855,3 ; population FR 68 882 600 (p), UE 451 284 558 (ep) | API `migr_resfirst`, `tps00001` | Conforme, avec réserve : taux calculé ; total UE arrondi par Eurostat ; population provisoire |
| Nomenclature DGEF | 384 230 (dans les notes) | Idem, 2025 provisoire ; économique 51 190, familial 91 100, étudiants 117 970, humanitaire 92 610, divers 31 360 | PDF de la DGEF | Conforme, avec réserve : provisoire ; périmètre différent d'Eurostat |
| Regroupement familial | 17 812 (2024, dans les notes) ; visas 23 662 (2025) | Idem ; 2025 « nd » pour les titres | PDF de la DGEF | Conforme. Visas : « Périmètre France, toutes nationalités » ; titres : pays tiers |

**Conclusion.** Aucun chiffre du fichier n'est faux. Les points de 2008 à 2023 par motif sont ceux de l'API d'Eurostat, lus par le script ; la double vérification du 09/11/2026 n'a recoupé que 2024 et 2025.

**Pages consultées** le 09/11/2026 : l'API d'Eurostat (les sept réponses du script) et le PDF de la DGEF ; le site du ministère (immigration.interieur.gouv.fr) répond 403.

## Réserves

- Les séries Eurostat et DGEF n'ont pas le même périmètre (377 462 contre 384 230 en 2025) ; la page ne les additionne pas et ne les mélange pas.
- Le rang de la France (21e sur 27) n'est pas recalculé par le script.
- Les admissions exceptionnelles au séjour (28 610 en 2025, DGEF) et le stock de titres ne sont pas saisis.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script : 2024 et 2025 recoupés avec la recherche contre-vérifiée ; les années antérieures ne l'ont pas été.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Eurostat : réutilisation permise, commerciale comprise, mention « Source : Eurostat » et modifications signalées (https://ec.europa.eu/eurostat/help/copyright-notice) ;
  - citation seule : Ministère de l'Intérieur (DGEF) (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
