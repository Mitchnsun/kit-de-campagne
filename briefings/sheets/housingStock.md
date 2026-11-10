# `housingStock` · Le parc de logements (saisi à la main)

**Vérifiée le 10/11/2026** : double vérification sur le web, aucun écart de valeur ; les 8 séries de la BDM relues valeur par valeur (45 chacune), les parts recalculées sur les comptes. Réserves reprises ci-dessous (années provisoires, ruptures de LOVAC, date de situation de LOVAC ambiguë). La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `housingStock`, dossier « Pouvoir d'achat et logement » (`purchasingPower`), volet « Le parc » de la page composite `housing` (voir `housing.md`), page de type série, recherche du 09/11/2026 |
| Données | `briefings/manual/housingStock.json`, saisi à la main le 2026-11-10 depuis la BDM de l'Insee (dataflow PARC-LOGEMENTS, mis à jour le 30/09/2026), le fichier France de LOVAC et l'API d'Eurostat (valeurs relues par la contre-vérification) |
| Sources | 1. Insee, « Parc de logements au 1er janvier 2026, Insee Focus n° 388 », https://www.insee.fr/fr/statistiques/9055697, séries BDM https://www.insee.fr/fr/statistiques/serie/001791241 (et 001791242, 001791243, 001791244, 001791247, 001791251, 001791252, 001791253), Licence Ouverte 2.0. 2. Ministère de la Transition écologique (DGALN, traitement Cerema, source DGFiP 1767 bis Com), « Logements vacants du parc privé par commune, département, région, France, de 2020 à 2026 », https://www.data.gouv.fr/datasets/61816c6e23197bb34835228e, fichier https://static.data.gouv.fr/resources/logements-vacants-du-parc-prive-par-commune-departement-region-france/20260625-163737/lovac-opendata-france26.csv, Licence Ouverte 2.0 (indiquée sur data.gouv.fr). 3. Eurostat, « Distribution de la population par statut d'occupation du logement, par type de ménage et par groupe de revenu » (`ilc_lvho02`), https://ec.europa.eu/eurostat/databrowser/view/ilc_lvho02/default/table?lang=fr, licence Eurostat (« Source : Eurostat »), pour l'affirmation et le `readFirst` |
| Dates de publication | 2026-09-30 (Insee Focus n° 388, « Paru le » de la page et mise à jour de la BDM) ; 2026-06-25 (mise à jour du jeu LOVAC sur data.gouv.fr) ; 2026-10-20 (mise à jour de `ilc_lvho02`) |
| Séries | `dwellings`, `mainResidences`, `secondaryHomes`, `vacant` : logements, résidences principales, résidences secondaires et logements occasionnels, logements vacants au 1er janvier, France hors Mayotte, 1982 à 2026, 45 points chacune, comptes de l'Insee en milliers saisis × 1 000 (38 617 000 en 2026 = « 38 617 milliers ») ; 2024, 2025 et 2026 provisoires. `owners`, `privateTenants`, `publicTenants`, `rentFree` : propriétaires, locataires d'un bailleur privé, d'un bailleur public, logés gratuitement, en % des ménages, 1982 à 2026, 45 points, mêmes années provisoires. `privateVacant` (3 160 235) et `privateVacantOver2Years` (1 179 845) : un seul point, le millésime 2026 de LOVAC (colonnes `pp_vacant` et `pp_vacant_plus_2ans`) |
| Chiffre clé | 38 617 000 logements au 1er janvier 2026 (provisoire), en hausse (38 380 000 en 2025) ; à côté, les logements vacants (2 926 000) et les ménages propriétaires (57,3 %) |
| Règles | Saisie à la main. Cinq vues : « Logements » (logements et résidences principales, les quatre comptes au tableau), « Vacants » (vacants et résidences secondaires), « Vacants du privé » (deux barres LOVAC), « Propriétaires » (les quatre statuts au tableau), « Locataires » (privé et public). Les parts du parc (82,7 / 9,7 / 7,6 %) sont celles que l'Insee publie, dans une note ; la série des parts de vacants n'est pas saisie (calculée). Les millésimes 2020 à 2025 de LOVAC ne sont pas saisis : deux ruptures de série (2023, 2025), « ne pas calculer de variation ». Non saisis : le statut d'occupation de l'enquête Logement (57,4 %, Insee Première n° 2090, une autre source), le surpeuplement de l'Insee |
| Première édition | À remplir à la publication |

## « À savoir »

