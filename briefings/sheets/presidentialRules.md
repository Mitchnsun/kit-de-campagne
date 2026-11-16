# `presidentialRules` · Les règles de la présidentielle (saisie à la main)

**Vérifiée le 16/11/2026** : chaque règle, chaque date de 2027 et chaque montant recoupés avec le rapport de recherche du 15/11/2026 et sa double vérification sur le web par un agent Claude (modèle Sonnet), 15/11/2026, sans écart non expliqué ; les citations relues mot à mot le 16/11/2026 (section « Lecture des textes »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `presidentialRules`, dossier « Institutions » (`institutions`, aussi dans « Électorat »), page de type « règles » (`rules`, décision du PO du 16/11/2026), nature « Texte en vigueur » (`law`), ticket #443 de l'app |
| Données | `briefings/manual/presidentialRules.json`, saisi à la main le 2026-11-16 depuis les textes en vigueur |
| Sources | Dans l'ordre du registre : (0) Légifrance, loi n° 62-1292 du 6 novembre 1962 relative à l'élection du Président de la République au suffrage universel, version en vigueur au 16/11/2026, `https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000684037` ; (1) Légifrance, code électoral, version du 01/07/2026, `https://www.legifrance.gouv.fr/codes/texte_lc/LEGITEXT000006070239` ; (2) Légifrance, loi n° 77-808 du 19 juillet 1977 relative à la publication et à la diffusion de certains sondages d'opinion, version en vigueur au 16/11/2026, `https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000522846` ; (3) Conseil constitutionnel, Constitution du 4 octobre 1958, texte en vigueur lu le 15/11/2026, `https://www.conseil-constitutionnel.fr/le-bloc-de-constitutionnalite/texte-integral-de-la-constitution-du-4-octobre-1958-en-vigueur` (en anglais : `https://www.conseil-constitutionnel.fr/en/constitution-of-4-october-1958`) ; (4) Conseil constitutionnel, décision n° 2019-1 RIP du 9 mai 2019, JORF du 15/05/2019, `https://www.conseil-constitutionnel.fr/decision/2019/20191RIP.htm` (en anglais : `/en/decision/2019/20191RIP.htm`) ; (5) CNCCFP, « Guide à l'usage des candidats à l'élection du Président de la République et de leur mandataire, édition 2026-2027 », version corrigée et mise à jour au 11/06/2026, `https://cnccfp.fr/wp-content/uploads/2026/04/Guide-a-lusage-des-candidats-a-lelection-du-President-de-la-Republique-2027.pdf` ; (6) Service-Public.fr, « Les dates de l'élection présidentielle de 2027 sont annoncées », publié le 02/07/2026, `https://www.service-public.gouv.fr/particuliers/actualites/A15053` |
| Licences | Légifrance : « Sauf mention contraire, tous les contenus de ce site sont sous licence etalab-2.0 » (pied de page, lu le 16/11/2026 ; la base LEGI sur data.gouv.fr est sous la Licence Ouverte 1.0) ; Service-Public.fr : etalab-2.0 ; Conseil constitutionnel : reproduction libre avec citation du site, de la date et de l'intitulé (mentions légales), cité seulement ; CNCCFP : reproduction avec intégrité, source, date et lien, « ne peuvent être utilisées à des fins commerciales ou publicitaires », cité seulement |
| Série | `requiredSponsorships` : les parrainages requis pour la présidentielle de 2027, 500 (loi n° 62-1292, art. 3, I), un point. La série de 1965 à 2022 (100 puis 500 depuis la loi organique n° 76-528) n'est pas saisie : les années 1965, 1969 et 1974 demandent une source à part |
| Chiffre clé | 500 parrainages, 2027, sans tendance |
| Règles (`provisions`) | 28 lignes : chacune son article, son texte exact (sans guillemets, « […] » là où des mots sont omis, capitales accentuées et espaces de la typographie de l'app, les mots du texte), sa source, et son chiffre (avec son unité, la source où il se lit, `calcul`) ou la date du calendrier qu'elle fixe |
| Calendrier (`milestones`) | 10 dates, dans l'ordre : leur statut (`computed`, `announced`), l'heure quand le texte la donne, « au plus tard » (`deadline`), l'article ou la source |
| Calculs | Dans le fichier : 185 parlementaires (un cinquième de 577 + 348) ; les dates `computed`. Dans l'app : les remboursements au plus (4,75 % et 47,5 % des plafonds), et un dixième des inscrits des listes principales et consulaires de `registeredVoters` (4 981 342 avec le fichier de 2026), arrondi au-dessus, chacun dit « calcul » |
| Règles de saisie | Jamais une valeur du moteur : les dates et seuils des textes, jamais les semaines du jeu ni ses réglages. La page cite la loi, pas le guide de la CNCCFP, sur le seuil de 5 % |
| Première édition | À remplir à la publication |

À actualiser : au décret de convocation (#370 de l'app : les dates de 2027 passent de « annoncée » et « calculée » à « fixée »), le 01/01/2027 au plus tard (la voie électronique des parrainages entre dans l'art. 3, I : la note 4 est à réécrire), à la recommandation de l'Arcom pour 2027 (non parue au 15/11/2026), et à toute modification des textes cités.

## Les règles et leurs dates

| Ligne | Article | Chiffre ou date | Vérification |
| --- | --- | --- | --- |
| `sponsorships` | Loi n° 62-1292, art. 3, I | 500 | Légifrance (16/11/2026) |
| `departments` | Art. 3, I | 30 | Légifrance (16/11/2026), phrase entière |
| `filing` | Art. 3, I | 12/03/2027 à 18 h (calcul : sixième vendredi avant le 18/04/2027 : 16/04, 09/04, 02/04, 26/03, 19/03, 12/03) | Légifrance ; décision n° 2022-198 PDR, note 3 |
| `sponsorsPublished` | Art. 3, I | au plus tard le 10/04/2027 (18/04 − 8 jours) | Légifrance (16/11/2026) |
| `candidatesList` | Art. 3, I | au plus tard le 26/03/2027 (quatrième vendredi) | Légifrance (16/11/2026) |
| `fundingPeriod` | Art. 3, II | 01/04/2026 (l'année qui précède le 01/04/2027) | Légifrance ; guide de la CNCCFP, 1.1 (« débute le 1er avril 2026 ») |
| `firstRoundCap` | Art. 3, II | 16 851 000 € (CNCCFP, guide, p. 5 du PDF), 13,7 M€ dans la loi | Légifrance ; guide ; 13,7 × 1,23 = 16,851 (coefficient du décret n° 2009-1730, réponse ministérielle de 2010) |
| `finalistCap` | Art. 3, II | 22 509 000 € (CNCCFP), 18,3 M€ dans la loi | idem ; 18,3 × 1,23 = 22,509 |
| `capFreeze` | Code électoral, art. L. 52-11 | — | codes.droit.org, mise à jour du 2026-07-01 |
| `spendingOverrun` | Art. 3, II | — | Légifrance (16/11/2026) |
| `advance` | Art. 3, V | 200 000 € | Légifrance (16/11/2026) ; guide de la CNCCFP |
| `refundBase` | Art. 3, V | 4,75 % | Légifrance ; guide, 1.5 |
| `refundOver5` | Art. 3, V | 47,5 % au-delà de 5 % | Légifrance (« plus de 5 % ») ; réponse ministérielle de 2010 (« plus de 5 % ») |
| `convocation` | Art. 1 bis | au plus tard le 07/02/2027 (18/04 − 70 jours) | Légifrance (16/11/2026) |
| `commercialAds` | Code électoral, art. L. 52-1 | 01/10/2026 (six mois avant le 01/04/2027) | codes.droit.org (« d'une élection ») |
| `officialCampaign` | Code électoral, art. L. 47 A | 05/04/2027 (deuxième lundi avant le 18/04) | codes.droit.org |
| `secondRound` | Constitution, art. 7 | 02/05/2027, annoncée | miroir du Conseil constitutionnel ; Service-Public |
| `equity` | Art. 3, I bis | dès la liste, au plus tard le 26/03/2027 | Légifrance (16/11/2026) et recueil du Sénat (voir plus bas) |
| `equality` | Art. 3, I bis | 05/04/2027 | idem |
| `pollingSilence` | Loi n° 77-808, art. 11 | 17/04/2027 à 0 h | Commission des sondages ; Légifrance (16/11/2026) |
| `earlierPolls` | Loi n° 77-808, art. 11 | — | Commission des sondages |
| `votingHours` | Art. 3, II bis | — | Légifrance (16/11/2026) et recueil du Sénat |
| `results` | Code électoral, art. L. 52-2, II (la République, circonscription unique) | — | codes.droit.org ; seconde vérification du 16/11/2026 |
| `deputies`, `senators` | Constitution, art. 24 | 577, 348 | miroir du Conseil constitutionnel |
| `ripMembers` | Constitution, art. 11 | 185 (calcul) | miroir du Conseil constitutionnel ; 925 / 5 |
| `ripVoters` | Constitution, art. 11 | calculé dans l'app sur `registeredVoters` | miroir du Conseil constitutionnel |
| `rip2019` | Décision n° 2019-1 RIP, cons. 11 | 4 717 396 | miroir du Conseil constitutionnel (FR et EN) |

Dates de 2027 : premier tour le 18/04/2027, second tour le 02/05/2027 (les samedis 17/04 et 01/05 en Guadeloupe, Martinique, Guyane, à Saint-Pierre-et-Miquelon, Saint-Barthélemy, Saint-Martin et en Polynésie française), annoncées par le Gouvernement au Conseil des ministres du 01/07/2026 (Service-Public, 02/07/2026 : « ont été fixées par le Gouvernement ») ; le décret de convocation n'est pas paru au 16/11/2026. Le compte rendu du Conseil des ministres sur elysee.fr contient deux coquilles (rapport de recherche) : il n'est pas cité.

## Lecture des textes

Légifrance renvoie un défi Cloudflare aux scripts : la page de la loi n° 62-1292 a été lue le 16/11/2026 par WebFetch (« En vigueur au 16/11/2026 »), qui ne rend que des extraits de moins de 125 caractères. Chaque citation de cette loi a été recoupée mot à mot :
- avec le texte entier du « Recueil des textes relatifs aux pouvoirs publics » du Sénat, `https://www.senat.fr/reglement/pouvoirs_publics16.html` (lu le 16/11/2026 ; version antérieure à 2021 : il nomme encore le CSA, publie la liste « quinze jours au moins » avant le scrutin et donne une avance de 153 000 €). Les phrases inchangées depuis sont identiques mot à mot aux extraits de Légifrance (seuil de 500, trente départements et un dixième, dix-huit heures, publication des noms, plafonds de 13,7 et 18,3 M€, dépassement, heures du vote, 4,75 % et 47,5 %) ;
- pour les passages modifiés depuis, avec les seuls extraits de Légifrance du 16/11/2026 : « La liste des candidats est préalablement établie par le Conseil constitutionnel » (et non « Cette liste est », version du Sénat), « Au plus tard le quatrième vendredi », « une somme de 200 000 euros », « l'Autorité de régulation de la communication audiovisuelle et numérique », l'art. 1 bis.
- Temps de parole (art. 3, I bis) : la double vérification n'avait pas de citation mot à mot (l'outil paraphrasait). Le 16/11/2026, Légifrance en extraits (« A compter de la publication de la liste des candidats et jusqu'à la veille du début de la campagne, » ; « les éditeurs de services de communication audiovisuelle respectent, sous le contrôle de l'Autorité » ; « de régulation de la communication audiovisuelle et numérique, le principe d'égalité ») et le recueil du Sénat (texte de 2016, mêmes mots, « Conseil supérieur de l'audiovisuel » en place de l'Arcom) concordent. La citation s'arrête à « le principe d'équité […] » et « le principe d'égalité […] ».
- Fin de la phrase du remboursement (« Elle ne peut excéder le montant des dépenses du candidat retracées dans son compte de campagne. ») et fin de la phrase du mandataire (« les fonds destinés au financement de la campagne ») : recueil du Sénat seulement ; le guide de la CNCCFP (1.5) dit la même règle du remboursement.
- Code électoral : copie de codes.droit.org, « mise à jour du 2026-07-01 », tirée des données de Légifrance, d'où la version du 01/07/2026 de la source (1). L. 52-1 se cite avec « d'une élection » (le guide de la CNCCFP écrit « de l'élection »).
- Loi n° 77-808 : texte de la Commission des sondages, recoupé par Légifrance le 16/11/2026 (« En vigueur au 16 novembre 2026 », art. 11 modifié par la loi n° 2016-508, art. 6).

## « À savoir »

1. Les plafonds de la loi (13,7 et 18,3 M€) actualisés par décret puis gelés depuis 2012, 16,851 et 22,509 M€ appliqués par la CNCCFP, 23 % de plus. Sources : loi n° 62-1292, art. 3, II ; code électoral, art. L. 52-11 ; guide de la CNCCFP 2026-2027, 1.2 et p. 5 ; réponse ministérielle n° 81571 (JO AN du 14/12/2010, coefficient de 1,23, décret n° 2009-1730) ; calcul 16,851 / 13,7 = 22,509 / 18,3 = 1,23.
2. 47,5 % au-delà de 5 %, 4,75 % à 5 % tout juste et en dessous ; jamais plus que les dépenses ni que l'apport personnel. Sources : art. 3, V (« plus de 5 % ») ; guide de la CNCCFP, 1.5 (le plus petit des dépenses remboursables, de l'apport personnel et du maximum légal). Le guide écrit « au moins 5 % » pour les 47,5 % et « moins de 5 % » pour les 4,75 % : à 5 % tout juste, seule la loi tranche.
3. Les dates annoncées le 01/07/2026, le décret de convocation à venir, les autres dates calculées. Sources : Service-Public, 02/07/2026 ; art. 1 bis.
4. La voie électronique au plus tard au 01/01/2027, le texte en vigueur au 16/11/2026 ne prévoyant que la voie postale, le décret d'application « en attente », sa publication « envisagée en mars 2026 » (date dépassée). Sources : loi organique n° 2021-335 (texte adopté n° 575 de l'AN, première lecture, « au plus tard à compter du 1er janvier 2027 … « , ou par voie électronique » ») ; baromètre de l'application des lois de l'Assemblée nationale, `https://www.assemblee-nationale.fr/dyn/taux-application-lois/DLR5L15N41207` (« En attente d'application ») ; Légifrance (art. 3, I : « par voie postale »). À réécrire en janvier 2027.

## « Ce qu'on entend »

1. « Sous 5 % des voix, l'État ne rembourse rien » : réfuté par l'art. 3, V (4,75 % du plafond, 800 422,50 € au plus au premier tour, calcul de la page ; avance de 200 000 €), le remboursement venant après l'approbation du compte (art. 3, V).
2. « Le même temps de parole pour tous pendant toute la campagne » : réfuté par l'art. 3, I bis (équité, puis égalité à l'ouverture de la campagne officielle, le 05/04/2027, L. 47 A, calcul).
3. « Une candidature peut dépenser autant qu'elle veut » : réfuté par les plafonds (CNCCFP) et le reversement du dépassement (art. 3, II).
4. « Les sondages interdits toute la dernière semaine » : réfuté par l'art. 11 de la loi n° 77-808 (la veille et le jour du vote ; les sondages antérieurs restent diffusables).

## Double vérification

Faite le 15/11/2026 : double vérification sur le web par un agent Claude (modèle Sonnet), 15/11/2026, sans passer par le rapport de recherche. Extrait de son rapport (`check-gap-g1.md`, § 1) :

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Seuil du remboursement de 47,5 % | « plus de 5 % » | « ayant obtenu plus de 5 % du total des suffrages exprimés au premier tour » ; 4,75 % sinon ; 2010 : « plus de 5 % » | Légifrance (WebFetch) ; `https://questions.assemblee-nationale.fr/dyn/13/questions/QANR5L13QE81571.pdf` | Conforme |
| Guide de la CNCCFP sur le seuil | — | « au moins 5 % » pour le 47,5 %, « moins de 5 % » pour le 4,75 % (p. 9 du PDF) | guide de la CNCCFP | Conforme (incohérence du guide à 5 % tout juste : la page cite la loi) |
| Avance | 200 000 € | « une somme de 200 000 euros » | Légifrance ; guide | Conforme |
| Taux | 4,75 % ; 47,5 % | idem (guide 1.5) | guide | Conforme |
| Maxima calculés | 800 422,50 ; 8 004 225 ; 10 691 775 € | 16,851 M × 4,75 % ; × 47,5 % ; 22,509 M × 47,5 % | calcul | Conforme |
| Plafonds | 16 851 000 ; 22 509 000 € | « 16,851 millions d'euros … 22,509 millions » ; loi : 13,7 et 18,3 ; coefficient 1,23 | guide ; Légifrance ; QE 2010 | Conforme |
| Gel des plafonds | L. 52-11 | « Il n'est pas procédé à une telle actualisation à compter de 2012 … est nul » | `https://codes.droit.org/PDF/Code%20%C3%A9lectoral.pdf` | Conforme |
| Dépôt des parrainages | 12/03/2027, 18 h | « sixième vendredi précédant le premier tour de scrutin à dix-huit heures » | Légifrance ; calcul | Conforme |
| Liste des candidats | au plus tard le 26/03/2027 | « Au plus tard le quatrième vendredi » | Légifrance ; calcul | Conforme |
| Publication des parrainages | au plus tard le 10/04/2027 | « au moins deux fois par semaine » ; « Huit jours au moins avant le premier tour » | Légifrance ; calcul | Conforme |
| Décret de convocation | au plus tard le 07/02/2027 | « publié au moins dix semaines avant la date du premier tour de scrutin » | Légifrance ; calcul | Conforme |
| Temps de parole | équité puis égalité | « principe d'équité », « principe d'égalité » | Légifrance (paraphrase de l'outil) | Conforme (citation relue le 16/11/2026, section « Lecture des textes ») |
| Campagne officielle | 05/04/2027 | « deuxième lundi qui précède la date du scrutin » | codes.droit.org ; calcul | Conforme |
| L. 52-1 | 01/10/2026 | « Pendant les six mois précédant le premier jour du mois d'une élection … est interdite » | codes.droit.org | Conforme (« d'une », le code) |
| Silence des sondages | samedi 0 h, fin à la fermeture du dernier bureau de métropole | mot pour mot (version 2016-508) | `https://www.commission-des-sondages.fr/lois/lois.htm` | Conforme |
| Résultats, L. 52-2 | — | mot pour mot | codes.droit.org | Conforme |
| Heures du vote | 8 h à 19 h, 20 h au plus tard | confirmé | Légifrance | Conforme |
| Voie électronique | au plus tard le 01/01/2027, sans décret | texte adopté n° 575 (première lecture) ; baromètre : « En attente d'application » | `https://www.assemblee-nationale.fr/dyn/15/textes/l15t0575_texte-adopte-seance.pdf` | Écart expliqué (numéro II ou III non vérifié sur le texte final ; preuve négative partielle) |
| Députés, sénateurs | 577 ; 348 | « ne peut excéder cinq cent soixante-dix-sept » ; « … trois cent quarante-huit » | miroir officiel du Conseil constitutionnel | Conforme |
| RIP | un cinquième, un dixième | mot pour mot | idem | Conforme |
| Décision n° 2019-1 RIP | 4 717 396 | « … à recueillir est de 4 717 396. » | `https://www.conseil-constitutionnel.fr/decision/2019/20191RIP.htm` (miroir) | Conforme |
| Second tour | quatorzième jour | « le quatorzième jour suivant, à un second tour » | miroir | Conforme |
| Dates de 2027 | 18/04, 02/05 ; 17/04 et 01/05 outre-mer | mot pour mot ; publié le 02/07/2026 | `https://www.service-public.gouv.fr/particuliers/actualites/A15053` | Conforme |
| 185 ; un dixième des inscrits | 185 ; calculé dans l'app | 925 / 5 = 185 | calcul | Conforme ; le dixième n'est plus saisi dans le fichier |
| 100 parrainages de 1965 à 1974 | non saisi | « initialement 100 » (réponse ministérielle de 2025), années non précisées | QE 5709 | Non trouvé (série laissée de côté) |

**Conclusion.** Aucun écart non expliqué : le seuil de 5 % est celui de la loi, les dates de 2027 sont calculées ou annoncées, la voie électronique reste à revoir en janvier 2027.

**Seconde vérification, le 16/11/2026** : double vérification sur le web par un agent Claude (modèle Sonnet), 16/11/2026, des 28 citations, des chiffres, des dates et des calculs du fichier, des notes et des « Ce qu'on entend » : tous conformes, sauf deux points, corrigés le jour même.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| `results` (L. 52-2) | le I : « En cas d'élections générales, aucun résultat … en métropole, avant la fermeture du dernier bureau de vote sur le territoire métropolitain. » | Citation exacte, mais du I. Pour la présidentielle, circonscription unique, le II s'applique : « Par dérogation au premier alinéa du I, lorsque la République forme une circonscription unique, aucun résultat d'élection, partiel ou définitif, ne peut être communiqué au public par quelque moyen que ce soit avant la fermeture du dernier bureau de vote sur le territoire métropolitain. » | `https://codes.droit.org/PDF/Code%20%C3%A9lectoral.pdf` (mise à jour du 2026-07-01) | Écart expliqué : la ligne cite désormais le II (« Code électoral, art. L. 52-2, II »), relu mot à mot dans la même copie |
| Note 4 (voie électronique) | « en attente » | Baromètre de l'Assemblée : « En attente d'application — Publication éventuelle envisagée en mars 2026 », date dépassée | `https://www.assemblee-nationale.fr/dyn/taux-application-lois/DLR5L15N41207` | Conforme ; la note ajoute « publication envisagée en mars 2026 » (309 caractères en français) |

**Vérifications ajoutées le 16/11/2026** (au-delà de la recherche, à recouper) :
- Légifrance par WebFetch, `https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000684037` (« En vigueur au 16/11/2026 ») : les extraits cités à la section « Lecture des textes » (tête de l'art. 3, I ; la phrase des trente départements en entier ; la publication des noms ; l'art. 1 bis ; les deux paragraphes de l'art. 3, I bis ; le dépassement ; l'art. 3, II bis ; l'avance et les taux de l'art. 3, V).
- Légifrance par WebFetch, `https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000522846` : art. 11 en vigueur au 16/11/2026, mêmes mots que la Commission des sondages.
- Recueil du Sénat, `https://www.senat.fr/reglement/pouvoirs_publics16.html` (texte entier, version antérieure à 2021).
- Licence de Légifrance : `https://www.legifrance.gouv.fr/contenu/pied-de-page/open-data-et-api` (« Sauf mention contraire, tous les contenus de ce site sont sous licence etalab-2.0 »).
- Décision n° 2019-1 RIP en anglais : `https://webview-ccfr.sites.prod.conseilconstitutionnel.aquaray.com/en/decision/2019/20191RIP.htm` (« 4,717,396 »), miroir de `https://www.conseil-constitutionnel.fr/en/decision/2019/20191RIP.htm`.
- Non trouvé : une copie mot à mot du texte en vigueur de l'art. 3 en entier (Légifrance n'en rend que des extraits) ; si une autre proposition de référendum d'initiative partagée a reçu un nombre de soutiens après 2019 (la page ne dit pas « le seul »).

**Pages consultées** : celles du rapport de recherche et de sa vérification (15/11/2026), et celles ci-dessus (16/11/2026).

## Mises à jour

- **16/11/2026** (Mitchnsun/moi-president#457) : notes « À savoir » relues (revue d'un joueur, réécriture, recherches et contre-vérification par des agents Claude, modèle Sonnet, validées par le PO) ; notes (← ancien numéro) : 1 ← 3, 2 ← 1 réécrite, 3 ← 2 réécrite, 4 ← 4 corrigée (le décret d'application « en attente », publication « envisagée en mars 2026 », date périmée, retiré) ; sigle développé ; fait ajouté (note 4) : Légifrance, loi n° 62-1292 du 6 novembre 1962, version « En vigueur au 16/11/2026 », art. 3 et Assemblée nationale, question écrite n° 18789, JO du 6 octobre 2026, p. 9301, https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000684037 et https://www.assemblee-nationale.fr/dyn/17/questions/QANR5L17QE18789, seconde vérification : conforme, la loi organique de 2021 de la première phrase n'étant confirmée que par une source secondaire.
- **16/11/2026, seconde vérification** : la règle `results` cite le II de l'art. L. 52-2 (la présidentielle, circonscription unique) au lieu du I ; la note 4 dit la date de publication envisagée par l'Assemblée (mars 2026).

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
