# `removals` · Éloignements (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; réserves de champ et de lecture (des mesures, non des personnes ; un rapport entre départs et mesures d'une même année n'est pas un taux d'exécution ; taux par motif de la Cour sur les seuls éloignements forcés), reprises dans « À lire d'abord », « À savoir » et ci-dessous. La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `removals`, dossier « Immigration » (`immigration`), aussi dans « Sécurité » (`security`), page de type comparaison |
| Données | `briefings/manual/removals.json`, saisi à la main le 2026-11-09 depuis le rapport au Parlement 2025 de la DGEF, le rapport public thématique de la Cour des comptes (janvier 2024) et le PAP 2027 de la mission Immigration, asile et intégration, d'après la recherche contre-vérifiée du 09/11/2026 (`final-immigration.json`) |
| Sources | Ministère de l'Intérieur (DGEF), « Les étrangers en France 2025 – Rapport au Parlement » (PDF créé le 28/09/2026) ; Cour des comptes, « La politique de lutte contre l'immigration irrégulière » (rapport public thématique, 04/01/2024) ; Eurostat, « Enforcement of Immigration Legislation (migr_eil) », métadonnées en anglais seulement (mises à jour le 21/02/2024) ; Gouvernement, « Projet annuel de performances 2027, mission Immigration, asile et intégration » (copie de l'Assemblée nationale, PDF créé le 29/09/2026). Licence « citation seule » pour la DGEF, la Cour et le PAP (en français seulement), réutilisation libre avec mention de la source pour Eurostat |
| Séries | `removalsExecuted` : éloignements exécutés (forcés, aidés et spontanés), métropole, majeurs, tous pays, 2021 à 2025, 5 points (12 759, 14 947, 16 522, 21 011, 24 275) ; `removalMeasures` : mesures d'éloignement prononcées, métropole, tous pays, 2021 à 2025, 5 points (143 226, 153 042, 156 434, 145 107, 156 180) ; `detentionRemovalRate` : taux d'éloignement à l'issue d'un placement en CRA, %, 2024 (38,75) et 2025 (36), 2 points |
| Valeurs par catégorie | `removalsByType` (2025) : forcés 15 253, aidés 4 564, spontanés 4 458 ; `measuresByType` (2025) : retours de ressortissants de pays tiers 137 980, réadmissions de ressortissants de pays tiers vers l'UE 13 104, renvois de ressortissants de l'UE 5 096 ; `courtFindings` (2022) : éloignements et départs recensés en part des mesures 10 %, exécution des OQTF réputées exécutoires (DGEF) 12 % ; `forcedRateByGround` (période saisie « 2022 », cumul de 2019 à 2022) : condamnation pénale 45 %, menace à l'ordre public 23 %, transfert Dublin 14 %, entrée irrégulière 6 %, refus de titre 2 %, déboutés de l'asile 2 % |
| Chiffre clé | 24 275 éloignements exécutés en 2025, en hausse (21 011 en 2024) ; à côté, 156 180 mesures prononcées |
| Règles | Saisie à la main. Les années 2021 à 2024 des deux séries de la DGEF sont celles des lignes de tableau citées par la recherche (« Total mesures prononcées 143 226 153 042 156 434 145 107 156 180 + 7,6 % » ; « Total éloignements (A)+(B)+(C) 12 759 14 947 16 522 21 011 24 275 + 15,5 % »), colonnes 2021 à 2025 relues dans le PDF par l'agent qui a saisi la page. **Aucun rapport entre éloignements et mesures d'une même année n'est saisi ni affiché** (ni 24 275 / 156 180, ni les obligations et retours d'Eurostat) : la page le dit d'abord. Les deux séries sont dessinées dans des blocs séparés, chacune à son échelle. Une seule série de retours forcés est gardée (15 253, DGEF, métropole) : les 15 569 du PAP (champ non précisé) ne sont pas saisis. Le tableau n° 7 de la Cour compte sept motifs : le « maintien irrégulier sur le territoire » (9 %), absent du fichier vérifié, n'est pas saisi. Le cumul 2019-2022 est saisi avec la période « 2022 » (le lecteur n'accepte pas d'intervalle) ; la note du bloc et le titre du tableau disent « de 2019 à 2022 » |
| Première édition | À remplir à la publication |

## « À lire d'abord » (dans les locales de l'app)