1. Les 2,9 millions de vacants de 2026 comprennent la vacance de rotation (en vente, en location, en attente de succession, vétustes) : le chiffre vrai, pas un gisement ; « la vacance de courte durée est inhérente au fonctionnement du marché immobilier ». Source : Insee Focus n° 388 (phrase recopiée) ; BDM 001791244 (2 926 milliers).
2. 1 179 845 logements du parc privé vacants depuis plus de deux ans, millésime 2026, au 1er janvier 2025 selon le dictionnaire du fichier ; source fiscale ; ruptures de série en 2023 et 2025. Source : fichier France de LOVAC (« France;2026;; 3 160 235 ; 1 179 845 ») ; dictionnaire (« Nombre de logements vacants du parc privé depuis plus de deux ans au 01/01/2025 »).
3. 57,3 % de ménages propriétaires en 2026 (provisoire), dont 19,8 % d'accédants et 37,6 % de non-accédants, « quasi stable depuis 2011 ». Source : Insee Focus n° 388 (« En 2026, 57,3 % des ménages sont propriétaires de leur résidence principale […]. Cette part est quasi stable depuis 2011 ») ; BDM 001791248 et 001791249. Le résumé du même Focus écrit « quasi stable depuis 2014 » : la note reprend la phrase du corps du texte.
4. Bailleur public (17,3 % des ménages) : HLM, SEM, État ou collectivités, conventionné ou non, plus large que le parc RPLS (logements loués : 15,9 % des résidences principales). Source : BDM 001791251 et définition du Focus ; SDES, Datalab RPLS au 1er janvier 2025 (volet `socialHousing`).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Dans `briefings/notes/housingStock.json` (clé `claims`). Source de chaque chiffre de la réponse :

1. « On entend que les Français sont presque tous propriétaires. » 57,3 % des ménages en 2026 (provisoire) et « quasi stable depuis 2011 » : Insee Focus n° 388, BDM 001791247. 61,4 % de la population en 2025, 68,5 % dans l'UE : `ilc_lvho02` (cellules FR et EU27_2020 de 2025). 24e sur 27 : classement calculé sur les 27 valeurs de 2025 (SK 93,8 en tête ; derrière la France : DK 58,4, AT 54,2, DE 47,2 ; pas d'ex æquo), dit « calculé ». La réponse est celle du rapport final, telle quelle (416 caractères).

## Double vérification

Faite le 10/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-logement.md` : BDM retéléchargée (dataflow PARC-LOGEMENTS), page du Focus relue, fichier France et métadonnées de LOVAC rouverts, API d'Eurostat rouverte.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 38 617 000 (2026, provisoire) | BDM 001791241 « 2026 38617 (P) » ; « la France hors Mayotte compte 38,6 millions de logements » | https://www.insee.fr/fr/statistiques/9055697 | Conforme |
| Séries du parc | 4 × 45 valeurs | 45 valeurs par série comparées une à une ; parts recalculées 82,68 / 9,74 / 7,58 | https://api.insee.fr/series/BDM/V1/data/PARC-LOGEMENTS | Conforme |
| Statuts d'occupation | 4 × 45 valeurs | Idem, 2024-2026 provisoires | idem | Conforme |
| Vacants 2019 et 2026 | 2 947 000 ; 2 926 000 | « passant de 8,1 % à 7,6 % » ; 8,06 calculé pour 2019 | Insee Focus n° 388 | Conforme |
| LOVAC | 3 160 235 ; 1 179 845 | Ligne France du fichier, relue | fichier France de LOVAC | Conforme, avec réserve : date de situation ambiguë (« au 01/01/2025 » au dictionnaire, « au 1er janvier, de 2020 à 2026 » sur la fiche) |
| Propriétaires, Eurostat (affirmation) | 61,4 % ; 68,5 % ; 24e | Cellules FR et EU27_2020 2025 ; 27 pays triés | `ilc_lvho02` | Conforme (rang calculé) |

**Conclusion.** Aucun chiffre du fichier n'est faux ; les années récentes sont provisoires, et LOVAC n'est pas lu comme une évolution.

**Pages consultées** le 10/11/2026 : les URL ci-dessus.

## Réserves

- 2024, 2025 et 2026 sont provisoires ; les logements « non ordinaires » sont hors champ ; Mayotte n'est pas comprise.
- Les comptes de l'Insee sont au millier : le fichier les écrit × 1 000, la note de la vue le dit.
- LOVAC : source fiscale, deux ruptures de série, date de situation ambiguë ; le parc privé de 2026 n'est pas fourni (aucune part calculée).
- Le taux de propriétaires d'Eurostat (personnes) et celui de l'Insee (ménages) ne se comparent pas : le `readFirst` et l'affirmation le disent.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert la BDM, LOVAC et Eurostat.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée : Licence Ouverte 2.0 (Insee, data.gouv.fr), licence Eurostat.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
