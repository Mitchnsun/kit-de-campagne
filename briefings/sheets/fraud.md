# `fraud` · Fraude sociale et fiscale (page composite)

La page « Fraude sociale et fiscale » n'a pas de fichier : ses deux volets ont le leur (`socialFraud` et `taxFraud`, saisis à la main le 2026-11-09, voir `socialFraud.md` et `taxFraud.md`). Cette fiche porte ce qui leur est commun.

**Vérifiée le 09/11/2026** : aucun chiffre faux dans les fichiers (voir les fiches des volets). La licence des sources n'a pas été vérifiée.

## Ce que la page dit, et ne dit pas

- Quatre grandeurs sont à ne pas confondre : la fraude évaluée (une estimation statistique), la fraude détectée, la fraude évitée et la fraude recouvrée (des sommes constatées par les caisses ou l'administration). Seule la première se compare à une ampleur du phénomène, et elle n'existe que pour la fraude sociale.
- Il n'existe aucune estimation officielle de la fraude fiscale totale (Cour des comptes, 16/12/2025). La page ne place donc aucun montant de fraude fiscale à côté des 14 Md€ de fraude sociale évaluée. L'écart de TVA (12,1 Md€ en 2023) mêle fraude, erreurs et faillites ; les droits rappelés (17,4 Md€ en 2024) ne sont pas encaissés (11,4 Md€).
- Les deux volets ne se comparent pas entre eux : la fraude sociale évaluée est un total pour la sécurité sociale (millésimes variables), l'écart de TVA ne couvre qu'un impôt, les sommes du contrôle fiscal sont des résultats d'administration.
- Les montants détectés et recouvrés de la fraude sociale comptent les fautes avec les fraudes.
- Le registre porte la page sans source propre (`sources` vide) ; les sources sont celles des volets, toutes en licence « citation seule ». Le jeu cite des chiffres et ne redistribue aucun fichier.

Liens avec le jeu (registre de l'app) : thème « Économie » ; mesures `fightFraud`, `sickLeaveControl`, `residenceForBenefits`. Les chiffres du kit ne contiennent aucune donnée interne du jeu.

## Double vérification commune

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, en rouvrant chaque URL du rapport de recherche (PDF passés à `pdftotext`) sans passer par un fichier de données. Le détail ligne à ligne est dans les fiches des volets. Ce qui est commun :

- Producteurs : tous officiels (HCFiPS, Cour des comptes, Commission européenne, DGFiP). Aucun chiffre ne vient d'une source de syndicat, de think tank ou de presse ; le chiffre syndical de 80 à 100 Md€ est cité par la Cour des comptes, qui le juge « au minimum une approximation, voire une affirmation gratuite ».
- Bilan : aucun écart numérique, aucun chiffre du fichier non retrouvé. Plusieurs réserves de formulation, reprises dans les notes et les réponses « Ce qu'on entend » : le HCFiPS n'écrit pas « minimum » pour le 14 Md€ ; la Cour n'écrit pas que le 80 à 100 Md€ « mesure en réalité » l'écart fiscal ; les données du 80 à 100 Md€ sont « de 2012 ou de 2013 ».
- Sources de seconde main (officielles, mais pas du producteur du chiffre) : la C2S (Cour des comptes d'après la DSS, volet social). Le détail par organisme de l'évaluation de 2024 (Sénat citant le HCFiPS) n'est pas saisi.
- Sources inaccessibles le 09/11/2026 (403, 503, connexion coupée) : bilan du contrôle fiscal 2025 (economie.gouv.fr), Ameli, DREES, Dares, Urssaf, Légifrance. Aucun chiffre de ces documents n'est dans les fichiers. Chiffres de la liste « à confirmer » du rapport, non confirmés et non utilisés : 17,1 Md€ notifiés et 11,4 Md€ encaissés en 2025, 1 503 M€ de redressements Urssaf en 2025, 3,057 Md€ détectés selon le bilan du gouvernement. Les 11,4 Md€ encaissés en 2024 sont, eux, confirmés par la Cour.
- Plus récent : aucune publication plus récente du même producteur trouvée au 09/11/2026 pour les chiffres du fichier (note du HCFiPS de janvier 2026, rapport de la Cour de mai 2026, rapport de la Cour de décembre 2025, rapport de la Commission de décembre 2025). La loi n° 2026-534 du 25 juin 2026 prévoit selon la recherche une évaluation publique annuelle avant le 30 juin ; non trouvée, à chercher sur senat.fr et Légifrance.
- Comparaisons internes bien signalées : estimé contre détecté contre recouvré ; erreurs contre fraude ; écart de TVA de la Commission contre fourchette de la DGFiP (6 à 10 Md€ en 2019, entreprises déclarantes seulement ; non comparables).

**Conclusion.** Les deux volets sont vérifiés, sans écart numérique ; la page ne doit afficher aucun total de fraude fiscale ni comparer la fraude sociale évaluée aux sommes du contrôle fiscal.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script (voir les fiches des volets).
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais (voir `socialFraud.md` et `taxFraud.md`).
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
