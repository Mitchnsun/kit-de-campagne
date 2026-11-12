# `minimumIncomes` · Travailler ou toucher le RSA ? (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; réserves de lecture reprises dans « À savoir » et « Ce qu'on entend », la première étant que **service-public.gouv.fr ne date pas ses barèmes** : seule la mention « Vérifié le … » de chaque page est lue. La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `minimumIncomes`, dossier « Pouvoir d'achat » (`purchasingPower`), aussi dans « Travail » (`alsoIn: ['work']`), page de type comparaison |
| Données | `briefings/manual/minimumIncomes.json`, saisi à la main le 2026-11-09 depuis quatre fiches de service-public.gouv.fr et trois classeurs du jeu « Minima sociaux, RSA et prime d'activité » de la DREES |
| Sources | DILA, service-public.gouv.fr : « RSA : demandeur de 25 ans et plus » (F19778, vérifié le 01/04/2026), https://www.service-public.gouv.fr/particuliers/vosdroits/F19778 ; « Smic (salaire minimum interprofessionnel de croissance) » (F2300, vérifié le 01/06/2026), https://www.service-public.gouv.fr/particuliers/vosdroits/F2300 ; « Prime d'activité : salarié ou fonctionnaire » (F2882, vérifié le 01/06/2026), https://www.service-public.gouv.fr/particuliers/vosdroits/F2882 ; « Allocation de solidarité aux personnes âgées (Aspa) » (F16871, vérifié le 23/06/2026), https://www.service-public.gouv.fr/particuliers/vosdroits/F16871 ; licence « citation seule », en français seulement. DREES, « Minima sociaux, RSA et prime d'activité » : page du jeu https://data.drees.solidarites-sante.gouv.fr/explore/dataset/336_minima-sociaux-rsa-et-prime-d-activite/ (adresse de la plateforme, non ouverte ici : DREES inaccessible le 09/11/2026) et ses trois classeurs : données nationales par dispositif (tableau 2, `dataUrl` du registre) https://data.drees.solidarites-sante.gouv.fr/api/v2/catalog/datasets/336_minima-sociaux-rsa-et-prime-d-activite/attachments/minima_sociaux_donnees_nationales_par_dispositif_xlsx ; RSA et prime d'activité, données nationales (tableau 3) https://data.drees.solidarites-sante.gouv.fr/api/v2/catalog/datasets/336_minima-sociaux-rsa-et-prime-d-activite/attachments/rsa_et_prime_d_activite_donnees_nationales_xlsx ; données de dépenses par dispositif (tableau 1) https://data.drees.solidarites-sante.gouv.fr/api/v2/catalog/datasets/336_minima-sociaux-rsa-et-prime-d-activite/attachments/minima_sociaux_donnees_de_depenses_par_dispositif_xlsx ; licence non vérifiée, « citation seule » |
| Séries | `rsaSingle` : RSA d'une personne seule, montant forfaitaire maximal, € par mois, « 2026 », 1 point (651,69) ; `allowances` : allocations de minima sociaux versées au 31 décembre, 2024, 1 point (4 418 500, des allocations, pas des personnes) ; `rsaCoveredPeople` : personnes couvertes par le RSA (allocataire, conjoint, personnes à charge), France, 2024, 1 point (3 658 700) |
| Valeurs par catégorie | `singlePerson` (« 2026 », € par mois) : RSA 651,69 ; minimum vieillesse (Aspa, brut) 1 043,59 ; Smic net 1 477,93 (la référence hachurée, « à titre indicatif »). `calculation` (« 2026 », €) : forfait logement d'une personne 78,20 ; forfait de la prime d'activité 638,28. `recipients` (2024, allocataires au 31 décembre, France) : RSA 1 840 200 ; AAH 1 397 800 ; minimum vieillesse (ASV et Aspa) 754 500 ; ASS 265 000. `spending` (2024, Md€, euros constants 2024) : RSA 12,358 ; AAH 13,839 ; minimum vieillesse 4,586 ; ensemble 33,291 (la référence hachurée) |
| Chiffre clé | 651,69 € de RSA par mois au plus pour une personne seule, période « 2026 », sans tendance (un seul point) |
| Règles | Saisie à la main. La période « 2026 » des barèmes est l'année de la vérification des pages, pas une date de barème : le RSA « depuis le 1er avril 2026 » est une déduction (revalorisation annuelle du 1er avril), le Smic net est celui du 1er juin 2026 (confirmé par la circulaire Cnav n° 2026-16 pour le brut), l'Aspa est « depuis le 1er janvier 2026 ». Le ratio Smic net / RSA (2,3 fois) et le RSA avec forfait logement (573,49 €) sont calculés : ils ne sont dans aucune série, seulement dans l'affirmation 1, avec « calculé ». Les allocataires par dispositif ne s'additionnent pas. Le RSA compte 1 840 200 allocataires (le fichier ne dit pas « foyers ») et couvre 3 658 700 personnes : les deux ne sont pas mis côte à côte dans un même graphique. Les allocataires de la prime d'activité (4 812 900), le Smic brut (Cnav) et la réforme de la prime d'activité de 2026 (Cnaf), vérifiés, ne sont pas saisis : ils ne sont pas demandés pour cette page |
| Première édition | À remplir à la publication |

