# `debtCost` · Ce que coûte la dette (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart sur les chiffres saisis ; réserves de lecture reprises ci-dessous. La licence des sources citées seulement n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `debtCost`, dossier « Économie et fiscalité » (`economy`), page de type comparaison, recherche « Ce qu'on entend » du 09/11/2026 |
| Données | `briefings/manual/debtCost.json`, saisi à la main le 2026-11-09 depuis le tableau 3.201 de l'Insee, l'avis n° HCFP-2026-5, le projet de loi de finances pour 2027 (n° 3210) et son projet annuel de performances « Engagements financiers de l'État » |
| Sources | 1. Insee, « Dépenses et recettes des administrations publiques en 2025 », https://www.insee.fr/fr/statistiques/8988845, tableau https://www.insee.fr/fr/statistiques/fichier/8988845/t_3201_fr.xlsx (28/08/2026), Licence Ouverte 2.0. 2. Haut Conseil des finances publiques, « Avis n° HCFP-2026-5 relatif aux projets de lois de finances et de financement de la sécurité sociale pour l'année 2027 », https://www.hcfp.fr/sites/default/files/2026-10/Avis%20HCFP%202026-5%20-%20PLF-PLFSS%202027.pdf (25/09/2026), citation seule. 3. Assemblée nationale, « Projet de loi de finances pour 2027, n° 3210 », https://www.assemblee-nationale.fr/dyn/opendata/PRJLANR5L17B3210.pdf (01/10/2026), Licence Ouverte 1.0 comme pour `financeBill`. 4. Direction du budget, « Projet annuel de performances 2027, Engagements financiers de l'État », https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128231/file/PAP%202027%20-%20Engagements%20financiers%20de%20l%27Etat.pdf (01/10/2026), citation seule. 5. Cour des comptes, « La situation et les perspectives des finances publiques », https://www.ccomptes.fr/fr/publications/la-situation-et-les-perspectives-des-finances-publiques-17, synthèse https://www.ccomptes.fr/sites/default/files/2026-06/20260625-synthese-RSPFP-2026.pdf (25/06/2026), citation seule. 6. Insee, « Dépenses des administrations publiques ventilées par fonction en 2024 », https://www.insee.fr/fr/statistiques/8574707, tableau T_3301 (27/03/2026), Licence Ouverte 2.0. 7. Insee, « Dette et déficit publics au sens de Maastricht en 2025 », https://www.insee.fr/fr/statistiques/8988843 (28/08/2026), Licence Ouverte 2.0. 8. Insee, « Bilan démographique 2025 », Insee Première n° 2087, https://www.insee.fr/fr/statistiques/8719824 (13/01/2026), Licence Ouverte 2.0. Toutes en français seulement |
| Séries | `apuInterest` : intérêts (D41) versés par toutes les administrations publiques, Md€, 2022 à 2025, 4 points (50,9 ; 53,4 ; 60,1 ; 65,7), 2024 semi-définitif et 2025 provisoire comme dans `publicFinances` ; `apuInterestForecast` : charge d'intérêts de toutes les administrations prévue par le Gouvernement (HCFP, § 115), Md€, 2026 et 2027, 2 points (79,2 ; 91), statut `projection` ; `stateCharge` : charge de la dette du budget de l'État, SNCF Réseau comprise, exécutée, Md€, 2025, 1 point (51,6) ; `stateChargeForecast` : la même, révisée pour 2026 et au projet pour 2027, Md€, 2 points (63,4 ; 72,9), statut `projection` |
| Chiffre clé | 65,7 Md€ d'intérêts versés par toutes les administrations publiques en 2025 (provisoire), en hausse (60,1 Md€ en 2024) ; à côté, la charge de la dette du budget de l'État en 2025, 51,6 Md€ |
| Règles | Saisie à la main. Toutes administrations (comptabilité nationale) et budget de l'État ne sont jamais dans la même série ni le même bloc, pas plus que l'exécuté et le prévu : quatre séries, deux vues, un bloc par série. Les prévisions portent le statut `projection`, dites « prévision » sur la page. La loi de finances initiale 2026 de l'État (59,3 Md€) n'est pas saisie. Le taux des OAT (3,35 %) et le choc d'un point de taux sont dans « À savoir », pas en série : la page écrit un taux au dixième. La dette par habitant, calculée, n'est qu'une affirmation, avec sa précaution |
| Première édition | À remplir à la publication |

## « À savoir »

