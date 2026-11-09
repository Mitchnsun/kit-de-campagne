# `publicSpending` · Où va l'argent public (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, un écart de décompte corrigé (rang de l'OCDE sur 36 pays, et non 37) ; réserves de lecture reprises ci-dessous. La licence des sources citées seulement n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `publicSpending`, dossier « Économie et fiscalité » (`economy`), page de type comparaison, recherche « Ce qu'on entend » du 09/11/2026 |
| Données | `briefings/manual/publicSpending.json`, saisi à la main le 2026-11-09 depuis le tableau T_3301 de l'Insee, l'API et les communiqués d'Eurostat, l'API de l'OCDE et le projet annuel de performances « Pouvoirs publics » |
| Sources | 1. Insee, « Dépenses des administrations publiques ventilées par fonction en 2024 », https://www.insee.fr/fr/statistiques/8574707, tableau https://www.insee.fr/fr/statistiques/fichier/8574707/T_3301.xlsx (27/03/2026), Licence Ouverte 2.0, en français seulement. 2. Insee, « Dépenses et recettes des administrations publiques en 2025 », https://www.insee.fr/fr/statistiques/8988845 (28/08/2026 ; tableaux 3.201 et 3.217), Licence Ouverte 2.0, en français seulement. 3. Eurostat, « Dépenses des administrations publiques par fonction (CFAP) », jeu `gov_10a_exp`, https://ec.europa.eu/eurostat/databrowser/view/gov_10a_exp/default/table?lang=fr (mise à jour du 21/10/2026), conditions d'Eurostat. 4. Eurostat, « Euro area government deficit at 3.0% and EU at 3.1% of GDP », https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-21102026-ap (21/10/2026), conditions d'Eurostat, en anglais. 5. Eurostat, « EU and euro area tax-to-GDP ratio up in 2025 », https://ec.europa.eu/eurostat/web/products-eurostat-news/w/ddn-20261029-3 (29/10/2026), conditions d'Eurostat, en anglais. 6. OCDE, « Revenue Statistics 2025 », jeu `DSD_REV_COMP_OECD@DF_RSOECD` lu par l'API https://sdmx.oecd.org/public/rest/data/OECD.CTP.TPS,DSD_REV_COMP_OECD@DF_RSOECD,/.TAX_REV.S13._T._T.PT_B1GQ.A?startPeriod=2023&endPeriod=2024&format=csvfilewithlabels (12/2025), citation seule. 7. Direction du budget, « Projet annuel de performances 2027, Pouvoirs publics », https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128255/file/PAP%202027%20-%20Pouvoirs%20publics.pdf (01/10/2026), citation seule, en français seulement |
| Séries | `socialProtection` : dépenses de protection sociale de toutes les administrations, Md€, 2024 provisoire, 1 point (693,0) ; `totalSpending` : total des dépenses par fonction, Md€, 2024 provisoire, 1 point (1 671,8) ; `assemblyBudget` : dépenses de l'Assemblée nationale, €, 2025 exécuté (629 260 000) et 2027 prévu (642 950 000, statut `projection`) ; `senateBudget` : dépenses du Sénat, €, 2025 exécuté (358 750 000) et 2027 prévu (383 343 590, statut `projection`) |
| Valeurs par catégorie | `byFunction` : dépenses par fonction (COFOG), Md€, 2024 provisoire, 10 fonctions (protection sociale 693,0 ; santé 261,2 ; services généraux 181,1 ; affaires économiques 166,1 ; enseignement 148,6 ; défense 54,2 ; ordre et sécurité publics 52,1 ; loisirs, culture et culte 43,1 ; logement et équipements collectifs 42,1 ; protection de l'environnement 30,3) ; `functionsFrance` et `functionsEu` : dépenses par fonction en % du PIB, 2024, France (provisoire) et UE à 27, 8 catégories dont « dont vieillesse » ; `deficit`, `debt`, `spending` : déficit, dette et dépenses publics en % du PIB, 2025, France, quelques voisins et UE ; `taxesEu` : impôts et cotisations sociales en % du PIB, 2025 (Eurostat) ; `taxesOecd` : recettes fiscales en % du PIB, 2024 (OCDE), avec la moyenne de l'OCDE |
| Chiffre clé | 693,0 Md€ (écrit 693 Md€) de dépenses de protection sociale en 2024 (provisoire), premier poste, sans tendance saisie ; à côté, l'ensemble des dépenses par fonction, 1 671,8 Md€ |
| Règles | Saisie à la main. Le déficit est écrit en positif, comme dans `publicFinances`. Chaque bloc a sa propre échelle et l'UE (ou la moyenne de l'OCDE) en référence hachurée ; les autres pays ne sont pas classés. Un rang recalculé par la contre-vérification n'est jamais une valeur : il est dit dans la note du bloc, avec « recalculé ». La « zone euro » d'Eurostat (20 pays en 2025) n'est pas saisie. Le poids des assemblées dans la dépense (0,06 %), calculé, n'est qu'une affirmation |
| Première édition | À remplir à la publication |