« Rapporter les éloignements d'une année aux mesures prononcées la même année ne donne pas un taux d'exécution : Eurostat précise que les départs d'une année peuvent répondre à des mesures d'années précédentes. Le « 10 % » de la Cour des comptes est un tel rapport, qu'elle assortit de réserves. » Source : métadonnées d'Eurostat, https://ec.europa.eu/eurostat/cache/metadata/en/migr_eil_esms.htm (« Persons who left the territory within the year may have been subject to an obligation to leave in a previous year. As such, the number of persons who actually left the territory may be greater than those who were subject to an obligation to leave in the same year. ») ; Cour des comptes (réserves : comptage partiel des départs volontaires, personnes comptées plusieurs fois). La Cour des comptes ne dit pas elle-même que les départs d'une année répondent à des mesures antérieures : la phrase est attribuée à Eurostat seul.

## « À savoir »

1. Les mesures prononcées comptent des décisions, non des personnes : selon la Cour des comptes, certaines personnes ont plusieurs OQTF et sont comptées plusieurs fois. Les mesures de la DGEF comprennent aussi des réadmissions vers un autre État de l'UE et des renvois de ressortissants de l'UE. Source : Cour des comptes, https://www.ccomptes.fr/sites/default/files/2024-02/20240104_Politique-lutte-contre-immigration-irreguliere.pdf (« certaines personnes disposent de plusieurs OQTF et sont donc comptées plusieurs fois ») ; DGEF, rapport au Parlement 2025, https://www.immigration.interieur.gouv.fr/sites/dgef/files/medias/documents/2026-10/INTV2623196X_Rapport%20au_Parlement_2025_28sept2026.pdf (tableau « Mesures d'éloignement prononcées », champ « France métropolitaine, tous pays »).
2. Les éloignements exécutés de la DGEF comptent les majeurs partis de métropole, tous pays, Mayotte et l'outre-mer exclus. Selon la DGEF, depuis la loi du 26 janvier 2024, l'aide au retour volontaire ne peut être accordée qu'à l'appui d'une mesure d'éloignement. Source : DGEF, même rapport (champ « France métropolitaine, tous pays, majeurs » ; « Depuis l'entrée en vigueur de la loi n° 2024-42 du 26 janvier 2024 […] l'aide au retour volontaire ne peut être accordée qu'à l'appui d'une mesure d'éloignement »).
3. Le « 10 % » de la Cour des comptes rapporte 15 400 éloignements ou départs volontaires recensés en 2022 à 153 042 mesures prononcées, dont 134 280 OQTF. La Cour note que les départs volontaires sont comptés en partie ; la DGEF évalue à 12 % l'exécution des OQTF réputées exécutoires. Source : Cour des comptes (« la police aux frontières n'a dénombré que 15 400 éloignements ou départs volontaires, soit 10 % des mesures prononcées » ; « la direction générale des étrangers en France évalue à 12 % le taux d'exécution des OQTF réputées exécutoires » ; « le comptage partiel des départs volontaires »).
4. Les taux par motif de la Cour des comptes, cumulés de 2019 à 2022, ne comptent que les éloignements forcés, ni retours aidés ni départs spontanés. Selon la Cour, son système d'information (GESTEL) ne couvre pas tous les éloignements forcés. Source : Cour des comptes, tableau n° 7 et sa note (« Cet écart s'explique par l'incomplétude du système d'information GESTEL, qui ne couvre pas tous les éloignements forcés »).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/removals.json` (clé `claims`, français et anglais). Source de chaque chiffre de la réponse :

1. « On entend que les étrangers délinquants ne sont pas expulsés. » 45 % et 23 % : Cour des comptes, tableau n° 7 (« Condamnation pénale 7 225 3 273 45 % » ; « Menace à l'ordre public 27 598 6 305 23 % »). 36 % : PAP 2027, indicateur 3.1 (« nombre total de ressortissants éloignés à l'issue de leur placement en CRA divisé par le nombre total de personnes placées en CRA »).
2. « On entend qu'il y a 1, 2 ou 3 millions de clandestins. » « est incertain » : Cour des comptes (« Le nombre d'étrangers en situation irrégulière présents en France est incertain. ») ; « avec toutefois plusieurs limites » : DGEF (« Le volume d'étrangers en situation irrégulière peut également être estimé par le biais du nombre de bénéficiaires de l'aide médicale d'État avec toutefois plusieurs limites. ») ; 175 051 interpellations : DGEF, tableau « Nombre d'interpellations » (+19 %). Les 159 460 étrangers trouvés en situation irrégulière d'Eurostat (`migr_eipre`), cités par la recherche, ne sont pas dans les sources de la page : la réponse ne les reprend pas.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après son rapport `verify-immigration.md` : PDF de la DGEF, de la Cour des comptes et du PAP re-téléchargés, métadonnées d'Eurostat rouvertes. Aucun écart de valeur.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Mesures prononcées | 156 180 (2025) et la série 2021-2024 | « Total mesures prononcées 143 226 153 042 156 434 145 107 156 180 + 7,6 % » ; 137 980 + 13 104 + 5 096 | https://www.immigration.interieur.gouv.fr/sites/dgef/files/medias/documents/2026-10/INTV2623196X_Rapport%20au_Parlement_2025_28sept2026.pdf | Conforme, avec réserve : champ « France métropolitaine, tous pays » (ressortissants de l'UE et réadmissions compris, pas seulement des OQTF) ; coquille p. 64 (« 156 180 en 2024 ») |
| Chiffre clé, éloignements exécutés | 24 275 (2025) et la série 2021-2024 | « Total éloignements (A)+(B)+(C) 12 759 14 947 16 522 21 011 24 275 + 15,5 % » ; 15 253 forcés, 4 564 aidés, 4 458 spontanés | même PDF | Conforme (champ : métropole, majeurs). Le tableau « Total sorties » vaut aussi 24 275 mais −10,8 % (autre série, départs D et E à 0 en 2025) : non saisi |
| Taux d'éloignement après rétention | 38,75 % (2024) ; 36 % (2025) | « Taux d'éloignement à l'issue d'un placement en CRA % 38,75 36 » | https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128237/file/PAP%202027%20-%20Immigration%20asile%20et%20int%C3%A9gration.pdf | Conforme, avec réserve : indicateur de performance ; la cible 2027 (70 %) est un objectif, non saisi |
| « 10 % » de la Cour | 10 % ; 12 % (2022) | 15 400 / 153 042 = 10,06 % ; « évalue à 12 % le taux d'exécution des OQTF réputées exécutoires » | https://www.ccomptes.fr/sites/default/files/2024-02/20240104_Politique-lutte-contre-immigration-irreguliere.pdf | Conforme. La Cour signale le comptage partiel des départs volontaires et les personnes comptées plusieurs fois |
| Taux d'éloignement forcé par motif | 45, 23, 14, 6, 2, 2 % (cumul 2019-2022) | Recalculé : 45,3 % ; 22,8 % ; 2,15 % | même PDF, tableau n° 7 | Conforme, avec réserve : éloignements forcés seulement, GESTEL incomplet ; le motif « maintien irrégulier » (9 %) n'est pas dans le fichier |
| Précision d'Eurostat | texte de « À lire d'abord » | « Persons who left the territory within the year may have been subject to an obligation to leave in a previous year. » | https://ec.europa.eu/eurostat/cache/metadata/en/migr_eil_esms.htm | Conforme. Métadonnées mises à jour le 21/02/2024 (relu le 09/11/2026 par l'agent qui a saisi la page ; l'URL en français sert la même page en anglais) |
| Interpellations | 175 051 (dans l'affirmation 4) | « Nombre d'interpellations 120 898 119 386 123 800 147 156 175 051 + 19 % » | PDF de la DGEF | Conforme |
| Pas de chiffre officiel | phrases de l'affirmation 4 | Les deux phrases sont textuelles | PDF de la DGEF et de la Cour | Conforme |

**Conclusion.** Aucun chiffre du fichier n'est faux. Le rapport 24 275 / 156 180, exact (15,5 %), n'est pas un taux d'exécution : la contre-vérification déconseille de l'afficher, la page ne l'affiche pas.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus. Le bilan provisoire de janvier 2026 du ministère (immigration.interieur.gouv.fr, 403) n'a pas pu être ouvert.

## Réserves

- Deux séries de retours forcés existent pour 2025 : 15 253 (rapport au Parlement, métropole) et 15 569 (PAP, champ non précisé, renvois UE, retours pays tiers, remises Schengen et Dublin compris). Seule la première est saisie.
- Les obligations de quitter le territoire et les retours d'Eurostat (France 137 550 et 18 930 en 2025) ne sont pas saisis : un rapport entre eux n'est pas un taux, selon Eurostat.
- Le cumul 2019-2022 de la Cour porte la période « 2022 » dans le fichier.
- Aucune publication plus récente de la Cour des comptes sur les OQTF n'a été cherchée.

## Mises à jour

**09/11/2026** : le bloc « Ce qu'on entend » ne garde que les fausses vérités que les chiffres de la page démentent (décision du PO) : affirmations retirées : « On entend que les OQTF ne sont jamais exécutées, que 7 % ou 10 % seulement le sont. » ; « On entend que les déboutés de l'asile ne partent jamais. ».

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert les documents.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée : le registre dit « citation seule » pour la DGEF, la Cour et le PAP (chiffres cités, aucun fichier redistribué) ; le PDF de la DGEF interdit la reproduction à usage collectif sans autorisation et demande la citation de la source.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
