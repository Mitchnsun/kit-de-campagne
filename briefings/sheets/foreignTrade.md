# `foreignTrade` · Commerce extérieur (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; la valeur de 2025 retenue est la plus récente (6 novembre 2026), la première publication (février 2026) est dite dans une note ; réserves de lecture reprises ci-dessous. La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `foreignTrade`, dossier « Économie et fiscalité » (`economy`), volet « Commerce » de la page composite `competitiveness` (voir `competitiveness.md`), page de type série, recherche « Ce qu'on entend » du 09/11/2026 |
| Données | `briefings/manual/foreignTrade.json`, saisi le 2026-11-09 depuis la série annuelle FAB-FAB des Douanes (fichier `FAB1971.XLS`, mise à jour de la publication des données de septembre 2026), l'analyse annuelle 2025 des Douanes et l'API d'Eurostat (`tipsbp20`) ; valeurs lues par script dans les fichiers téléchargés |
| Sources | 1. Douanes, « Le chiffre du commerce extérieur – 3e trimestre 2026 », https://lekiosque.finances.gouv.fr/fichiers/Etudes/Thematiques/3T2026.pdf (6 novembre 2026), données : « La série annuelle FAB-FAB depuis 1971 », https://lekiosque.finances.gouv.fr/site_fr/telechargement/transfert_file.asp?id=8, citation seule, en français. 2. Douanes, « Le chiffre du commerce extérieur – Analyse annuelle 2025 », https://www.douane.gouv.fr/sites/default/files/2026-02/09/chiffre-comex-Analyse-Annuelle-2025.pdf (6 février 2026), citation seule, en français. 3. Eurostat, « Current account balance - annual data », jeu `tipsbp20`, https://ec.europa.eu/eurostat/databrowser/view/tipsbp20/default/table?lang=fr (et `lang=en`), API https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/tipsbp20?unit=PC_GDP&unit=MIO_NAC&geo=FR&geo=DE&sinceTimePeriod=2000 (mise à jour du 28/10/2026), conditions d'Eurostat |
| Séries | `tradeBalance` : solde commercial des biens FAB/FAB, matériel militaire et estimations sous le seuil compris, données brutes, Md€ (M€ du fichier divisés par 1 000), 1971 à 2025, 55 points (1971 : 0,871 ; 2019 : −58,128 ; 2020 : −63,559 ; 2021 : −84,939 ; 2022 : −160,296 ; 2023 : −96,858 ; 2024 : −77,757 ; 2025 : −65,273), ruptures 1988 et 1991 (mises en garde du fichier). `currentAccountFrance` et `currentAccountGermany` : solde des transactions courantes vis-à-vis du reste du monde, en % du PIB, non désaisonnalisé, 2000 à 2025, 26 points chacune (France 2025 : −0,4 ; Allemagne 2025 : +4,4). `worldExportShare` : part de la France dans les exportations mondiales de marchandises, 2025 seulement, 2,6 % (analyse annuelle des Douanes, d'après l'OMC) |
| Chiffre clé | −65,273 Md€ en 2025 (affiché −65,3 Md€), tendance à la hausse (−77,757 en 2024) ; à côté : part des exportations mondiales (2,6 %) et solde des transactions courantes de 2025 (−0,4 % du PIB) |
| Règles | Saisie à la main. La valeur de 2025 est celle de la publication du 6 novembre 2026 ; les −69,2 Md€ de la première publication (6 février 2026) ne sont que dans « À savoir » et l'affirmation, avec leur date. Les dernières années sont révisées à chaque publication : aucune n'est marquée provisoire, faute d'un statut écrit dans le fichier, la note de la vue le dit. Ruptures de 1988 (départements d'outre-mer dans le champ) et 1991 (lancements de Kourou) : `breaks`, d'après les mises en garde du fichier. Le solde courant est comparé à l'Allemagne seulement : ceux de l'UE et de la zone euro sont mesurés hors UE ou hors zone, non comparables (écartés par la contre-vérification). Le solde des biens de la balance des paiements (−58 026 M€) n'est pas saisi : autre concept que celui des Douanes |
| Première édition | À remplir à la publication |

## « À savoir »

