# `contributorsPerRetiree` · Cotisants et retraités (partie de la page « Retraites », saisie à la main)

**Vérifiée le 02/11/2026** : les valeurs saisies concordent avec les courbes du rapport de juin 2026 et de son diaporama (lecture des coordonnées des figures), et avec le texte arrondi (2,1 ; 1,8 ; 1,3). Corrigé : ce que compte le rapport (l'emploi total de la comptabilité nationale pour un retraité de droit direct, en France ou à l'étranger), 2025 marqué estimé (`provisional`) et non projeté, comme dans le rapport ; notes précisées.

**À décider (PO)** : le COR permet de reproduire les notes de son secrétariat général en citant la source ; « la reproduction des autres documents est soumise à l'accord de leur auteur ou éditeur ». Le kit cite des chiffres, jamais ses fichiers ni ses figures. La vérification conseille de demander l'accord du COR (info@cor-retraites.fr) avant de redistribuer cette série, comme pour le Citepa et le CEVIPOF.

| Champ | Valeur |
| --- | --- |
| Indicateur | `contributorsPerRetiree`, partie de la page composite `pensions` (avec `retirees`, DREES, à venir), dossier « Travail et retraites », ticket #28 (statut `planned`) |
| Données | `briefings/manual/contributorsPerRetiree.json`, saisi le 2026-11-02 depuis « Données juin 2026 – partie 2 » du COR, onglet « Fig 2.3 », ligne « 2.2b Rapport entre le nombre de cotisants et le nombre de retraités » (PO, 02/11/2026 : projections du COR saisies à la main), arrondi à deux décimales |
| Source | COR, rapport annuel de juin 2026, « Évolutions et perspectives des retraites en France », publié le 11/06/2026, figure 2.3 ; chiffres cités ; en français seulement (pas de version anglaise du rapport ni de sa synthèse) |
| Série | `contributorsPerRetiree` : cotisants par retraité de droit direct, observé de 2002 à 2024, 2025 estimé, projeté de 2026 à 2070 dans le scénario de référence (statut `projection`) |
| Chiffre clé | 1,77 cotisant par retraité en 2024, en baisse (2,14 en 2002 ; quasi stable depuis 2012, entre 1,72 et 1,78) |
| Première édition | À remplir à la publication |

À actualiser : à chaque rapport annuel du COR (juin) ; toute la série projetée change avec les hypothèses.

Attention : 2024 (1,7743) et 2025 (1,7706) sont proches d'une limite d'arrondi ; les valeurs viennent du fichier du COR, pas d'une lecture de graphique.

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans ouvrir le fichier de données du COR. Son rapport, tel quel :

Date de la vérification : 2 novembre 2026. Vérification faite sur le web uniquement. Le fichier « Données_RA2026_P2.xlsx » n'a pas été ouvert (consigne), ni aucun autre fichier xlsx du COR. Rien n'a été lu ni modifié sous `/home/user`.

### 0. Méthode, niveaux de preuve et limites


Chaque valeur du rapport est classée selon sa provenance :

