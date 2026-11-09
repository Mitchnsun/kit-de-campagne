# `livretA` · Taux du Livret A

**Vérifiée le 09/11/2026** : double vérification sur le web. Les 34 niveaux du taux depuis octobre 1981 sont conformes, mois et taux ; avant 1982, quatre fenêtres de la série de la Banque de France diffèrent des barèmes de l'IPP et de l'histoire du Livret A publiée par la Caisse des dépôts (section « Double vérification ») : **écart non tranché, à décider par le PO** avant l'entrée dans une édition (garder la série depuis 1966, celle du producteur, ou la faire commencer en octobre 1981).

| Champ | Valeur |
| --- | --- |
| Indicateur | `livretA`, dossier « Pouvoir d'achat et logement » (`purchasingPower`), page de type série, ticket #307 de l'app (un chiffre public que le quiz du débat pourra demander) ; « Dans votre campagne » : le thème Pouvoir d'achat et la mesure de l'emprunt national pour la défense (`nationalDefenceLoan`), rémunéré au taux du Livret A |
| Données | `briefings/data/livretA.json`, écrit par `yarn briefings livretA` le 2026-11-09 |
| Sources | Banque de France, Webstat, « Taux du Livret A » (série `MIR1.M.FR.B.L23FRLA.D.R.A.2230U6.EUR.O`, jeu MIR1), page https://webstat.banque-france.fr/fr/catalogue/mir1/MIR1.M.FR.B.L23FRLA.D.R.A.2230U6.EUR.O (anglais : https://webstat.banque-france.fr/en/catalog/mir1/MIR1.M.FR.B.L23FRLA.D.R.A.2230U6.EUR.O), export CSV https://webstat.banque-france.fr/export/csv/fr/catalogue/mir1/MIR1.M.FR.B.L23FRLA.D.R.A.2230U6.EUR.O ; mise à jour le 30/10/2026 (`updated_at` du dernier mois). Citée seulement (`citation-only`) : la fiche de la série ne nomme aucune licence, data.gouv.fr indique « licence non spécifiée » pour le jeu MIR1, et les conditions générales de Webstat demandent « en toute hypothèse » de mentionner la source |
| Séries | `rate` : taux annuel du Livret A en vigueur chaque mois, en %, mensuel, 1966-01 à 2026-11, 731 points, tous au statut normal (`OBS_STATUS` A) et libres (`OBS_CONF` F) ; 43 paliers |
| Chiffre clé | 1,70 % depuis août 2026 (le 1er août), en hausse après 1,50 % (février à juillet 2026) |
| Règles | Le script lit l'export CSV de la série (l'API de Webstat demande une clé, `Authorization: Apikey`, pas l'export) ; il vérifie la clé de la série, son titre « Taux du Livret A », la fréquence mensuelle et l'unité en % ; il écarte un mois postérieur à celui de la récupération, et un dernier mois qui ne serait pas définitif (un mois non définitif avant lui fait échouer le script). Le chiffre clé est le taux en vigueur, au mois où il a pris effet, comme pour le Smic. La page écrit les taux au centième (« 2,25 % »), comme les arrêtés. Un changement au 16 du mois (16 juin 1998, 16 octobre 1981…) tombe dans le mois de son entrée en vigueur |
| Première édition | À remplir à la publication |

## « À savoir »

