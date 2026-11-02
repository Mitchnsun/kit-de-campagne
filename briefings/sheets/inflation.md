# `inflation` · Inflation

**Vérifiée le 02/11/2026** : double vérification sur le web, sans écart (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `inflation`, dossier « Économie et fiscalité » (`economy`), page de type série, ticket #24 de l'app (page pilote) |
| Données | `briefings/data/inflation.json`, écrit par `yarn briefings inflation` le 2026-11-02 |
| Sources | Insee, « Indice des prix à la consommation », https://www.insee.fr/fr/metadonnees/source/indicateur/p1653/description ; séries de la BDM par son API SDMX, sans clé (https://api.insee.fr/series/BDM/V1/data/SERIES_BDM/) ; Licence Ouverte 2.0 (« Source : Insee », avec la date de mise à jour) |
| Séries | `cpi` : IPC, glissement annuel, ensemble des ménages, France, base 2025, BDM `011814632`, 1997-01 à 2026-09, 357 points ; `hicp` : IPCH, même champ, BDM `011812232`, 1997-01 à 2026-09, 357 points ; `cpiAnnual` : IPC, variation annuelle moyenne, BDM `011814640`, 1997 à 2025, 29 points |
| Chiffre clé | +3,1 % en septembre 2026 (IPC), en hausse après +2,4 % en août ; IPCH +3,4 % |
| Règles | Chiffres définitifs seulement (PO, 02/11/2026) : l'estimation provisoire de fin de mois est écartée, et les deux séries mensuelles s'arrêtent au dernier mois définitif dans les deux. Date de publication retenue : la dernière mise à jour des séries lues (2026-10-30) |
| Première édition | À remplir à la publication |

## « À savoir »

1. Depuis janvier 2026, l'Insee publie l'indice en base 2025, avec la nomenclature eCOICOP v2. Les séries remontent à 1996. Sources : Informations rapides n° 32 du 3 février 2026 (https://www.insee.fr/fr/statistiques/fichier/version-html/8734269/IR32_IPCprov_jan26.pdf) ; « La méthode en bref » (https://www.insee.fr/fr/statistiques/documentation/IPC_Note_methodologique_en_bref_2026.pdf) ; rétropolation : https://www.insee.fr/fr/statistiques/documentation/IPC_operations_changement_annee_2026.pdf.
2. Le chiffre publié à la fin du mois est provisoire ; le définitif paraît vers le milieu du mois suivant et peut le réviser (septembre 2026 : 3,0 % provisoire le 30 septembre, 3,1 % définitif le 15 octobre). Sources : « La méthode en bref » ; Informations rapides n° 247 (https://www.insee.fr/fr/statistiques/9080209).
3. L'IPCH se calcule autrement que l'IPC : d'autres pondérations, et des prix de santé nets des remboursements (l'IPC suit des prix bruts). Source : Informations rapides n° 247, « Pour en savoir plus ».

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans appeler l'API de la BDM qu'utilise le script.

Méthode : aucun appel à `api.insee.fr`. Sources utilisées : Informations rapides et notes de l'Insee (PDF lus en texte), API de diffusion d'Eurostat (`ec.europa.eu/eurostat/api`, jeu `prc_hicp_minr`, IPCH en ECOICOP v2, mis à jour le 2026-10-16), tables FRED de la série OCDE « Consumer Price Index: Total for France » (taux de croissance sur un an, 1956 à 2025-03), API de la Banque mondiale (FP.CPI.TOTL.ZG, mise à jour le 2026-10-08), Trading Economics et presse. Précaution : Eurostat, l'OCDE et la Banque mondiale reprennent des données de l'Insee ; elles sont indépendantes du script (autre canal de diffusion, autre calcul d'arrondi), pas de l'Insee lui-même.

Les séries de l'Insee en base 2025 ont été rétropolées avec la contrainte que l'indice d'ensemble soit identique en ancienne et en nouvelle base (document `IPC_operations_changement_annee_2026.pdf`). Aucun écart de base n'est donc attendu sur les glissements annuels d'ensemble, et aucun n'a été observé (voir les lignes sur l'IPC historique : valeurs en base 2015 identiques à l'arrondi près).

### Chiffres clés

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| IPC, septembre 2026, glissement annuel | +3,1 % | +3,1 % (titre, texte et tableau « Ensemble » : indice 103,07, +3,1 % sur 12 mois). Résultats définitifs, Informations rapides n° 247 | https://www.insee.fr/fr/statistiques/9080209 ; https://www.insee.fr/fr/statistiques/fichier/version-html/9080209/IR247_IPCdef_sept26.pdf | Conforme |
| IPC, août 2026 | +2,4 % | +2,4 % (« après +2,4 % en août ») | idem | Conforme |
| Tendance « up » (sept. vs août) | up | +0,7 point ; l'Insee écrit « Hausse de l'inflation » | idem | Conforme |
| IPCH, septembre 2026 | +3,4 % | +3,4 % (Insee). Eurostat, France, TOTAL, RCH_A : 3,4 | idem ; Eurostat `prc_hicp_minr` (lien en bas) | Conforme |
| IPCH, août 2026 | +2,6 % | +2,6 % (Insee). Eurostat : 2,6 | idem ; Eurostat | Conforme |
| Estimation provisoire d'octobre 2026 laissée de côté (+3,4 %, publiée le 2026-10-30) | exclue volontairement | L'estimation existe bien : « En octobre 2026, les prix à la consommation augmenteraient de 3,4 % sur un an » (IR n° 266, 30 octobre 2026), IPCH +3,8 % ; l'Insee avertit que les indices provisoires sont calculés sur un champ restreint ; résultats définitifs le 13 novembre 2026. L'exclusion est cohérente | https://www.insee.fr/fr/statistiques/fichier/version-html/9107965/IR266_IPCprov_oct26.pdf | Conforme |
| Publication des chiffres définitifs de septembre | Informations rapides n° 247, 2026-10-15 | « Informations Rapides · 15 octobre 2026 · n° 247 » | https://www.insee.fr/fr/statistiques/9080209 | Conforme |
| Révision éventuelle de septembre | non précisée dans le fichier | Par rapport au provisoire du 30 septembre (3,0 %), l'IPC annuel est révisé de +0,1 point ; IPCH annuel confirmé (3,4 %) | IR n° 247, section « Révisions » | Conforme (info utile pour l'« À savoir » 2) |

### Séries mensuelles

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Nombre de points IPC et plage | 357 points, 1997-01 à 2026-09 | 29 ans x 12 + 9 = 357. Eurostat renvoie 357 points IPCH France de 1997-01 à 2026-09 (dernier point : septembre 2026, octobre absent). Les séries Insee en base 2025 débutent en janvier 1996 (indices) ; le glissement annuel existe donc à partir de 1997-01 | Eurostat ; https://www.plus.transformation.gouv.fr/experiences/7343137_impossible-trouver-lindice-que-je-cherche (réponse de l'Insee du 05/05/2026) ; https://www.insee.fr/fr/statistiques/documentation/IPC_operations_changement_annee_2026.pdf | Conforme |
| IPC, premier point 1997-01 | 1,8 | 1,76 (OCDE via FRED), soit 1,8 à l'arrondi | https://fred.stlouisfed.org/data/CPALTT01FRM659N.txt | Conforme (série en base 2015) |
| IPC, maximum 2023-02 | 6,3 | Insee IR n° 63 (15 mars 2023) : +6,3 % en février 2023 (base 2015). OCDE/FRED : 6,28, maximum de 1997-01 à 2025-03. Après mars 2025, aucune valeur proche (septembre 2026 : 3,1) | https://www.insee.fr/fr/statistiques/6966536 ; FRED | Conforme (un écart de base 2015/2025 n'apparaît pas) |
| IPC, minimum 2009-07 | -0,7 | OCDE/FRED : -0,73, minimum de 1997-01 à 2025-03. Trading Economics : plus bas historique -0,7 % en juillet 2009 | FRED ; https://tradingeconomics.com/france/inflation-cpi | Conforme |
| IPC, 1999-01 | 0,2 | 0,24 (OCDE/FRED) | FRED | Conforme |
| IPC, 2003-06 | 2,0 | 1,97 (OCDE/FRED) | FRED | Conforme |
| IPC, 2010-10 | 1,6 | 1,59 (OCDE/FRED) | FRED | Conforme |
| IPC, 2013-11 | 0,7 | 0,68 (OCDE/FRED) | FRED | Conforme |
| IPC, 2024-10 | 1,2 | 1,23 (OCDE/FRED) | FRED | Conforme |
| IPCH, maximum 2023-02 | 7,3 | Eurostat : 7,3 (maximum 1997-2026) ; Insee IR n° 63 : IPCH +7,3 % ; Trading Economics : record 7,30 % en février 2023 | Eurostat ; https://www.insee.fr/fr/statistiques/6966536 ; https://tradingeconomics.com/france/harmonised-inflation-rate-yoy | Conforme |
| IPCH, minimum 2009-07 | -0,8 | Eurostat : -0,8 (minimum) ; Trading Economics : -0,80 % en juillet 2009 | idem | Conforme |
| IPCH, 1999-01 | 0,3 | Eurostat : 0,3 | Eurostat | Conforme |
| IPCH, 2010-10 | 1,8 | Eurostat : 1,8 | Eurostat | Conforme |
| IPCH, 2013-11 | 0,8 | Eurostat : 0,8 | Eurostat | Conforme |
| IPCH, 2024-10 | 1,6 | Eurostat : 1,6 | Eurostat | Conforme |

Remarque : je n'ai pas de second canal pour comparer les 357 points de l'IPC un par un après mars 2025 (la série OCDE s'arrête à 2025-03). Les points d'échantillon, le maximum et le minimum ont été recoupés ; pour l'IPCH, les 357 points sont disponibles chez Eurostat et les points d'échantillon, le maximum et le minimum concordent tous.

### Moyenne annuelle

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2022 / 2023 / 2024 / 2025 | 5,2 / 4,9 / 2,0 / 0,9 | Insee IR n° 8 (15 janvier 2026) : « +0,9 %, après +2,0 % en 2024 (...) +4,9 % en 2023 et +5,2 % en 2022 ». Même chose dans « L'essentiel sur... l'inflation » (23 mars 2026, base 2025). Banque mondiale : 5,22 / 4,88 / 1,997 / 0,944 | https://www.insee.fr/fr/statistiques/fichier/version-html/8726461/IR08_IPCan-2025.pdf ; https://www.insee.fr/fr/statistiques/4268033 ; https://api.worldbank.org/v2/country/FRA/indicator/FP.CPI.TOTL.ZG | Conforme (les tableaux de l'IR n° 8 sont en base 2015 ; la page de mars 2026 en base 2025 donne les mêmes valeurs : pas d'écart de base) |
| 2015 | 0,0 | 0,0 (tableau annuel de la page Insee 4268033) ; Banque mondiale : 0,04 | https://www.insee.fr/fr/statistiques/4268033 | Conforme |
| 2009 | 0,1 | 0,1 (idem) ; Banque mondiale : 0,09 | idem | Conforme |
| 1997 | 1,2 | Pas dans la page Insee (elle commence en 2000). Banque mondiale : 1,20 | https://api.worldbank.org/v2/country/FRA/indicator/FP.CPI.TOTL.ZG?date=1997:2025 | Conforme (source secondaire seulement) |

### Dates et pages sources

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Dernière mise à jour de la série IPC (011814632) | 2026-10-30 | La date de publication des estimations provisoires d'octobre est bien le 30 octobre 2026 (IR n° 266). La page série est rendue en JavaScript : seul le titre est lisible, pas la date de mise à jour. Un miroir tiers (fgeerolf.com) indique « dernière observation : oct. 2026 », « dernière mise à jour des données : 31 oct. 2026 » pour l'ensemble de son jeu, sans pouvoir distinguer cette série | https://www.insee.fr/fr/statistiques/9107965 (IR n° 266) | Non trouvé (cohérent, non confirmé directement) |
| Dernière mise à jour de la série IPCH (011812232) | 2026-10-15 | 15 octobre 2026 = date des résultats définitifs de septembre (IR n° 247). Eurostat (mise à jour du jeu le 2026-10-16) s'arrête à septembre 2026 pour la France. Date affichée par la série elle-même : non lisible | IR n° 247 ; Eurostat | Non trouvé (cohérent, non confirmé directement) |
| Dernière mise à jour de la moyenne annuelle (011814640) | 2026-02-27 | Aucune source trouvée. Jalons connus : IR n° 8 le 15 janvier 2026 ; note « La méthode en bref » mise à jour en février 2026 ; première publication en base 2025 le 3 février 2026 | https://www.insee.fr/fr/statistiques/documentation/IPC_Note_methodologique_en_bref_2026.pdf | Non trouvé |
| Identifiants de séries | 011814632 (IPC), 011812232 (IPCH), 011814640 (moyenne annuelle) | Les pages `serie/<id>` existent (HTTP 200) et leur titre correspond : « Indice des prix à la consommation - Base 2025 - Glissement annuel - Ensemble des ménages - France - Nomenclature Coicop : 00 - Ensemble » ; IPCH, même libellé avec « harmonisé » ; « Indice annuel des prix à la consommation - Base 2025 - Variation annuelle... » | https://www.insee.fr/fr/statistiques/serie/011814632 ; .../011812232 ; .../011814640 | Conforme |
| Page `p1653/description` en ligne et conforme | « Indice des prix à la consommation » | HTTP 200, titre « Description − Indice des prix à la consommation | Insee ». Dit : « L'IPC base 2025 constitue la 9e génération d'indice. Il est entré en service en janvier 2026 », que l'IPC est publié chaque mois au Journal officiel et indexe des contrats, la pension alimentaire, le Smic. Elle ne mentionne ni eCOICOP v2, ni le calendrier provisoire/définitif, ni l'IPCH net des remboursements | https://www.insee.fr/fr/metadonnees/source/indicateur/p1653/description | Conforme pour la base 2025 ; ne couvre pas les autres « À savoir » |
| Page `statistiques/4268033` en ligne et conforme | (page de l'inflation) | HTTP 200, « L'essentiel sur... l'inflation », 23 mars 2026 : IPC base 2025, 9e génération, janvier 2026 ; nomenclature eCOICOP v2 ; moyennes annuelles 2000-2025 ; définition de l'IPCH | https://www.insee.fr/fr/statistiques/4268033 | Conforme |
| Licence de réutilisation | Licence Ouverte / Etalab 2.0 | Confirmée. Texte exact : « Sauf mention contraire, les informations publiques diffusées sur ce site (...) sont mises à disposition sous la Licence Ouverte / Open Licence version 2.0 (Etalab). Cette licence autorise la réutilisation libre, y compris à des fins commerciales, sous réserve de mentionner la source sous la forme « Source : Insee », de mentionner la date de dernière mise à jour des données lorsque celle-ci est connue et de ne pas altérer le sens des informations ou induire en erreur quant à leur interprétation. » (page « Mentions légales et crédits », mise à jour le 13/04/2026). La même page demande aussi de limiter la fréquence des requêtes automatisées | https://www.insee.fr/fr/information/2008466 | Conforme |

Attribution demandée par l'Insee : « Source : Insee », avec la date de dernière mise à jour des données quand elle est connue, sans altérer le sens des informations.

### Les trois affirmations « À savoir »

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| (1) Depuis janvier 2026, IPC en base 2025 avec eCOICOP v2 ; séries base 2015 arrêtées en décembre 2025 | Affirmation | Confirmée. IR n° 7 (15 janvier 2026) : « À partir de janvier 2026 (...) l'année de base 100 deviendra 2025 (...) refonte de la nomenclature (...) eCoicop ». IR n° 32 (3 février 2026) : « depuis les résultats de janvier 2026, les indices de prix à la consommation sont publiés en base 2025 ». Note de l'Insee : nomenclature « COICOP dans sa version 2 (eCOICOPv2) ». Réponse de la Direction générale de l'Insee du 05/05/2026 (relayée sur plus.transformation.gouv.fr) : « Les séries IPC en base 2015 sont toutes arrêtées à décembre 2025. » Nuance : les séries en base 2025 sont rétropolées à partir de janvier 1996 ; le glissement annuel démarre donc en 1997-01, ce qui correspond au fichier | https://www.insee.fr/fr/statistiques/fichier/version-html/8726809/IR07_IPCdef_dec25.pdf ; https://www.insee.fr/fr/statistiques/fichier/version-html/8734269/IR32_IPCprov_jan26.pdf ; https://www.insee.fr/fr/statistiques/documentation/IPC_Note_methodologique_en_bref_2026.pdf ; https://www.plus.transformation.gouv.fr/experiences/7343137_impossible-trouver-lindice-que-je-cherche | Conforme (la phrase « séries base 2015 arrêtées » repose sur une réponse de l'Insee relayée par un tiers, pas sur une page insee.fr que j'ai pu lire) |
| (2) Le chiffre de fin de mois est une estimation provisoire ; le définitif vient vers le 15 du mois suivant et peut être révisé | Affirmation | Confirmée sur le fond. IR n° 266 : « cette publication s'appuie sur des données provisoires (...) résultats définitifs publiés le 13 novembre 2026 ». Note de l'Insee : « L'Insee publie un indice provisoire à la fin de chaque mois. Cet indice est susceptible d'être révisé par l'indice définitif », « L'IPC définitif est publié mensuellement autour du 13 du mois suivant ». Exemple de révision : septembre 2026, 3,0 % provisoire (30 septembre) puis 3,1 % définitif (15 octobre). Nuance de date : l'Insee écrit « autour du 13 » ; dates réelles : 15 janvier, 18 février (janvier), 15 octobre (septembre), 13 novembre (octobre, annoncée). « Vers le 15 » reste acceptable ; « à la mi-mois » serait plus sûr | https://www.insee.fr/fr/statistiques/fichier/version-html/9107965/IR266_IPCprov_oct26.pdf ; https://www.insee.fr/fr/statistiques/documentation/IPC_Note_methodologique_en_bref_2026.pdf ; IR n° 247 | Conforme (avec nuance de date) |
| (3) L'IPCH diffère de l'IPC notamment parce que les prix de santé sont nets des remboursements | Affirmation | Confirmée mot pour mot : « La principale différence entre l'IPCH et l'IPC porte sur les dépenses de santé : l'IPCH suit des prix nets des remboursements de la sécurité sociale tandis que l'IPC suit des prix bruts. » Nuance chiffrée : en septembre 2026, l'écart IPCH-IPC (0,34 point) est dû pour 0,33 point aux différences de pondération et pour 0,01 point seulement aux prix nets/bruts. Le champ diffère aussi (l'IPCH inclut l'éducation et la santé non marchandes, exclut les loyers imputés des propriétaires occupants) | IR n° 247 (« Pour en savoir plus » et paragraphe sur l'écart) ; note méthodologique 2026 | Conforme (le « notamment » est juste en définition, mais pas en ordre de grandeur ce mois-ci) |

### Conclusion

Aucun écart réel. Toutes les valeurs du fichier ont été retrouvées : IPC de septembre 2026 à +3,1 % (août +2,4 %), IPCH à +3,4 % (août +2,6 %), minimum, maximum et points d'échantillon des deux séries mensuelles, moyennes annuelles 2022 à 2025, 2015, 2009 et 1997. Aucun écart lié au changement de base 2025 n'apparaît, ce que la méthode de rétropolation de l'Insee prévoit (indice d'ensemble identique en ancienne et en nouvelle base). L'estimation provisoire d'octobre (+3,4 %, IPCH +3,8 %) existe bien et il est cohérent de ne pas l'utiliser, car les définitifs arrivent le 13 novembre 2026.

Limites :
- Les trois dates de dernière mise à jour des séries (2026-10-30, 2026-10-15, 2026-02-27) ne sont pas lisibles sur les pages `serie/<id>` (rendues en JavaScript) : « Non trouvé ». Les deux premières sont compatibles avec les publications du 30 et du 15 octobre ; la troisième n'a aucun support indépendant.
- Pour l'IPC, la comparaison mensuelle complète n'est possible que jusqu'en mars 2025 (série OCDE) ; au-delà, seuls août et septembre 2026 ont été recoupés avec l'Insee.
- La Banque de France n'a rien publié de retrouvé sur ces chiffres de septembre 2026 : « Non trouvé » (une recherche, aucun résultat exploitable).
- 1997 = 1,2 repose sur la Banque mondiale seule.

Points de rédaction repris dans les « À savoir » :
- « vers le milieu du mois suivant » plutôt que « vers le 15 » : l'Insee dit « autour du 13 » ;
- l'écart entre l'IPCH et l'IPC tient aussi aux pondérations, qui en expliquent l'essentiel en septembre 2026 ;
- la phrase sur l'arrêt des séries en base 2015, qui ne repose que sur une réponse de l'Insee relayée par un tiers, n'est pas reprise ;
- « Source : Insee » et la date de mise à jour des données figurent dans le bloc source de la page (licence).

### URLs consultées (toutes le 2026-11-02)

Insee
- https://www.insee.fr/fr/statistiques/9080209 (IR n° 247, définitifs septembre 2026)
- https://www.insee.fr/fr/statistiques/fichier/version-html/9080209/IR247_IPCdef_sept26.pdf (PDF lu en texte)
- https://www.insee.fr/fr/statistiques/fichier/version-html/9107965/IR266_IPCprov_oct26.pdf (IR n° 266, provisoire octobre 2026)
- https://www.insee.fr/fr/statistiques/fichier/version-html/8726461/IR08_IPCan-2025.pdf (IR n° 8, moyennes annuelles 2025)
- https://www.insee.fr/fr/statistiques/fichier/version-html/8726809/IR07_IPCdef_dec25.pdf (IR n° 7, décembre 2025)
- https://www.insee.fr/fr/statistiques/fichier/version-html/8734269/IR32_IPCprov_jan26.pdf (IR n° 32, janvier 2026)
- https://www.insee.fr/fr/statistiques/6966536 (IR n° 63, février 2023)
- https://www.insee.fr/fr/statistiques/documentation/IPC_operations_changement_annee_2026.pdf
- https://www.insee.fr/fr/statistiques/documentation/IPC_Note_methodologique_en_bref_2026.pdf
- https://www.insee.fr/fr/metadonnees/source/indicateur/p1653/description
- https://www.insee.fr/fr/statistiques/4268033
- https://www.insee.fr/fr/statistiques/serie/011814632 ; https://www.insee.fr/fr/statistiques/serie/011812232 ; https://www.insee.fr/fr/statistiques/serie/011814640 (titres seulement)
- https://www.insee.fr/fr/information/2008466 (licence)
- https://insee.fr/fr/information/1302169 (FAQ, sans contenu utile)

Autres sources
- https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/prc_hicp_minr?format=JSON&lang=EN&geo=FR&coicop18=TOTAL&unit=RCH_A (Eurostat, IPCH France, mis à jour le 2026-10-16)
- https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/prc_hicp_manr?format=JSON&lang=EN&geo=FR&coicop=CP00&unit=RCH_A (ancien jeu Eurostat, gelé au 2026-02-06 ; non utilisé pour les verdicts)
- https://fred.stlouisfed.org/data/CPALTT01FRM659N.txt (OCDE via FRED, IPC France, jusqu'à 2025-03)
- https://api.worldbank.org/v2/country/FRA/indicator/FP.CPI.TOTL.ZG?format=json&per_page=100&date=1997:2025 (Banque mondiale)
- https://tradingeconomics.com/france/inflation-cpi ; https://tradingeconomics.com/france/harmonised-inflation-rate-yoy
- https://www.plus.transformation.gouv.fr/experiences/7343137_impossible-trouver-lindice-que-je-cherche (réponse de l'Insee du 05/05/2026)
- https://fgeerolf.com/data/insee/IPC-2025.html (miroir tiers, indication de date seulement)
- Presse repérée par recherche : https://www.optionfinance.fr/info-financiere-en-continu/d/2026-10-15-france-linflation-revisee-en-hausse-pour-septembre.html (HTTP 403 à la lecture directe, titre seul vu en résultat de recherche)
- Banque de France : recherche faite, aucune page exploitable.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
