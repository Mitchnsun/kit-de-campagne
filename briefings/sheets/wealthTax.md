# `wealthTax` · Impôt sur la fortune : ISF puis IFI (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; une synthèse de la recherche corrigée (le comité n'écrit pas « aucun effet sur l'investissement » mais « aucun effet de l'ISF sur l'activité des ETI ») ; réserves de lecture reprises ci-dessous. La licence des sources citées seulement n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `wealthTax`, dossier « Économie et fiscalité » (`economy`), page de type série, recherche « Ce qu'on entend » du 09/11/2026 |
| Données | `briefings/manual/wealthTax.json`, saisi à la main le 2026-11-09 depuis le tableau 3.217 de l'Insee, le fichier de l'ISF de la DGFiP et les DGFiP Statistiques n° 23 et n° 45 |
| Sources | 1. Insee, « Tableau 3.217 – Principaux impôts par catégorie », dans « Dépenses et recettes des administrations publiques en 2025 », https://www.insee.fr/fr/statistiques/8988845, fichier https://www.insee.fr/fr/statistiques/fichier/8988845/t_3217_fr.xlsx (page du 28/08/2026), Licence Ouverte 2.0, en français seulement. 2. DGFiP, « L'ISF - montants et nombres des déclarations de 1999 à 2017 », ressource du jeu data.gouv.fr « Impôt de solidarité sur la fortune - Impôt sur la fortune immobilière par collectivité territoriale », https://www.impots.gouv.fr/sites/default/files/media/stats/isf_montants_declares_nombres_1999_2017.xls (24/10/2019), Licence Ouverte, en français seulement. 3. DGFiP, « L'impôt sur la fortune immobilière en 2025 » (DGFiP Statistiques n° 45, avril 2026), https://www.impots.gouv.fr/sites/default/files/media/9_statistiques/0_etudes_et_stats/0_publications/dgfip_statistiques/2026/num45_04/dgfip_stat_45_ifi_2025.pdf, et « L'impôt sur la fortune immobilière en 2023 » (n° 23, avril 2024), https://www.impots.gouv.fr/sites/default/files/media/9_statistiques/0_etudes_et_stats/0_publications/dgfip_statistiques/2024/num23_04/dgfip_stats_ifi_2023.xlsx (14/04/2026, mise en ligne du n° 45 selon la recherche), citation seule, en français seulement. 4. France Stratégie, « Comité d'évaluation des réformes de la fiscalité du capital – Rapport final », avis du comité https://www.strategie-plan.gouv.fr/files/files/Publications/Rapport/fs-2023-rapport-isf-quatrieme_rapport_complet_17octobre_avis_0.pdf et rapport complet https://www.strategie-plan.gouv.fr/files/files/Publications/Rapport/fs-2023-rapport-isf-quatrieme_rapport_complet_17octobre_2.pdf (16/10/2023), citation seule, en français seulement. 5. Cour des comptes, « L'impôt sur la fortune immobilière », observations définitives, https://www.ccomptes.fr/fr/documents/68192 (25/01/2024), citation seule, en français seulement |
| Séries | `revenue` : rendement de l'impôt sur la fortune (« Impôt sur la fortune (IFI, ex ISF) »), Md€ courants, comptabilité nationale, Insee, feuille `T_3217` ligne 88, 1995 à 2025, 31 points (1,292 … 5,068 en 2017 ; 1,847 en 2018 … 2,682 en 2024, `semiDefinitive` ; 2,714 en 2025, `provisional`). `isfTaxpayers` : foyers redevables de l'ISF (nombre de déclarations), DGFiP, 1999 à 2017, 19 points (212 868 … 593 878 en 2010 ; 291 630 en 2011 … 358 198 en 2017). `ifiTaxpayers` : foyers ayant reçu un avis d'IFI, DGFiP, 2018 à 2025, 8 points (132 720 ; 139 150 ; 143 340 ; 152 690 ; 164 000 ; 175 980 ; 186 100 ; 193 600) |
| Chiffre clé | 2,714 Md€ (écrit 2,71 Md€) d'impôt sur la fortune immobilière en 2025, compte provisoire, tendance à la hausse (2,682 en 2024) ; à côté, les foyers imposés à l'IFI la même année, 193 600 |
| Règles | Saisie à la main. Deux vues : « Rendement » (`revenue`) et « Foyers » (`isfTaxpayers`, `ifiTaxpayers`, deux lignes qui ne se chevauchent pas). La page écrit le rendement au centième de milliard (`digits`), l'Insee le donnant au millième. Une seule ligne d'impôt, comme l'Insee : l'ISF jusqu'en 2017, l'IFI depuis 2018, restes d'ISF compris de 2018 à 2022, ce que la note de la vue dit. Aucune rupture saisie (`breaks`) : ni l'Insee ni la DGFiP ne la marquent dans leurs fichiers ; la note de la vue dit le passage à l'IFI et le relèvement du seuil de l'ISF en 2011. Les valeurs d'avant 1995 (OCDE, autre source) ne sont pas saisies, ni les montants déclarés ou émis, ni les recettes budgétaires, ni les prévisions des lois de finances : seule la comptabilité nationale fait la série, les autres bases sont dans « À savoir » |
| Première édition | À remplir à la publication |

