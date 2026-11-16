# `defenceMeans` · Les moyens des armées (page composite)

La page « Les moyens des armées » n'a pas de fichier : ses trois volets ont le leur (`defenceBudget`, `natoShare` et `defenceStaff`, saisis à la main le 2026-11-16, voir `defenceBudget.md`, `natoShare.md` et `defenceStaff.md`), dans l'ordre de leurs onglets : « Budget », « OTAN », « Effectifs ». Ticket #442 de l'app (inventaire des chiffres absents des Dossiers, DE3, décision du PO du 15/11/2026 ; les deux chiffres clés, décision du 16/11/2026). Cette fiche porte ce qui leur est commun.

**Vérifiée le 16/11/2026** : double vérification sur le web par un agent Claude (modèle Sonnet), 15/11/2026, sans écart non expliqué (voir les fiches des volets).

## Ce que la page dit, et ne dit pas

- Trois périmètres, jamais additionnés ni mis côte à côte sans leur nom : la programmation militaire (crédits de paiement de la mission « Défense » hors contributions au compte « Pensions »), le budget voté ou demandé (les mêmes crédits, contributions aux pensions comprises), l'OTAN (ses propres dépenses de défense, pensions versées comprises, gendarmerie en partie, rapportées au PIB en volume aux prix de 2021). Le texte lu d'abord (`readFirst`) du premier onglet les nomme.
- Chiffre clé de la ligne de la page (celui du premier volet, PO, 03/11/2026) : le budget voté pour 2026, **66,5 Md€** de crédits de paiement, pensions comprises (66 475 476 236 €). Pensions comprises, comme `stateBudget` compte chaque mission (73,15 Md€ pour la Défense au projet pour 2027, 62,12 Md€ exécutés en 2025) : la page ne double pas ses chiffres, elle ne reprend que le total de la mission.
- Chiffre clé du volet OTAN : **2,04 % du PIB en 2025, une estimation de l'OTAN** (stable : 2,04 % en 2024) ; 2,22 % en 2026, une estimation aussi, à côté (décision du PO du 16/11/2026, ticket #442).
- Chiffre clé du volet des effectifs : **48 801 réservistes opérationnels fin 2025**, en hausse (43 797 fin 2024).
- Les montants de l'OTAN en euros (67,6 Md€ en 2026, estimation) ne sont pas saisis : ils ne se mettent pas à côté des 57,1 Md€ de la loi.
- Prévisions et estimations marquées : la programmation de 2027 à 2030, le projet de budget pour 2027 et les cibles de réservistes de 2026 à 2029 ont le statut `projection`, dits « prévision » par la page ; les années 2025 et 2026 de l'OTAN ont le statut `provisional`, dites « estimation ».
- Pas de « Ce qu'on entend » : l'affirmation proposée par la recherche (« la France ne consacre même pas 2 % de son PIB à sa défense ») tient sur un périmètre (le budget hors pensions rapporté au PIB) et tombe sur un autre (l'OTAN, 2,04 % en 2024) ; une affirmation que les chiffres ne réfutent que sur un périmètre n'a pas sa place (PO, 09/11/2026). La source de l'affirmation n'a pas été trouvée non plus. « L'armée coûte plus que l'école » est déjà sur `stateBudget`.
- Nom du ministère : chaque document est cité avec ses mots. Le projet annuel de performances écrit surtout « ministère des Armées » (et « ministère des Armées et des Anciens combattants ») ; la loi du 16 août 2026, « ministère de la défense » ; la fiche `ukraineAid` cite le rapport du « Ministère des Armées et des Anciens combattants ». La page dit « le ministère ».
- Licences : la loi, citée (le texte définitif est lu sur le site de l'Assemblée nationale, « citation seule » comme les projets de loi de `stateBudget`) ; le projet annuel de performances, Licence Ouverte 2.0 comme le projet de loi de finances ; l'OTAN, ses conditions « Use of NATO content and brand » (valeur de licence `nato` dans l'app, avec le lien vers ces conditions).

Liens avec le jeu (registre de l'app) : thème « Défense et Europe » ; mesures `reservists`, `voluntaryMilitaryService`, `nationalDefenceLoan`, `europeanDefenceLoan`, `armsExpropriation`, `leaveNato`. Aucune carte du jeu ne porte sur les moyens des armées (le 11-Novembre, `armisticeDay`, est une cérémonie) : au PO de choisir. Les chiffres du kit ne contiennent aucune donnée interne du jeu.

## Double vérification commune

Faite le 15/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, fichiers retéléchargés et relus (openpyxl, `pdftotext`, HTML nettoyé) : la loi (T.A. n° 325 de l'Assemblée nationale), la décision n° 2026-907 DC, l'avis n° HCFP-2026-1, le projet annuel de performances 2027 « Défense », les fichiers de l'OTAN de 2025 et 2026, l'audition du général Crach. Le détail ligne à ligne est dans les fiches des volets. Bilan : aucun écart de valeur ; quatre écarts de lecture, repris dans les fiches : la décision n° 2026-907 DC n'a été saisie que sur les articles 25, 31, 32, 33 et 35 (au fond) et 41 (sa place dans la loi), et ne censure rien ; la note des estimations de l'OTAN est en A75 du « Tableau 3 » (A71 est celle du « Tableau 1 ») ; les conditions de l'OTAN existent (rapport de recherche : « citation seule », faute de les avoir trouvées) ; l'écart de 0,2 Md€ entre la loi (57,1 Md€ hors pensions pour 2026) et la loi de finances pour 2026 (56,90 Md€ hors pensions, calculé) reste sans explication, et une note le dit.

Relue le 16/11/2026 à la construction de la page : la décision n° 2026-907 DC (dispositif « Sont conformes à la Constitution »), les conditions de l'OTAN et ses deux pages « Dépenses de défense et engagement des 5 % » (français et anglais), la première page du communiqué de l'OTAN en français, le statut des pages du projet annuel de performances (p. 10, 23, 92, 106, 236-237).

## Mises à jour

- **16/11/2026** (décision du PO) : le volet `natoShare` reste `planned` jusqu'à la réponse de l'OTAN sur l'usage de son nom dans un jeu (voir `natoShare.md`) : la page a deux onglets, « Budget » et « Effectifs », et le chiffre de sa ligne reste celui du budget. Le texte lu d'abord nomme toujours les trois périmètres, sans renvoyer à un onglet de l'OTAN ; aucune note ne cite plus un chiffre de l'OTAN (`defenceStaff.md`). Le « 80 000 » de 2030 est un nombre de réservistes à recruter, pas un effectif (`defenceStaff.md`).

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans le document saisi (voir les fiches des volets).
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais (voir `defenceBudget.md`, `natoShare.md` et `defenceStaff.md`).
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande (l'OTAN : « clearly credited or sourced to NATO »).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO (dont l'absence de « Ce qu'on entend » et les conditions de l'OTAN, voir `natoShare.md`).