## « À savoir »

1. Les dépenses par fonction sont celles de 2024, dernière année publiée, en compte provisoire ; celles de 2025 paraîtront en décembre 2026, et le total diffère un peu du compte semi-définitif de `publicFinances`. Source : Insee, page 8574707 et page https://www.insee.fr/fr/statistiques/8988847 (les tableaux 3.301 à 3.307 « seront publiés en décembre 2026 »), d'après la contre-vérification.
2. Le ratio d'Eurostat n'est pas le taux de prélèvements obligatoires de l'Insee ; les chiffres de l'OCDE portent sur 2024, avec une moyenne non pondérée. Source : Eurostat, communiqué du 29/10/2026 et précaution de la recherche vérifiée (« Eurostat compte les cotisations sociales imputées et ne déduit pas les crédits d'impôt ») ; OCDE, API (ligne « OECD_REP »).
3. Les rangs : déficit 4e, dette 3e, impôts et cotisations 1re de l'UE, donnés par Eurostat ; dépenses 2e, recalculé ; OCDE 2e sur 36 pays disponibles, recalculé. Source : communiqué Eurostat du 21/10/2026 (« The highest deficits were recorded in Romania (‑7.8%), Poland (-7.2%), Belgium (-5.2%) and France (‑5.1%) » ; « the highest registered in Greece (145.4%), Italy (136.7%), France (115.7%) ») ; communiqué du 29/10/2026 (« the highest shares of taxes and social contributions as a percentage of GDP recorded in France (46.0%), Belgium (44.7%), Denmark (44.3%) and Austria (43.9%) ») ; classements des dépenses et de l'OCDE refaits par la contre-vérification sur l'API (Finlande 57,5 ; France 57,3 ; Danemark 45,18 ; France 43,46, Japon et Australie absents).
4. Les budgets des assemblées sont votés par chacune ; ceux de 2027 sont prévisionnels ; à l'Assemblée, les charges parlementaires (350,28 M€) comprennent les collaborateurs (203,72 M€). Source : PAP « Pouvoirs publics », p. 17-22.

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/publicSpending.json` (clé `claims`, français et anglais), reprise de la recherche vérifiée du 09/11/2026 sans changer sa formulation. Source de chaque chiffre de la réponse :

1. « On entend que l'IFI, qui a remplacé l'ISF, ne rapporte rien. » 5,07 (2017), 1,85 (2018), 2,71 Md€ (2025), TVA 208,8, CSG 156,6, impôt sur le revenu 103,6 Md€ : Insee, tableau 3.217 (« Impôt sur la fortune (IFI, ex ISF) »), droits constatés de la comptabilité nationale.
2. « On entend que le Parlement coûte une fortune. » 642,95 M€, 53,80 M€ et 383,34 M€ : PAP « Pouvoirs publics », p. 17-22 et 29-30. 988,0 M€ = 629,26 + 358,75 ; 0,06 % calculé sur 1 714,1 Md€ de dépenses publiques en 2025 (Insee, tableau 3.201) : deux comptabilités différentes, le mot « calculé » le dit.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-finances.md` : chaque source rouverte par `curl`, l'API d'Eurostat et celle de l'OCDE interrogées, les classements refaits sur les 27 pays de l'UE.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé et dépenses par fonction | 693,0 ; 261,2 ; 181,1 ; 166,1 ; 148,6 ; 54,2 ; 52,1 ; 43,1 ; 42,1 ; 30,3 ; total 1 671,8 Md€ | cellules 693,029 ; 261,156 ; 181,103 ; 166,073 ; 148,64 ; 54,199 ; 52,113 ; 43,068 ; 42,129 ; 30,285 ; 1 671,794 ; vieillesse 391,954 ; dette 58,87 | https://www.insee.fr/fr/statistiques/fichier/8574707/T_3301.xlsx | Conforme, avec réserve sur la date (voir « Réserves ») |
| Fonctions en % du PIB | France 23,7 ; 13,4 ; 8,9 ; 6,2 ; 5,7 ; 5,1 ; 1,9 ; 1,8 — UE 19,5 ; 10,6 ; 7,3 ; 6,0 ; 5,3 ; 4,7 ; 1,5 ; 1,7 | identique ; valeurs de la France marquées « p » | API `gov_10a_exp` (mise à jour du 21/10/2026) | Conforme |
| Déficit et dette 2025 | France 5,1 et 115,7 ; Allemagne 2,9 et 62,8 ; Italie 3,1 et 136,7 ; Espagne 2,4 et 100,5 ; UE 3,1 et 81,5 | identique ; rangs refaits : déficit 4e, dette 3e | communiqué du 21/10/2026 (URL ci-dessus) | Conforme |
| Dépenses 2025 | France 57,3 ; Finlande 57,5 ; Italie 51,1 ; Allemagne 50,1 ; UE 49,4 | identique ; rang refait : 2e | API `gov_10a_main` et communiqué du 21/10/2026 | Conforme |
| Impôts et cotisations 2025 | France 46,0 ; Belgique 44,7 ; Danemark 44,3 ; Autriche 43,9 ; Allemagne 41,4 ; UE 40,7 | identique ; Allemagne et Belgique provisoires ; rang refait : 1re | communiqué du 29/10/2026 (URL ci-dessus) | Conforme |
| Recettes fiscales OCDE 2024 | France 43,5 ; Danemark 45,2 ; Autriche 43,4 ; Allemagne 38,0 ; Royaume-Uni 34,4 ; États-Unis 25,6 ; moyenne 34,1 | identique (43,462209 ; 45,177061 ; …) ; 36 pays plus la ligne de moyenne | API de l'OCDE (URL ci-dessus) | Écart corrigé : « 2e sur 37 » de la recherche devient « 2e sur 36 pays disponibles » |
| Budgets des assemblées | Assemblée 629,26 (2025) et 642,95 M€ (2027) ; Sénat 358,75 (2025) et 383 343 590 € (2027) | « Le budget de l'Assemblée nationale pour 2027 prévoit un total de dépenses de 642,95 M€ » ; « 629,26 M€ » ; « Le budget du Sénat pour 2027 prévoit un total de dépenses de 383 343 590 » ; « 358,75 M€ » | PAP « Pouvoirs publics » (URL ci-dessus) | Conforme |

**Conclusion.** Aucun chiffre du fichier n'est faux. Les rangs et le poids des assemblées sont recalculés ou calculés, et dits tels.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus ; la page Insee 8574707 (« Paru le 27/03/2026 ») rouverte le 09/11/2026 pour le titre et la date de la source 1 ; les titres français des jeux d'Eurostat lus par son API (`lang=FR`) le même jour.

## Réserves

- Culture, logement et environnement (43,1 ; 42,1 ; 30,3 Md€) et, en % du PIB, services généraux et affaires économiques (6,2 et 6,0 ; 5,7 et 5,3) viennent du tableau de la contre-vérification (lignes 17 et 18 de `verify-finances.md`), pas du résumé du JSON vérifié, qui ne les reprenait pas : mêmes tableaux, cellules retrouvées.
- La contre-vérification n'a pas retrouvé la date du 27/03/2026 du tableau T_3301 ; la page Insee 8574707 la donne, le fichier porte une date de création du 28/11/2025.
- Le total des fonctions en % du PIB d'Eurostat (57,3 % en 2024) diffère du ratio principal de 2024 (57,0 %) : pour la France seule, les montants de l'Insee font référence.
- La page de l'OCDE et la phrase sur le rang de la France n'ont pas pu être ouvertes (403) : valeurs lues par l'API seulement.
- Les budgets des assemblées et la dépense publique relèvent de comptabilités différentes : le 0,06 % est un ordre de grandeur calculé.

## Mises à jour

**09/11/2026** : le bloc « Ce qu'on entend » ne garde que les fausses vérités que les chiffres de la page démentent (décision du PO) : affirmations retirées : « On entend que la France est le pays qui dépense le plus. » ; « On entend que la France est le pays le plus taxé d'Europe, voire du monde. » ; reformulées : « On entend que l'ISF rapportait des milliards et que l'IFI ne rapporte rien. » devient « On entend que l'IFI, qui a remplacé l'ISF, ne rapporte rien. » ; « On entend que le Parlement coûte une fortune et qu'il faut supprimer des députés. » devient « On entend que le Parlement coûte une fortune. ».

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source. Il n'y a pas de script : la contre-vérification a rouvert les documents et interrogé les API.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée pour l'OCDE et le PAP (« citation seule » au registre).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
