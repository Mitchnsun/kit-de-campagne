# `financeBill` · Projet de loi de finances (saisi à la main)

**Vérifiée le 02/11/2026** : tous les chiffres saisis concordent avec au moins une autre source officielle (avis n° 2026-5 du HCFP, dossier de presse « Budget 2027 », rapport économique, social et financier, projets annuels de performances, rapport de la commission des finances, Insee pour 2025) ; aucune erreur de transcription. Notes reprises de la vérification (périmètre des soldes, prévisions incertaines, crédits bruts, santé).

**À dater dans la page** : à l'Assemblée nationale, l'article liminaire a été supprimé en séance le 14/10/2026 (amendement I-312) ; ses chiffres restent ceux du projet déposé, repris par le rapport économique et l'avis du HCFP. Au 02/11/2026, la première partie est en discussion, son vote solennel prévu le 03/11 ; la seconde partie (état B) n'est pas commencée. Ces chiffres sont à remplacer par ceux de la loi votée.

| Champ | Valeur |
| --- | --- |
| Indicateur | `financeBill`, ticket #141, dossier « Économie et fiscalité » (statut `planned`), à côté de `publicFinances` (PO, 02/11/2026 : un indicateur à part, saisi à la main) |
| Données | `briefings/manual/financeBill.json`, saisi le 2026-11-02 depuis le texte du projet |
| Source | Direction du budget, « Projet de loi de finances pour 2027 », mis en ligne le 01/10/2026, jour de son dépôt à l'Assemblée nationale (n° 3210) : page https://www.budget.gouv.fr/documentation/documents-budgetaires/exercice-2027/PLF2027, PDF https://www.budget.gouv.fr/documentation/file-download/33478 ; Licence Ouverte 2.0 ; en français seulement. Cité depuis le PDF des données ouvertes de l'Assemblée (https://www.assemblee-nationale.fr/dyn/opendata/PRJLANR5L17B3210.pdf) jusqu'au 12/11/2026 (#356) : les pages citées plus bas sont les siennes |
| Séries | `publicBalance` : solde public, en % du PIB, 2025 (exécution) puis 2026 et 2027 (prévisions, statut `projection`), article liminaire ; `publicDebt` : dette au sens de Maastricht, en % du PIB, idem ; `stateBalance` : solde général du budget de l'État en 2027, −156,4 Md€ (article 57 : budget général, budgets annexes, comptes spéciaux) |
| Valeurs par catégorie | `missionCredits` : crédits de paiement 2027 de onze missions ou programmes de l'état B, en Md€ arrondis à 0,1 (enseignement scolaire 90,9 ; défense 73,2, pensions comprises ; charge de la dette 72,4, programme 117 ; … ; santé 1,8) ; total de l'état B 615,1 Md€ bruts, dont 144,5 Md€ de remboursements et dégrèvements (mission non reprise) |
| Chiffre clé | Déficit public visé de 5,0 % du PIB en 2027, après 5,4 % prévu en 2026 |
| Première édition | À remplir à la publication |

À actualiser : à la loi de finances votée (fin décembre), puis à chaque projet (octobre). Le déficit 2025 en milliards diffère entre le projet et le HCFP (−151,6 Md€) et l'Insee (−152,5 Md€), pour un même 5,1 % : écart non expliqué, seuls les pourcentages sont saisis.

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web et recoupe le projet avec les autres documents officiels (budget.gouv.fr a refusé l'accès). Son rapport, tel quel :

Méthode : chaque chiffre de la saisie a été relu dans le PDF du projet (n° 3210) pour localiser l'article, puis recoupé dans au moins un autre document : dossier de presse du ministère, rapport économique, social et financier (RESF), projets annuels de performances (PAP, hébergés par l'Assemblée nationale), avis HCFP n° 2026-5, rapport de la commission des finances n° 3291 rectifié, Insee Première n° 2106.

Limites d'accès (à connaître) :
- `budget.gouv.fr` et `economie.gouv.fr` renvoient **403** (protection anti-robot Incapsula) : je ne les ai pas contournés. Les documents du ministère ont été lus ailleurs : `presse.economie.gouv.fr` (dossier de presse), `tresor.economie.gouv.fr` (RESF), et les PAP publiés sur `assemblee-nationale.fr`.
- Les sites de presse ou de cabinets cités plus bas sont des sources **secondaires** ; je le dis à chaque fois qu'une valeur ne vient que d'eux ou d'un résumé de moteur de recherche.

---

### 0. Écarts et nuances à retenir (version courte)

1. **L'article liminaire n'existe plus dans le texte examiné par l'Assemblée** : les députés l'ont supprimé en séance (amendement I-312, adopté le 14 octobre 2026) après que la commission des finances l'a aussi supprimé (4 amendements de suppression). Les chiffres de la saisie restent exacts pour le projet **tel que déposé** (et dans le RESF, le dossier de presse, l'avis HCFP), mais ils ne figurent plus dans le texte provisoire de l'Assemblée du 2 novembre. À dater dans le jeu.
2. **« Solde général » (−156 394 M€) n'est pas le « solde du budget général »** (−156 582 M€) : le premier ajoute budgets annexes (+221) et comptes spéciaux (−33). La saisie dit « solde général du budget de l'État » : c'est correct, mais le libellé prête à confusion.
3. **« Dépenses nettes » 474 946 M€ (article 57)** = budget général, **net des remboursements et dégrèvements d'impôts d'État**, **hors prélèvements sur recettes** (74,0 Md€) et **hors fonds de concours** (6,1 Md€). Le dossier de presse et le rapport de la commission, eux, appellent « dépenses nettes » **548,9 Md€** (= 474,9 + 43,1 + 30,9 de prélèvements sur recettes). Écart de périmètre, pas d'erreur.
4. **Les 615,1 Md€ de l'état B sont bruts** : ils contiennent la mission « Remboursements et dégrèvements » (144,5 Md€, dont 140,2 d'impôts d'État), qui est la **plus grosse mission en crédits de paiement** et **n'est pas dans la liste saisie**. La liste de 11 lignes n'est donc pas « les plus gros postes de l'état B ».
5. **Défense 73,2 Md€** inclut les contributions au CAS Pensions ; le ministère présente **63,4 Md€ « hors pensions »** (PAP Défense). Écart de périmètre.
6. **« Charge de la dette » 72,4 Md€** = le seul programme 117. Avec la dette reprise de SNCF Réseau : 72,9 Md€ (mission « Engagements financiers de l'État » : 74,5 Md€). La charge d'intérêts de **toutes les administrations** (comptabilité nationale) est de **91,2 Md€** en 2027. Quatre chiffres différents pour « la charge de la dette ».
7. **Déficit 2025 en milliards d'euros** : le projet et l'avis HCFP donnent −151,6 Md€, l'Insee −152,5 Md€ (mai 2026, et déjà −152,5 en mars). Le pourcentage (−5,1 % du PIB) est identique ; la saisie n'utilise que le pourcentage. À signaler si le jeu affiche des milliards.
8. **Le HCFP ne qualifie pas d'un adjectif unique le déficit de 5,0 % en 2027** : il juge « plausible » le 5,4 % de 2026, « optimiste » la croissance de 1,0 %, et dit que le solde 2027 « est exposé aux risques » et subordonné à l'adoption des mesures (citations en section 2).
9. **Erreurs repérées dans des sources secondaires** : un cabinet (KPMG) date le rejet en commission du « 2 octobre » ; le dossier officiel donne **7 au 9 octobre**. Un site de suivi (legiwatch) donne un examen en séance « jusqu'au 17 novembre » et des dates incohérentes. Je ne les ai pas utilisés.

---

### 1. Tableaux de vérification

#### 1.1 Article liminaire (ensemble des administrations publiques, en % du PIB)

| Élément | Valeur saisie | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Dépôt | 1er octobre 2026, n° 3210, 17e législature | « déposé le jeudi 1er octobre 2026 », n° 3210 ; couverture du PDF : « Enregistré à la présidence de l'Assemblée nationale le 1er octobre 2026, N° 3210 », « Dix-septième législature » | https://www.assemblee-nationale.fr/dyn/17/textes/l17b3210_projet-loi ; https://www.assemblee-nationale.fr/dyn/17/dossiers/PLF_2027 ; https://www.assemblee-nationale.fr/dyn/opendata/PRJLANR5L17B3210.pdf | Conforme |
| Solde effectif 2025 | −5,1 (exécution) | −5,1 (colonne 2025 de l'article liminaire, p. 29 du projet). Même valeur : tableau 12 et annexe 2 de l'avis HCFP ; « Exécution 2025 : −5,1 » dans « Chiffres clés » du dossier de presse ; Insee : « 152,5 Md€, soit 5,1 % du PIB » | PDF du projet (ci-dessus) ; https://www.hcfp.fr/sites/default/files/2026-10/Avis%20HCFP%202026-5%20-%20PLF-PLFSS%202027.pdf (p. 29 et 49) ; https://presse.economie.gouv.fr/dp-budget-2027/ (PDF : https://presse.economie.gouv.fr/download?n=1076%20-%20DP%20-%20Budget%202027-pdf&id=184723, « Chiffres clés ») ; https://www.insee.fr/fr/statistiques/8997691 (Insee Première n° 2106, 29/05/2026) | Conforme (en %). Écart de montant : voir ligne « 2025 en Md€ » plus bas |
| Solde effectif 2026 | −5,4 (prévision d'exécution) | −5,4 (projet) ; « Révisé 2026 : −5,4 » (dossier de presse) ; « le déficit public prévu s'établirait à 5,4 % du PIB, après 5,1 % en 2025 » (texte de l'article liminaire) ; RESF : « En 2026, le solde public s'établirait à −5,4 % » | PDF du projet, p. 29–30 ; dossier de presse ; https://www.tresor.economie.gouv.fr/Articles/2026/10/06/le-rapport-economique-social-et-financier-resf-2027-est-publie | Conforme |
| Solde effectif 2027 | −5,0 (PLF) | −5,0 (projet, HCFP, dossier de presse, RESF : « En 2027, le solde public s'établirait à −5,0 % du PIB ») ; −158,1 Md€ pour un PIB nominal de 3 135,0 Md€ (annexe 2 de l'avis HCFP) | idem ; avis HCFP p. 49 | Conforme |
| Dette (Maastricht) 2025 | 115,7 | 115,7 (projet, HCFP, dossier de presse). Insee : « La dette publique s'établit à 115,7 % du PIB » (3 460,5 Md€), publication du 29/05/2026 | idem ; https://www.insee.fr/fr/statistiques/fichier/8997691/ip2106.pdf | Conforme |
| Dette 2026 | 119,3 | 119,3 (projet, HCFP annexe 2, dossier de presse : « En 2026, la dette publique atteint 119,3 % du PIB ») | idem | Conforme |
| Dette 2027 | 121,7 | 121,7 (projet ; HCFP § 113 : « 121,7 % du PIB, soit 3,0 points au-dessus de celle du PLF 2026 » ; dossier de presse) | idem ; avis HCFP p. 37 | Conforme |
| Chiffre clé | déficit public visé de 5,0 % du PIB en 2027, après 5,4 % en 2026 | Exposé général du projet : « La cible de déficit public, à 5,0 % du PIB en 2027 » ; dossier de presse : « le Gouvernement a fixé une cible de déficit de 5,0 % du PIB » ; 2026 révisé de −5,0 % (LFI) à −5,4 % | PDF du projet (exposé des motifs, début du document) ; dossier de presse | Conforme |
| 2025 en Md€ (non saisi, à signaler) | — | Projet / HCFP / commission : **−151,6 Md€** (APUC −130,3 ; APUL −15,6 ; ASSO −5,8). Insee : **−152,5 Md€** (ASSO −6,7). Insee affichait déjà 152,5 Md€ le 27/03/2026 | avis HCFP p. 49 ; rapport de la commission n° 3291 tome I (tableaux « Décomposition des retraitements » et « Évolution du solde public par sous-secteur ») https://www.assemblee-nationale.fr/dyn/17/rapports/cion_fin/l17b3291-ti_rapport-fond.pdf ; https://www.insee.fr/fr/statistiques/fichier/8997691/ip2106.pdf ; https://www.insee.fr/fr/statistiques/8956575 | Écart (0,9 Md€ sur la composante sécurité sociale ; non expliqué dans les documents lus ; sans effet sur le pourcentage arrondi) |
| Statut de l'article liminaire | (non saisi) | Dans le texte provisoire de l'Assemblée du 2 novembre : « Article liminaire (Supprimé) » ; amendement I-312 « Supprimer cet article », **adopté le 14 octobre 2026** ; en commission : 4 amendements de suppression adoptés | https://www.assemblee-nationale.fr/dyn/17/montage/seance/l17b3210_montage-seance.pdf ; https://www.assemblee-nationale.fr/dyn/17/amendements/3210A/AN/312 ; https://www.assemblee-nationale.fr/dyn/opendata/RAPPANR5L17B3291-tII-v1.html | Écart expliqué (les chiffres restent ceux du projet déposé ; l'article n'est plus dans le texte de l'Assemblée) |

#### 1.2 Article 57 (équilibre général), en millions d'euros

| Élément | Valeur saisie | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Solde général | −156 394 M€ (−156,4 Md€) | « Solde général −156 394 » (p. 164 du projet) ; « Déficit à financer 156,4 » (même article, II) ; commission : « Solde budgétaire de l'État −156,4 » ; dossier de presse : « SOLDE GÉNÉRAL −124,2 (2025) / −134,6 (LFI 2026) / −137,2 (révisé 2026) / −156,4 (PLF 2027) » ; le RESF 2027 (PDF du Trésor) porte le même tableau « SOLDE GENERAL −124,2 / −134,6 / −137,2 / −156,4 » | PDF du projet ; https://www.assemblee-nationale.fr/dyn/opendata/RAPPANR5L17B3291-tII-v1.html (article 57 et état A) ; dossier de presse (« Solde général du budget de l'État ») ; https://www.tresor.economie.gouv.fr/Articles/03454e04-445d-4ce6-832b-cff601a11485/files/56839f98-37fc-48d8-b502-81cac5a48cad | Conforme. Nuance : le solde du seul budget général est −156 582 ; solde général = −156 582 + 221 (budgets annexes) − 33 (comptes spéciaux) |
| Dépenses du budget général | « dépenses nettes » 474 946 M€ | 474 946 (ligne « dépenses » du budget général, p. 164). Note *** du projet : « Dépenses budgétaires brutes, minorées des remboursements et dégrèvements d'impôts d'État ». Commission : « plafonnées […] à 474,9 milliards d'euros hors fonds de concours, déduction faite des remboursements et dégrèvements sur impôts d'État ». Avec fonds de concours : 481 050 | PDF du projet ; rapport de la commission tome I p. 131–132 (« Dépenses nettes (article 57) : 474 946 ») et tome II | Conforme. Écart de périmètre avec le dossier de presse (548,9 Md€, prélèvements sur recettes inclus) : voir section 1.4 |

#### 1.3 État B (crédits de paiement 2027, budget général)

Tous les montants viennent de l'état B du projet (article 58 ; état B p. 245–251 de la pagination du document) et ont été retrouvés **à l'euro près** dans le PAP de chaque mission (hébergés par l'Assemblée nationale, URLs en fin de rapport). Arrondis à 0,1 Md€ contrôlés un par un.

| Élément | Valeur saisie | CP dans l'état B (€) | Contrôle PAP | Verdict |
|---|---|---|---|---|
| Enseignement scolaire | 90,9 | 90 859 899 196 | identique (PAP Enseignement scolaire) | Conforme |
| Défense | 73,2 | 73 153 440 797 | identique ; **PAP : « 63,4 Md€ en CP hors pensions »** | Conforme ; Écart de périmètre expliqué (contributions CAS Pensions incluses dans l'état B) |
| Programme « Charge de la dette et trésorerie de l'État » | 72,4 | 72 373 000 000 (crédits évaluatifs ; programme 117) | identique (PAP Engagements financiers de l'État) | Conforme ; voir nuance 6 (72,9 avec SNCF Réseau ; mission 74 451 969 739) |
| Solidarité, insertion et égalité des chances | 32,2 | 32 185 662 632 | identique | Conforme |
| Recherche et enseignement supérieur | 32,1 | 32 054 506 425 | identique | Conforme |
| Sécurités | 26,6 | 26 635 378 954 | identique | Conforme |
| Écologie, développement et mobilité durables | 23,4 | 23 413 423 208 | identique | Conforme |
| Travail, emploi et administration des ministères sociaux | 18,9 | 18 851 988 905 | identique | Conforme |
| Justice | 13,4 | 13 431 798 805 | identique | Conforme |
| Immigration, asile et intégration | 2,1 | 2 087 596 615 | identique | Conforme |
| Santé | 1,8 | 1 769 033 258 | identique | Conforme |
| Total CP du budget général (brut) | 615,1 | **615 139 875 333** (article 58) ; commission : « Le total des crédits inscrits à l'état B […] s'élève à 615,1 milliards d'euros, en hausse de 21,3 milliards d'euros par rapport à la loi de finances pour 2026 » ; tableau : 615 140 | PDF du projet p. 168 (article 58) et p. 251 (total de l'état B) ; commission tome I p. 131–132 | Conforme ; brut (voir 1.4) |
| Omission à noter | (non saisi) | Mission « Remboursements et dégrèvements » : 144 505 838 201 € (dont impôts d'État 140 193 417 535 ; impôts locaux 4 312 420 666) ; mission « Engagements financiers de l'État » : 74 451 969 739 € | PDF du projet p. 247 (Engagements financiers) et p. 250 (Remboursements et dégrèvements) ; PAP Remboursements et dégrèvements | Écart (liste non exhaustive : la première ligne par taille manque) |

Source de la classification « mission / programme » : le libellé « Charge de la dette et trésorerie de l'État (crédits évaluatifs) » est un **programme** de la mission « Engagements financiers de l'État » dans l'état B (p. 247 du projet) et dans le dossier de presse (« programme 117 »).

#### 1.4 Écarts de périmètre (brut / net / fonds de concours / budget général seulement)

| Agrégat | Montant 2027 | Ce qu'il contient | Source |
|---|---|---|---|
| Total CP du budget général, état B (article 58) | 615 139,9 M€ | Brut ; inclut tout le programme « Remboursements et dégrèvements » (144 505,8) ; **hors** fonds de concours ; hors prélèvements sur recettes ; hors budgets annexes et comptes spéciaux | art. 58 ; commission tome I |
| − remboursements et dégrèvements d'impôts d'État (programme 200) | −140 193,4 M€ | Remboursements ayant trait aux recettes | état B ; commission |
| = Dépenses nettes du budget général (article 57) | 474 946 M€ | Les remboursements et dégrèvements d'**impôts locaux** (4 312,4) restent comptés (règle depuis la réforme de la LOLF de 2021, selon la commission) | art. 57 ; commission tome I |
| + fonds de concours et attributions de produits | +6 104 M€ → 481 050 M€ | « Montants nets pour le budget général, y compris fonds de concours » | art. 57 |
| + prélèvements sur recettes (UE 30,9 ; collectivités 43,1) | → **548,9 Md€** | Convention du dossier de presse et du rapport de la commission (tome I) : les PSR sont inclus dans « dépenses » | dossier de presse « Solde général du budget de l'État » ; commission tome I p. 75 |
| Budgets annexes (charges) | 2 771 M€ | | art. 57 |
| Comptes spéciaux (CAS + CCF, charges) | 237 327 M€ (CAS 75 470 + CCF 161 857 selon art. 57) | | art. 57 ; commission tome I p. 132 |
| Ensemble des dépenses de l'État (état B + C + D) | 715 045 M€ | | commission tome I p. 132 |

Anomalie mineure : le tome II du rapport de la commission écrit « le total des dépenses nettes du budget général de l'État prévu pour 2026 s'élève à 525,7 milliards d'euros, hors fonds de concours » en assimilant les PSR à des dépenses. Ce chiffre (525,7, et « 2026 ») ne cadre ni avec 548,9 (tome I et dossier de presse) ni avec 474,9 + 74,0 : probable reste du texte de l'an passé. Je ne l'ai pas utilisé.

---

### 2. Le HCFP et la prévision de déficit de 5,0 % (point 2)

Avis HCFP n° 2026-5, daté du **25 septembre 2026** dans le PDF (la page du site affiche « 1 octobre 2026 », date de mise en ligne). Pages ci-dessous = pages du PDF. https://www.hcfp.fr/liste-avis/avis-ndeg2026-5-lois-de-finances-2027 ; PDF : https://www.hcfp.fr/sites/default/files/2026-10/Avis%20HCFP%202026-5%20-%20PLF-PLFSS%202027.pdf

**Le HCFP n'applique pas « réaliste », « optimiste » ou « plausible » à la prévision de solde 2027.** Citations exactes :

- § 93, p. 28 (conclusion sur le solde) :
  « l'actualisation de la prévision de solde public pour 2026 à 5,4 % du PIB est plausible, bien que des aléas significatifs entourent encore cette prévision en dépenses et en recettes et se renforcent au vu des dernières évolutions ; »
  « la prévision de solde public pour 2027 est exposée aux risques soulignés sur le scénario économique et aux incertitudes relatives au rendement des mesures. De plus, l'application de mesures en dépenses comme en recettes, et donc la prévision de solde public, sont subordonnées notamment à l'adoption des lois financières et de dispositions réglementaires : si elles n'étaient pas adoptées, l'équilibre financier prévu ne pourrait être maintenu qu'en remplaçant les mesures prévues par d'autres de rendement équivalent. »
- Synthèse, p. 2, croissance 2027 : « Le Haut Conseil estime quant à lui que le chiffre de croissance retenu par le Gouvernement apparaît comme optimiste au regard des dernières évolutions. » ; « Au total, les aléas à la baisse sont majoritaires. »
- Synthèse, p. 2, recettes : « Le Haut Conseil estime qu'une telle élasticité globale est réaliste et que la prévision d'évolution spontanée des prélèvements est cohérente avec le scénario économique, avec un aléa baissier en cas de croissance plus faible. »
- Synthèse, p. 2, dépenses : « Le Haut Conseil estime que si l'ensemble de ces mesures est effectivement mis en œuvre, la prévision de dépense présentée est atteignable. »
- Synthèse, p. 3 : « Le Haut Conseil rappelle résolument que l'ambition de réduction du déficit affichée pour 2027 est un minimum au regard de la situation alarmante des finances publiques. Même avec l'effort d'ajustement projeté en 2027, le redressement des comptes publics se fait à un rythme ralenti : à 5 % du PIB, le déficit public resterait voisin du niveau où il se situait déjà en 2025 et encore supérieur à celui atteint à la sortie de la crise du Covid en 2022. Le déficit est en outre presque intégralement de nature structurelle et non le reflet d'une récession économique. »
- Contexte, p. 1 : « Le contexte national est également marqué par une incertitude importante, y compris relativement à l'adoption même du budget pour 2027. »
- Dette, § 113 (p. 36–37) : ratio de dette « prévu en 2027 à 121,7 % du PIB » ; la synthèse parle d'une hausse « de plus de 3,5 points en 2026 et de près de 2,5 points en 2027, le faisant approcher 122 % ».
- Version anglaise officielle : « The forecast for the public balance in 2027 is exposed to the risks identified in the economic scenario and to uncertainties regarding the yield of the measures. » (§ 93, p. 28) ; première ligne du PDF : « Please consult the French version for the exact terms approved by the HCFP ».

Source secondaire sur l'effet du travail de la commission : LCP et Legifiscal (résumés lus via moteur de recherche ou page de presse) rapportent une estimation du rapporteur général selon laquelle le texte de la commission porterait le déficit à environ 5,35–5,4 % du PIB ; non recoupée dans un document officiel lu.

---

### 3. Déficit public et solde budgétaire de l'État (point 3)

| Notion | Définition sourcée | Valeur 2027 | Source |
|---|---|---|---|
| Déficit public (Maastricht, toutes administrations publiques) | Insee : « La capacité ou le besoin de financement des administrations publiques est le solde du compte non financier, égal aux recettes diminuées des dépenses. Il correspond au déficit public au sens de Maastricht. » Couvre État, organismes divers d'administration centrale (ODAC), administrations publiques locales (APUL), administrations de sécurité sociale (ASSO) | −5,0 % du PIB ; **−158,1 Md€** | Insee Première n° 2106 (rubrique « Définitions ») https://www.insee.fr/fr/statistiques/fichier/8997691/ip2106.pdf ; HCFP annexe 2 |
| Solde budgétaire / « solde général » de l'État (comptabilité budgétaire) | Commission : « Le solde budgétaire de l'État est constitué par la somme du solde du budget général, des budgets annexes et des comptes spéciaux. » ; comptabilité de trésorerie (encaissements et décaissements) | −156,4 Md€ (budget général −156,6 ; budgets annexes +0,2 ; comptes spéciaux ≈ 0) | commission tome I p. 73–77 et tome II (article 57) |
| Déficit de l'État en comptabilité nationale | Même acteur, autre règle de comptabilisation | −156,2 Md€ (écart de 0,2 Md€ : matériel militaire enregistré à la livraison, +1,1 ; décalage des quotas carbone, −0,7) | commission tome I p. 76–77 |

Chiffres utiles pour ne pas confondre (calculs à partir des tableaux de la commission, tome I p. 78, « Évolution du solde public par sous-secteur ») :
- 2026 : solde budgétaire de l'État −137,2 Md€ pour un déficit public de −164,9 Md€ (soit « plus de 83 % du déficit public », phrase de la commission).
- 2027 : −156,4 Md€ contre −158,1 Md€ de déficit public : les deux montants sont presque égaux en euros (rapport de 99 %, calcul personnel), parce que les ASSO (+7,1) compensent presque les APUL (−8,4) et les ODAC (−0,6). Ce rapprochement est un hasard de l'année ; les deux notions restent distinctes.
- 2025 : Insee, déficit de l'**État en comptabilité nationale** −128,1 Md€, alors que le déficit **budgétaire** de l'État était de −124,2 Md€ (dossier de presse), et le déficit public de −152,5 Md€ (Insee).

---

### 4. Licence, version anglaise (point 4)

#### 4.1 Licence

Ce n'est pas un avis juridique ; ce sont les mentions lues.

| Source | Ce que dit la mention | URL |
|---|---|---|
| Portail « données ouvertes » de l'Assemblée | « Licence Ouverte / Open Licence » conçue par Etalab : autorise « la reproduction, la redistribution, l'adaptation et l'exploitation commerciale des données » ; « mention de la paternité » obligatoire. Le texte de la page date de 2011 (« Depuis novembre 2011 ») et **ne précise pas de version** (la « 2.0 » n'est pas écrite sur la page). | https://data.assemblee-nationale.fr/licence-ouverte-open-licence |
| Mentions légales du site assemblee-nationale.fr | Les documents « publics » ou « officiels », dont « les débats et les documents parlementaires », ne sont couverts par aucun droit d'auteur (art. L.122-5 du code de la propriété intellectuelle) et « peuvent donc être reproduits librement » ; mais « les informations utilisées ne doivent l'être qu'à des fins personnelles, associatives ou professionnelles, toute utilisation ou reproduction à des fins commerciales ou publicitaires étant interdite » ; reproduction « sous réserve de la gratuité de leur diffusion, du respect de l'intégrité des documents reproduits, de la mention du nom de l'auteur, de la source, et d'un lien renvoyant vers le document original en ligne » | https://www.assemblee-nationale.fr/dyn/info-site |
| Le PDF du projet n° 3210 | Aucune mention de licence dans le texte extrait du PDF (métadonnées : créé le 1er octobre 2026). Rien ne dit que ce fichier, situé sous `/dyn/opendata/`, relève de la Licence Ouverte. | https://www.assemblee-nationale.fr/dyn/opendata/PRJLANR5L17B3210.pdf |
| Dossier de presse du ministère (`presse.economie.gouv.fr`) | « Sauf mention contraire, tous les contenus de ce site sont sous licence etalab-2.0 » | https://presse.economie.gouv.fr/dp-budget-2027/ |
| DG Trésor (RESF) | Réutilisation « non commerciale, et notamment pédagogique » autorisée à condition de respecter l'intégrité des informations, d'en préciser l'origine et la date de publication ; usage commercial ou promotionnel soumis à autorisation expresse | https://www.tresor.economie.gouv.fr/Institutionnel/mentions-legales |
| HCFP | Reproduction autorisée sous réserve de la mention explicite de hcfp.fr comme source et de l'intégrité du contenu (pas de coupes ni de commentaires non distingués qui altèrent le sens) | https://www.hcfp.fr/mentions-legales |
| Insee Première n° 2106 | « Reproduction partielle autorisée sous réserve de la mention de la source et de l'auteur » | https://www.insee.fr/fr/statistiques/fichier/8997691/ip2106.pdf |

Conclusion licence : les **données ouvertes** de l'Assemblée sont en Licence Ouverte (version non précisée sur la page) ; pour les **documents** du site (projet de loi, rapports), la mention légale autorise la reproduction **gratuite**, avec intégrité, auteur, source et lien, et interdit l'usage commercial. Pour un jeu éducatif : citer le document et l'URL, ne pas reproduire des pages entières. Je n'ai pas pu lire les mentions de `budget.gouv.fr` (403).

#### 4.2 Version anglaise

- **HCFP : oui.** Avis en anglais, avec l'avertissement « Please consult the French version for the exact terms approved by the HCFP » : https://www.hcfp.fr/sites/default/files/2026-10/Opinion%20HCFP%20no%202026-5%20-%20PLF-PLFSS%202027.pdf ; page : https://www.hcfp.fr/en/liste-avis/opinion-ndeg2026-5-draft-budget-bills-2027 .
- **Projet de loi, RESF, PAP, dossier de presse : version anglaise non trouvée** (tous en français). Le site anglais de l'Assemblée ne mentionne aucune traduction du projet ni des documents budgétaires (page d'accueil anglaise lue : https://www.assemblee-nationale.fr/dyn/langues/welcome-to-the-english-website-of-the-french-national-assembly). La DG Trésor a une section « The French Treasury (English Pages) » : je n'y ai pas trouvé le RESF 2027. Absence non prouvée pour `budget.gouv.fr`, inaccessible (403).
- Presse anglophone (secondaire) : France 24, Yahoo Finance, ING, Deloitte (résumés de moteur de recherche, non ouverts).

---

### 5. Où en est le texte au 2 novembre 2026 (point 5)

| Date | Fait | Source | Fiabilité |
|---|---|---|---|
| 1er oct. 2026 | Dépôt du PLF n° 3210 (mise en ligne 18 h 50), renvoyé à la commission des finances | https://www.assemblee-nationale.fr/dyn/17/dossiers/PLF_2027 | Officielle |
| 7 au 9 oct. | Commission des finances : « a examiné puis rejeté la première partie du projet de loi de finances pour 2027 » (pas de décompte sur cette page) | https://www.assemblee-nationale.fr/dyn/17/organes/commissions-permanentes/finances/actualites/projet-de-loi-de-finances-pour-2027-examen-de-la-premiere-partie | Officielle |
| 9 oct. (soir) | Décompte : 31 voix contre, 3 pour, 2 abstentions | https://lcp.fr/actualites/budget-2027-les-deputes-rejettent-en-commission-la-partie-recettes-du-projet-de-loi-de | Presse (LCP), non retrouvé dans un document officiel lu |
| 10 oct. | Rapport n° 3291 rectifié déposé (tome I publié ; tome II disponible en version « opendata ») | https://www.assemblee-nationale.fr/dyn/17/rapports/cion_fin/l17b3291_rapport-fond | Officielle |
| 13 oct. | Début de la discussion en séance publique de la première partie | dossier législatif (étape « Discussion en séance publique, mardi 13 octobre 2026 ») | Officielle |
| 14 oct. | Amendement I-312 (groupe LFI), « ARTICLE LIMINAIRE – Supprimer cet article », **adopté** | https://www.assemblee-nationale.fr/dyn/17/amendements/3210A/AN/312 | Officielle (le décompte « 135 voix contre 53 » ne vient que d'un cabinet d'avocats, https://www.avocat-fiscaliste-semon.paris/fiscal-watch-2027/articles/73884c477179ff03/ : secondaire) |
| 20 au 23 oct. | PLFSS 2027 (texte distinct, n° 3211) : « Texte rejeté » par l'Assemblée le 23 octobre (T.A. n° 358) ; transmis au Sénat le 2 novembre (n° 138) | https://www.assemblee-nationale.fr/dyn/17/dossiers/PLFSS_2027 | Officielle |
| 27 oct. au 2 nov. | « L'Assemblée nationale poursuit l'examen de la première partie » ; « Le vote solennel sur la première partie du projet de loi de finances pour 2027 est inscrit à l'ordre du jour de la séance publique du **mardi 3 novembre, après-midi** » (page sans date affichée) | https://www.assemblee-nationale.fr/dyn/actualites-accueil-hub/examen-de-la-premiere-partie-du-projet-de-loi-de-finances-pour-2027 | Officielle |
| 2 nov. | Texte provisoire « à l'issue de la troisième séance du 30 octobre 2026 » : article liminaire « (Supprimé) » ; articles 16, 19 à 33 et 42 à 54 « (Non examinés) » ; l'article 57 n'apparaît pas dans ce texte | https://www.assemblee-nationale.fr/dyn/17/montage/seance/l17b3210_montage-seance.pdf | Officielle (document « établi à titre provisoire ») |
| 2 nov. | Deux séances sur la première partie (« Première partie (suite) », amendements après l'article 16, puis articles 19 à 21 et 23 ; compte rendu provisoire de 22 h 51) | https://www.assemblee-nationale.fr/dyn/17/comptes-rendus/seance/session-ordinaire-de-2026-2027/deuxieme-seance-du-lundi-02-novembre-2026 | Officielle (provisoire) |

Constats, sans rien supposer :
- **Aucun vote de la première partie en séance à la date du 2 novembre** dans les documents officiels lus ; le vote solennel est inscrit au 3 novembre. La seconde partie (les missions, donc l'état B, article 58) n'est pas commencée. L'article 57 (équilibre) clôt la première partie ; il n'apparaît pas dans le texte provisoire du 2 novembre (le document s'arrête à l'article 56), donc, a priori, il n'a pas encore été examiné en séance (déduction de ma part, pas une mention du document).
- Le dossier législatif n'affiche aucune étape « texte adopté », ni Sénat, ni commission mixte paritaire pour le PLF.
- Si la première partie était rejetée, la première lecture s'arrêterait (source secondaire : https://nosparlementaires.fr/actualites/budget-2027-dossier-plf-88-articles-ce-que-les-deputes-ont-deja-vote , qui rappelle le rejet des premières parties 2025 et 2026) ; ce même site annonçait un vote le 20 octobre (calendrier dépassé) et un vote sur l'ensemble le 17 novembre (non confirmé officiellement).
- Les chiffres de l'état B et de l'article 57 de la saisie sont donc ceux du **projet déposé**, non modifiés à ce jour par un vote de séance. La commission avait modifié l'article 57 par deux amendements identiques (interdiction des emprunts indexés sur l'inflation), mais son texte est sans portée puisqu'elle a rejeté la première partie.

---

### 6. Notes « À savoir » : évaluation et rédaction proposée (320 caractères au plus)

#### Note 1 (solde public et solde de l'État) : confirmée, avec une précision

Ce qui est correct : le déficit public « au sens de Maastricht » est le besoin de financement de toutes les administrations (Insee) ; le solde général de l'État est la somme du budget général, des budgets annexes et des comptes spéciaux (commission). −5,0 % et −156,4 Md€ sont dans le projet. Précision : « visé » et « serait » (ce sont des cibles), et le solde de l'État est en comptabilité budgétaire.

Rédaction proposée (285 caractères) :
« Le déficit public (toutes les administrations publiques, au sens de Maastricht) n'est pas le solde du budget de l'État. Le projet vise −5,0 % du PIB en 2027 pour le premier ; le solde général du budget de l'État (budget général, budgets annexes, comptes spéciaux) serait de −156,4 Md€. »

#### Note 2 (prévisions modifiables) : confirmée, à nuancer

Faits : 2025 est un résultat mesuré (Insee, mai 2026 ; l'Insee avait publié 115,6 % de dette en mars puis 115,7 % en mai : même un chiffre « mesuré » est révisé) ; 2026 est une « prévision d'exécution » ; 2027 est la prévision du projet. Le HCFP : « incertitude importante, y compris relativement à l'adoption même du budget pour 2027 ». Le Parlement a déjà modifié le texte (article liminaire supprimé). Éviter d'écrire « la loi votée remplacera le projet » sans réserve : l'adoption n'est pas acquise (HCFP).

Rédaction proposée (240 caractères) :
« Les chiffres de 2026 et de 2027 sont des prévisions du Gouvernement, pas des résultats ; seul 2025 est mesuré (Insee). Le Parlement peut modifier le projet : la loi finalement votée remplacera ces chiffres, et son adoption reste incertaine. »

#### Note 3 (crédits de paiement bruts, charge de la dette) : confirmée, précision nécessaire sur « bruts »

« Bruts » est ambigu. Dans l'état B, le total de 615,1 Md€ inclut 144,5 Md€ de remboursements et dégrèvements (le chiffre net de l'article 57 est 474,9 Md€) et exclut les fonds de concours (+6,1) et les prélèvements sur recettes (74,0). La charge de la dette est bien un programme (117) de la mission « Engagements financiers de l'État ». Autre nuance utile : les 72,4 Md€ sont ceux de l'État ; la charge d'intérêts de toutes les administrations est de 91,2 Md€ (dossier de presse).

Rédaction proposée (261 caractères) :
« Les crédits de paiement sont ceux de l'état B du projet, en montants bruts : le total de 615,1 Md€ inclut 144,5 Md€ de remboursements et dégrèvements d'impôts. La charge de la dette (72,4 Md€) est un programme de la mission « Engagements financiers de l'État ». »

#### Note 4 (santé et Sécurité sociale) : confirmée

Faits : mission « Santé » = 1 769 033 258 € de CP (état B), composée de la prévention et offre de soins, de la protection maladie (1,2 Md€) et du reversement FRR (0,24 Md€) ; l'Ondam 2027 du projet de loi de financement de la sécurité sociale est de **278,7 Md€** (273,3 en 2026 révisé), soit +2,0 % (dossier de presse, tableau Ondam). Le PLFSS 2027 a été rejeté par l'Assemblée le 23 octobre et est au Sénat : le chiffre de l'Ondam est donc celui du projet, pas d'une loi adoptée.

Rédaction proposée (214 caractères) :
« La santé est financée surtout par la Sécurité sociale (loi de financement : objectif de dépenses d'assurance maladie de 278,7 Md€ en 2027), pas par la mission « Santé » du budget de l'État, qui ne pèse que 1,8 Md€. »

---

### 7. Conclusion

#### Écarts d'abord

1. **Article liminaire supprimé** dans le texte de l'Assemblée (commission, puis amendement I-312 adopté en séance le 14 octobre 2026) : les chiffres de la saisie sont ceux du projet déposé, pas du texte en cours d'examen. Écart expliqué.
2. **Déficit 2025 en Md€ : 151,6 (projet, HCFP) contre 152,5 (Insee)** ; même pourcentage (−5,1 %). Écart non expliqué dans les documents lus.
3. **Libellés** : « solde général » (−156 394) ≠ « solde du budget général » (−156 582) ; « dépenses nettes » 474,9 Md€ (article 57) ≠ 548,9 Md€ (dossier de presse, prélèvements sur recettes inclus). Écarts de périmètre expliqués.
4. **Périmètres de l'état B** : 615,1 Md€ brut incluant 144,5 Md€ de remboursements et dégrèvements ; Défense 73,2 avec pensions contre 63,4 hors pensions ; charge de la dette 72,4 (programme 117) contre 72,9 (avec SNCF Réseau), 74,5 (mission) et 91,2 (intérêts de toutes les administrations). La liste saisie omet la mission « Remboursements et dégrèvements ».
5. **Le HCFP** n'a pas qualifié le déficit 2027 de « réaliste » ou « optimiste » : il dit le solde 2027 « exposé aux risques » et subordonné à l'adoption des mesures ; l'adjectif « optimiste » vise la croissance (1,0 %), « plausible » vise le 5,4 % de 2026.
6. **Sources secondaires fautives** : date du 2 octobre pour le rejet en commission (KPMG), dates de séance de legiwatch. Non retenues.

#### Conformes

Tous les autres chiffres de la saisie : dépôt (1er octobre 2026, n° 3210), soldes −5,1 / −5,4 / −5,0, dettes 115,7 / 119,3 / 121,7, chiffre clé 5,0 % après 5,4 %, article 57 (−156 394 ; 474 946), et les **onze lignes de l'état B plus le total 615,1**, retrouvés à l'euro près dans l'état B et dans les PAP.

#### État du texte au 2 novembre 2026

Première lecture à l'Assemblée, **première partie en cours d'examen en séance** (commission : première partie rejetée les 7 au 9 octobre ; vote solennel de la première partie inscrit au 3 novembre, après-midi, non encore intervenu). Seconde partie non commencée. Aucun vote sur la première partie ni sur l'ensemble du texte (des amendements et articles isolés ont été votés). Le PLFSS, lui, a été rejeté par l'Assemblée le 23 octobre.

#### Licence et anglais

Données ouvertes de l'Assemblée : Licence Ouverte (version non précisée sur la page) ; documents du site : reproduction gratuite avec intégrité, source et lien, usage commercial interdit ; dossier de presse du ministère : etalab-2.0. Version anglaise : avis du HCFP uniquement ; pas trouvée pour le projet, le RESF, les PAP ni le dossier de presse (`budget.gouv.fr` inaccessible).

---

### 8. URLs consultées

#### Ouvertes et lues (primaires, officielles ou ministère)

- https://www.assemblee-nationale.fr/dyn/opendata/PRJLANR5L17B3210.pdf (projet n° 3210, téléchargé)
- https://www.assemblee-nationale.fr/dyn/17/textes/l17b3210_projet-loi
- https://www.assemblee-nationale.fr/dyn/17/dossiers/PLF_2027
- https://www.assemblee-nationale.fr/dyn/17/dossiers/PLF_2027/rapports
- https://www.assemblee-nationale.fr/dyn/17/dossiers/PLFSS_2027
- https://www.assemblee-nationale.fr/dyn/17/rapports/cion_fin/l17b3291_rapport-fond ; tome I PDF https://www.assemblee-nationale.fr/dyn/17/rapports/cion_fin/l17b3291-ti_rapport-fond.pdf ; tome II https://www.assemblee-nationale.fr/dyn/opendata/RAPPANR5L17B3291-tII-v1.html
- https://www.assemblee-nationale.fr/dyn/17/organes/commissions-permanentes/finances/actualites/projet-de-loi-de-finances-pour-2027-examen-de-la-premiere-partie
- https://www.assemblee-nationale.fr/dyn/actualites-accueil-hub/examen-de-la-premiere-partie-du-projet-de-loi-de-finances-pour-2027
- https://www.assemblee-nationale.fr/dyn/17/montage/seance/l17b3210_montage-seance.pdf
- https://www.assemblee-nationale.fr/dyn/17/amendements/3210A/AN/312
- https://www.assemblee-nationale.fr/dyn/17/comptes-rendus/seance ; https://www.assemblee-nationale.fr/dyn/17/comptes-rendus/seance/session-ordinaire-de-2026-2027/deuxieme-seance-du-lundi-02-novembre-2026
- https://www.assemblee-nationale.fr/dyn/budget-et-securite-sociale
- https://www.assemblee-nationale.fr/dyn/info-site ; https://data.assemblee-nationale.fr/ ; https://data.assemblee-nationale.fr/licence-ouverte-open-licence
- https://www.assemblee-nationale.fr/dyn/langues/welcome-to-the-english-website-of-the-french-national-assembly
- PAP 2027 (hébergés par l'Assemblée) : Enseignement scolaire https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128234/file/PAP%202027%20-%20Enseignement%20scolaire.pdf ; Défense https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128221/file/PAP%202027%20-%20D%C3%A9fense.pdf ; Engagements financiers de l'État https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128231/file/PAP%202027%20-%20Engagements%20financiers%20de%20l%27Etat.pdf ; Solidarité https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128278/file/PAP%202027%20-%20Solidarit%C3%A9%20insertion%20et%20%C3%A9galit%C3%A9%20des%20chances.pdf ; Recherche et enseignement supérieur https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128257/file/PAP%202027%20-%20Recherche%20et%20enseignement%20sup%C3%A9rieur.pdf ; Sécurités https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128275/file/PAP%202027%20-%20S%C3%A9curit%C3%A9s.pdf ; Écologie https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128225/file/PAP%202027%20-%20Ecologie%20d%C3%A9veloppement%20et%20mobilit%C3%A9s%20durables.pdf ; Travail https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128284/file/PAP%202027%20-%20Travail%20emploi%20et%20administration%20des%20minist%C3%A8res%20sociaux.pdf ; Justice https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128243/file/PAP%202027%20-%20Justice.pdf ; Immigration https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128237/file/PAP%202027%20-%20Immigration%20asile%20et%20int%C3%A9gration.pdf ; Santé https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128269/file/PAP%202027%20-%20Sant%C3%A9.pdf ; Remboursements et dégrèvements https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128264/file/PAP%202027%20-%20Remboursements%20et%20d%C3%A9gr%C3%A8vements.pdf
- https://www.hcfp.fr/liste-avis/avis-ndeg2026-5-lois-de-finances-2027 ; avis PDF (FR) https://www.hcfp.fr/sites/default/files/2026-10/Avis%20HCFP%202026-5%20-%20PLF-PLFSS%202027.pdf ; avis (EN) https://www.hcfp.fr/sites/default/files/2026-10/Opinion%20HCFP%20no%202026-5%20-%20PLF-PLFSS%202027.pdf ; page EN https://www.hcfp.fr/en/liste-avis/opinion-ndeg2026-5-draft-budget-bills-2027 ; https://www.hcfp.fr/mentions-legales
- https://presse.economie.gouv.fr/dp-budget-2027/ (page) et PDF https://presse.economie.gouv.fr/download?n=1076%20-%20DP%20-%20Budget%202027-pdf&id=184723 (dossier de presse « Budget 2027 », 1er octobre 2026)
- https://www.tresor.economie.gouv.fr/Articles/2026/10/06/le-rapport-economique-social-et-financier-resf-2027-est-publie ; RESF PDF https://www.tresor.economie.gouv.fr/Articles/03454e04-445d-4ce6-832b-cff601a11485/files/56839f98-37fc-48d8-b502-81cac5a48cad (téléchargé ; utilisé pour le tableau « SOLDE GENERAL » −156,4 et la mention du solde public −5,0 % ; je n'ai pas relu le reste du rapport) ; https://www.tresor.economie.gouv.fr/Institutionnel/mentions-legales
- Insee : https://www.insee.fr/fr/statistiques/8997691 ; https://www.insee.fr/fr/statistiques/fichier/8997691/ip2106.pdf ; https://www.insee.fr/fr/statistiques/8956575

#### Ouvertes et lues (secondaires, presse ou cabinets)

- https://lcp.fr/actualites/budget-2027-les-deputes-rejettent-en-commission-la-partie-recettes-du-projet-de-loi-de (décompte 31 / 3 / 2)
- https://www.avocat-fiscaliste-semon.paris/fiscal-watch-2027/articles/73884c477179ff03/ (décompte 135 / 53, non retrouvé officiellement)
- https://nosparlementaires.fr/actualites/budget-2027-dossier-plf-88-articles-ce-que-les-deputes-ont-deja-vote (calendrier initial, dépassé)
- https://www.legiwatch.fr/loi/plf-2027/ (dates incohérentes : écarté)
- https://kpmg.com/av/fr/avocats/eclairages/2026/10/loi-de-finances-2027-toute-l-actualite.html (date du rejet erronée : écarté)

#### Vues seulement dans des résumés de moteur de recherche (non ouvertes, non utilisées comme preuve)

- https://www.lafinancepourtous.com/2026/10/08/projet-de-loi-de-finances-le-budget-2027-sous-haute-tension/ ; https://fr.euronews.com/2026/10/01/budget-2027-le-gouvernement-propose-un-effort-de-54-milliards-deuros-pour-ramener-le-defic ; https://www.lemondedudroit.fr/fiscal/310-finances-publiques/106025-plf-2027-depot-a-l-an.html ; https://www.legifiscal.fr/actualites-fiscales/4684-plf-2027-commission-finances-rejette-partie-recettes-creuse-deficit-environ-10-md.html ; https://think.ing.com/articles/frances-budget-offers-no-quick-relief-for-bond-markets/ ; https://www.france24.com/en/live-news/20261001-france-unveils-cost-cutting-2027-budget-as-borrowing-costs-rise ; https://econotimes.com/France-s-Draft-Budget-Puts-2027-Interest-Bill-at-91-2-Billion-1758002 ; https://www.journaldeleconomie.fr/deficit-dette-chiffres-insee/ (dette 115,6 % en mars)

#### Inaccessibles

- https://www.budget.gouv.fr/ (et sous-pages), https://www.economie.gouv.fr/ (403, protection anti-robot ; non contourné)

## Mises à jour

- **03/11/2026, décision du PO** : la page dit « chiffres du projet déposé », avec une note sur l'article liminaire supprimé en séance à l'Assemblée le 14/10/2026. La loi de finances pour 2027, une fois promulguée, sera saisie dans une nouvelle édition ; la navette n'est pas suivie.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Direction du budget : Licence Ouverte 2.0 (« licence ouverte Etalab 2.0 »), mention de la source et de sa date de dernière mise à jour, contenus de tiers et photos exclus (https://www.budget.gouv.fr/mentions-legales, lues le 12/11/2026). Ces documents étaient cités depuis l'Assemblée nationale, dont les mentions légales (https://www.assemblee-nationale.fr/dyn/info-site) interdisent la réutilisation commerciale : le PO a décidé le 12/11/2026 de les citer depuis budget.gouv.fr. Le projet de loi de finances pour 2027 y est mis en ligne le 01/10/2026, jour de son dépôt (n° 3210 à l'Assemblée) ; ses chiffres, lus dans le PDF de l'Assemblée, ont été relus le 12/11/2026 dans celui du Budget (`PLF-2027_web.pdf`, 391 pages) : identiques, articles 57 et 58 compris. Les pages citées dans cette fiche restent celles de l'Assemblée ; dans le PDF du Budget, le tableau de synthèse passe de la p. 14 à la p. 17, l'article liminaire des p. 29–30 aux p. 33–34, l'article 57 de la p. 164 aux p. 188–189 et l'état B des p. 245–251 aux p. 275–281.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
