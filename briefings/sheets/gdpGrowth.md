# `gdpGrowth` · PIB et croissance

**Vérifiée le 02/11/2026** : double vérification sur le web, sans écart sur les chiffres (section « Double vérification ») ; un lien corrigé (la version anglaise de l'Insee Première n° 2105).

| Champ | Valeur |
| --- | --- |
| Indicateur | `gdpGrowth`, partie de la page composite `growth` (« PIB et croissance »), dossier « Économie et fiscalité » (`economy`), page de type série à deux volets (annuel, trimestriel), ticket #25 de l'app |
| Données | `briefings/data/gdpGrowth.json`, écrit par `yarn briefings gdpGrowth` le 2026-11-02 |
| Sources | Insee, « Les comptes de la Nation en 2025 », Insee Première n° 2105, https://www.insee.fr/fr/statistiques/8996855 (en anglais : https://www.insee.fr/en/statistiques/9003381) ; Insee, « Comptes nationaux trimestriels », https://www.insee.fr/fr/metadonnees/source/serie/s1185 ; séries de la BDM par son API SDMX, sans clé ; Licence Ouverte 2.0 |
| Séries | `growth` : PIB, évolution en volume, comptes annuels base 2020, BDM `011779995`, 2000 à 2025 ; `gdp` : PIB à prix courants, en milliards d'euros (BDM `011779992`, en millions), 2000 à 2025 ; `quarterly` : PIB, évolution en volume, CVS-CJO, BDM `011794844`, les 8 derniers trimestres (2024-T4 à 2026-T3) |
| Statuts | 2025 provisoire, 2024 semi-définitif, 2023 et avant définitifs (comptes annuels) ; tous les trimestres sont marqués définitifs par l'Insee |
| Chiffre clé | +0,8 % en 2025 (provisoire), en baisse après +1,5 % en 2024 ; 3e trimestre 2026 : -0,1 % (première estimation) |
| Règles | Les années provisoires et semi-définitives entrent avec leur statut (PO, 02/11/2026). Les barres annuelles partent de 2000, le volet trimestriel montre les 8 derniers trimestres (#25). Les projections de la Banque de France, saisies à la main d'après un PDF, ne sont pas encore dans le fichier |
| Première édition | À remplir à la publication |

## « À savoir »

1. Les comptes nationaux sont en base 2020 depuis mai 2024 (le 31 mai 2024). Source : note méthodologique de l'Insee « Comptes nationaux trimestriels ».
2. La croissance d'une année paraît d'abord provisoire au printemps suivant, puis semi-définitive un an plus tard, puis définitive encore un an après (fin mai de l'année A+3). Source : Insee Première n° 2105 et note de révision du 3 juin 2026.
3. La croissance trimestrielle est corrigée des variations saisonnières et des jours ouvrables (CVS-CJO), pas la croissance annuelle : en 2025, +0,8 % brute et +0,9 % corrigée. Source : Insee Première n° 2105.
4. Le premier chiffre d'un trimestre paraît environ un mois après sa fin, puis il est révisé : le 2e trimestre 2026 est passé de +0,2 % (30 juillet, n° 184) à 0,0 % (28 août, n° 212). Le 3e trimestre 2026 (-0,1 %) sera détaillé le 27 novembre 2026.

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans appeler l'API de la BDM qu'utilise le script.

Date de la vérification : 2026-11-02. Méthode : pages et PDF publiés par l'Insee (hors `api.insee.fr`), base de diffusion Eurostat (API de diffusion `ec.europa.eu/eurostat`, mise à jour 2026-10-30 pour le trimestriel et 2026-10-22 pour l'annuel), notes méthodologiques de l'Insee. Aucun fichier du projet n'a été modifié.

Limite : Eurostat reçoit ses données de l'Insee, c'est donc un canal de diffusion distinct mais pas une mesure indépendante. Les valeurs annuelles à trois décimales ont été recalculées à partir des niveaux en volume chaînés (millions d'euros 2020) d'Eurostat, pas lues telles quelles.

Sigles : CVS-CJO = corrigé des variations saisonnières et des effets des jours ouvrables ; Insee Première n° 2105 = « Les comptes de la Nation en 2025 ».

### 1. Croissance annuelle du PIB en volume (BDM 011779995, %)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2025 (provisoire) | 0,805 | 0,8 publié par l'Insee ; 0,805 recalculé (2 646 745,6 / 2 625 622,0) ; Eurostat 0,8 (drapeau « p ») | https://www.insee.fr/fr/statistiques/8996855 (Insee Première n° 2105, tableau 1) ; https://www.insee.fr/fr/statistiques/2830613 ; Eurostat `nama_10_gdp` | Conforme |
| 2024 (semi-définitif) | 1,504 | 1,5 publié (page 2830613 : « (sd) semi-définitives ») ; 1,504 recalculé ; Eurostat 1,5 (drapeau « p », voir note) | https://www.insee.fr/fr/statistiques/2830613 ; Eurostat `nama_10_gdp` | Conforme |
| 2023 (définitif) | 1,633 | 1,6 publié ; 1,633 recalculé. Insee Première n° 2105 : « compte définitif 2023 », croissance révisée à +1,6 % | https://www.insee.fr/fr/statistiques/8996855 (encadré) ; https://www.insee.fr/fr/statistiques/2830613 | Conforme |
| 2022 | 2,717 | 2,7 publié ; 2,717 recalculé | https://www.insee.fr/fr/statistiques/2830613 ; Eurostat `nama_10_gdp` | Conforme |
| 2021 | 6,882 | 6,9 publié ; 6,882 recalculé | idem | Conforme |
| 2020 | -7,441 | -7,4 publié ; -7,441 recalculé | idem | Conforme |
| 2001 | 1,899 | Eurostat 1,9 ; 1,899 recalculé. Absent de la page Insee 2830613, qui ne montre que 2020 à 2025 | Eurostat `nama_10_gdp` | Conforme (source Eurostat seule) |
| 2000 | 4,141 | Eurostat 4,1 ; 4,141 recalculé. Absent de la page Insee 2830613 | Eurostat `nama_10_gdp` | Conforme (source Eurostat seule) |
| Chiffre clé « +0,8 % en 2025, en baisse par rapport à 2024 » | +0,8 % ; 2024 = 1,5 % | « le PIB (en volume, sans correction des jours ouvrés) croît de 0,8 %, après une croissance de +1,5 % en 2024 » ; titre : « Le PIB ralentit » | https://www.insee.fr/fr/statistiques/8996855 | Conforme |

Note : Eurostat marque 2024 « p » (provisoire) alors que l'Insee le qualifie de semi-définitif. C'est un écart de libellé : Eurostat n'a pas de drapeau « semi-définitif ».

### 2. PIB annuel aux prix courants (BDM 011779992, milliards d'euros)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2025 (provisoire) | 2 991,056 | Insee : 2 991,1 Md€ (« Le PIB augmente de 0,8 % en 2025 en volume et atteint 2 991,1 milliards d'euros ») ; Eurostat `CP_MEUR` : 2 991 055,9 M€ | https://www.insee.fr/fr/statistiques/8996855 ; https://www.insee.fr/en/statistiques/9003381 ; Eurostat `nama_10_gdp` | Conforme |
| 2024 (semi-définitif) | 2 935,236 | Eurostat : 2 935 236,2 M€ (non publié en valeur courante sur les pages Insee consultées) | Eurostat `nama_10_gdp` | Conforme (source Eurostat seule) |
| 2023 | 2 833,826 | Eurostat : 2 833 826,4 M€ | Eurostat `nama_10_gdp` | Conforme (source Eurostat seule) |
| 2000 | 1 473,517 | Eurostat : 1 473 517,3 M€ | Eurostat `nama_10_gdp` | Conforme (source Eurostat seule) |

### 3. Croissance trimestrielle du PIB en volume, CVS-CJO (BDM 011794844, %)

Valeurs de l'Insee : tableau de la page « Évolution du PIB et de ses composantes, données trimestrielles » (paru le 30/10/2026, commence à 2025-T2). Valeurs Eurostat : `namq_10_gdp`, `CLV_PCH_PRE`, `SCA`, mise à jour 2026-10-30.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| 2024-T4 | -0,1 | Eurostat -0,1. Absent de la page Insee 2830547 (qui commence en 2025-T2). Les publications de 2025 (Informations rapides n° 109 : « après -0,1 % ») donnaient aussi -0,1 | Eurostat `namq_10_gdp` ; https://www.insee.fr/fr/statistiques/8566074 | Conforme (source Eurostat seule) |
| 2025-T1 | 0,2 | Eurostat 0,2. Absent de la page Insee 2830547. Les versions antérieures donnaient 0,1 (première estimation et détaillé de février 2026) | Eurostat `namq_10_gdp` ; https://www.insee.fr/fr/statistiques/8885657 (0,1) | Écart expliqué : la valeur actuelle est 0,2 (révision du profil, voir conclusion) |
| 2025-T2 (« ? » dans la demande) | non précisé | 0,2 (Insee et Eurostat). Les versions antérieures donnaient 0,3 | https://www.insee.fr/fr/statistiques/2830547 ; Eurostat `namq_10_gdp` | Valeur à retenir : 0,2 |
| 2025-T3 | 0,5 | 0,5 (Insee et Eurostat). Les publications de mai à août 2026 donnaient 0,4 | https://www.insee.fr/fr/statistiques/2830547 ; Eurostat `namq_10_gdp` | Conforme |
| 2025-T4 | 0,2 | 0,2 (Insee, tableau de l'Informations rapides n° 263 et page 2830547). 0,3 dans les publications de juillet et août 2026 | https://www.insee.fr/fr/statistiques/fichier/version-html/9111036/IR263_CNT1e_%203T2026.pdf ; https://www.insee.fr/fr/statistiques/2830547 | Conforme |
| 2026-T1 | -0,2 | -0,2 (Insee, Eurostat). Première estimation du 30 avril : -0,1 ; révisé à -0,2 le 28 août | https://www.insee.fr/fr/statistiques/2830547 ; Informations rapides n° 212 (28 août 2026) | Conforme |
| 2026-T2 | 0,0 | 0,0 (Insee, Eurostat). Première estimation du 30 juillet : +0,2 ; révisé à 0,0 le 28 août. Pas de nouvelle révision le 30 octobre (« n'est pas révisée (après arrondi) ») | Informations rapides n° 212 du 28 août 2026 (page Insee https://www.insee.fr/fr/statistiques/9039499 ; texte lu sur une copie du PDF, https://static.poder360.com.br/uploads/2026/08/PIB-Franca-2-trimestre-28-ago-2026.pdf) ; https://www.insee.fr/fr/statistiques/fichier/version-html/9111036/IR263_CNT1e_%203T2026.pdf | Conforme |
| 2026-T3 (première estimation) | -0,1 | -0,1, « Le PIB recule légèrement au troisième trimestre 2026 (-0,1 % après 0,0 %) », Informations rapides n° 263 du 30 octobre 2026 ; Eurostat -0,1 | https://www.insee.fr/fr/statistiques/fichier/version-html/9111036/IR263_CNT1e_%203T2026.pdf ; https://www.insee.fr/fr/statistiques/2830547 | Conforme |

### 4. Dates, statuts et pages sources

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Dernière mise à jour des séries annuelles | 2026-05-29 | 29 mai 2026 : Insee Première n° 2105, Insee Résultats « Comptes nationaux annuels en 2025 », note de révision datée du 3 juin 2026 qui parle de la publication « du 29 mai 2026 ». Pas de révision du PIB annuel depuis : la publication du 28 août 2026 ne mentionne que les tableaux annuels de finances publiques 2025 et une correction de l'emploi, et les valeurs recalculées depuis Eurostat (mise à jour 22 octobre) sont identiques à celles du fichier | https://www.insee.fr/fr/statistiques/8996855 ; https://www.insee.fr/fr/statistiques/8988793 ; https://www.insee.fr/fr/statistiques/fichier/8988934/Note_revisions_2023a2025.pdf | Conforme |
| Dernière mise à jour des séries trimestrielles | 2026-10-30 | Informations rapides n° 263 du 30 octobre 2026 ; page 2830547 « Paru le 30/10/2026 » ; Eurostat mis à jour le 2026-10-30 | https://www.insee.fr/fr/statistiques/2830547 | Conforme |
| Première estimation du T3 2026 publiée le 2026-10-30 | oui | Oui : « Informations Rapides · 30 octobre 2026 · n° 263 ». Prochaines publications : résultats détaillés du T3 le 27 novembre 2026, première estimation du T4 le 29 janvier 2027 | https://www.insee.fr/fr/statistiques/fichier/version-html/9111036/IR263_CNT1e_%203T2026.pdf | Conforme |
| Statuts : 2025 provisoire, 2024 semi-définitif, 2023 définitif | idem | Insee Première n° 2105 : « compte provisoire de l'année 2025 », « compte définitif 2023 et compte semi-définitif 2024, en base 2020 » ; page 2830613 : 2025 « (p) provisoires », 2024 « (sd) semi-définitives » | https://www.insee.fr/fr/statistiques/8996855 ; https://www.insee.fr/fr/statistiques/2830613 | Conforme |
| Page « Les comptes de la Nation en 2025 » (live ? dit ce que le jeu affirme ?) | n° 2105, 8996855 | Page en ligne : Insee Première n° 2105, mai 2026 (29/05/2026), +0,8 %, 2 991,1 Md€, 2025 provisoire, 2024 semi-définitif, base 2020 | https://www.insee.fr/fr/statistiques/8996855 | Conforme |
| Version anglaise de cette page | question posée | L'URL `https://www.insee.fr/en/statistiques/8996855` renvoie une erreur HTTP 404. La version anglaise existe sous un autre identifiant : « National French account in 2025 », Insee Première n° 2105, https://www.insee.fr/en/statistiques/9003381 (en ligne, paru le 29/05/2026, 0,8 % et 1,5 %). Le dossier anglais « The national accounts in 2025 » est en ligne aussi (https://www.insee.fr/en/statistiques/8988863) | https://www.insee.fr/en/statistiques/9003381 | Écart : le lien anglais ne se déduit pas du lien français en changeant `fr` en `en`. Utiliser 9003381 |
| Page métadonnées « Comptes nationaux trimestriels » (fr) | s1185 | En ligne. Objectifs : trimestrialiser les comptes annuels passés et décrire rapidement le passé récent ; « le compte provisoire, publié environ quatre mois après la fin de l'année considérée ». Elle ne mentionne ni la base 2020, ni les 30 jours, ni les révisions (cela se trouve dans la note méthodologique liée, voir section 5). Date affichée « Paru le 02/11/2026 » : c'est la date du jour, probablement une date dynamique | https://www.insee.fr/fr/metadonnees/source/serie/s1185 | Conforme (page en ligne, contenu partiel) |
| Page métadonnées (en) | s1185 en | En ligne, titre « Quarterly national accounts », mêmes contenus qu'en français | https://www.insee.fr/en/metadonnees/source/serie/s1185 | Conforme |
| Intitulés des séries BDM | 011779995, 011779992, 011794844 | 011779995 : « Comptes nationaux annuels base 2020 - Produit intérieur brut - Evolution en volume - Prix chaîné année de base (non équilibré) » ; 011779992 : « … Produit intérieur brut approche produit - Total des secteurs institutionnels - Total des produits - Prix courant » ; 011794844 : « Comptes trimestriels (base 2020) - Évolution du Produit intérieur brut total - Volume aux prix de l'année précédente chaînés - Série CVS-CJO » | https://www.insee.fr/fr/statistiques/serie/011779995 ; …/011779992 ; …/011794844 | Conforme |

### 5. Énoncés « À savoir »

Source principale pour les quatre : note méthodologique de l'Insee « Comptes nationaux trimestriels » (dernière mise à jour 31/05/2024), https://www.insee.fr/fr/statistiques/fichier/8540823/Comptes_m.pdf ; la note de révision du 3 juin 2026 (https://www.insee.fr/fr/statistiques/fichier/8988934/Note_revisions_2023a2025.pdf) et l'Insee Première n° 2105 la complètent.

| Énoncé | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| (1) Comptes nationaux en base 2020 depuis mai 2024 | « depuis mai 2024 » | « Après les bases 2010 et 2014, les comptes nationaux sont passés le 31 mai 2024 à la base 2020 » ; annonce préalable : « À l'occasion de la publication des comptes nationaux le 31 mai 2024, l'Insee mettra en œuvre le passage en nouvelle base 2020 » ; la page 8988793 le répète. Toutes les publications de 2026 consultées portent « base 2020 » | https://www.insee.fr/fr/statistiques/fichier/8540823/Comptes_m.pdf ; https://www.insee.fr/fr/information/7768619 ; https://www.insee.fr/fr/statistiques/8988793 | Conforme |
| (2) Compte provisoire, puis semi-définitif, puis définitif environ trois ans après, révisés à chaque fois | idem | Confirmé : « Chaque année, les comptes définitifs (année N-3), semi-définitif (année N-2) et provisoire (année N-1) sont publiés en mai de l'année N et révisent les estimations annuelles ». Le provisoire de l'année Y paraît fin mai Y+1 (environ quatre mois après la fin de l'année), le semi-définitif fin mai Y+2, le définitif fin mai Y+3, soit environ deux ans et cinq mois après la fin de l'année Y. Révisions constatées en mai 2026 : croissance 2023 relevée de 0,2 point (à 1,6 %), croissance 2024 relevée de 0,3 point (à 1,5 %) ; 2025 non révisé (0,9 % CJO) par rapport à la dernière estimation trimestrielle | Comptes_m.pdf ; Note_revisions_2023a2025.pdf ; Insee Première n° 2105 (encadré) | Conforme, avec une nuance de formulation : « environ trois ans plus tard » s'entend comme « fin mai de la troisième année suivante », donc deux ans après le provisoire. Formulation sans ambiguïté : « le compte définitif paraît au printemps de la troisième année qui suit » |
| (3) Trimestriel CVS-CJO, annuel non corrigé des jours ouvrables, donc écart possible | idem | Confirmé : « la seule différence entre le compte trimestriel annualisé et le compte annuel réside dans le fait que ce dernier n'est pas corrigé des jours ouvrables ». Exemple chiffré pour 2025 : « la croissance du PIB, corrigée de l'effet des jours ouvrables (CJO), avait été estimée à +0,9 % … L'effet des jours ouvrables est négatif sur la croissance en 2025, la croissance non corrigée des jours ouvrés est donc de +0,8 % ». Le tableau de l'Informations rapides n° 263 donne bien 0,9 pour « 2025 » en CVS-CJO | Comptes_m.pdf ; Insee Première n° 2105 (encadré et résumé « sans correction des jours ouvrés ») ; https://www.insee.fr/fr/statistiques/fichier/version-html/9111036/IR263_CNT1e_%203T2026.pdf | Conforme. Exemple utile pour le jeu : 2025 vaut +0,8 % (annuel brut) et +0,9 % (moyenne CVS-CJO des trimestres) |
| (4) Un trimestre est estimé environ 30 jours après sa fin, puis révisé (par ex. le T2 2026) | idem | Confirmé : « La Première estimation est publiée à la fin du premier mois du trimestre suivant » ; le détaillé « moins de 60 jours après la fin du trimestre » ; les comptes trimestriels peuvent être révisés (indicateurs manquants remplacés, CVS révisés, comptes annuels, changement de base). Cas du T2 2026 : première estimation de +0,2 % le 30 juillet 2026 (n° 184), puis 0,0 % le 28 août 2026 (n° 212), « revue à la baisse de 0,2 point après arrondi », en raison d'une production agricole plus dégradée et de prix de services marchands plus dynamiques. Le T1 2026 est passé de -0,1 à -0,2 à cette occasion. Le T3 2026 (publié le 30 octobre, soit 30 jours après le 30 septembre) est dans le même cas | Comptes_m.pdf ; Informations rapides n° 212 (copie du PDF ci-dessus) ; https://www.insee.fr/fr/statistiques/fichier/version-html/9033097/IR184-CNT1e-2T2026.pdf (n° 184, 30 juillet 2026) ; Informations rapides n° 263 | Conforme |

### Conclusion

Aucun écart réel sur les chiffres. Les huit croissances annuelles (à trois décimales, recalculées depuis les niveaux chaînés d'Eurostat), les quatre PIB en valeur courante (exacts à la décimale du milliard, trois décimales comprises), les chiffres clés (+0,8 % en 2025, 1,5 % en 2024, 2 991,1 Md€), les statuts, les dates de mise à jour et les huit trimestres sont conformes aux sources consultées.

À signaler :

1. Lien anglais : `https://www.insee.fr/en/statistiques/8996855` donne une erreur 404. La version anglaise de l'Insee Première n° 2105 est `https://www.insee.fr/en/statistiques/9003381` (titre « National French account in 2025 »). Les deux pages de métadonnées s1185 (fr et en) sont en ligne.
2. 2025-Q1 = 0,2 : valeur conforme à la version actuelle (Eurostat, 30 octobre 2026), mais la page Insee consultée ne remonte qu'à 2025-T2 : je n'ai pas pu la confirmer sur une page de l'Insee. Les publications de janvier-février 2026 donnaient 0,1. De même, 2025-T2 vaut maintenant 0,2 (0,3 auparavant), 2025-T3 0,5 (0,4 dans les publications de mai à août 2026) et 2025-T4 0,2 (0,3 en juillet-août). Le profil trimestriel est donc révisé à chaque publication, ce qui illustre l'énoncé (4). Les valeurs du fichier correspondent à la version du 30 octobre 2026 ; prévoir un nouveau contrôle après le 27 novembre 2026 (résultats détaillés du T3 2026).
3. Le T3 2026 (-0,1) est une première estimation, susceptible d'être révisée le 27 novembre 2026, comme le T2 2026 l'a été de +0,2 à 0,0.
4. Énoncé (2) : exact, mais « environ trois ans plus tard » est approximatif. Le définitif paraît fin mai de la troisième année qui suit l'année concernée, soit deux ans après le provisoire.
5. Énoncé (3) : le texte de l'Insee confirme que 2025 est à +0,8 % en annuel brut et +0,9 % en moyenne CVS-CJO. Si le jeu affiche les deux types de chiffres, cet exemple explique l'écart.
6. Eurostat qualifie 2024 de « provisoire » alors que l'Insee parle de semi-définitif : différence de libellé, pas de valeur.
7. Eurostat n'est pas une source totalement indépendante de l'Insee (il reçoit ses données de l'Insee). Les valeurs de 2000, 2001 et du PIB en valeur de 2023, 2024 et 2000 n'ont pas été lues sur une page de l'Insee (la page 2830613 ne montre que 2020 à 2025, en volume). Non trouvé sur une page de l'Insee pour ces points ; je n'ai pas consulté la Banque de France ni l'OCDE.

### URLs consultées (2026-11-02)

Insee :
- https://www.insee.fr/fr/statistiques/8996855 (Insee Première n° 2105, version HTML)
- https://www.insee.fr/fr/statistiques/fichier/version-html/8996855/IP2105.pdf (texte intégral de l'Insee Première n° 2105)
- https://www.insee.fr/en/statistiques/8996855 (404)
- https://www.insee.fr/en/statistiques/9003381 (version anglaise de l'Insee Première n° 2105)
- https://www.insee.fr/fr/statistiques/8988793 (Insee Résultats « Comptes nationaux annuels en 2025 »)
- https://www.insee.fr/en/statistiques/8988793 (404)
- https://www.insee.fr/en/statistiques/8988863?sommaire=8988972 (dossier anglais « The national accounts in 2025 »)
- https://www.insee.fr/fr/statistiques/2830613 (PIB annuel de 1950 à 2025)
- https://www.insee.fr/fr/statistiques/2830547 (PIB trimestriel, paru le 30/10/2026)
- https://www.insee.fr/fr/statistiques/fichier/8988934/Note_revisions_2023a2025.pdf (note de révision du 3 juin 2026)
- https://www.insee.fr/fr/statistiques/fichier/version-html/9111036/IR263_CNT1e_%203T2026.pdf (Informations rapides n° 263, 30 octobre 2026)
- https://www.insee.fr/fr/statistiques/fichier/version-html/9033097/IR184-CNT1e-2T2026.pdf (Informations rapides n° 184, 30 juillet 2026)
- https://www.insee.fr/fr/statistiques/9039499 (page Insee de l'Informations rapides n° 212, 28 août 2026 : repérée par la recherche, texte lu sur la copie https://static.poder360.com.br/uploads/2026/08/PIB-Franca-2-trimestre-28-ago-2026.pdf, dont le contenu porte l'en-tête « Insee, Informations Rapides · 28 août 2026 · n° 212 »)
- https://www.insee.fr/fr/statistiques/fichier/version-html/8999175/IR133_CNTdet_1T2026.pdf (n° 133, 29 mai 2026)
- https://www.insee.fr/fr/statistiques/fichier/8885657/IR51_CNTdet_4T2025.pdf (n° 51, 27 février 2026) et https://www.insee.fr/fr/statistiques/8732913 (n° 25, 30 janvier 2026)
- https://www.insee.fr/fr/metadonnees/source/serie/s1185 et https://www.insee.fr/en/metadonnees/source/serie/s1185
- https://www.insee.fr/fr/statistiques/fichier/8540823/Comptes_m.pdf (note méthodologique « Comptes nationaux trimestriels », mise à jour 31/05/2024)
- https://www.insee.fr/fr/information/7768619 (annonce du passage en base 2020)
- https://www.insee.fr/fr/statistiques/serie/011779995, …/011779992, …/011794844 (intitulés des séries)

Eurostat (API de diffusion, consultée par `curl`) :
- https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/namq_10_gdp?geo=FR&unit=CLV_PCH_PRE&s_adj=SCA&na_item=B1GQ&sinceTimePeriod=2024-Q3 (trimestriel, mise à jour 2026-10-30)
- https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/nama_10_gdp?geo=FR&na_item=B1GQ&unit=CLV_PCH_PRE (puis `CP_MEUR`, puis `CLV20_MEUR`), annuel, mise à jour 2026-10-22

Presse et autres (recoupement, pas utilisés comme preuve principale) :
- https://www.journaldunet.com/business/1553251-la-croissance-economique-de-la-france-atteint-0-2-au-deuxieme-trimestre-2026-selon-la-premiere-estimation-de-l-insee/ (T2 2026 à +0,2 le 30 juillet)
- https://etudes-economiques.credit-agricole.com/s3-b-dj-prod-drupal-internet/s3fs-public/document/documents-2026-07/Persp26-163-France-Flash-PIB-20260730.pdf (Crédit Agricole, Flash PIB du 30 juillet 2026)
- Résultats de recherche : economiematin.fr, france-epargne.fr, optionfinance.fr (T3 2026 à -0,1 le 30 octobre ; T2 ramené à zéro)

## Mises à jour

- **03/11/2026, projections de la Banque de France (#25)** : relevées par le PO sur banque-france.fr, que les scripts ne peuvent pas lire. « Projections macroéconomiques intermédiaires – Septembre 2026 », mises en ligne le 15/09/2026, hypothèses de l'Eurosystème arrêtées au 19/08/2026. Croissance du PIB : 0,4 % en 2026, 0,9 % en 2027, 1,2 % en 2028. IPCH : 2,3 %, 1,9 %, 1,6 % ; hors énergie et alimentation : 1,6 %, 2,3 %, 1,9 %. Édition précédente (juin 2026) : PIB 0,5 / 0,9 / 1,2 %, IPCH 2,5 / 1,7 / 1,7 %.
- **Double vérification** (agent Claude Sonnet, sans le site de la Banque de France) : les neuf valeurs de septembre et celles de juin sont conformes (Daf-Mag et Franceinfo lus, résumés des pages de la Banque de France). « Intermédiaires », le 15/09 et le gel au 19/08 sont conformes. Non trouvé : les conditions de réutilisation de la Banque de France (mentions légales en 403). Un indicateur ne pouvant avoir à la fois des données de script et une saisie à la main, la page devient composite (PO, 03/11/2026 : un volet à part) : `growth`, « PIB et croissance », avec deux parties, `gdpGrowth` (ces comptes nationaux) et `growthProjections` (les projections, voir `growthProjections.md`).

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