- **[T] Texte primaire** : phrase ou étiquette de figure publiée dans un document du COR, téléchargé brut et lu par moi.
- **[G] Lecture graphique** : le texte du rapport ne donne que « 2,1 », « 1,8 », « 1,3 » (une décimale). Pour obtenir les valeurs à deux décimales, j'ai lu les **coordonnées vectorielles de la courbe** dans les PDF du COR (figure 2.3 du rapport, graphique du diaporama, figure 2.4b du rapport de juin 2025), en calibrant les axes sur les graduations tracées dans le même PDF. Ce n'est **pas une valeur publiée en clair** : c'est un calcul de ma part, précis à environ ± 0,003 (vérifié sur les points étiquetés : 2,1 en 2002, 1,3 en 2070). Il confirme les arrondis, il ne remplace pas la lecture du fichier de données.
- **[S] Secondaire** : presse, think tank, administration non éditrice des chiffres (IFRAP, Reuters, Trésor, Cercle de l'Épargne, Statista).
- **[R] Résumé de moteur de recherche** : repris d'un résumé fourni par l'outil de recherche, non relu à la source. Quand je le cite, je le dis.

Les outils de lecture web (WebFetch) renvoient un résumé produit par un petit modèle. Pour tout ce qui compte, j'ai donc **retéléchargé la page ou le PDF brut** et relu le texte moi-même (pages COR, informations éditeur, Insee, IFRAP, Trésor). Seuls Reuters/GV Wire et Statista ne reposent que sur un résumé d'outil de lecture.

---

### 1. Les valeurs saisies

Légende des sources : voir la section 9 pour les URL complètes (numérotées [U1], [U2]…).

| Élément | Valeur saisie | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Observé, 2002 | 2,14 | [T] texte : « passant de 2,1 à 1,8 en 2025 » ; étiquette « 2,1 » sur la figure 2.3. [G] 2,139 (rapport 2026), 2,139 (diaporama), 2,138 (rapport 2025) | [U3] p. 72-73 (fichier `RA_Part2_Chap1.pdf`), [U5] diap. 20, [U7] fig. 2.4b | **Conforme** (le texte ne donne que 2,1 ; 2,14 vient de la lecture graphique) |
| Observé, 2003 | 2,10 | [T] aucune mention dans le texte. [G] 2,099 (rapport 2026), 2,099 (diaporama), 2,098 (rapport 2025) | [U3] fig. 2.3, [U5] diap. 20, [U7] fig. 2.4b | **Conforme** (lecture graphique seule) |
| Observé, 2023 | 1,78 | [T] rapport de juin 2025 : « 1,8 cotisant par retraité de droit direct en 2023 », avec 30,4 millions de cotisants et 17,1 millions de retraités (30,4 / 17,1 = 1,778). [G] 1,7785 (rapport 2026), 1,7788 (diaporama), 1,7788 (rapport 2025) | [U7] p. 61 et 63 ; [U3] fig. 2.3 ; [U5] diap. 20 | **Conforme** (la valeur de 2023 n'a pas bougé entre les deux rapports) |
| Observé, 2024 | 1,77 | [T] pas citée dans le texte (le texte donne 2025). [G] 1,7745 (rapport 2026), 1,7744 (diaporama). La courbe grise « Obs » du rapport s'arrête en 2024 | [U3] fig. 2.3, [U5] diap. 20 | **Conforme**, avec une réserve : 1,7745 est à 0,0005 de la frontière 1,775 entre 1,77 et 1,78, et ma lecture est précise à ± 0,003. Je ne peux pas départager 1,77 et 1,78 sans le fichier |
| Chiffre clé : 1,77 cotisant par retraité en 2024, « en baisse » | 1,77, en baisse | [G] baisse nette de 2,14 (2002) à 1,73 vers 2014-2016, puis stabilité entre 1,72 et 1,78 jusqu'en 2024 ; de 2023 à 2024 : 1,7785 → 1,7745 (– 0,004). [T] « s'est dégradé depuis 2002, passant de 2,1 à 1,8 en 2025 » | [U3] p. 72 | **Écart expliqué** : « en baisse » est vrai depuis 2002 et la projection baisse ensuite, mais la série est quasi stable depuis une douzaine d'années. À formuler avec la période (« depuis 2002 ») |
| Projeté, 2025 | 1,77 | [T] « 1,8 en 2025 » (une décimale) ; étiquette « 1,8 » sur la courbe rouge. Recalcul sur les chiffres arrondis du texte : 30,6 M / 17,4 M = 1,759 (fourchette d'arrondi 1,751 à 1,767). [G] 1,7706 (rapport), 1,7699 (diaporama) | [U3] p. 72-73 ; [U5] diap. 20 | **Conforme**, mais en limite haute : 1,77 dépasse de peu la fourchette de recalcul (1,767), ce qui reste dans la marge de ma lecture graphique. À confirmer par le fichier |
| Projeté, 2026 | 1,76 | [G] 1,7588 (rapport), 1,7598 (diaporama). Aucune mention dans le texte | [U3] fig. 2.3, [U5] diap. 20 | **Conforme** (lecture graphique seule) |
| Projeté, 2070 | 1,30 | [T] « ce ratio s'établirait à 1,3 cotisant par retraités dans le scénario de référence » ; étiquette « 1,3 ». Recalcul : 28,9 M / 22,1 M = 1,308 (fourchette 1,302 à 1,314). [G] 1,3039 (rapport), 1,3047 (diaporama) | [U3] p. 72-73 ; [U5] diap. 20 | **Conforme** |
| Statut « projection » pour chaque année projetée | projection | [T] note 62 : « Les derniers chiffres disponibles sont ceux de 2024. Les chiffres 2025 sont estimés. » [G] dans la figure du rapport, la courbe observée couvre 2002-2024 et la courbe « Sc. Ref » commence en 2024 (point de raccord) ; **dans le diaporama du 11 juin, la courbe observée va jusqu'en 2025** et la rouge commence en 2025 | [U3] p. 72 note 62 ; [U5] diap. 20 | **Écart expliqué** : le rapport (PDF du 30 juin 2026, identique dans le PDF complet de juillet) traite 2025 comme estimé, le diaporama du 11 juin comme observé. Le statut « projection » de 2025 suit le rapport ; l'étiquette « estimation » serait plus exacte |
| Publication | jeudi 11 juin 2026 | [T] « Le Conseil d'orientation des retraites a publié le jeudi 11 juin son treizième rapport annuel » ; diaporama daté « 11/06/2026 » ; le 11 juin 2026 est bien un jeudi. [S] Reuters (via GV Wire) daté du 11 juin 2026 | [U1], [U5], [U13] | **Conforme**. Précision : les PDF en ligne ont été remis en ligne après le 11 juin (chapitre 2-1 : 30 juin 2026 ; PDF complet dans le dossier `2026-07`) ; le texte lu est identique |
| Libellé d'axe du fichier : « Cotisants / retraités de droit direct » | cette formule | [T] titre de la figure 2.3 : « Rapport entre le nombre de cotisants et le nombre de retraités » ; le texte parle de « retraités de droit direct » ; juin 2025 : « 1,8 cotisant par retraité de droit direct » | [U3] p. 73 ; [U7] p. 61 | **Non trouvé** (littéral, le fichier n'a pas été ouvert) ; cohérent avec le texte |
| Onglet « Fig 2.3 », ligne « 2.2b » | Fig 2.3 / 2.2b | [T] la figure 2.3 du rapport 2026 est bien « Les déterminants de l'évolution de la masse des pensions » (panneau de droite : le ratio). Dans le rapport 2025 la même figure était la 2.4 | [U3] ; [U7] fig. 2.4 | **Conforme** pour le numéro de figure ; **non trouvé** pour la ligne « 2.2b » |

#### Lecture graphique détaillée (pour mémoire)

| Année | Rapport 2026 (PDF du 30/06) | Diaporama (11/06) | Rapport 2025 (fig. 2.4b) | Saisie |
|---|---|---|---|---|
| 2002 | 2,139 | 2,139 | 2,138 | 2,14 |
| 2003 | 2,099 | 2,099 | 2,098 | 2,10 |
| 2023 | 1,7785 | 1,7788 | 1,7788 | 1,78 |
| 2024 | 1,7745 | 1,7744 | (projeté 1,7788) | 1,77 |
| 2025 | 1,7706 | 1,7699 | (projeté 1,7621) | 1,77 |
| 2026 | 1,7588 | 1,7598 | non lu | 1,76 |
| 2070 | 1,3039 | 1,3047 | 1,4107 | 1,30 |

Le rapport 2025 projetait 1,4 en 2070 (texte : « environ 1,4 à l'horizon de la projection »), le rapport 2026 projette 1,3 : la projection a donc été révisée.

---

### 2. Point 1 : ce que compte le rapport au numérateur et au dénominateur

Citations du rapport, partie 2, chapitre 1, p. 72-73 [U3] :

- Texte : « Le rapport démographique entre les cotisants et les retraités s'est dégradé depuis 2002, passant de 2,1 à 1,8 en 2025 [note 62], en particulier sous l'effet du vieillissement des générations du baby-boom. […] À l'horizon 2070, ce ratio s'établirait à 1,3 cotisant par retraités dans le scénario de référence. »
- « Le nombre de cotisants, évalué à 30,6 millions [note 63] en 2025, continuerait d'augmenter jusqu'à la fin des années 2030 et diminuerait ensuite à partir de 2040 pour s'établir à 28,9 millions en 2070. Le nombre de retraités de droit direct [note 64] progresserait quant à lui sur toute la période de projection. Il passerait ainsi de 17,4 millions en 2025 à 22,1 millions en 2070. »
- **Note 63 (numérateur)** : « L'indicateur retenu ici est l'emploi total issu des données de la comptabilité nationale de l'Insee. »
- **Note 64 (dénominateur)** : « Le nombre de retraités est estimé à partir des données des modèles Ancêtre et Trajectoire de la Drees. Il s'agit du champ des retraités vivant en France et à l'étranger. »
- **Note 62** : « Le nombre de retraités et la pension moyenne sont ceux du modèle Ancêtre de la Drees. Les derniers chiffres disponibles sont ceux de 2024. Les chiffres 2025 sont estimés. »
- Sources de la figure 2.3 : « projections COR - juin 2026, comptes nationaux de l'Insee base 2020, rapports à la CCSS 2002-2025, Dares (activité partielle) et Drees, modèle Ancètre 2024 ».

Ce que cela donne :

- **Numérateur** : le COR appelle « cotisants » l'**emploi total** de la comptabilité nationale de l'Insee (30,6 millions en 2025). Le rapport ne dit pas « cotisants de l'ensemble des régimes » pour cet indicateur. L'emploi total couvre tout le monde, quel que soit le régime, mais ce n'est pas un décompte de cotisants par régime.
- **Dénominateur** : les **retraités de droit direct, vivant en France et à l'étranger** (note 64). Pour la décomposition des dépenses (figure 2.2), le champ est précisé ainsi : « ensemble des régimes de retraite français légalement obligatoires, y compris FSV, hors RAFP. Retraités ayant au moins un droit direct de retraite » ([U3] p. 71) : un polypensionné compte une fois. Je n'ai pas trouvé cette précision écrite spécifiquement sous la figure 2.3 ; je la rapporte comme le champ du même chapitre.
- **Piège de lecture** : sous la figure 2.3, « Champ : pour la pension moyenne, personnes retraitées de droit direct (…) résidant en France ». Cela concerne le panneau de gauche (pension moyenne), pas le ratio. Le ratio, lui, compte les retraités « en France et à l'étranger ».
- **Autre mesure à ne pas mélanger** : la synthèse (p. 11) et le diaporama (diap. 34) citent, d'après l'IPP, « 1,29 cotisant par retraité » pour le régime de la fonction publique de l'État, « 2,25 pour le régime général » et « **2,05 pour l'ensemble des régimes** » en 2020. Ce 2,05 est un calcul par régimes (IPP), distinct de la série du COR, qui vaut environ 1,72 en 2020 selon ma lecture de la figure ([G] 1,7157). Si on écrit « cotisants de l'ensemble des régimes », on invite à rapprocher 1,77 de 2,05.
- La figure 2.7 du rapport donne le ratio **par régime** (« retraités vivant en France ou à l'étranger percevant au moins une pension de ces régimes ») : autre mesure, hors sujet pour la saisie.

Le même libellé existe dans le rapport de juin 2025 (note 46 : « L'indicateur retenu ici est l'emploi total issu des données de la comptabilité nationale de l'Insee » ; 30,4 millions de cotisants et 17,1 millions de retraités de droit direct en 2023) [U7] p. 61-63. La définition est donc stable d'un rapport à l'autre.

Secondaire [S] : le communiqué du Cercle de l'Épargne du 5 juin 2026 (avant le rapport) évoque « 17,2 millions de retraités de droit direct fin 2023 », ce qui concorde avec les 17,1 millions du rapport 2025 [U15].

Remarque de nom de document : le PDF complet du rapport ([U2], dossier `2026-07`) porte « Partie 2 – Chapitre 2 » en pied de page des mêmes pages que le fichier de chapitre (« Partie 2 – Chapitre 1 »). Le texte est identique ; j'ai cité le fichier de chapitre.

---

### 3. Point 2 : hypothèses du scénario de référence de juin 2026

| Hypothèse | Valeur saisie | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Fécondité | 1,45 enfant par femme à partir de 2028 | [T] « Scénario de référence : hypothèses démographiques centrales de l'Insee (poursuite des gains d'espérance de vie, fécondité de 1,45 enfant par femme à partir de 2028 et solde migratoire net de 150 000 personnes par an), croissance annuelle de la productivité horaire du travail de 0,7 % et taux de chômage de 7,0 % (à partir de 2040). » Synthèse : « un taux de fécondité de 1,45 enfant par femme à partir de 2028 […] contre 1,8 auparavant ». Insee : « l'ICF poursuivrait sa baisse jusqu'à 1,45 enfant par femme en 2028 (il était de 1,56 en 2025), puis se stabiliserait » | [U3] sous la fig. 2.3 ; [U6] synthèse p. 1 ; [U8] p. 33 (§1.1, « convergence à horizon 2028 pour le central ») ; [U10] Insee Résultats du 08/06/2026 | **Conforme** |
| Solde migratoire | + 150 000 personnes par an | [T] synthèse : « un solde migratoire annuel de +150 000 personnes dès 2026 » ; Insee : « le solde migratoire est supposé constant à partir de 2026, à +150 000 personnes par an » (fourchette ± 80 000). Le rapport 2025 retenait + 70 000 | [U6] p. 1 ; [U8] p. 34 (§1.2) ; [U10] | **Conforme** (le « dès 2026 » est utile à ajouter) |
| Productivité horaire | + 0,7 % par an | [T] « L'hypothèse de croissance de la productivité horaire du travail retenue dans le scénario de référence s'établit à 0,7 % par an **à compter de 2040**, conformément à l'exercice précédent » ; entre 2030 et 2040 : convergence graduelle depuis les hypothèses à court terme du gouvernement (la productivité horaire a progressé de 1,5 % en 2025). Variantes : 0,4 % et 1,0 % | [U8] p. 46 (productivité) et p. 42 (convergence 2030-2040) | **Conforme**, avec nuance : c'est une hypothèse de long terme, atteinte en 2040 |
| Chômage | 7 % à partir de 2040 | [T] « Le COR a décidé de conserver une cible de taux de chômage de 7 % à partir de 2040 pour le scénario de référence » ; observé 7,7 % en 2025, 8,1 % au premier trimestre 2026. Variantes : 5 % et 10 % | [U8] p. 48 | **Conforme** |
| Espérance de vie (non saisie, pour mémoire) | – | [T] « gains d'espérance de vie légèrement revus à la baisse » ; Insee : espérance de vie à la naissance en 2070 de 89,5 ans (femmes) et 86,7 ans (hommes) | [U6] ; [U10] | Information complémentaire |

Date des hypothèses : la synthèse parle d'un jeu d'hypothèses de l'Insee « publié en avril 2026 » ; la publication Insee Résultats portant les projections de population 2026 est datée du 8 juin 2026 [U10]. Les deux dates sont exactes, pour deux publications différentes.

---

### 4. Point 3 : « rapport démographique » de la population et rapport cotisants / retraités

Le COR publie **les deux**, dans le même rapport :

- **Rapport démographique de la population** : 20-64 ans rapportés aux 65 ans et plus. Partie 1, chapitre 1, §1.5, p. 37-38 [U4], figure 1.5 : « La baisse du rapport démographique des 20-64 ans sur les 65 ans et plus s'est accélérée à partir de 2009 – année où il est compté 3,6 personnes de 20 à 64 ans par personne de 65 ans et plus (2,5 en 2025 selon les données provisoires) […] en 2070, il y aurait environ 1,62 personne de 20-64 ans par personne de 65 ans et plus dans le scénario de référence. Ce ratio était de 1,76 dans le cadre des précédentes projections démographiques. » Le diaporama (diap. 9) donne 2,53 pour le point récent ; la synthèse (p. 5) répète 3,6 → 2,5 → 1,62 [U5], [U6].
- **Rapport cotisants / retraités** : partie 2, chapitre 1 (valeurs de la saisie).
- **Comment le COR les distingue** : note 35 de la partie 1 [U4] : « Ce rapport diffère du rapport entre le nombre de cotisants et le nombre de retraités dans la mesure où il faut prendre également en compte les taux d'activité aux différents âges. Les cotisants ne correspondent ainsi pas exactement aux effectifs âgés de 20 à 64 ans et les retraités à ceux âgés de 65 ans et plus. » La phrase d'introduction du §1.5 dit que le premier détermine « en grande partie » les évolutions du second.

**Piège de vocabulaire** : le COR emploie lui-même « rapport démographique » pour les deux. La partie 2 écrit « Le rapport démographique entre les cotisants et les retraités s'est dégradé depuis 2002, passant de 2,1 à 1,8 en 2025 » [U3] p. 72. La note prévue (« le rapport démographique de la population ») reste juste, mais il vaut mieux nommer les tranches d'âge, comme elle le fait déjà.

**La confusion existe dans la pratique** : la note Trésor-Éco n° 406 du 8 octobre 2026 écrit, à propos des cotisants et des retraités : « Alors qu'on comptait plus de quatre cotisants pour un retraité en 1990, ce ratio n'est plus que d'environ 2,5 en 2025 et atteindrait 1,6 en 2070 » [U11] [S, page HTML brute]. Ces deux valeurs (2,5 et 1,6) correspondent au rapport 20-64 ans / 65 ans et plus du COR (2,53 et 1,62), pas au rapport cotisants / retraités (1,8 et 1,3). Autre source secondaire : le Cercle de l'Épargne (5 juin 2026) écrit « environ 1,7 aujourd'hui ; entre 1,3 et 1,4 à l'horizon 2070 » [U15], sur des chiffres antérieurs au rapport 2026.

---

### 5. Notes « À savoir » : verdict et rédaction proposée

Les longueurs sont comptées avec des espaces ordinaires ; à adapter à la typographie du projet (espaces insécables avant « % » et « : »).

#### Note 1 (définition) : à corriger

Texte prévu : « Le rapport compte les cotisants de l'ensemble des régimes de retraite pour un retraité de droit direct. »

Verdict : **Écart.**

- Le rapport ne dit pas « cotisants de l'ensemble des régimes » : il retient « l'emploi total issu des données de la comptabilité nationale de l'Insee » (note 63, [U3]).
- « Un retraité de droit direct » est exact, mais le champ est précisé : retraités vivant en France **et à l'étranger** (note 64).
- La même publication cite ailleurs « 2,05 pour l'ensemble des régimes » (2020, IPP) : un lecteur pourrait rapprocher ce 2,05 de la note.

Rédaction proposée (218 caractères) :

> Le COR rapporte l'emploi total de la comptabilité nationale (30,6 millions en 2025), qui lui sert de nombre de cotisants, au nombre de retraités de droit direct vivant en France ou à l'étranger (17,4 millions en 2025).

#### Note 2 (hypothèses) : confirmée, avec deux précisions

Texte prévu : « À partir de 2025, ce sont des projections du scénario de référence du COR (fécondité de 1,45 enfant par femme à partir de 2028, solde migratoire de +150 000 personnes par an, productivité horaire +0,7 % par an, chômage de 7 % à partir de 2040) : elles changent à chaque rapport. »

Verdict : **Conforme**, avec nuances.

- Les quatre hypothèses sont exactes (section 3).
- 2025 est une **estimation** (note 62) et non une projection pure ; le diaporama du 11 juin la traite même comme observée.
- La productivité à + 0,7 % est atteinte « à compter de 2040 » (convergence entre 2030 et 2040).
- « Elles changent à chaque rapport » est exact : le rapport de juin 2025 retenait une fécondité de 1,8 et un solde de + 70 000, et projetait environ 1,4 en 2070.

Rédaction proposée (249 caractères) :

> Dès 2025 (année estimée), ce sont des projections du scénario de référence du COR de juin 2026 : fécondité de 1,45 enfant par femme dès 2028, solde migratoire de +150 000 personnes par an, productivité horaire +0,7 % par an, chômage de 7 % dès 2040.

Variante, si l'on veut garder « à long terme » pour la productivité (262 caractères) : remplacer « productivité horaire +0,7 % par an » par « productivité horaire +0,7 % par an à long terme ».

#### Note 3 (autre rapport) : confirmée, avec une précision de vocabulaire

Texte prévu : « Ce n'est pas le rapport démographique de la population (les 20-64 ans rapportés aux 65 ans et plus), que le COR publie aussi. »

Verdict : **Conforme.** Le COR publie bien les deux (section 4). Les ordres de grandeur (2,5 en 2025, 1,62 en 2070) aident à ne pas les confondre, et le COR emploie « rapport démographique » pour les deux : il faut garder la mention des tranches d'âge.

Rédaction proposée (209 caractères) :

> Ce n'est pas le rapport démographique de la population, qui rapporte les 20-64 ans aux 65 ans et plus (environ 2,5 en 2025, 1,62 en 2070). Le COR publie les deux ; le second ignore les taux d'activité par âge.

#### Note 4 (facultative) : les projections bougent

Pas dans la liste initiale ; utile pour illustrer « elles changent à chaque rapport ». Sources : [U7] p. 61 (« environ 1,4 à l'horizon de la projection ») et [U3] p. 72 (« 1,3 »), hypothèses de juin 2025 dans [U6] p. 1 (fécondité de 1,8, solde de + 70 000).

Rédaction proposée (193 caractères) :

> Ces projections changent à chaque rapport : celui de juin 2025 (fécondité de 1,8, solde migratoire de +70 000 par an) donnait environ 1,4 cotisant par retraité en 2070, contre 1,3 en juin 2026.

---

### 6. Réutilisation et version anglaise

#### Conditions de réutilisation (page « Informations éditeur », relue en HTML brut le 2 novembre 2026) [U12]

Textes de la page, mot pour mot :

- « Les notes préparées par le secrétariat général du COR dans le cadre des séances plénières sont rendues publiques mais n'engagent pas le Conseil. Elles peuvent être reproduites en mentionnant la source : "Document de travail préparé par le secrétariat général du COR". »
- « La reproduction des autres documents est soumise à l'accord de leur auteur ou éditeur. »
- Éditeur : Secrétariat général du Conseil d'orientation des retraites, 20 avenue de Ségur, TSA 30728, 75334 Paris cedex 07 ; info@cor-retraites.fr ; directeur de la publication : M. Gilbert Cette ; codirecteur : M. Emmanuel Bretin.

Ce que la page **ne dit pas** :

- Elle ne parle ni des rapports annuels, ni des fichiers de données, ni du diaporama.
- Elle ne cite aucune licence (ni « Licence ouverte » / Etalab, ni Creative Commons).
- La page est aussi celle du lien « Mentions légales » du pied de page.

Lecture (c'est mon interprétation, pas un avis juridique) :

- Le rapport annuel n'est pas une « note préparée par le secrétariat général dans le cadre des séances plénières » au sens strict. La page de la publication attribue pourtant le rapport, le diaporama et les fichiers de données au « Secrétariat général du COR » [U1], ce qui laisse une ambiguïté.
- Lecture prudente : la reproduction d'un document entier (PDF, figure, fichier xlsx) demande l'accord du COR ; citer des chiffres en indiquant la source n'est pas visé par ces deux phrases.
- À faire confirmer par écrit à info@cor-retraites.fr si le jeu doit reproduire des figures ou des tableaux, ou redistribuer les fichiers.
- Aucune mention « Licence ouverte » trouvée sur la page « Informations éditeur », sur la page du rapport ni dans les PDF lus (recherche des mots « licence », « reproduction », « Etalab »). Une recherche web ne montre aucun jeu de données du COR sur data.gouv.fr ([R], résumé de moteur de recherche, non vérifié sur le catalogue). Le fait que l'État publie souvent ses données sous Licence ouverte ne s'applique donc pas automatiquement ici : aucune source consultée ne dit que le COR l'applique.
- Je n'ai pas vérifié sur Légifrance le régime général de réutilisation des informations publiques (CRPA). Je ne tire donc aucune conclusion de ce côté.

#### Version anglaise

- Le site du COR a une page en anglais, « Pensions Advisory Council » (`/pensions-advisory-council`), lue en HTML brut le 2 novembre 2026 [U14]. Elle liste des **résumés de séances plénières en anglais** (« Brief of plenary session… », de janvier 2018 à décembre 2025) et un seul résumé de rapport annuel : « **Summary - COR Annual report June 2021** ».
- Les pages des rapports annuels de **juin 2026, juin 2025, juin 2024 et juin 2023** ne proposent aucun document en anglais (recherche des mots « anglais / English » et des PDF « version anglaise » dans le HTML brut) ; seule la page de juin 2021 en a un (`Synthèse_version_anglaise.pdf`).
- Conclusion : **pas de version anglaise officielle trouvée** du rapport de juin 2026 ni de sa synthèse, au 2 novembre 2026. Pour une version anglaise du jeu, il faudra traduire soi-même les notes et indiquer que c'est une traduction.
- Couverture en anglais, secondaire [S] : Reuters, 11 juin 2026 (via GV Wire), mentionne la fécondité « 1.45 children per woman […] from 1.8 previously » ; ne mentionne pas le ratio cotisants / retraités ([U13], résumé d'outil de lecture seulement).

---

### 7. Autres constats

- **La synthèse du rapport (PDF) ne donne pas la série cotisants / retraités** (2,1 → 1,8 → 1,3). Elle ne cite que le rapport démographique 20-64 / 65+ (3,6 → 2,5 → 1,62) et les chiffres IPP de 2020 (1,29 / 2,25 / 2,05). Les valeurs de la saisie viennent donc du chapitre 1 de la partie 2, de la figure 2.3 et du diaporama (diap. 20). Il y a deux versions de la synthèse sur le site (12 juin et 30 juin 2026), avec le même texte sur ces points.
- **IFRAP** (secondaire, article du 16 juin 2026, page HTML brute) recopie mot pour mot la phrase du rapport : « le rapport démographique entre les cotisants et les retraités s'est dégradé depuis 2002, passant de 2,1 à 1,8 en 2025 » ; ce qui confirme que ce texte est celui du rapport 2026 [U9].
- **Statista** [S] a une page « Ratio between the number of employed people contributing to the pension system and the number of retirees » (2002-2070), mais datée du 22 janvier 2026 (donc antérieure au rapport) et valeurs masquées : sans intérêt pour la vérification [U16] (résumé d'outil de lecture seulement).

---

### 8. Conclusion

**Écarts et réserves d'abord :**

1. **Note 1 à corriger.** Le rapport compte l'**emploi total de la comptabilité nationale** (30,6 millions en 2025) au numérateur, pas des « cotisants de l'ensemble des régimes ». Au dénominateur : les retraités de droit direct, **en France et à l'étranger** (17,4 millions en 2025). Le même rapport cite aussi un « 2,05 pour l'ensemble des régimes » (IPP, 2020), qui est une autre mesure.
2. **Statut de 2025 ambigu.** Le rapport (note 62) traite 2025 comme une année **estimée** ; le diaporama du 11 juin trace encore la courbe « observée » jusqu'en 2025. Le statut « projection » suit le rapport ; « estimation » serait plus exact.
3. **« En baisse » à situer.** Vrai depuis 2002 (2,14 → 1,77), mais la série est quasi stable depuis une douzaine d'années (1,72 à 1,78) ; de 2023 à 2024, la baisse est de l'ordre de 0,004.
4. **Valeurs à deux décimales non publiées en clair.** Le texte du rapport ne donne que 2,1, 1,8 et 1,3. Mes valeurs à deux décimales viennent d'une lecture des coordonnées des courbes (précision ± 0,003) : elles concordent avec la saisie sur les sept années, mais **2024 (1,7745) et 2025 (1,7706) sont à la frontière d'arrondi** et ne peuvent être tranchées sans le fichier. Pour 2025, le recalcul à partir des chiffres arrondis du texte (30,6 / 17,4) donne 1,76, à la limite de la fourchette d'arrondi.
5. **Non vérifiable sans ouvrir le fichier** : le libellé d'axe exact (« Cotisants / retraités de droit direct ») et la ligne « 2.2b ». Seul le numéro de figure (2.3) est confirmé.
6. **Réutilisation** : la page « Informations éditeur » n'autorise explicitement que la reproduction des « notes préparées par le secrétariat général… dans le cadre des séances plénières » (avec la mention « Document de travail préparé par le secrétariat général du COR »). Pour les autres documents : « soumise à l'accord de leur auteur ou éditeur ». Aucune licence ouverte n'est annoncée ; rapports annuels et données ne sont pas nommés.
7. **Pas de version anglaise** du rapport de juin 2026 ni de sa synthèse (dernier résumé de rapport annuel en anglais : juin 2021).
8. **Confusion fréquente avec le rapport démographique 20-64 / 65+**, y compris dans une publication du Trésor du 8 octobre 2026 (2,5 en 2025 ; 1,6 en 2070). Le COR emploie lui-même « rapport démographique » pour les deux.

**Confirmé :**

- Les sept valeurs saisies (2002, 2003, 2023, 2024, 2025, 2026, 2070) concordent avec les courbes du rapport 2026, du diaporama du 11 juin et du rapport 2025 (pour 2002, 2003, 2023), et avec le texte arrondi (2,1 ; 1,8 ; 1,3).
- Hypothèses du scénario de référence (fécondité 1,45 dès 2028, solde migratoire + 150 000 par an dès 2026, productivité horaire + 0,7 % par an à compter de 2040, chômage 7 % à partir de 2040) : confirmées par le rapport, la synthèse et l'Insee.
- Publication le jeudi 11 juin 2026 (treizième rapport annuel) : confirmée.
- Le COR publie bien le rapport démographique 20-64 / 65+ (3,6 en 2009, 2,5 en 2025, 1,62 en 2070) et explique en note 35 la différence avec le rapport cotisants / retraités.

---

### 9. URL consultées

Téléchargées brutes et lues (primaires, sauf mention) :

- [U1] Page du rapport annuel de juin 2026 (date « jeudi 11 juin », liste des documents, auteur « Secrétariat général du COR », sélecteur de langues) : https://www.cor-retraites.fr/rapports-du-cor/rapport-annuel-cor-juin-2026-evolutions-perspectives-retraites-france
- [U2] Rapport complet (PDF, dossier 2026-07) : https://www.cor-retraites.fr/sites/default/files/2026-07/RA_2026_def_1.pdf
- [U3] Partie 2, chapitre 1 (ratio cotisants / retraités, figure 2.3, notes 62 à 64) : https://www.cor-retraites.fr/sites/default/files/2026-06/RA_Part2_Chap1.pdf
- [U4] Partie 1, chapitre 1 (hypothèses, §1.5 rapport démographique, note 35) : https://www.cor-retraites.fr/sites/default/files/2026-06/RA_Part1_Chap1.pdf
- [U5] Diaporama de la séance plénière du 11 juin 2026 (diap. 9, 20, 34) : https://www.cor-retraites.fr/sites/default/files/2026-06/Pr%C3%A9sentation_Pl%C3%A9ni%C3%A8re.pdf
- [U6] Synthèse (deux versions identiques sur ces points) : https://www.cor-retraites.fr/sites/default/files/2026-06/Synth%C3%A8se_RA_2026_0.pdf et https://www.cor-retraites.fr/sites/default/files/2026-06/Synth%C3%A8se%20RA.pdf
- Introduction du rapport (consultée, rien d'utile pour le ratio) : https://www.cor-retraites.fr/sites/default/files/2026-06/Intro%20RA.pdf
- Annexe méthodologique (consultée ; mentionne le rapport comme dimension de l'abaque du COR) : https://www.cor-retraites.fr/sites/default/files/2026-06/Annexe_m%C3%A9thodo_en_ligne_2026.pdf
- [U7] Rapport annuel de juin 2025 (fig. 2.4b, p. 61-63) : https://www.cor-retraites.fr/sites/default/files/2025-06/RA_2025_def_publi.pdf
- [U8] (même fichier que [U4] ; pages 33-34 pour fécondité et solde migratoire, 42 pour la convergence 2030-2040, 46 pour la productivité, 48 pour le chômage)
- [U12] Informations éditeur / mentions légales : https://www.cor-retraites.fr/informations-editeur
- [U14] Page en anglais du COR : https://www.cor-retraites.fr/pensions-advisory-council ; liste des rapports : https://www.cor-retraites.fr/documents/rapports-du-cor ; pages des rapports de 2025, 2024, 2023, 2021 : https://www.cor-retraites.fr/rapports-du-cor/rapport-annuel-cor-juin-2025-evolutions-perspectives-retraites-france , https://www.cor-retraites.fr/rapports-du-cor/rapport-annuel-cor-juin-2024-evolutions-perspectives-retraites-france , https://www.cor-retraites.fr/rapports-du-cor/rapport-annuel-cor-juin-2023-evolutions-perspectives-retraites-france , https://www.cor-retraites.fr/rapports-du-cor/rapport-annuel-cor-juin-2021-evolutions-perspectives-retraites-france
- [U10] Insee, « Projections de population 2026 pour la France », Insee Résultats, paru le 08/06/2026 (page HTML brute) : https://www.insee.fr/fr/statistiques/8991068

Secondaires :

- [U9] IFRAP, « Les six angles morts du rapport du COR », 16 juin 2026 (HTML brut) : https://www.ifrap.org/retraite/les-six-angles-morts-du-rapport-du-cor
- [U11] Trésor-Éco n° 406, 8 octobre 2026 (HTML brut) : https://www.tresor.economie.gouv.fr/Articles/2026/10/08/le-systeme-de-retraite-face-aux-defis-demographiques
- [U15] Cercle de l'Épargne, communiqué du 5 juin 2026 (PDF brut) : https://cercledelepargne.com/wp-content/uploads/2026/06/CP-NOTE-RAPPORT-COR-2026.pdf
- [U13] Reuters via GV Wire, 11 juin 2026 (résumé d'outil de lecture seulement) : https://gvwire.com/2026/06/11/falling-births-to-hit-frances-pension-deficit-from-2045/
- [U16] Statista (résumé d'outil de lecture seulement, valeurs masquées) : https://www.statista.com/statistics/1654307/report-number-contributors-retirees-france/

Résumés de moteur de recherche ([R], non utilisés comme preuve) : recherches sur le ratio 2002-2025, sur la presse de juin 2026, sur data.gouv.fr (aucun jeu COR repéré), sur les licences de réutilisation (CRPA, décret 2017-638 : hors sujet pour trancher le cas du COR), sur l'IPP (chiffres 1,29 / 2,25 / 2,05 non retrouvés à la source IPP ; ils sont cités par le COR lui-même dans [U6] p. 11 et [U5] diap. 34).

Fichiers de lecture graphique (dans le dossier de téléchargements) : `fig23.svg` (figure 2.3 du rapport), `slide20.svg` (diaporama), `fig24_2025.svg` (figure 2.4b du rapport 2025), `fig23_full.svg` (contrôle sur le PDF complet : mêmes nombres de points, 23 observés et 47 projetés pour le ratio).

## Mises à jour

- **03/11/2026, décision du PO** : écrire au COR (info@cor-retraites.fr) avant de redistribuer cette série. Elle reste dans le kit ; l'indicateur reste `planned`, donc hors des éditions, jusqu'à sa réponse.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