1. La formule : arrêté du 27 janvier 2021 relatif aux taux d'intérêt des produits d'épargne réglementée (NOR ECOT2101218A, JORF du 11/02/2021, texte 11), article 1er, I, 1° : le taux est le plus élevé de (a) « la moyenne arithmétique entre la moyenne semestrielle des taux à court terme en euros (€STR) » et « l'inflation en France mesurée par la moyenne semestrielle de la variation sur les douze derniers mois connus de l'indice INSEE mensuel des prix à la consommation, hors tabac » et (b) 0,5 %, « après arrondi au dixième de point le plus proche ». L'article 1er est en vigueur depuis le 12/02/2021, sans modification (Légifrance). Le calcul d'août 2026 : communiqué de la Banque de France du 15/07/2026, « une moyenne semestrielle de l'IPC hors tabac en glissement annuel à 1,52 % et un taux €STR moyen à 1,95 % […] de janvier à juin 2026, le taux du livret A ressortant de la formule est de 1,7 % » ((1,52 + 1,95) / 2 = 1,735, arrondi à 1,7).
2. Qui le fixe, et quand : même arrêté, article 1er, II : la Banque de France calcule les taux « chaque année les 15 janvier et 15 juillet » ; le directeur général du Trésor fait publier les nouveaux taux au Journal officiel, applicables le 16 du mois de leur publication, ou le 1er du mois suivant si elle a lieu après le 15 (d'où le 1er février et le 1er août) ; en cas de « circonstances exceptionnelles », ou si la formule ne préserve pas le pouvoir d'achat, le gouverneur transmet ses propositions au ministre chargé de l'économie ; au 15 avril et au 15 octobre, le gouverneur peut proposer une révision au 1er mai ou au 1er novembre (le 1er mai 2009 dans la série). En pratique, le gouverneur propose et l'arrêté fixe : l'arrêté du 28 juillet 2026 (NOR ECOT2619969A, JORF n° 0175 du 29/07/2026) vise « le courrier du gouverneur de la Banque de France du 15 juillet 2026 » et fixe le Livret A à 1,70 % « pour la période du 1er août 2026 au 31 janvier 2027 », signé par le directeur général du Trésor ; service-public (15/07/2026, mis à jour le 31/07/2026) : « Le ministère de l'Économie et des Finances vient d'annoncer une augmentation de ce taux […] en suivant les préconisations du gouverneur de la Banque de France ».
3. Le plus haut et le plus bas : lus dans la série (8,5 % de 1981-10 à 1983-07 ; 0,5 % de 2020-02 à 2022-01), conformes aux barèmes de l'IPP (16/10/1981 à 8,5 % jusqu'au 01/08/1983 ; 01/02/2020 à 0,5 % jusqu'au 01/02/2022).
4. LDDS, LEP et fiscalité : service-public, actualité A15818 (LDDS à 1,7 % du 1er août 2026 au 31 janvier 2027 ; LEP maintenu à 2,5 %, « comme entre le 1er février et le 31 juillet 2026 ») et fiche F2365, vérifiée le 01/08/2026 (« Les intérêts sont exonérés d'impôt sur le revenu et de prélèvements sociaux »). L'arrêté de 2021 (article 1er, I, 1°) fait du taux du LDDS celui du Livret A.

Non repris : le gel de 2023 (le taux maintenu à 3 % jusqu'en janvier 2025), faute d'avoir relu les textes ; le plafond des dépôts (22 950 €), hors du sujet de la page.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Opus) qui cherche sur le web, sans relire l'export de Webstat que lit le script. Publications comparées : les barèmes de l'IPP (Institut des politiques publiques), qui datent chaque taux et citent l'arrêté ou l'avis ; la page « Livret A » de Wikipédia en français, dont le tableau cite Georges Constantin, *Le Livret A : une histoire de l'épargne populaire* (Caisse des dépôts et consignations, La Documentation française, 1999) ; le Journal officiel et service-public pour 2026 ; un tableau de taux moyens annuels (toutsurmesfinances, qui dit s'appuyer sur la Banque de France, donc pas indépendant).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé | 1,7 % depuis 2026-08 | 1,70 % du 1er août 2026 au 31 janvier 2027 ; 1,7 % « à compter du 1er août 2026 (contre 1,5 % entre le 1er février et le 31 juillet 2026) » | arrêté du 28/07/2026 (Légifrance) ; service-public A15818 | Conforme |
| Taux précédent | 1,5 % de 2026-02 à 2026-07 | 1,5 % depuis le 1er février 2026 | service-public A15818 ; presse (Moneyvox, France Transactions) | Conforme |
| Résultat de la formule, août 2026 | 1,7 % | 1,7 % (IPC hors tabac 1,52 %, €STR 1,95 %, janvier à juin 2026) | communiqué de la Banque de France du 15/07/2026 | Conforme |
| Paliers de 1981-10 à 2025-08 (32 changements) | 8,5 (1981-10) ; 7,5 (1983-08) ; 6,5 (1984-08) ; 6 (1985-07) ; 4,5 (1986-05) ; 3,5 (1996-03) ; 3 (1998-06) ; 2,25 (1999-08) ; 3 (2000-07) ; 2,25 (2003-08) ; 2 (2005-08) ; 2,25 (2006-02) ; 2,75 (2006-08) ; 3 (2007-08) ; 3,5 (2008-02) ; 4 (2008-08) ; 2,5 (2009-02) ; 1,75 (2009-05) ; 1,25 (2009-08) ; 1,75 (2010-08) ; 2 (2011-02) ; 2,25 (2011-08) ; 1,75 (2013-02) ; 1,25 (2013-08) ; 1 (2014-08) ; 0,75 (2015-08) ; 0,5 (2020-02) ; 1 (2022-02) ; 2 (2022-08) ; 3 (2023-02) ; 2,4 (2025-02) ; 1,7 (2025-08) | Les mêmes taux, aux mêmes mois (date d'effet le 1er ou le 16 du mois) ; l'IPP s'arrête au 01/08/2025 | barèmes IPP | Conforme |
| Paliers de 1966-01, 1969-06, 1974-01, 1975-01 et 1976-01 | 3 ; 4 ; 6 ; 7,5 ; 6,5 | Les mêmes, aux mêmes dates (1er janvier 1966, 1er juin 1969, 1er janvier 1974, 1975 et 1976) | barèmes IPP ; Wikipédia (Constantin, CDC) | Conforme |
| 1968 | 3 % toute l'année, 3,5 % en 1969-01 | 3,5 % dès le 1er janvier 1968 | barèmes IPP ; Wikipédia (Constantin, CDC) ; le taux moyen annuel de 1968 publié par toutsurmesfinances (3,00 %) suit la Banque de France | Écart non tranché |
| Premier semestre 1970 | 4 % de 1970-01 à 1970-06, 4,25 % en 1970-07 | 4,25 % dès le 1er janvier 1970 | barèmes IPP ; Wikipédia ; taux moyen annuel 1970 de toutsurmesfinances : 4,125 %, comme la Banque de France | Écart non tranché |
| Second semestre 1974 | 6,5 % de 1974-07 à 1974-12 | Aucun changement en juillet 1974 : 6 % jusqu'au 1er janvier 1975 | barèmes IPP ; Wikipédia ; taux moyen 1974 de toutsurmesfinances : 6,25 %, comme la Banque de France | Écart non tranché |
| Avril 1980 à septembre 1981 | 7,5 % de 1980-04 à 1981-09 | Aucun changement en 1980 : 6,5 % jusqu'au 16 octobre 1981 | barèmes IPP ; Wikipédia ; taux moyens 1980 et 1981 de toutsurmesfinances : 7,25 % et 7,75 %, comme la Banque de France | Écart non tranché |
| Méthode et calendrier (« À savoir » 1 et 2) | formule, plancher 0,5 %, calcul les 15 janvier et 15 juillet, 1er février et 1er août | Texte de l'arrêté du 27 janvier 2021 (JORF du 11/02/2021, PDF du JO) ; article 1er en vigueur depuis le 12/02/2021 sans modification | Journal officiel (copie PDF hébergée par le Cercle de l'Épargne) ; Légifrance | Conforme |
| LDDS, LEP, fiscalité (« À savoir » 4) | LDDS au même taux ; LEP 2,5 % depuis le 1er février 2026 ; intérêts exonérés | Identiques | service-public A15818 et F2365 ; arrêté de 2021 | Conforme |
| Licence | citée seulement | Aucune licence sur la fiche de la série (métadonnées Opendatasoft : `license` nul) ; data.gouv.fr, jeu « Webstat MIR1 » : licence non spécifiée, renvoi aux mentions légales de Webstat (page chargée en JavaScript, non lue) ; conditions générales de Webstat : « mentionner la source des jeux de données en cas de réutilisation » | Webstat (API du catalogue, CGU) ; data.gouv.fr | Conforme (citée, comme les projections de la Banque de France) |

Les quatre écarts ne touchent que des taux antérieurs à octobre 1981. Deux publications concordantes (l'IPP, qui ne cite pas de texte pour ces dates, et le tableau de Wikipédia, qui cite l'histoire du Livret A de la Caisse des dépôts) contre la série du producteur ; les taux moyens annuels publiés ailleurs suivent la Banque de France mais disent s'appuyer sur elle. Piste non vérifiée : une prime ou un complément de rémunération compté par la Banque de France et pas par les autres. Aucun arrêté de ces années n'a été relu.

**Conclusion.** Le chiffre clé, le taux précédent et les 34 niveaux depuis octobre 1981 sont conformes ; avant 1982, quatre fenêtres restent en écart non tranché, que le PO décide (série du producteur depuis 1966, ou début en 1981-10, une constante du script).

**Pages consultées** (le 09/11/2026) :

- https://www.legifrance.gouv.fr/eli/arrete/2026/7/28/ECOT2619969A/jo/texte (arrêté du 28 juillet 2026)
- https://www.legifrance.gouv.fr/loda/id/JORFTEXT000043114027 (arrêté du 27 janvier 2021, version en vigueur)
- https://cercledelepargne.com/wp-content/uploads/2015/01/joe_20210211_0036_0011.pdf (JORF du 11/02/2021, texte 11, lu avec `pdftotext`)
- https://www.service-public.gouv.fr/particuliers/actualites/A15818 ; https://www.service-public.gouv.fr/particuliers/vosdroits/F2365
- https://www.banque-france.fr/fr/communiques-de-presse/le-gouverneur-de-la-banque-de-france-propose-de-relever-le-taux-du-livret-17-et-de-maintenir-celui (lu par un outil de résumé ; accès direct refusé)
- https://baremes.ipp.eu/parameters/taxation-du-capital/taxation_capital.epargne.livret_a/table
- https://fr.wikipedia.org/wiki/Livret_A (tableau de l'historique des taux, lu par un outil de résumé)
- https://www.toutsurmesfinances.com/placements/livret-a-et-livret-bleu-historique-du-taux-moyen-annuel-depuis-1970.html (mis à jour le 03/11/2026)
- https://webstat.banque-france.fr/api/explore/v2.1/catalog/datasets/mir1-m-fr-b-l23frla-d-r-a-2230u6-eur-o (métadonnées de la série : titre, 1966-01 à 2026-11, deux décimales) ; https://webstat.banque-france.fr/terms/terms-and-conditions/?flg=fr-fr
- https://www.data.gouv.fr/api/1/datasets/webstat-mir1-1/
- Moneyvox et France Transactions (taux de février 2026), vus dans un moteur de recherche seulement

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Les quatre fenêtres d'avant 1982 tranchées par le PO.
- [ ] Relue par le PO.