## « À savoir »

1. Service-public.gouv.fr ne date pas ses barèmes du RSA et de la prime d'activité, ni son Smic net : ses pages indiquent seulement la date de leur vérification (1er avril 2026 pour le RSA, 1er juin 2026 pour la prime d'activité et le Smic). Le Smic net y est donné « à titre indicatif ». Source : F19778 (« Vérifié le 01 avril 2026 »), F2882 et F2300 (« Vérifié le 01 juin 2026 » ; « Le montant du Smic net est donné à titre indicatif . »), URL ci-dessus.
2. Le RSA est un montant maximal, versé par foyer et diminué de ses ressources. Si le foyer touche une aide au logement, est hébergé gratuitement ou est propriétaire, un forfait logement est ajouté à ses ressources, donc retiré du RSA. L'Aspa est aussi un montant maximal, brut. Source : F19778 (« Le montant du RSA pour une personne seule est de 651,69 € . » ; tableau du forfait logement : « 1 78,20 € ») ; F16871 (« Le montant maximum attribué par mois est de 1 043,59 € , soit 12 523,14 € maximum par an (montants bruts). » ; allocation différentielle).
3. La condition de 5 ans de titre de séjour permettant de travailler est l'une des conditions de séjour possibles pour un étranger hors Union européenne, pas la seule. Elle vaut pour le RSA comme pour la prime d'activité ; pour le RSA, elle ne s'applique pas aux Algériens. Source : F19778 (« Avoir depuis au moins 5 ans un titre de séjour permettant de travailler en France (cette condition n'est pas applicable aux personnes de nationalité algérienne) ») et F2882 (même condition de 5 ans) ; l'exemption des Algériens n'a été lue que pour le RSA.
4. Les 4 418 500 allocations de minima sociaux versées fin 2024 ne sont pas autant de personnes : une personne peut en cumuler plusieurs. Le RSA couvre 3 658 700 personnes (allocataires, conjoints et personnes à charge) : ce nombre ne se compare pas à ses 1 840 200 allocataires. Source : DREES, données nationales par dispositif, tableau 2 (« Il s'agit d'un nombre d'allocations versées et non d'un nombre d'allocataires corrigé des doubles-comptes ») ; RSA et prime d'activité, tableau 3, bloc « France » (« La "population couverte par le RSA" désigne l'allocataire, le conjoint et les personnes à charge. »).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/minimumIncomes.json` (clé `claims`, français et anglais), reprise des affirmations relues du rapport de recherche du 09/11/2026. Source de chaque chiffre de la réponse :

1. « On entend qu'on gagne plus au RSA qu'en travaillant au Smic. » 651,69 € et le forfait logement de 78,20 € : F19778 ; 573,49 € : calculé (651,69 − 78,20). 1 477,93 € net, « à titre indicatif » : F2300. 2,3 fois : calculé (1 477,93 / 651,69 = 2,27), avant impôt, avant prime d'activité et avant aides au logement. La réponse dit qu'elle compare un salaire net à un minimum social, pas deux revenus disponibles. Aucun cas type officiel (revenu disponible) n'est cité : la fiche de la DREES qui en donne n'a pas pu être ouverte.
2. « On entend que les étrangers touchent le RSA dès leur arrivée. » 5 ans de titre de séjour permettant de travailler, exceptions (carte de résident, réfugiés, apatrides, protection subsidiaire), non applicable aux Algériens : F19778. Même condition de 5 ans pour la prime d'activité : F2882.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web (rapport `verify-social.md`) : les quatre fiches de service-public.gouv.fr rouvertes, les trois classeurs de la DREES lus cellule par cellule (Python ; site de la DREES intermittent, fichiers obtenus après plusieurs essais). Producteurs officiels seulement. Aucun écart de valeur, aucun chiffre non retrouvé.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, RSA personne seule | 651,69 € (« 2026 ») | 651,69 € ; page « Vérifié le 01 avril 2026 » | F19778 | Conforme avec réserve : la page ne date pas le barème |
| Forfait logement | 78,20 € | « 1 78,20 € 2 156,41 € 3 ou + 193,55 € » ; 651,69 − 78,20 = 573,49 refait | F19778 | Conforme avec réserve (même réserve de date) |
| Smic net | 1 477,93 € | 1 477,93 € (9,74 € de l'heure), « à titre indicatif », page vérifiée le 01/06/2026 ; brut 1 867,02 € confirmé par la circulaire Cnav n° 2026-16 | F2300 | Conforme avec réserve : indicatif, avant impôt |
| Forfait de la prime d'activité | 638,28 € | « Le montant forfaitaire … est égal à 638,28 € . » | F2882 | Conforme avec réserve : barème non daté par la page |
| Aspa | 1 043,59 € brut | « 1 043,59 € , soit 12 523,14 € maximum par an (montants bruts) », section « vous vivez seul », depuis le 1er janvier 2026 | F16871 | Conforme |
| Condition de 5 ans | « À savoir » 3, affirmation 2 | retrouvée ; non applicable aux Algériens ; idem pour la prime d'activité | F19778, F2882 | Conforme |
| Allocations versées | 4 418 500 | tableau 2, « Ensemble (7) » = 4 418 500 (2024) ; note : « non d'allocataires corrigé des doubles-comptes » | classeur par dispositif (URL ci-dessus) | Conforme (date de mise à jour non lue dans le fichier) |
| Allocataires par dispositif | 1 840 200 / 1 397 800 / 754 500 / 265 000 | retrouvés (France, 2024) | classeur par dispositif | Conforme avec réserve : « foyers » n'est pas écrit dans le fichier |
| Personnes couvertes par le RSA | 3 658 700 | bloc « France » ; recoupé : 2 696 900 RSA seul + 961 900 RSA et prime d'activité = 3 658 800 (arrondi) | classeur RSA et prime d'activité | Conforme |
| Dépenses par dispositif | 33,291 / 12,358 / 13,839 / 4,586 Md€ | 33 291 / 12 358 / 13 839 / 4 586 M€, euros constants 2024 | classeur des dépenses | Conforme avec réserve : prime de Noël, indus et rappels compris ; ASV de premier étage exclue |
| Ratio Smic net / RSA | 2,3 (affirmation 1) | 1 477,93 / 651,69 = 2,27 refait | calcul | Conforme avec réserve : un salaire net face à un minimum social, avant prime d'activité |
| Dates de publication | 2026-04-01, 2026-06-01 (deux fiches), 2026-06-23, 2025-12-03 | dates « Vérifié le … » des fiches ; DREES : date du rapport d'origine (non lue dans les fichiers) | URL ci-dessus | Conforme avec réserve : ce ne sont pas des dates de barème ni, pour la DREES, une date lue |

**Conclusion.** Aucun chiffre du fichier n'est faux. Les barèmes ne sont pas datés par leur source, et le RSA face au Smic n'est pas une comparaison de revenus disponibles : la page le dit avant le chiffre.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus (DREES par ses fichiers). Sources inaccessibles, sans aucun chiffre utilisé : fiche 04 du panorama 2025 de la DREES (cas types), Légifrance (décret n° 2026-219 du 30 mars 2026, date du barème du RSA), études de la DREES sur le non-recours au RSA et à la prime d'activité.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert les fiches et les classeurs eux-mêmes ; le Smic net a été recoupé avec le brut de la circulaire Cnav.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - citation seule : DILA, service-public.gouv.fr, DREES (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
