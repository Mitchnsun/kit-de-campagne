# `businessAid` · Les aides publiques aux entreprises (page composite)

La page « Les aides publiques aux entreprises » n'a pas de fichier : ses quatre volets ont le leur (`aidAmounts`, `aidRecipients`, `aidEurope` et `productionTaxes`, saisis à la main le 2026-11-09, voir `aidAmounts.md`, `aidRecipients.md`, `aidEurope.md` et `productionTaxes.md`), dans l'ordre de leurs onglets : « Combien », « À qui, pour quoi », « En Europe », « Impôts de production ». Cette fiche porte ce qui leur est commun.

**Vérifiée le 09/11/2026** : aucun chiffre faux dans les fichiers (voir les fiches des volets). La licence des sources n'a pas été vérifiée.

## Ce que la page dit, et ne dit pas

- Il n'existe pas un montant des aides aux entreprises, mais des périmètres. Chaque total s'affiche avec son périmètre, son année et son producteur, dans un bloc à lui, et n'est jamais additionné à un autre ni soustrait d'un autre : 59,8 et 166,1 Md€ (Gouvernement, exécution 2024), 108 et 211 Md€ (Sénat, 2023), 82 et 187 Md€ puis 111,9 Md€ (HCSP, 2023), 139,4 à 223,2 Md€ (France Stratégie, 2019).
- Cette précaution est le « À savoir » lu en premier (`readFirst`) du premier onglet, « Combien », celui que la page ouvre : une page composite n'a pas de textes à elle dans l'app, chaque volet a les siens. Il dit aussi que les aides budgétaires du rapport du Gouvernement ne sont pas des crédits de paiement des missions (elles agrègent des dépenses de l'État hors personnel et des charges d'opérateurs : ne pas les rapprocher de la page « Le budget de l'État, mission par mission »), et que les aides d'État de la Commission européenne excluent les mesures générales. Le volet « En Europe » a son propre `readFirst` : ni les aides d'État ni les subventions de la comptabilité nationale ne sont le total des aides. Le volet « À qui, pour quoi » a le sien : aucun document officiel ne répartit l'ensemble des aides par taille.
- Les prêts et garanties ne se comptent pas de la même façon d'un producteur à l'autre (décaissements de l'année pour le Gouvernement, interventions de Bpifrance pour le Sénat, équivalent-subvention pour le HCSP en 2025) : ils ne s'additionnent pas.
- Les répartitions par taille sont celles de deux dispositifs (CIR-recherche, allègements de cotisations), en parts et non en montants.
- Les impôts de production ne sont pas des aides : le dernier volet le dit dans son titre et ses notes. Il sert à situer les mesures du jeu « Un pacte avec les entreprises » (50 Md€ d'impôts de production en moins, et autant d'aides supprimées) et « Baisser les impôts de production ». Les ordres de grandeur de 50 Md€ face aux impôts de production et aux périmètres d'aides sont dans une note, avec le mot « calculé », sans juger la mesure.
- Les chiffres de seconde main ne sont que dans une note qui le dit : les 88 Md€ de l'IGF (2022), lus dans le rapport du Gouvernement. Celui du CPO (plus de 170 Md€ vers 2010, lu chez le HCSP) n'est pas utilisé.
- Les calculs (parts, sommes, rapports à 50 Md€) ne sont jamais dans une série : seulement dans des notes, avec « calculé ».
- La page « Où va l'argent public » affiche aussi 166,1 Md€, pour la fonction « affaires économiques » de l'Insee en 2024 (selon la recherche, chiffre du kit non revérifié ici) : même nombre, rien de commun. La page n'en parle pas ; à garder en tête à la relecture.

Liens avec le jeu (registre de l'app) : thème « Économie » ; mesures `businessPact` et `productionTax`. Aucune mesure ni carte du moteur ne porte sur le crédit d'impôt recherche, les allègements de cotisations ou l'apprentissage : aucun autre lien. Les chiffres du kit ne contiennent aucune donnée interne du jeu.

## Ce qu'on entend

Aucune affirmation (règle du PO du 09/11/2026 : seules les fausses vérités que les chiffres de la page démentent). La contre-vérification n'en a trouvé aucune : chaque affirmation fréquente est confirmée, ou ne se dément que sur un périmètre. Affirmations écartées (`excluded` du rapport final) : « 200 milliards d'aides sans contreparties » (confirmé au sens large du Sénat, 211 Md€, plancher ; démenti sur les autres périmètres) ; « la France aide moins ses entreprises que l'Allemagne » (vrai en euros pour les aides d'État, faux en part du PIB, et faux en euros pour les subventions de la comptabilité nationale) ; « les aides vont aux grandes entreprises » (dépend du dispositif) ; « c'est le premier poste du budget de l'État » (non démontrable avec des chiffres de même nature) ; « les entreprises françaises sont les plus taxées » (hors sujet, confirmé en partie) ; « le CIR est la plus grosse niche fiscale » (non établi pour le PLF 2027).

## Double vérification commune

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après le rapport `verify-aides.md` : chaque source retéléchargée (`curl`), PDF lus avec `pdftotext`, classeurs avec openpyxl, API d'Eurostat rouverte, graphiques lus sur les pages rendues en image. Le détail ligne à ligne est dans les fiches des volets. Ce qui est commun :

- Producteurs : tous officiels (Gouvernement dans ses annexes au projet de loi de finances, direction de la sécurité sociale, Cour des comptes, Sénat, HCSP, France Stratégie, direction générale du Trésor, ministère de la Recherche, DGFiP, Commission européenne, Eurostat). Écartés comme sources de chiffres : l'étude du Clersé commandée par un syndicat, Rexecode, iFRAP, Fipeco, Institut Montaigne, CGT, FO, Attac ; une estimation orale ministérielle sans méthode publiée.
- Bilan : aucun chiffre faux au sens d'un écart de valeur. Trois erreurs de méthode du rapport de recherche corrigées : la comparaison des aides budgétaires du rapport du Gouvernement à la mission Enseignement scolaire (« même nature » : faux), l'explication du CICE dans la série D3 (non établie par la source, retirée), les « montants nominaux » de Bpifrance chez le Sénat (non écrits par le rapport).
- Dates corrigées : Scoreboard publié le 15/01/2026 (PDF du 12/01) ; rapport du HCSP « juillet 2026 » ; rapport du Gouvernement sans date de dépôt ni numéro dans son texte.
- Sources à ouvrir par le PO (non ouvertes, aucun de leurs chiffres n'est dans les fichiers, sauf le total de l'IGF lu dans le rapport du Gouvernement) : tome II des voies et moyens du PLF 2027, rapport de l'IGF n° 2023-M-105-03, rapport du CPO d'octobre 2010, bilan d'activité 2023 de Bpifrance, outil de données du Scoreboard, numéro et date de dépôt du rapport du Gouvernement.

**Conclusion.** Les quatre volets sont vérifiés, sans écart numérique ; la page ne doit afficher aucun total qui additionne deux périmètres, ni comparer les aides budgétaires du rapport du Gouvernement aux crédits des missions.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script (voir les fiches des volets).
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais (voir les fiches des volets).
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