1. Les intérêts mesurés par l'Insee sont ceux de toutes les administrations publiques, en comptabilité nationale ; la charge de la dette de l'État relève de son budget et compte en 2027 une provision de 8,5 Md€ pour l'indexation des titres sur l'inflation, sans décaissement. Source : Insee, tableau 3.201 (ligne « Intérêts (D41) ») ; projet de loi de finances pour 2027, n° 3210 (« la neutralisation de la provision annuelle pour indexation du capital des titres indexés (-8,5 milliards d'euros), inscrite en dépense dans le déficit budgétaire à financer alors qu'elle ne génère pas de besoin en trésorerie »).
2. Les montants de 2026 et de 2027 sont des prévisions du Gouvernement, non votées : 91 Md€ d'intérêts en 2027 pour toutes les administrations, soit 2,9 points de PIB ; le HCFP juge optimiste la croissance de 2027 retenue par le Gouvernement. Source : avis n° HCFP-2026-5, § 115 (« La charge d'intérêts atteindrait 2,9 points de PIB (soit 91 Md€ courants) en 2027 dans la prévision présentée au Haut Conseil ») et synthèse (« le chiffre de croissance pour 2027 retenu par le Gouvernement apparaît comme optimiste au regard des dernières évolutions »).
3. Le taux moyen à l'émission des OAT est passé d'un taux nul en moyenne en 2021 à 1,70 % en 2022 et 3,35 % en 2025 ; c'est le taux des emprunts nouveaux, pas le coût moyen de toute la dette. Source : Cour des comptes, synthèse du 25/06/2026 (« le taux moyen à l'émission des obligations assimilables du Trésor (OAT) s'est élevé à 3,35 % en 2025, alors qu'il n'était que de 1,70 % en 2022 et nul en moyenne en 2021 »).
4. Une hausse d'un point de tous les taux au 1er janvier 2027 alourdirait la charge de la dette négociable de l'État de 3,4 Md€ la première année et d'environ 19 Md€ la cinquième. Source : projet annuel de performances « Engagements financiers de l'État », p. 39-41 (« L'effet d'un choc de +1 % (+100 points de base) par rapport au scénario de référence, qui interviendrait le 1er janvier 2027, sur l'ensemble de la courbe […] serait de 3,4 Md€ la première année, d'environ 19 Md€ la cinquième année » ; « En raison du refinancement progressif de la dette, l'impact sur le taux d'intérêt moyen de l'ensemble de la dette serait graduel »). Évaluation en comptabilité maastrichtienne.

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/debtCost.json` (clé `claims`, français et anglais), reprise de la recherche vérifiée du 09/11/2026 sans changer sa formulation. Source de chaque chiffre de la réponse :

1. « On entend que les intérêts de la dette, c'est 91 milliards (ou 66, ou 72). » 65,7 Md€ en 2025 : Insee, tableau 3.201. 91 Md€ en 2027 : avis n° HCFP-2026-5, § 115. 51,6 Md€ (2025) et 72,9 Md€ (2027) : projet de loi de finances pour 2027, tableau de l'équilibre (« Charge de la dette (yc SNCF) 51,6 59,3 63,4 +4,1 72,9 »).
2. « On entend que la charge de la dette est devenue le premier budget de l'État, devant l'Éducation et la Défense. » 72,9 ; 73,2 (Défense, 73 153 440 797 €) ; 90,9 Md€ (Enseignement scolaire, 90 859 899 196 €) : projet de loi de finances pour 2027, état B. 58,9 et 148,6 Md€ : Insee, tableau T_3301 (2024). Citation : Cour des comptes, page de la publication du 25/06/2026. Réserve : les crédits des missions comprennent les cotisations au compte « Pensions » ; l'affirmation « hors pensions, l'Éducation descend sous la charge de la dette » n'a pas été retrouvée et n'est pas reprise.
3. « On entend que l'État ne rembourse jamais sa dette et ne paie que les intérêts. » 179,5 Md€ d'amortissements et 340,0 Md€ d'émissions en 2027 : projet de loi de finances pour 2027, tableau de financement (« le besoin de financement s'établit à 339,7 milliards d'euros »).
4. « On entend que les fonctionnaires creusent la dette, ou que c'est la faute des collectivités. » 370,0 Md€ en 2025 : Insee, tableau 3.201 (ligne « Rémunération des salariés (D1) ») ; 21,6 % calculé sur 1 714,1 Md€ de dépenses (même tableau). 30 % et 2 % : avis n° HCFP-2026-5, tableau 10, que le Haut Conseil dit « mêle[r] à la fois dépenses en comptabilité nationale et budgétaire ».

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-finances.md` : chaque source rouverte par `curl`, lue avec `pdftotext` ou `openpyxl`, sans passer par les fichiers de l'agent de recherche. Aucun écart sur les chiffres saisis.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, intérêts de toutes les administrations | 50,9 ; 53,4 ; 60,1 ; 65,7 Md€ (2022-2025) | Ligne « Intérêts (D41) » identique ; la Cour écrit « la charge de la dette a atteint 65,7 Md€ (2,2 points de PIB) » | https://www.insee.fr/fr/statistiques/fichier/8988845/t_3201_fr.xlsx | Conforme |
| Prévision des intérêts | 79,2 (2026) ; 91 Md€ (2027) | « le Gouvernement prévoit une charge d'intérêts de 79,2 Md€ » ; « 2,9 points de PIB (soit 91 Md€ courants) en 2027 » | avis HCFP (URL ci-dessus) | Conforme |
| Charge de la dette de l'État | 51,6 ; 63,4 ; 72,9 Md€ | « Charge de la dette (yc SNCF) 51,6 59,3 63,4 +4,1 72,9 +9,6 +13,7 » (page 14) | https://www.assemblee-nationale.fr/dyn/opendata/PRJLANR5L17B3210.pdf | Conforme |
| Taux des OAT | 0 ; 1,70 ; 3,35 % | phrase de la synthèse identique | synthèse de la Cour (URL ci-dessus) | Conforme |
| Choc d'un point | 3,4 puis environ 19 Md€ | identique ; « +3,4 » apparaît aussi comme effet taux 2025-2026, autre chose | PAP « Engagements financiers de l'État », p. 39-41 | Conforme |
| Remboursements et émissions | 179,5 et 340,0 Md€ | identique ; besoin de 339,7 Md€ | projet de loi de finances (URL ci-dessus) | Conforme |
| Dette et dette nette | 3 460,1 et 3 242,7 Md€ | tableaux 3.101 et 3.103 identiques (fin 2025 révisé à 3 242,8 dans la série trimestrielle, sans effet) | https://www.insee.fr/fr/statistiques/fichier/8988843/t_3101_fr.xlsx | Conforme |
| Population | 69,1 millions | « Au 1er janvier 2026, la population en France est estimée à 69,1 millions d'habitants » | https://www.insee.fr/fr/statistiques/8719824 | Conforme |
| Dépenses par fonction | 58,9 et 148,6 Md€ (2024) | cellules 58,87 et 148,64 du tableau T_3301 | https://www.insee.fr/fr/statistiques/fichier/8574707/T_3301.xlsx | Conforme, avec réserve sur la date (voir « Réserves ») |

**Conclusion.** Aucun chiffre du fichier n'est faux. Les montants de toutes les administrations et du budget de l'État, comme l'exécuté et le prévu, sont des chiffres différents : la page ne les additionne ni ne les met dans un même bloc.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus. La page Insee 8574707 (« Paru le 27/03/2026 ») a été rouverte le 09/11/2026 pour le titre et la date de la source 6.

## Réserves

- Le chiffre 2025 de l'Insee est provisoire. Hors correction des services d'intermédiation financière (D41G), les intérêts de 2025 sont de 64,7 Md€.
- La charge de la dette de l'État de 72,9 Md€ (SNCF Réseau comprise) n'est ni le programme 117 entier (72,4 Md€, celui de `financeBill`), ni la charge de la dette négociable hors trésorerie du PAP (71,9 Md€). Deux hausses 2026-2027 coexistent (+9,6 Md€ au projet, +10,3 Md€ au PAP) : aucune n'est saisie.
- La contre-vérification n'a pas retrouvé la date du 27/03/2026 du tableau T_3301 ; la page Insee 8574707 la donne (« Paru le 27/03/2026 »), le fichier porte une date de création du 28/11/2025. Les dépenses 2025 par fonction paraîtront en décembre 2026.
- La dette par habitant et la part des rémunérations dans la dépense sont calculées, et dites telles.

## Mises à jour

**09/11/2026** : le bloc « Ce qu'on entend » ne garde que les fausses vérités que les chiffres de la page démentent (décision du PO) : affirmations retirées : « On entend que la dette, c'est 50 000 € par Français. ».
- **09/11/2026** : l'affirmation sur la dette par habitant revient, à la demande du PO, sous la forme d'une fausse vérité (« chaque Français doit 50 000 € à cause de la dette publique ») : la dette publique est celle des administrations, pas une dette personnelle exigible des habitants ; le calcul (environ 50 100 €, 3 460,1 Md€ pour 69,1 millions d'habitants) et la dette nette (3 242,7 Md€) restent ceux de la contre-vérification.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source. Il n'y a pas de script : la contre-vérification a rouvert les documents eux-mêmes.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Insee : Licence Ouverte 2.0, mention « Source : Insee » et date de dernière mise à jour (https://www.insee.fr/fr/information/2008466) ;
  - Assemblée nationale : la « Licence Ouverte 1.0 » du registre est déduite ; les mentions légales du site (https://www.assemblee-nationale.fr/dyn/info-site, lues le 12/11/2026) interdisent la réutilisation commerciale et ne permettent la reproduction que si sa diffusion est gratuite. Le PO a décidé le 12/11/2026 de citer ces documents depuis la Direction du budget : en attente de la lecture de budget.gouv.fr ;
  - citation seule : Haut Conseil des finances publiques, Direction du budget, Cour des comptes (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
