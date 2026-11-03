# `turnoutByAge` · Participation électorale par âge

**Vérifiée le 02/11/2026** : double vérification sur le web, toutes les valeurs conformes (section « Double vérification ») ; les « À savoir » reformulés d'après elle (les sondages, les champs, le regroupement en cinq tranches).

| Champ | Valeur |
| --- | --- |
| Indicateur | `turnoutByAge`, dossier « Électorat » (`electorate`), aussi dans « Institutions », page de type comparaison, ticket #34 de l'app (statut `planned` : les chiffres et la fiche avant la page) |
| Données | `briefings/data/turnoutByAge.json`, écrit par `yarn briefings turnoutByAge` le 2026-11-02 |
| Sources | Insee, « Vingt ans de participation électorale », Insee Première n° 1929, https://www.insee.fr/fr/statistiques/6658143 (anglais, résumé : https://www.insee.fr/en/statistiques/6675143), `ip1929.xlsx`, Figure 5 ; Insee, « Élections présidentielle et législatives de 2022 : seul un tiers des électeurs a voté à tous les tours », Insee Première n° 1928, https://www.insee.fr/fr/statistiques/6658145 (anglais, résumé : https://www.insee.fr/en/statistiques/6674605), `ip1928.xlsx`, Figures 2 et 3 ; les deux parues le 17/11/2022 ; Insee, bilan démographique 2025 (POP3, onglet 2022), pour les poids des cinq tranches ; Licence Ouverte 2.0 |
| Séries | 16 séries annuelles, 2002, 2007, 2012, 2017, 2022 : participation aux deux tours de la présidentielle et des législatives, ensemble et par tranche (18-29, 30-64, 65 ans ou plus), France métropolitaine (IP1929) |
| Valeurs par catégorie | 2022, métropole et DOM (IP1928), 15 tranches d'âge et l'ensemble : vote systématique, intermittent, abstention systématique ; a voté à au moins un tour de la présidentielle, des législatives ; `populationByAge` (POP3 2022) ; `presidentialAtLeastOnceByBand` : 74,2 / 81,2 / 88,9 / 89,2 / 73,8 % dans les cinq tranches du jeu, comme #34 les a calculées |
| Chiffre clé | 77,9 % de votants au 1er tour de la présidentielle 2022 (France métropolitaine), en baisse après 81,2 % en 2017 |
| Règles | Les cinq tranches (18-29, 30-44, 45-59, 60-74, 75 ans ou plus) sont un regroupement du jeu (#150), pas une publication de l'Insee : chaque tranche est la moyenne des tranches de l'IP1928 qu'elle contient, pondérée par leur population de 2022 (décision de #34). Pondérer par les inscrits serait plus juste, mais l'Insee ne publie pas les inscrits par tranche de 5 ans ; la moyenne pondérée par la population ne retombe donc pas exactement sur l'ensemble de 82,6 % |
| Première édition | À remplir à la publication |

## « À savoir »

1. 22 % (Ifop-Fiducial, interrogés le 10 avril de 11 h à 18 h, chiffres redressés sur les résultats) et 46 % (Ipsos Sopra Steria, interrogés du 6 au 9 avril) d'abstention chez les 25-34 ans au 1er tour 2022, lus dans les PDF des sondeurs ; chez les 18-24 ans, les deux s'accordent (41 et 42 %) : la note ne cite que l'écart des 25-34 ans, sans le généraliser.
2. 77,9 % (enquête, métropole) contre 73,69 % officiels (35 923 707 votants sur 48 747 876 inscrits, décision du Conseil constitutionnel n° 2022-195 PDR) ; l'Insee attribue l'écart aux collectivités d'outre-mer, aux Français de l'étranger et aux inscrits non résidents.
3. IP1929 : métropole pour toutes les années, même si l'enquête couvre les DOM depuis 2017 (Mayotte en 2022) ; IP1928 : métropole et DOM, inscrits de nationalité française, majeurs au 10 avril 2022. La date « depuis 2012 » de la page source s1255 n'est pas reprise.
4. 82,6 % ont voté à au moins un tour de la présidentielle, contre 77,9 % au 1er tour ; le regroupement en cinq tranches est dit « calcul du jeu ».

À actualiser : aucune enquête 2027 annoncée par l'Insee (enquête « ponctuelle ou apériodique ») ; présidentielle au printemps 2027.

## Double vérification

Faite le 02/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans relire les deux fichiers XLSX. Son rapport, tel quel :

Date de la consultation : 2026-11-02. Travail fait uniquement à partir du web, sans lire ni les deux XLSX de l'Insee ni aucun fichier de `/home/user`.

### Méthode et limites

- Pages Insee (publications, page source s1255, mentions légales, Insee Première de 2017) : téléchargées en HTML brut avec `curl`, texte et tableaux des figures extraits et relus. Ce sont les tableaux HTML de chaque figure (pas les XLSX). Les résumés renvoyés par l'outil de lecture de pages (petit modèle) ont été recoupés avec ce HTML brut ; quand les deux divergeaient, c'est le HTML brut qui fait foi (voir « Pièges rencontrés »).
- Sondages : PDF des rapports Ipsos et Ifop téléchargés et lus avec `pdftotext`.
- Ministère de l'Intérieur : le site officiel (`resultats-elections.interieur.gouv.fr`, `interieur.gouv.fr`) et `info.gouv.fr` répondent 403 depuis cet environnement, donc je n'ai pas pu lire la page du ministère. Les chiffres officiels viennent de la décision du Conseil constitutionnel (proclamation, mêmes données), de Wikipedia (secondaire) et de rapports de sondeurs qui redressent sur les résultats officiels.
- Le plafond de recherches web de la session a été atteint en cours de travail. Je n'ai donc pas pu chercher l'Insee Première de 2012, ni une annonce de l'Insee sur une enquête 2027 (aucune annonce trouvée sur les pages consultées, voir le sujet 6).
- Les valeurs qui ne viennent que d'un résumé de moteur de recherche (et non de la page elle-même) sont signalées « (résumé de recherche seul) ».

### Sujet 1. IP1929, Figure 5 (inscrits résidant en France métropolitaine)

Page : https://www.insee.fr/fr/statistiques/6658143. La « Figure 5 » du texte se décline en quatre tableaux : 5a (1er tour de la présidentielle), 5b (2d tour), 5c (1er tour des législatives), 5d (2d tour). Colonnes : Année, 18-29 ans, 30-64 ans, 65 ans ou plus, Ensemble. Ci-dessous les valeurs sont dans l'ordre « Ensemble / 18-29 / 30-64 / 65 ou plus ».

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Présidentielle 1er tour 2002 | 73,6 / 65,8 / 75,9 / 73,3 | 73,6 / 65,8 / 75,9 / 73,3 | https://www.insee.fr/fr/statistiques/6658143 (Fig. 5a, HTML brut) | Conforme |
| Présidentielle 1er tour 2007 | 86,2 / 82,1 / 88,9 / 82,3 | 86,2 / 82,1 / 88,9 / 82,3 | idem (Fig. 5a) | Conforme |
| Présidentielle 1er tour 2017 | 81,2 / 71,4 / 85,7 / 78,3 | 81,2 / 71,4 / 85,7 / 78,3 | idem (Fig. 5a) | Conforme |
| Présidentielle 1er tour 2022 | 77,9 / 67,2 / 81,7 / 77,0 | 77,9 / 67,2 / 81,7 / 77,0 | idem (Fig. 5a) | Conforme |
| Présidentielle 2d tour 2022 | 75,5 / 63,1 / 78,8 / 76,5 | 75,5 / 63,1 / 78,8 / 76,5 | idem (Fig. 5b) | Conforme |
| Législatives 1er tour 2022 | 50,6 / 27,9 / 52,0 / 61,0 | 50,6 / 27,9 / 52,0 / 61,0 | idem (Fig. 5c) | Conforme |
| Législatives 2d tour 2022 | 48,5 / 27,5 / 49,1 / 59,1 | 48,5 / 27,5 / 49,1 / 59,1 | idem (Fig. 5d) | Conforme |
| Phrase « Lecture » | « en 2022, 67,2 % des inscrits ayant entre 18 et 29 ans ont voté au premier tour de l'élection présidentielle » | Identique mot pour mot (Fig. 5a, avec le point final) | idem | Conforme |
| Champ | inscrits résidant en France métropolitaine | « personnes inscrites sur les listes électorales et résidant en France métropolitaine. » (Fig. 5a à 5d) | idem | Conforme |
| Chiffre clé 77,9 % en 2022, contre 81,2 % en 2017 | 77,9 et 81,2 | 77,9 et 81,2 dans le tableau de la Figure 2 (ligne « Présidentielle - 1er tour ») et dans la colonne Ensemble de la Fig. 5a. Le texte dit seulement « La participation à la présidentielle a baissé en 2022 (de 3 points environ, au premier comme au second tour) » : il n'y a pas d'encadré « chiffres clés » sur la page. Écart réel : 3,3 points | idem | Conforme (valeurs) ; voir la remarque |
| Recoupement avec le texte de l'étude | (non fourni) | « 67 % des 18-29 ans contre 77 % des 65 ans ou plus, soit 10 points » ; « seuls 28 % des moins de 30 ans [...] 59 % des 65 ans ou plus, soit 31 points » ; 2002 : « 66 % contre 73 % » (7 points) et « 45 % contre 70 % » (25 points). Tous cohérents avec les tableaux | idem ; résumé anglais : https://www.insee.fr/en/statistiques/6675143 | Conforme |
| Titre | « Vingt ans de participation électorale » | Titre complet : « Vingt ans de participation électorale : en 2022, les écarts selon l'âge et le diplôme continuent de se creuser » (Insee Première n° 1929, novembre 2022, Élisabeth Algava et Kilian Bloch) | idem | Conforme (titre raccourci) |

Remarques sur le sujet 1 :
- L'année 2012 existe dans les tableaux et n'est pas dans le fichier : 1er tour de la présidentielle 2012 = 82,2 / 73,8 / 86,4 / 78,6 (Fig. 5a). Si l'absence est voulue, rien à corriger.
- Aucune autre source indépendante ne donne les participations au 1er tour par tranche d'âge de ces années. Les Insee Première de 2017 (n° 1670 et n° 1671) ne contiennent pas de tableau « participation par tour selon l'âge » ; leur Figure 1 (vote systématique 47,6 % en 2002 et 35,9 % en 2017) est cohérente avec la Figure 1 de l'IP1929. Pour la série par âge, la seule source web est donc l'IP1929 elle-même.
- Note 1 de la Figure 2 de l'IP1929 : la ligne « Législatives - 2d tour » s'entend « en dehors des situations où le député a été élu au premier tour ». Utile si le kit décrit le 2d tour des législatives.
- Les valeurs sont des estimations d'enquête arrondies à 0,1 point : l'enquête porte sur un échantillon, pas sur un décompte exhaustif (aucun intervalle de confiance n'est publié sur la page).

### Sujet 2. IP1928, Figure 2 (comportements de vote par âge)

Page : https://www.insee.fr/fr/statistiques/6658145 (Kilian Bloch, Insee Première n° 1928, novembre 2022). Champ de la Figure 2 : « inscrits sur les listes électorales en France (métropole ou DOM) et résidant en France en 2020 (2021 pour Mayotte) ; champ différent de celui du ministère de l'Intérieur, voir Sources ».

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Ensemble : vote systématique / intermittent / abstention systématique | 36,4 / 47,3 / 16,3 | 36,4 / 47,3 / 16,3 (ligne « Ensemble », total 100,0) | https://www.insee.fr/fr/statistiques/6658145 (Fig. 2, HTML brut) | Conforme |
| 18-24 ans | 16,4 / 59,8 / 23,8 | 16,4 / 59,8 / 23,8 | idem | Conforme |
| 30-34 ans | 19,8 / 57,2 / 22,9 | 19,8 / 57,2 / 22,9 (la ligne somme 99,9 : arrondi de l'Insee) | idem | Conforme |
| 75-79 ans | 53,4 / 33,4 / 13,2 | 53,4 / 33,4 / 13,2 | idem | Conforme |
| 90 ans ou plus | 21,0 / 23,5 / 55,6 | 21,0 / 23,5 / 55,6 (la ligne somme 100,1 : arrondi de l'Insee) | idem | Conforme |
| Phrase « Lecture » | « 19,8 % des 30-34 ans ont voté systématiquement » | « 19,8 % des 30-34 ans ont voté systématiquement à chaque tour des élections. » | idem | Conforme |
| Titre | « seul un tiers des électeurs a voté à tous les tours » | Titre exact : « Élections présidentielle et législatives de 2022 : seul un tiers des électeurs a voté à tous les tours ». Le chiffre est 36,4 % (texte : 36 %), donc « un tiers » est un arrondi à la baisse de l'Insee. Version anglaise : « only one third of registered voters voted in all rounds » | idem ; https://www.insee.fr/en/statistiques/6674605 | Conforme |
| Champ | inscrits en France (métropole ou DOM), résidant en France en 2020 (2021 Mayotte) | Texte identique. Section Sources : échantillon de personnes « résidant en France (métropole ou DOM) en 2020 (2021 pour Mayotte), majeures le 10 avril 2022, de nationalité française, inscrites sur les listes électorales en France et en capacité de voter » ; 34 000 inscrits ; échantillon représentatif par région sauf Guyane et Mayotte | idem | Conforme (précisions à reprendre dans la note 3) |

Recoupement du texte : « 24 % des 18-34 ans » d'abstention systématique, « 60 % des 18-24 ans » intermittents contre « 24 % des 90 ans ou plus » (23,5), vote systématique « majoritaire parmi les 70-79 ans » (52,8 et 53,4) : cohérents avec le tableau.

Recoupement avec l'autre publication (champ métropole seule, IP1929 Figure 3, 2022, systématique / intermittent / abstention) : 18-24 ans 16,7 / 60,3 / 23,0 ; 30-34 ans 19,9 / 57,6 / 22,5 ; 75-79 ans 54,1 / 33,2 / 12,7 ; 90 ans ou plus 21,4 / 23,3 / 55,3. Les écarts avec l'IP1928 (métropole et DOM) sont de 0,8 point au plus : c'est l'effet du champ, pas une erreur. Pour l'ensemble : IP1929 Fig. 1 (métropole) 37,0 / 47,2 / 15,8, contre 36,4 / 47,3 / 16,3 (IP1928).

### Sujet 3. IP1928, Figure 3 (au moins un tour)

Page : https://www.insee.fr/fr/statistiques/6658145 (Fig. 3, mêmes champ et source que la Figure 2).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Au moins un tour de la présidentielle, ensemble | 82,6 | 82,6 (texte : « 83 % des inscrits ») | https://www.insee.fr/fr/statistiques/6658145 | Conforme |
| Idem, 18-24 ans | 74,8 | 74,8 | idem | Conforme |
| Idem, 75-79 ans | 85,6 | 85,6 | idem | Conforme |
| Idem, 90 ans ou plus | 43,2 | 43,2 | idem | Conforme |
| Au moins un tour des législatives, ensemble | 58,0 | 58,0 (texte : « 58 % pour les élections législatives ») | idem | Conforme |
| Idem, 18-24 ans | 34,8 | 34,8 | idem | Conforme |
| Idem, 75-79 ans | 73,6 | 73,6 | idem | Conforme |
| Phrase « Lecture » | « 73,6 % des 75-79 ans ont voté à au moins un tour des élections législatives, contre 34,8 % des 18-24 ans » | « 73,6 % des 75-79 ans ont voté à au moins un tour des élections législatives, contre 34,8 % des 18-24 ans. » | idem | Conforme |

Contrôle de cohérence interne : dans la Figure 1 de l'IP1928, la ligne « Aucun » à la présidentielle totalise 17,4 % (donc 82,6 % ont voté au moins une fois) et la colonne « Aucun » aux législatives totalise 42,0 % (donc 58,0 %). Pour mémoire, 90 ans ou plus aux législatives : 33,3. L'enquête de 2017 (IP1670, champ un peu différent) donnait 85 % et 58 % : https://www.insee.fr/fr/statistiques/3138704.

### Sujet 4. Champ de l'Insee et écart avec le ministère de l'Intérieur (77,9 % contre 73,7 %)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Insee, 1er tour 2022, inscrits résidant en France métropolitaine | 77,9 % | 77,9 % (Fig. 2 et Fig. 5a de l'IP1929) | https://www.insee.fr/fr/statistiques/6658143 | Conforme |
| Ministère de l'Intérieur, 1er tour 2022, France entière | 73,7 % | 73,69 %. La décision du Conseil constitutionnel n° 2022-195 PDR du 13 avril 2022 (art. 1er) donne 48 747 876 inscrits et 35 923 707 votants, soit 73,69 % (calcul de ma part : 73,693 %), 26,31 % d'abstention. Wikipedia donne aussi 48 747 876 inscrits et 73,69 %. La version du 11 avril du rapport Ipsos affiche 73,7 / 26,3 pour l'ensemble (la version du 10 avril : 74 / 26), soit le résultat officiel. Le site du ministère lui-même est resté inaccessible (403) | https://www.conseil-constitutionnel.fr/decision/2022/2022195PDR.htm ; https://blog.landot-avocats.net/2022/04/13/election-presidentielle-voici-les-deux-decisions-du-conseil-constitutionnel-rendues-a-linstant-resultats-du-1er-tour-candidats-presents-au-2nd-tour/ ; https://en.wikipedia.org/wiki/2022_French_presidential_election | Conforme (73,7 est l'arrondi de 73,69) |
| Écart | 4,2 points | 4,2 points (77,9 − 73,69 = 4,21) | calcul | Conforme |
| Raison de l'écart | « champ : inscrits à l'étranger, personnes non retrouvées... » | L'Insee donne lui-même la raison, par champ : « le ministère de l'Intérieur prend en compte les inscrits en France, y compris dans les collectivités d'outre-mer ainsi que les Français inscrits à l'étranger. De plus, il prend en compte l'ensemble des inscrits des régions françaises même si ces inscrits ne résident pas en France. » L'enquête, elle, porte sur des personnes résidant en France, de nationalité française, inscrites en France et « en capacité de voter » ; et l'étude de l'IP1929 se restreint à la métropole. L'IP1670 (2017) précise que le ministère inclut aussi Mayotte et la Nouvelle-Calédonie. Rien n'est dit de « personnes non retrouvées » | https://www.insee.fr/fr/statistiques/6658145 (Sources) ; https://www.insee.fr/fr/statistiques/6658143 (Sources) ; https://www.insee.fr/fr/statistiques/3138704 | Écart expliqué (par le champ, pas par des « non-retrouvés ») |

Ordre de grandeur de la part des Français de l'étranger (calcul de ma part, à titre indicatif) : ils sont « plus d'1,4 million » d'inscrits et leur abstention au 1er tour 2022 est de 64,9 % (page ASFE https://alliancesolidaire.org/2022/04/21/resultats-du-1er-tour-de-lelection-presidentielle-des-francais-de-letranger-quelle-est-lanalyse-des-senateurs-asfe/ ; un résumé de recherche seul, Le Petit Journal, parlait de 1 435 746 inscrits et 504 291 votants, soit 35,12 %, non retrouvé sur la page). En les retirant du total, la participation nationale passerait d'environ 73,7 % à environ 74,8-74,9 %, soit +1,1 à +1,2 point. Le reste de l'écart (environ 3 points) tiendrait à l'exclusion des DOM/COM (participation faible) de la métropole, et aux inscrits qui ne résident pas en France : l'Insee ne publie pas de décomposition, je n'en ai pas trouvé. Par ailleurs, Ifop affiche 74,9 % de participation pour 2022 « redressée sur la base des résultats officiels publiés par le ministère de l'Intérieur lundi 11 avril 2022 » (rapport Ifop-Fiducial, cité au sujet 5), valeur qui coïncide avec mon calcul hors étranger : hypothèse, non confirmée.

Le même écart existe aux autres scrutins, et il s'est creusé : Insee (métropole) contre officiel (France entière, Conseil constitutionnel via Wikipedia, secondaire) : 2002 73,6 contre 71,60 (+2,0) ; 2007 86,2 contre 83,77 (+2,4) ; 2017 81,2 contre 77,77 (+3,4) ; 2022 77,9 contre 73,69 (+4,2). Sources : https://en.wikipedia.org/wiki/2002_French_presidential_election ; https://en.wikipedia.org/wiki/2007_French_presidential_election ; https://en.wikipedia.org/wiki/2017_French_presidential_election. Second tour 2022 : 75,5 (Insee) contre 71,99 (Wikipedia).

Autres précisions du champ : le vote blanc ou nul est un vote avec émargement, donc compté comme une participation (IP1670, 2017) ; l'Insee relève la participation sur les listes d'émargement en préfecture dans les dix jours qui suivent le scrutin, pour un échantillon (34 000 inscrits en 2022, environ 40 000 par édition métropolitaine avant).

### Sujet 5. Sondages de 2022 (notes seulement)

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Ifop, abstention des 25-34 ans, 1er tour 2022 | 22 % | 22 % (votants 78, abstentionnistes 22). Tranches Ifop : 18-24 (59 / 41), 25-34 (78 / 22), 35-49 (73 / 27), 50-64 (78 / 22), 65 ans et plus (78 / 22) ; ensemble 74,9 / 25,1 | Rapport Ifop-Fiducial pour TF1 et LCI, « Sondage jour du vote : Profil des électeurs et clés du scrutin (1er tour) », 10 avril 2022, version détaillée du 11 avril : https://www.ifopgroup.com/wp-content/uploads/2022/04/118997-rapport-jdv-pre22-t1-det-11.04.pdf (le miroir ifop.com a répondu 503 / erreur TLS) | Conforme |
| Ipsos, abstention des 25-34 ans, 1er tour 2022 | 46 % | 46 % (votants 54, abstentionnistes 46). Tranches Ipsos : 18-24 (58 / 42), 25-34 (54 / 46), 35-49 (78 / 22, puis 77 / 23 dans la version du 11 avril), 50-59 (80 / 20), 60-69 (88 / 12), 70 ans et plus (77 / 23) ; ensemble 74 / 26 (version du 10 avril), 73,7 / 26,3 (version du 11 avril) | Rapport Ipsos Sopra Steria, « Sociologie des électorats et profil des abstentionnistes », versions du 10 avril 20 h 30 et du 11 avril 11 h 30 : https://www.ipsos.com/sites/default/files/ct/news/documents/2022-04/Ipsos%20Sopra%20Steria_Sociologie%20des%20e%CC%81lectorats_10%20Avril%2020h30.pdf ; https://www.ipsos.com/sites/default/files/ct/news/documents/2023-10/Ipsos%20Sopra%20Steria_Sociologie%20des%20electorats_11%20Avril%2011h30.pdf ; Wikipedia reprend aussi 58 % et 54 % de participation (18-24, 25-34) | Conforme |
| Tranches d'âge (à noter dans le texte) | non précisées | Les deux sondeurs ont la même tranche 25-34 ans, mais des découpages différents ailleurs : Ipsos 18-24 / 25-34 / 35-49 / 50-59 / 60-69 / 70+ ; Ifop 18-24 / 25-34 / 35-49 / 50-64 / 65+ ; l'Insee 18-29 / 30-64 / 65+ (IP1929) ou des tranches de 5 ans (IP1928) | idem | Complément |
| Méthodes | « déclaratifs » | Ipsos : 4 000 inscrits, internet (panel), quotas, terrain du 6 au 9 avril 2022, donc avant le scrutin (intention). Ifop : 3 784 inscrits, questionnaire auto-administré en ligne, quotas, terrain le 10 avril de 11 h à 18 h, donc le jour du vote, avant la fermeture des bureaux ; les chiffres affichés sont redressés sur les résultats officiels (note du rapport) | idem | Complément |

Constats utiles :
- Pour les 18-24 ans les deux sondeurs s'accordent (41 % et 42 %) ; l'écart de 24 points ne porte que sur les 25-34 ans. À titre de repère, l'Insee mesure 32,8 % d'abstention au 1er tour chez les 18-29 ans (100 − 67,2, métropole), et, chez les 25-34 ans, moins de 27 % de non-votants aux deux tours de la présidentielle (73,3 % des 25-29 ans et 76,1 % des 30-34 ans ont voté au moins une fois, IP1928 Fig. 3). Les deux sondages se situent donc de part et d'autre de la mesure réelle ; les bandes ne sont pas identiques, ce n'est qu'un repère.
- Un résumé de recherche donnait « 42 % des 18-24 ans et 46 % des 25-34 ans » (franceinfo) : confirmé par le PDF Ipsos, pas par la page franceinfo que je n'ai pas ouverte.

### Sujet 6. Dates, prochaine édition, licence

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| Date de publication de l'IP1929 | 17/11/2022 | « Paru le 17/11/2022 » (HTML) | https://www.insee.fr/fr/statistiques/6658143 | Conforme |
| Date de publication de l'IP1928 | 17/11/2022 | « Paru le 17/11/2022 » (HTML) | https://www.insee.fr/fr/statistiques/6658145 | Conforme |
| Date « Paru le » de la page source s1255 | (non fourni) | « Paru le 02/11/2026 » : c'est la date du jour de la consultation, donc une date de page générée, pas une date de données. La dernière mise à jour des métadonnées est le 15/11/2022 (page « Mise à jour des métadonnées »). La page https://www.insee.fr/fr/information/6659405 (« La participation électorale aux élections présidentielle et législatives de 2022 ») porte « Dernière mise à jour le 17/11/2022 » | https://www.insee.fr/fr/metadonnees/source/serie/s1255 ; https://www.insee.fr/fr/metadonnees/source/serie/s1255/maj-metadonnees | Écart expliqué : ne pas citer le 02/11/2026 comme date de l'enquête |
| Prochaines données : présidentielle 2027 | 2027 | Rien d'annoncé par l'Insee : la page s1255 indique « Ponctuelle ou apériodique » (fréquence de diffusion) et aucune échéance. Pour l'élection, Wikipedia (secondaire, sans décret cité) donne le 1er tour le 18 avril 2027 et le 2d le 2 mai 2027. Attention : depuis la dissolution du 9 juin 2024 (législatives anticipées les 30 juin et 7 juillet 2024, Wikipedia), les législatives et la présidentielle ne tombent plus la même année ; le dispositif de l'Insee suppose « ces deux élections ont lieu la même année » (s1255). Je n'ai pas trouvé si l'enquête sera refaite en 2027, ni sur quel champ | https://www.insee.fr/fr/metadonnees/source/serie/s1255/frequence-diffusion ; https://en.wikipedia.org/wiki/2027_French_presidential_election ; https://en.wikipedia.org/wiki/2024_French_legislative_election | Non trouvé (aucune annonce) ; à formuler comme « pas de prochaine édition annoncée » |
| Licence | Licence Ouverte 2.0 | Mentions légales : « Sauf mention contraire, les informations publiques diffusées sur ce site (données, bases de données, publications, fichiers téléchargeables) sont mises à disposition sous la Licence Ouverte / Open Licence version 2.0 (Etalab). » Conditions : mentionner « Source : Insee », la date de dernière mise à jour des données quand elle est connue, ne pas altérer le sens ni induire en erreur. Les pages des deux publications ne portent pas de licence propre | https://www.insee.fr/fr/information/2008466 | Conforme |

### Sujet 7. Versions anglaises

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
|---|---|---|---|---|
| IP1929 en anglais | (non fourni) | Identifiant différent : https://www.insee.fr/en/statistiques/6675143, « Twenty years of electoral participation: in 2022, age and education gaps have continued to widen » (Insee Première n° 1929, Paru le 17/11/2022). Seul le résumé est en anglais : pas de figures, pas de PDF ni de XLSX. Le même identifiant que le français (`/en/statistiques/6658143`) donne 404 | https://www.insee.fr/en/statistiques/6675143 | Trouvé |
| IP1928 en anglais | (non fourni) | https://www.insee.fr/en/statistiques/6674605, « 2022 presidential and legislative elections: only one third of registered voters voted in all rounds » (Paru le 17/11/2022). Résumé seul ; `/en/statistiques/6658145` donne 404 | https://www.insee.fr/en/statistiques/6674605 | Trouvé |
| Source s1255 en anglais | (non fourni) | Même identifiant : https://www.insee.fr/en/metadonnees/source/serie/s1255, « Survey of electoral participation » ; documentation : https://www.insee.fr/en/metadonnees/source/serie/s1255/presentation | https://www.insee.fr/en/metadonnees/source/serie/s1255 | Trouvé |
| Insee Première de 2017 en anglais (pour mémoire) | (non fourni) | IP1671 : https://www.insee.fr/en/statistiques/3181766 ; IP1670 : https://www.insee.fr/en/statistiques/3181763. Versions françaises : https://www.insee.fr/fr/statistiques/3140794 et https://www.insee.fr/fr/statistiques/3138704 | idem | Trouvé |

### Les quatre notes « À savoir »

#### Note 1. « L'Insee mesure la participation réelle, relevée sur les listes d'émargement ; les sondages sont déclaratifs et divergent (22 % et 46 % d'abstention chez les 25-34 ans au 1er tour de 2022) »

Vérifié :
- Insee : participation relevée par des agents de l'Insee qui consultent les listes d'émargement en préfecture « dans les dix jours qui suivent le scrutin, comme tout électeur peut le faire » (IP1928 et IP1929, Sources). Ce n'est pas une déclaration. C'est un relevé sur un échantillon (34 000 inscrits en 2022), pas un décompte exhaustif.
- 22 % (Ifop-Fiducial) et 46 % (Ipsos Sopra Steria), 25-34 ans, 1er tour 2022 : exacts. Précision de méthode : Ipsos a interrogé du 6 au 9 avril, avant le vote ; Ifop le 10 avril de 11 h à 18 h, avec des chiffres redressés sur les résultats officiels. Les deux sont en ligne et par quotas.

Points à corriger ou à préciser :
- « Divergent » est vrai pour les 25-34 ans, pas pour les 18-24 ans (41 % contre 42 %). Mieux vaut le dire pour ne pas laisser croire à une divergence générale.
- « Les sondages » est un peu large : ce sont deux sondages du jour du vote.

Proposition : « L'Insee mesure la participation réelle, relevée sur les listes d'émargement en préfecture ; les sondages sont déclaratifs (questionnaires en ligne par quotas) et peuvent s'écarter beaucoup l'un de l'autre : au 1er tour de 2022, l'abstention des 25-34 ans est de 22 % pour Ifop-Fiducial et de 46 % pour Ipsos Sopra Steria. »

#### Note 2. « L'enquête compte les inscrits résidant en France : 77,9 % au 1er tour de 2022, contre 73,7 % pour le ministère de l'Intérieur »

Vérifié : 77,9 % (Insee, IP1929) et 73,69 % (officiel, Conseil constitutionnel) ; la raison est bien le champ, expliquée par l'Insee.

Points à corriger ou à préciser :
- Le 77,9 % est un chiffre pour la France métropolitaine (champ commun 2002-2022), pas pour « la France » : le dire. L'enquête 2022 couvre aussi les DOM, mais ce n'est pas le champ du 77,9 %.
- Le champ du ministère est plus large : inscrits des collectivités d'outre-mer et Français inscrits à l'étranger, et inscrits qui ne résident pas en France. La formulation « inscrits résidant en France » côté Insee est exacte, mais n'explique pas l'écart sans l'autre moitié.
- L'écart a augmenté d'une édition à l'autre (+2,0 en 2002, +3,4 en 2017, +4,2 en 2022) : ne pas présenter 4,2 points comme un écart « de principe ».

Proposition : « L'enquête de l'Insee ne compte que les inscrits qui résident en France (ici la France métropolitaine) : 77,9 % au 1er tour de 2022, contre 73,7 % pour le ministère de l'Intérieur, dont le champ inclut aussi les inscrits de l'outre-mer et ceux de l'étranger. »

#### Note 3. « Champs : France métropolitaine pour les tours depuis 2002 (IP1929), France métropolitaine et départements d'outre-mer pour les comportements de 2022 (IP1928) »

Vérifié, avec des nuances :
- IP1929 : toutes les figures sont sur « les inscrits résidant en France métropolitaine », y compris 2017 et 2022, alors que l'enquête couvre les DOM depuis 2017 (Guadeloupe, Guyane, Martinique, La Réunion) et Mayotte depuis 2022. L'étude se limite à la métropole « pour comparer les résultats de 2002 à 2022 sur un champ commun » (IP1929, Sources ; IP1671 : « En 2017, pour la première fois »). La note doit donc dire que la restriction à la métropole vaut pour toutes les années, 2017 et 2022 comprises.
- IP1928 : inscrits en France (métropole ou DOM, Mayotte comprise), résidant en France en 2020 (2021 pour Mayotte), de nationalité française, majeurs le 10 avril 2022, en capacité de voter. Représentativité régionale sauf Guyane et Mayotte.
- Incohérence à ne pas reprendre : la page source s1255 écrit que l'enquête a été « élargie aux DROM (hors Mayotte) » « depuis 2012 », alors que les deux Insee Première (n° 1671 de 2017 et n° 1929) disent 2017. La version anglaise de s1255 reprend « since 2012 ». Si le kit cite la date d'extension aux DOM, utiliser 2017 (deux publications concordantes, dont celle de 2017 « pour la première fois ») et signaler l'écart avec s1255.
- Ordre de grandeur de l'effet de champ sur un même scrutin (2022) : vote systématique 37,0 % (métropole, IP1929) contre 36,4 % (métropole et DOM, IP1928), abstention systématique 15,8 % contre 16,3 %.

Proposition : « Participations par tour (2002-2022) : inscrits résidant en France métropolitaine, champ commun à toutes les éditions, y compris 2017 et 2022. Comportements de 2022 (vote systématique, au moins un tour) : inscrits de nationalité française résidant en France métropolitaine ou dans un département d'outre-mer, Mayotte comprise. »

#### Note 4. « La part de ceux qui ont voté au moins une fois en 2022 n'est pas la participation au 1er tour ; dans les cinq tranches adultes de l'Insee, elle est pondérée par la population de 2022 »

Vérifié pour la première partie : « au moins un tour de la présidentielle » vaut 82,6 % (tous les inscrits, métropole et DOM) contre 77,9 % au 1er tour (métropole) et 75,5 % au 2d tour : 4,7 points de plus que le 1er tour pour l'ensemble. Chez les jeunes l'écart est plus grand : 74,8 % (18-24 ans) et 73,3 % (25-29 ans) au moins une fois, contre 67,2 % au 1er tour pour les 18-29 ans (écart d'environ 7 points, avec des champs un peu différents). Un jeune qui s'abstient au 1er tour et vote au 2d compte dans « au moins un tour ».

Points à corriger ou à préciser :
- L'Insee ne publie pas de « cinq tranches adultes » : l'IP1928 donne 15 tranches (18-24, 25-29, ..., 85-89, 90 ou plus, plus l'ensemble) et l'IP1929 trois (18-29, 30-64, 65 ou plus). Le regroupement en cinq tranches est donc un calcul du projet, à dire comme tel dans la note, avec la mention « calcul du projet à partir des tranches de 5 ans de l'Insee ».
- Ce que je n'ai pas pu vérifier : le choix de pondérer par « la population de 2022 ». L'Insee ne publie pas de poids. Les données de l'Insee portent sur les inscrits ; la pondération la plus proche est celle des inscrits par âge, pas celle de la population. Un contrôle simple : la moyenne pondérée des 15 tranches doit retomber sur 82,6 % (présidentielle) et 58,0 % (législatives), valeurs de la ligne « Ensemble ». Un écart notable avec des poids « population » signalerait que ces poids ne reflètent pas la structure par âge des inscrits.
- À dire aussi : « au moins un tour » compte les deux tours de la présidentielle ; ce n'est donc pas une probabilité de voter à un tour donné.

Proposition : « La part des inscrits ayant voté au moins une fois en 2022 (82,6 % à la présidentielle) est plus élevée que la participation au 1er tour (77,9 %) : elle compte aussi ceux qui n'ont voté qu'au 2d tour. Les cinq tranches d'âge sont un calcul du projet à partir des tranches de 5 ans de l'Insee, pondérées par [les inscrits / la population] de 2022. » (choisir selon ce que le calcul fait réellement.)

### Pièges rencontrés pendant la vérification

- Un premier résumé de l'outil de lecture de pages parlait d'un encadré « Chiffres clés » sur l'IP1929 : il n'existe pas dans le HTML brut. Les 77,9 et 81,2 ne sont que dans les tableaux.
- Un résumé de recherche affirmait ne pas trouver « 24 % des 18-34 ans » : la phrase est dans le résumé en tête de l'IP1928 (« 24 % des 18-34 ans »).
- La page s1255 en HTML : « En 1998, le dispositif suit pour la première fois plusieurs élections successives : [...] de 1988 », coquille de l'Insee (1988 attendu), sans effet sur les chiffres.
- Un résumé de recherche (UFE) donnait 77,80 % pour 2017 ; Wikipedia donne 77,77 % : je retiens 77,77 %, non confirmé sur la page du ministère.

### Conclusion

Écarts (à traiter en premier) :
1. Extension de l'enquête aux DOM : la page source s1255 dit « depuis 2012 », les Insee Première n° 1671 et n° 1929 disent 2017 (Mayotte : 2022). Ne pas écrire 2012 dans le kit ; signaler l'incohérence de l'Insee.
2. Note 3 : la formulation est juste mais incomplète. La restriction à la métropole de l'IP1929 couvre aussi 2017 et 2022, et le champ de l'IP1928 comprend la nationalité française, la majorité au 10 avril 2022 et l'absence de représentativité régionale pour la Guyane et Mayotte.
3. Note 4 : « cinq tranches adultes de l'Insee » est inexact (l'Insee en publie 15 ou 3) ; la pondération « par la population de 2022 » n'est pas vérifiable en ligne et un poids « inscrits » serait plus juste ; contrôle possible avec la ligne « Ensemble » (82,6 / 58,0).
4. Note 1 : l'écart de 22 % et 46 % ne vaut que pour les 25-34 ans ; chez les 18-24 ans les sondeurs s'accordent (41 % et 42 %).
5. Date de « Paru le » de la page s1255 (02/11/2026) : date de la page, pas de l'enquête.
6. Prochaine édition « présidentielle 2027 » : non annoncée par l'Insee ; depuis la dissolution de 2024, les deux élections ne tombent plus la même année.

Écarts expliqués : 77,9 % (Insee, métropole) contre 73,69 % (officiel, France entière) : champ, expliqué par l'Insee (outre-mer, Français de l'étranger, inscrits non résidents). Les écarts de 0,1 à 0,8 point entre l'IP1929 (métropole) et l'IP1928 (métropole et DOM) sur les comportements de 2022.

Conforme : toutes les valeurs des sujets 1, 2 et 3 (une comparaison valeur par valeur avec les tableaux HTML des figures 5a à 5d de l'IP1929 et des figures 2 et 3 de l'IP1928), les chiffres des deux sondages (Ifop 22 %, Ipsos 46 %), les dates du 17/11/2022 et la licence (Licence Ouverte 2.0, mention « Source : Insee »).

Non trouvé : annonce d'une enquête Insee en 2027 ; Insee Première de 2012 (plafond de recherche atteint) ; page du ministère de l'Intérieur (403).

### URL consultées (2026-11-02)

Insee (HTML brut) :
- https://www.insee.fr/fr/statistiques/6658143 (IP1929, français)
- https://www.insee.fr/fr/statistiques/6658145 (IP1928, français)
- https://www.insee.fr/en/statistiques/6675143 (IP1929, anglais, résumé)
- https://www.insee.fr/en/statistiques/6674605 (IP1928, anglais, résumé)
- https://www.insee.fr/en/statistiques/6658143 et https://www.insee.fr/en/statistiques/6658145 (404)
- https://www.insee.fr/fr/metadonnees/source/serie/s1255 ; https://www.insee.fr/en/metadonnees/source/serie/s1255 ; sous-pages /presentation, /frequence-diffusion, /maj-metadonnees, /documentation-methodologique, /unite-mesure, /produits (vide), en français ; /presentation en anglais
- https://www.insee.fr/fr/information/6659405 (page « La participation électorale aux élections présidentielle et législatives de 2022 »)
- https://www.insee.fr/fr/information/2008466 (mentions légales, licence)
- https://www.insee.fr/fr/statistiques/3140794 (IP1671, 2017) ; https://www.insee.fr/fr/statistiques/3138704 (IP1670, 2017) ; https://www.insee.fr/en/statistiques/3181766 ; https://www.insee.fr/en/statistiques/3181763

Résultats officiels et contexte :
- https://www.conseil-constitutionnel.fr/decision/2022/2022195PDR.htm (lecture par l'outil de pages)
- https://blog.landot-avocats.net/2022/04/13/election-presidentielle-voici-les-deux-decisions-du-conseil-constitutionnel-rendues-a-linstant-resultats-du-1er-tour-candidats-presents-au-2nd-tour/ (reproduit la décision)
- https://en.wikipedia.org/wiki/2022_French_presidential_election ; https://en.wikipedia.org/wiki/2017_French_presidential_election ; https://en.wikipedia.org/wiki/2007_French_presidential_election ; https://en.wikipedia.org/wiki/2002_French_presidential_election ; https://en.wikipedia.org/wiki/2024_French_legislative_election ; https://en.wikipedia.org/wiki/2027_French_presidential_election
- https://alliancesolidaire.org/2022/04/21/resultats-du-1er-tour-de-lelection-presidentielle-des-francais-de-letranger-quelle-est-lanalyse-des-senateurs-asfe/
- https://lepetitjournal.com/expat-politique/actualites/resultats-premier-tour-legislatives-francais-etranger-339557 (ouverte : ne contient pas les chiffres de la présidentielle)
- Inaccessibles (403) : https://www.resultats-elections.interieur.gouv.fr/presidentielle-2022/FE.html (redirige vers interieur.gouv.fr), https://www.info.gouv.fr/actualite/election-presidentielle-2022-les-resultats-du-premier-tour

Sondages (PDF lus) :
- https://www.ipsos.com/sites/default/files/ct/news/documents/2022-04/Ipsos%20Sopra%20Steria_Sociologie%20des%20e%CC%81lectorats_10%20Avril%2020h30.pdf
- https://www.ipsos.com/sites/default/files/ct/news/documents/2023-10/Ipsos%20Sopra%20Steria_Sociologie%20des%20electorats_11%20Avril%2011h30.pdf
- https://www.ifopgroup.com/wp-content/uploads/2022/04/118997-rapport-jdv-pre22-t1-det-11.04.pdf
- Inaccessibles : https://www.ifop.com/wp-content/uploads/2022/04/118997-Rapport-JDV-PRE22-T1-DET-11.04-1.pdf et https://www.ifop.com/wp-content/uploads/2022/04/118997-rapport-sdv-pre22-t1-21h05.pdf (503 / erreur TLS)

Pages repérées par un résumé de recherche seulement (non ouvertes) : https://www.franceinfo.fr/elections/presidentielle/presidentielle-2022-les-plus-jeunes-ont-vote-jean-luc-melenchon-les-plus-vieux-emmanuel-macron_5075344.html ; https://ufe.org/juridique-fiscalite/presidentielle-2022-1er-tour-resultats/ ; https://recef.org/wp-content/plugins/cpt-bibliotheque/telecharger.php?id=4213 ; https://www.objectifgard.com/actualites/editorial-municipales-2026-a-nimes-quand-les-chiffres-insee-eclairent-sur-le-futur-scrutin-153419.php ; https://catalogue.bnf.fr/ark:/12148/cb471685752.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
