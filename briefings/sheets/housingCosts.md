# `housingCosts` · Prix, taux d'effort et encadrement des loyers (saisi à la main)

**Vérifiée le 10/11/2026** : double vérification sur le web, deux écarts du rapport de recherche corrigés (taux brut du quart modeste en baisse, et non en hausse ; fin de l'encadrement le 23 novembre à Lyon et Villeurbanne) ; les 2 × 66 trimestres de prix relus. La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `housingCosts`, dossier « Pouvoir d'achat et logement » (`purchasingPower`), volet « Prix, taux d'effort, encadrement » de la page composite `housing` (voir `housing.md`), page de type série, recherche du 09/11/2026 |
| Données | `briefings/manual/housingCosts.json`, saisi à la main le 2026-11-10 depuis l'Insee Première n° 2128 (figures 1 et 3), la BDM de l'Insee (dataflow IPLA-IPLNA-2015, mis à jour le 08/09/2026) |
| Sources | 1. Insee, « Le logement pèse moins sur le budget des ménages en 2024 qu’il y a dix ans, sauf pour les plus modestes, Insee Première n° 2128 », https://www.insee.fr/fr/statistiques/9053584, Licence Ouverte 2.0. 2. Insee, « Au deuxième trimestre 2026, les prix des logements anciens reculent de 1,0 %, Informations rapides n° 216 », https://www.insee.fr/fr/statistiques/9040119, séries BDM 010567119 (CVS) et 010567118 (brute), Licence Ouverte 2.0. 3. Insee, « Indice des prix à la consommation », BDM 011815633 (Coicop 04.1, loyers d'habitation effectivement payés), 011814632 et 011814640 (ensemble), pour la note sur les loyers, Licence Ouverte 2.0. 4. DILA, service-public.gouv.fr, « En quoi consiste l'encadrement des loyers à respecter en zone tendue ? » (F1314), https://www.service-public.gouv.fr/particuliers/vosdroits/F1314, citation seulement. 5. Direction générale du Trésor, « Logement : des tensions structurelles pesant sur l'offre et la mobilité, Trésor-Éco n° 405 », https://www.tresor.economie.gouv.fr/Articles/2026/10/02/logement-des-tensions-structurelles-pesant-sur-l-offre-et-la-mobilite, citation seulement |
| Dates de publication | 2026-09-23 (IP 2128) ; 2026-09-08 (IR 216) ; 2026-10-30 (mise à jour de 011814632, glissement de septembre 2026) ; 2026-11-01 (F1314, « Vérifié le 01 novembre 2026 ») ; 2026-10-02 (page du Trésor-Éco) |
| Séries | Annuelles, début 2014 et début 2024 (enquêtes Logement) : `privateNet` (28,3 ; 25,4), `allNet` (18,3 ; 16,8), `poorestGross` (40,8 ; 39,0), `poorestNet` (31,0 ; 32,1) ; début 2024 seulement : `privateGross` (27,4), `socialNet` (24,0), `allGross` (17,5), `over40Private` (22), `over40Social` (18), `over40Accessing` (11). Trimestrielles : `priceIndex` (CVS, 010567119) et `priceIndexRaw` (brute, 010567118), base 100 en moyenne 2015, 2010 T1 à 2026 T2 (provisoire), 66 points chacune |
| Chiffre clé | 25,4 % des revenus des locataires du parc privé, début 2024 (taux d'effort net), en baisse (28,3 % début 2014) ; à côté, le taux net du quart le plus modeste (32,1 %) |
| Règles | Saisie à la main. Quatre vues : « Taux d'effort » (barres privé, social, ensemble ; brut et 2014 au tableau), « Les plus modestes » (brut et net), « Au-delà de 40 % », « Prix des logements anciens » (indice CVS, son plus haut trouvé dans les données). Les variations annuelles moyennes des prix (calculées) ne sont pas saisies. Les loyers de l'IPC sont dans une note, « calculé » : l'Insee ne publie pas leur glissement dans la BDM. L'ILH et l'IRL sont dans « Pouvoir d'achat » (`rentIndices`), pas ici. L'encadrement (territoires, dates, effet) est dans les notes, l'effet toujours avec la baisse de l'offre |
| Première édition | À remplir à la publication |

## « À savoir »

1. Taux d'effort net : dépenses de logement après aides (loyer, charges, énergie, eau, taxe foncière) rapportées aux revenus ; début 2024, hors ménages étudiants ; 25,4 % pour les locataires du privé, 24,0 % pour ceux du social. Source : IP 2128 (« Les locataires du parc privé ont le taux d’effort net le plus élevé, supérieur à celui des locataires du parc social (25,4 % contre 24,0 %) ») ; tableau de la figure 1.
2. Loyers de l'IPC : +1,6 % sur un an en septembre 2026 (calculé : indices 101,81 et 100,17), ensemble des prix +3,1 % (publié) ; en moyenne annuelle 2025, +2,3 % (calculé) contre +0,9 % (publié). Source : BDM 011815633, 011814632 et 011814640. Même nature (variations de l'IPC) : la comparaison est permise. À ne pas confondre avec le +1,6 % de l'ILH du 2e trimestre (coïncidence de valeur).
3. Neuf territoires encadrés ; baux signés jusqu'au 23 novembre 2026 à Lyon et Villeurbanne, jusqu'au 24 ailleurs. Source : F1314 (« dans certaines communes situées en zone tendue, le niveau du loyer est encadré […] il est plafonné » ; « jusqu’au 24 novembre 2026 » à Paris ; « jusqu’au 23 novembre 2026 » à Lyon et Villeurbanne). Les « 9 collectivités, 70 communes » du Sénat recoupent le compte.
4. Loyers modérés de 2 à 4 % en deux ans dans les métropoles concernées, offre locative privée en baisse de 8 % en deux ans dans les métropoles hors Île-de-France, sans effet mesuré à Paris. Source : Trésor-Éco n° 405, p. 2 : « Son évaluation, en mai 2026, confirme un effet de modération des loyers (–2 à –4 % en deux ans dans les métropoles concernées), mais souligne une baisse de –8 % de l'offre locative privée, en deux ans, dans les métropoles hors Île-de-France, (sans effet mesuré à Paris en raison des spécificités du marché locatif parisien) ». La phrase est relue dans le PDF (mise en page en deux colonnes) : « hors Île-de-France » et « sans effet mesuré à Paris » appartiennent à la même colonne ; le rapport final les avait tronqués.

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Aucune affirmation : « Les loyers explosent » est mixte (ILH +1,6 % ; loyers de l'IPC au-dessus de l'ensemble en 2025), écartée par le rapport final.

## Double vérification

Faite le 10/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-logement.md` : BDM retéléchargée, IP 2128 et IR 216 relus, F1314 et Trésor-Éco rouverts.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 25,4 % (début 2024) | Figure 1 : « Locataires du parc privé, 2024 : 27,4 brut, −2,0 aides, 25,4 net » ; 28,3 % début 2014 | https://www.insee.fr/fr/statistiques/9053584 | Conforme |
| Quart le plus modeste | brut 40,8 → 39,0 ; net 31,0 → 32,1 | Figure 3 et texte (« il s’est en revanche accru de 1,1 point […] il atteint 32,1 % ») | idem | Conforme ; écart du rapport de recherche corrigé |
| Au-delà de 40 % | 22 ; 18 ; 11 | Phrase de l'IP 2128 | idem | Conforme, avec réserve : la phrase ne dit pas « net » |
| Prix des logements anciens | 2 × 66 trimestres ; −0,8 % sur un an | Valeurs relues ; 125,1 contre 126,1 (brut) | https://www.insee.fr/fr/statistiques/9040119 | Conforme |
| Loyers de l'IPC (note) | +1,6 % ; +2,3 % | Indices relus, glissements recalculés | BDM 011815633 | Conforme, avec réserve : calculé |
| Encadrement | 9 territoires ; 23 et 24/11/2026 | F1314 ; Sénat (« 9 collectivités, 70 communes ») | https://www.service-public.gouv.fr/particuliers/vosdroits/F1314 | Conforme ; écart du rapport de recherche corrigé |
| Effet | −2 à −4 % ; −8 % d'offre | Trésor-Éco n° 405 | https://www.tresor.economie.gouv.fr/Articles/2026/10/02/logement-des-tensions-structurelles-pesant-sur-l-offre-et-la-mobilite | Conforme, avec réserve : de seconde main |

**Conclusion.** Aucun chiffre du fichier n'est faux ; l'effet de l'encadrement est de seconde main, toujours avec la baisse de l'offre.

**Pages consultées** le 10/11/2026 : les URL ci-dessus.

## Réserves

- L'effet de l'encadrement vient du rapport d'évaluation de mai 2026, cité par la DG Trésor : le rapport lui-même n'a pas été ouvert sur un site officiel. La commission des affaires économiques du Sénat écrit que « les effets à long terme de l'encadrement des loyers sur l'offre locative n'ont pas pu être étudiés » ; la note du Trésor parle de deux ans.
- La fin de l'expérimentation dépend de la prolongation en discussion (adoptée en commission au Sénat le 14/10/2026, vote final non vérifié) : à rouvrir avant le 23 novembre 2026.
- L'indice Notaires-Insee du 3e trimestre 2026 paraît le 24/11/2026 à 8 h 45 : la prochaine édition le remplacera.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert la BDM et les publications.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Insee : Licence Ouverte 2.0, mention « Source : Insee » et date de dernière mise à jour (https://www.insee.fr/fr/information/2008466) ;
  - citation seule : DILA, service-public.gouv.fr, Direction générale du Trésor (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