1. La valeur de 2025 est celle du 6 novembre 2026 (−65,3 Md€) ; la première publication du 6 février 2026 donnait −69,2 Md€ ; les années récentes sont révisées. Source : Douanes, 3T2026 (« Solde FAB/FAB (Md€) -77,8 -65,3 ») et fichier FAB1971 (« 2025,616341,681614,-65273,90.424 ») ; analyse annuelle 2025 (« En 2025, le solde commercial FAB/FAB en valeur augmente de 10,0 milliards d'euros par rapport à 2024 et s'établit à -69,2 Md€. »). La recherche relève les révisions successives : −69,2 (février), −67,9 (mai), −65,2 (août), −65,3 (novembre).
2. Le solde des Douanes ne compte que les biens ; le solde des transactions courantes ajoute les services et les revenus : −11,6 Md€ en 2025, soit −0,4 % du PIB. Source : Eurostat, `tipsbp20` (« FR 2025 => -0.4 » en % du PIB, « -11595.0 » en M€), d'après la Banque de France (son communiqué n'a pas été ouvert, site fermé aux scripts).
3. Part de marché mondiale : 2,6 % en 2025, −0,4 point depuis 2019, Allemagne −1,0 point ; 4e trimestre 2025 estimé, ratio dépendant du change. Source : Douanes, analyse annuelle 2025 (« En 2025, les exportations de la France représentent 2,6 % … du montant des exportations mondiales de marchandises » ; « la part de marché de la France a baissé de 0,4 point, une baisse proche de celle du Royaume-Uni (-0,3 point) mais inférieure à celle de l'Allemagne (-1,0 point) »). Chiffre non revu dans la publication de novembre 2026.
4. Deux ruptures de la série, 1988 et 1991. Source : fichier FAB1971, mises en garde (« Les séries depuis 1988 intègrent ce changement qui minimise les exportations : le déficit global de la France se creuse ainsi en 1988. » ; « Les séries depuis 1991 intègrent ce changement qui a plus fortement minimisé les exportations et donc pénalisé la balance commerciale. »).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

L'affirmation est dans `briefings/notes/foreignTrade.json` (clé `claims`, français et anglais). Source de chaque chiffre de la réponse :

1. « On entend que le déficit commercial de la France n'a jamais été aussi grave. » 65,3 Md€ en 2025, révisés le 6 novembre 2026 : Douanes, 3T2026 et FAB1971. 69,2 Md€ à la première publication : analyse annuelle du 6 février 2026. 160,3 Md€ en 2022, plus fort déficit de la série : FAB1971 (« 2022,601510,761806,-160296 » ; l'analyse de février écrivait −161,7 Md€, données antérieures). 58,1 Md€ en 2019 : FAB1971 (« 2019,509418,567546,-58128 »). −0,4 % du PIB : Eurostat, `tipsbp20`. Démentie par les chiffres de la page : le déficit de 2025 est près de 2,5 fois plus faible que celui de 2022 (calculé, dans cette fiche seulement) ; la réponse dit aussi qu'il reste plus creusé qu'en 2019.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-competitivite.md` (fichiers retéléchargés, PDF lus avec `pdftotext`, XLS converti). Les points des séries que le rapport ne cite pas (1971 à 2018, soldes courants de 2000 à 2024) ont été relus par l'agent de la page, par script, dans `FAB1971.XLS` et la réponse de l'API d'Eurostat.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, solde 2025 | −65,273 Md€ | « Solde FAB/FAB (Md€) -77,8 -65,3 » ; FAB1971 : −65 273 M€ | 3T2026 et FAB1971 (URL ci-dessus) | Conforme, avec réserve : données brutes, révisables ; concept des Douanes |
| Première publication | −69,2 Md€ (note seulement) | « s'établit à -69,2 Md€ » | analyse annuelle 2025 | Conforme : première publication, à citer avec sa date |
| Série 2019 à 2025 | −58,128 … −65,273 | mêmes valeurs dans FAB1971 | FAB1971 | Conforme |
| Point bas de 2022 | −160,296 | « 2022,601510,761806,-160296 » ; l'analyse de février citait −161,7 | FAB1971 | Conforme, série révisée |
| Part de marché | 2,6 % ; −0,4 point ; Allemagne −1,0 | phrases relues | analyse annuelle 2025 | Conforme, avec réserve : 4e trimestre estimé, change |
| Solde courant 2025 | France −0,4 ; Allemagne +4,4 (% du PIB) | `tipsbp20` (28/10/2026) ; −11 595 M€ (`bop_c6_a`, 02/10/2026) | API d'Eurostat | Conforme, avec réserve : UE et zone euro écartées ; Banque de France non ouverte |

**Conclusion.** Aucun chiffre du fichier n'est faux ; la valeur de 2025 est la plus récente, et sa première publication est dite avec sa date.

**Pages consultées** le 09/11/2026 : les documents et API des URL ci-dessus. Non ouverte : la balance des paiements de la Banque de France (https://www.banque-france.fr/fr/statistiques/balance-des-paiements/balance-des-paiements-de-la-france-2025-12, réponse 403).

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Pas de script : la double vérification a rouvert les fichiers des Douanes et l'API d'Eurostat.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée ; la mention des Douanes est lue (« source : douanes françaises, résultats de [mois année] »), celle d'Eurostat est celle de ses conditions.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
