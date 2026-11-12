# `foreignNationalsJustice` · Étrangers et justice (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; des réserves de lecture (parts des mis en cause de seconde main, valeurs lues sur un graphique, texte et figure qui ne s'accordent pas à l'arrondi, récidive au sens large), reprises dans « À savoir », dans les notes des blocs et dans « Ce qu'on entend ». La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `foreignNationalsJustice`, dossier « Sécurité et justice » (`security`), aussi dans « Immigration » (`alsoIn`), page de type comparaison, recherche du 09/11/2026 |
| Données | `briefings/manual/foreignNationalsJustice.json`, saisi à la main le 2026-11-09 depuis une réponse ministérielle publiée au Journal officiel et trois publications du ministère de la Justice (SSER) |
| Sources | 1. Ministère de la Justice, « Références statistiques Justice 2026, fiche 12.2 » (« Le milieu fermé - les personnes écrouées », 15/07/2026), https://www.justice.gouv.fr/sites/default/files/2026-07/RSJ2026%2012_2.pdf, figure 4b ; en tête parce qu'elle donne le chiffre clé (la page nomme le producteur de la première source sous le chiffre clé). 2. Ministère de l'Intérieur, « Réponse à la question écrite n° 9474, Journal officiel du 2 décembre 2025 » (p. 9879, 17e législature), https://www.assemblee-nationale.fr/dyn/17/questions/QANR5L17QE9474.pdf : le ministre y cite les rapports publics du SSMSI, chiffres de seconde main. 3. Ministère de la Justice, « Les chiffres clés de la Justice, édition 2026 » (28/10/2026), https://www.justice.gouv.fr/sites/default/files/2026-10/Chiffres_cles_Justice_2026.pdf, p. 20. 4. Ministère de la Justice, « Infos Rapides Justice n° 37 » (avril 2026), https://www.justice.gouv.fr/sites/default/files/2026-04/Infos_Rapides_Justice_n37.pdf, figure 2. Licence « citation seule » pour les quatre, en français seulement |
| Séries | `foreignIncarceratedShare` : part des étrangers parmi les personnes écrouées, %, mensuelle, « 2026-01 » (1er janvier 2026), 1 point (22,6 ; le chiffre clé). `foreignReleasedShare` : part des étrangers parmi les sortants de prison, %, 2021, 1 point (27,9). `foreignReoffending` : sortants étrangers de nouveau condamnés dans l'année, %, sortants de 2016 et de 2021, 2 points (25,2 ; 31,1). `frenchReoffending` : sortants français, mêmes années (35,2 ; 35,5) |
| Valeurs par catégorie | `suspectsForeignShare` (2024) : homicide 18 %, coups et blessures volontaires sur personne de plus de 15 ans 20 %, violences sexuelles 13 %, vol avec arme 22 %, vol violent sans arme 30 %, cambriolage de logement 38 %. `convictedByNationality` (2025, provisoire) : Français 83 %, étrangers 17 % (437 059 condamnés). `incarceratedByNationality` (1er janvier 2026) : Français 77,4 %, étrangers 22,6 % |
| Chiffre clé | 22,6 % d'étrangers parmi les personnes écrouées, période « 2026-01 » (au 1er janvier 2026), sans tendance (un seul point) |
| Règles | Règles du PO : un « À savoir » lu d'abord (`readFirst`) obligatoire ; aucune comparaison avec la part des étrangers dans la population, ni chiffre ni phrase ; aucune surreprésentation calculée ; une étape par bloc et par vue. Les parts parmi les mis en cause de 2024 viennent d'une réponse ministérielle (seconde main) ; celles des transports en commun (48 % et 80 %) ne sont pas saisies (année de la phrase et de la publication citée en désaccord, périmètre non précisé). Les parts des condamnés sont lues sur un graphique (arrondies, provisoires) : le chiffre clé est celui des écroués, publié avec sa décimale. Pour les écroués, la valeur de la figure (22,6 %) est saisie ; le texte de la fiche écrit 78 % de Français. La récidive des étrangers est saisie pour les sortants de 2016 et de 2021, pour montrer la hausse que la source décrit, à côté de celle des Français |
| Première édition | À remplir à la publication |

## « À savoir »

Le « À savoir » lu d'abord (`readFirst`, dans les textes de l'app, décidé par le PO) : un mis en cause n'est ni poursuivi ni condamné ; les parts des trois étapes ne se comparent pas entre elles ; à chaque étape, étrangers et Français n'ont pas les mêmes âges, sexes ni infractions. Les points du fichier de notes reprennent les précautions écrites par les sources elles-mêmes :