## « À savoir »

1. En 2018, l'IFI a remplacé l'ISF et ne taxe que le patrimoine immobilier ; de 2018 à 2022, les montants comprennent des restes d'ISF, 0,7 Md€ sur 1,9 Md€ en 2018 dans la ligne budgétaire. Source : Cour des comptes, observations définitives du 25/01/2024 (« Depuis que l'IFI a remplacé l'ISF en 2018, la ligne budgétaire comprend à la fois les recettes de l'IFI et les recettes résiduelles d'ISF. » ; tableau n° 2 : 1,9 dont 0,7 « ISF et autres » et 1,2 IFI en 2018) ; Insee, tableau 3.217 (une seule ligne « Impôt sur la fortune (IFI, ex ISF) ») ; assiette immobilière : recherche vérifiée (« L'assiette se limite au patrimoine immobilier »).
2. Le coût du remplacement estimé par le comité : 3,1 Md€ en 2018 (estimation de son premier rapport), « vraisemblablement supérieur à 4 milliards d'euros » en 2022. Source : France Stratégie, avis du comité, rapport final d'octobre 2023 (« En 2022, le coût budgétaire du remplacement de l'ISF par l'IFI serait vraisemblablement supérieur à 4 milliards d'euros » ; « le comité dans son premier rapport en 2019 estimait que le remplacement de l'ISF par l'IFI avait conduit en 2018 à une perte de recettes de 3,1 milliards »). Le 4,5 Md€ du comité, qui repose sur l'hypothèse « que les recettes d'ISF auraient crû au même rythme que les recettes d'IFI », n'est pas repris.
3. Trois bases comptables : 2,27 Md€ en comptabilité nationale (Insee), 2,4 Md€ de recettes budgétaires (Cour des comptes, ligne 1406) et 1,83 Md€ d'avis émis (DGFiP) en 2022. Source : Insee, tableau 3.217 (2022 : 2,27) ; Cour des comptes, tableau n° 2 (2022 : 2,4, « portant l'ensemble des recettes IFI et ISF à 2,4 Md € en 2022 ») ; DGFiP Statistiques n° 23, onglet « Graphique 1 » (2022 : 1,83). Les trois bases sont celles de la recherche vérifiée (droits constatés ; encaissements de l'année ; impôt dû au titre de l'année, hors contrôle).
4. 2025 est un compte provisoire, 2024 un compte semi-définitif ; euros courants. Source : Insee, note de révisions du 03/06/2026 (« comptes annuels complets bruts […] pour l'année n (compte provisoire), l'année n-1 (compte semi-définitif) et l'année n-2 (compte définitif) »), d'après la contre-vérification ; tableau 3.217 « En milliards d'euros ».

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/wealthTax.json` (clé `claims`, français et anglais). Les quatre de la recherche vérifiée et celle déplacée de `publicSpending` le 09/11/2026 ; aucune ne répète les chiffres d'une autre. Le comité est cité par ses phrases, jamais par une synthèse. Source de chaque chiffre de la réponse :

1. « On entend que l'ISF a été supprimé et qu'il n'y a plus d'impôt sur la fortune en France. » 193 600 foyers en 2025 : DGFiP Statistiques n° 45 (« En 2025, près de 193 600 foyers ont reçu de l'administration fiscale un avis d'impôt sur la fortune immobilière (IFI). »). 358 198 déclarations en 2017 : fichier de l'ISF de la DGFiP, feuille `nombres`. Le seuil de 1,3 M€ de la réponse de la recherche n'est pas repris : il n'est dans aucune phrase de source vérifiée pour l'IFI.
2. « On entend que l'IFI, qui a remplacé l'ISF, ne rapporte rien. » (déplacée de `publicSpending`) 5,07 (2017), 1,85 (2018), 2,71 Md€ (2025, provisoire) : Insee, tableau 3.217, ligne 88 (5,068 ; 1,847 ; 2,714). 2,3 Md€ d'avis émis en 2025 : DGFiP Statistiques n° 45 (« Ces avis représentent un montant total d'imposition de 2,3 Md€ »). Les deux bases sont dites différentes dans la réponse. Les montants de la TVA, de la CSG et de l'impôt sur le revenu que citait la réponse dans `publicSpending` ne sont pas repris : ce ne sont pas des chiffres de cette page.
3. « On entend que supprimer l'ISF n'a rien coûté à l'État, ou que la mesure s'est payée toute seule. » 3,1 milliards (2018) et « serait vraisemblablement supérieur à 4 milliards d'euros » (2022) : avis du comité, rapport final (phrases du point 2 de « À savoir »). « pas réussi à identifier d'impact mesurable sur l'activité économique », coût « dynamique » et « statique » : rapport complet, p. 215 (« Les études financées par le comité n'ayant pas réussi à identifier d'impact mesurable sur l'activité économique, nous ne sommes pas en mesure de produire une estimation du coût « dynamique » différente du coût « statique ». »).
4. « On entend que depuis la suppression de l'ISF, les contribuables fortunés reviennent en masse en France. » Avis du comité : « Depuis 2018, les retours de contribuables à l'IFI dépassent les départs à l'étranger » (380 retours contre 260 départs en moyenne de 2018 à 2021) ; « Cette évolution porte toutefois sur de petits effectifs, de l'ordre de quelques centaines » ; « on ne peut rigoureusement conclure à un effet causal » ; « Dans tous les cas, les effets trouvés sont de faible ampleur. »
5. « On entend que la suppression de l'ISF a relancé l'investissement des entreprises. » Avis du comité : « En revanche, aucun effet de l'ISF sur l'activité des ETI n'a pu être identifié » (dividendes et investissement des entreprises dont les actionnaires étaient assujettis, d'après la précaution vérifiée) ; « Il semble toutefois que cet impact sur les créations d'entreprises soit davantage dû au PFU et à l'IS qu'au remplacement de l'ISF par l'IFI. » ; « Beaucoup de questions restent ouvertes ». La contre-vérification a corrigé la synthèse de la recherche (« aucun effet sur l'investissement ») : la réponse cite la phrase.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-isf-juges.md` : tout retéléchargé (`curl`), classeurs lus avec openpyxl, PDF avec `pdftotext`.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Rendement, 1995 à 2025 (et chiffre clé) | 1,292 … 5,068 ; 1,847 … 2,682 ; 2,714 | les 31 valeurs identiques (comparaison par script) ; 2025 provisoire, 2024 semi-définitif (note de l'Insee du 03/06/2026) | fichier `t_3217_fr.xlsx` (URL ci-dessus) | Conforme, avec réserve : 2025 révisable ; restes d'ISF de 2018 à 2022 |
| Foyers de l'ISF, 1999 à 2017 | 212 868 … 358 198 | 19 années identiques au fichier xls ; Licence Ouverte confirmée sur data.gouv.fr | fichier de la DGFiP (URL ci-dessus) | Conforme, avec réserve : seuil relevé en 2011 |
| Foyers de l'IFI, 2018 à 2023 | 132 720 … 164 000 ; 175 980 | « Graphique 1 » du n° 23 (en milliers : 132,72 … 176) ; texte : « 175 980 foyers fiscaux ont reçu […] un avis » | DGFiP Statistiques n° 23 (URL ci-dessus) | Conforme, avec réserve : valeurs arrondies, en milliers |
| Foyers de l'IFI, 2024 et 2025 | 186 100 ; 193 600 | phrase et tableau 1 du n° 45 retrouvés ; le classeur dit 193 625 déclarants | DGFiP Statistiques n° 45 (URL ci-dessus) | Conforme |
| Restes d'ISF, ligne 1406 | 0,7 sur 1,9 (2018) ; 2,4 (2022) | texte retrouvé dans la version HTML ; cellules vides de 2018 déduites (0,7 + 1,2 = 1,9) | Cour des comptes (URL ci-dessus) | Conforme, avec réserve : tableau à revoir dans le PDF |
| Phrases du comité (coût, retours, ETI, PFU, questions ouvertes, p. 215) | citées | 22 phrases retrouvées mot pour mot | avis et rapport complet (URL ci-dessus) | Conforme |

**Conclusion.** Aucun chiffre du fichier n'est faux. Trois bases comptables donnent trois montants : la série suit l'Insee, et chaque autre montant cité dit sa base.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus.

## Réserves

- 2025 est un compte provisoire, qui peut être révisé ; l'Insee ne dit pas si 2012 (5,030) compte la contribution exceptionnelle de 2012.
- La répartition de 2018 entre restes d'ISF et IFI est lue dans la version HTML du document de la Cour ; le PDF n'a pas été ouvert.
- Les dates de mise en ligne n'ont pas été vérifiées par la contre-vérification : le n° 45 est daté du 14/04/2026 d'après la recherche (« avril 2026 » imprimé).
- Le nombre de redevables de l'ISF avant 1999 n'existe dans aucune source officielle ouverte.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la contre-vérification a rouvert chaque fichier et chaque document.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Licence Ouverte vérifiée pour le fichier de l'ISF (data.gouv.fr) ; non vérifiée pour les autres : le registre dit « Licence Ouverte » pour l'Insee et « citation seule » pour les DGFiP Statistiques, France Stratégie et la Cour des comptes.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