1. Les parts parmi les mis en cause de 2024 sont de seconde main : le ministre de l'Intérieur les cite dans une réponse publiée au Journal officiel, d'après les rapports publics du SSMSI. Seules les affaires élucidées comptent. Le bilan du SSMSI pour 2025, plus récent, n'a pas pu être lu. Source : réponse à la question écrite n° 9474 (« Ces rapports, publics, font par exemple apparaître qu'en 2024 les étrangers ont représenté ... ») ; bilan 2025 du SSMSI inaccessible (403).
2. Le ministère de l'Intérieur écrit que le SSMSI peut fournir, pour une agglomération ou un département, des données brutes « et difficilement interprétables » sur la part des étrangers dans la délinquance. Source : la même réponse (« ...le SSMSI peut fournir des données brutes - et difficilement interprétables - sur la part des étrangers dans la délinquance de telle ou telle agglomération ou d'un département »). La phrase vise les données locales : la note le dit, sans l'étendre aux parts nationales.
3. Les condamnations comptent aussi les infractions à la législation sur les étrangers. Les écroués comprennent des prévenus en attente de jugement (22 %) et des condamnés non détenus ; la fiche du ministère de la Justice écrit 78 % de Français dans son texte et 77,4 % dans sa figure. Source : précaution de lecture du fichier vérifié pour les condamnés (champ des Chiffres clés 2026 : « Crimes, délits, contraventions de 5e classe », toutes infractions comprises) ; fiche 12.2 (« Les personnes écrouées sont très majoritairement de nationalité française (78 %). » ; figure 4b : « Français 77,4 % ... Étranger 22,6 % »). Le nombre de condamnations pour infraction à la législation sur les étrangers (environ 2 300 par an) vient de l'Infostat n° 207, qui n'est pas une source de la page : il n'est pas cité.
4. Selon le ministère de la Justice, la récidive des sortants est entendue au sens large : toute nouvelle condamnation en France, pas forcément pour les mêmes faits. Chez les étrangers, le taux à un an passe de 25,2 % (sortants de 2016) à 31,1 % (2021), une « tendance à la hausse » selon la source. Source : Infos Rapides Justice n° 37 (« La tendance à la hausse se confirme également pour les personnes de nationalité étrangère avec un taux de récidive à un an de 31,1 % pour les sortants en 2021 »).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

L'affirmation est dans `briefings/notes/foreignNationalsJustice.json` (clé `claims`, français et anglais), reprise de l'affirmation relue du fichier vérifié. Source de chaque chiffre de la réponse :

1. « On entend que les étrangers commettent la plupart des délits. » De 13 % (violences sexuelles) à 38 % (cambriolages de logement) des mis en cause en 2024, pour les six infractions citées : réponse à la question écrite n° 9474. 437 059 condamnés, 83 % et 17 % (2025, provisoire) : Chiffres clés 2026, p. 20. 22,6 % des écroués au 1er janvier 2026 : fiche 12.2, figure 4b. La dernière phrase de la réponse du fichier vérifié (« Aucune de ces parts n'est rapportée à la population. ») est retirée, selon la règle du PO : aucune phrase ne rapporte ces parts à la population.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web : chaque source rouverte (PDF passés à `pdftotext`), d'après le rapport `verify-securite.md`. Les producteurs sont officiels (ministère de l'Intérieur, ministère de la Justice).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, écroués | 22,6 % (1er janvier 2026) | Figure 4b : « Français 77,4 % ... Étranger 22,6 % » ; texte : « (78 %) » | fiche 12.2 (URL de la source 1) | Conforme, avec réserve : texte et figure en désaccord à l'arrondi ; prévenus (22 %) et condamnés non détenus compris |
| Mis en cause, par infraction | 18 / 20 / 13 / 22 / 30 / 38 % (2024) | Phrase de la réponse, mot pour mot (« ...18 % des mis en cause pour homicide, 20 % ... coups et blessures volontaires sur personne de plus de 15 ans, 13 % ... violences sexuelles, 22 % ... vol avec arme, 30 % ... vol violent sans arme, 38 % ... cambriolage de logement ») | réponse à la question écrite n° 9474 (URL de la source 2) | Conforme, avec réserve : seconde main ; bilan 2025 du SSMSI non ouvert ; l'indicateur des coups et blessures a été remplacé en juillet 2025 |
| Condamnés | 17 % de 437 059 (2025) | Graphique « Nationalité » : Étrangers 17 %, Français 83 % ; « Données provisoires » | Chiffres clés 2026, p. 20 | Conforme, avec réserve : lu sur un graphique, provisoire |
| Sortants étrangers ; récidive à un an | 27,9 % ; 25,2 → 31,1 % (étrangers), 35,2 → 35,5 % (Français) | « ...la part des sortants de nationalité étrangère ... monte à 27,9 % (+ 3,5 points). » ; figure 2 | Infos Rapides Justice n° 37 | Conforme, avec réserve : récidive au sens large ; « tendance à la hausse » chez les étrangers |
| Dates de publication | 2026-07-15, 2025-12-02, 2026-10-28, 2026-04-01 | Fiche 12.2 (juillet 2026) ; JO du 2 décembre 2025 ; PDF créé le 28/10/2026 ; note d'avril 2026 (premier du mois retenu) | URL des sources | Conforme |

**Conclusion.** Aucun chiffre du fichier n'est faux. Les parts portent sur trois étapes qui ne se comparent pas ; celles des mis en cause sont de seconde main et peuvent avoir été remplacées par le bilan 2025 du SSMSI ; aucune n'est rapportée à la population.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus. Les pages de l'Intérieur (bilan 2025 du SSMSI, communiqué sur 2024) étaient inaccessibles (403) et ne servent à aucun chiffre du fichier.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert les documents eux-mêmes.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - citation seule : Ministère de la Justice, Ministère de l'Intérieur (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
