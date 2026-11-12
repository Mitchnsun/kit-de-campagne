# `stateMedicalAid` · Aide médicale de l'État (AME) (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; réserves de lecture (crédits 2027 d'un projet de loi non voté, part des dépenses de l'État de 2024, soins urgents non précisés dans la dépense 2025, règles lues sur service-public.gouv.fr et non sur Légifrance), reprises dans « À savoir » et ci-dessous. La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `stateMedicalAid`, dossier « Immigration » (`immigration`), aussi dans « Santé » (`health`), page de type comparaison |
| Données | `briefings/manual/stateMedicalAid.json`, saisi à la main le 2026-11-09 depuis le PAP 2027 de la mission Santé et la fiche 3.3 des Comptes de la Sécurité sociale de juin 2025, d'après la recherche contre-vérifiée du 09/11/2026 (`final-immigration.json`) |
| Sources | Gouvernement, « Projet annuel de performances 2027, mission Santé » (page https://www.budget.gouv.fr/documentation/documents-budgetaires/exercice-2027/projet-loi-finances/budget-general/sante, PDF https://www.budget.gouv.fr/documentation/file-download/33691, créé le 30/09/2026 ; cité depuis la copie de l'Assemblée nationale jusqu'au 12/11/2026, Licence Ouverte 2.0) ; Direction de la Sécurité sociale, « Les Comptes de la Sécurité sociale, juin 2025, fiche 3.3 L'Aide médicale de l'État » (PDF créé le 26/06/2025) ; DILA (service-public.gouv.fr), « Qu'est-ce que l'aide médicale de l'État (AME) ? » (vérifiée le 01/04/2026), « RSA : demandeur de 25 ans et plus » (01/04/2026), « Allocation de solidarité aux personnes âgées (Aspa) » (23/06/2026) ; Conseil constitutionnel, « Décision n° 2024-6 RIP du 11 avril 2024 ». Licence « citation seule » pour toutes les autres, en français seulement |
| Séries | `beneficiaries` : bénéficiaires de l'AME de droit commun au 31 décembre, 2024 (465 208) et 2025 (454 111), 2 points ; `spending` : dépense d'AME, Md€, 2025 (1,34), 1 point ; `requestedCredits` : crédits demandés pour l'action AME par le PLF 2027, Md€, 2027 (1,2083), 1 point, statut `projection` (« prévision » sur la page) ; `shareOfStateSpending` : part de l'AME dans les dépenses de l'État, %, 2024 (0,3), 1 point |
| Chiffre clé | 454 111 bénéficiaires au 31 décembre 2025, en baisse (465 208 fin 2024, −2,4 %) ; à côté, la dépense de 2025 (1,3 Md€ à l'écran, 1 340 M€ dans la source) et la part des dépenses de l'État de 2024 (0,3 %) |
| Règles | Saisie à la main. La part de 0,3 % est un ratio publié par la DSS (pas un calcul) : elle va en série, avec sa seule année, 2024 (dépense de 1 256 M€ cette année-là, non saisie : autre source que les 1 340 M€ de 2025). Les crédits 2027 sont ceux de l'action « 02 – Aide médicale de l'État » du PLF (1 208,3 M€) ; le programme 183 (1 216,3 M€) n'est pas saisi. Dépense constatée et crédits demandés sont deux séries distinctes, la note du bloc dit qu'ils sont de nature différente. Les montants s'affichent en Md€ au dixième (1,3 et 1,2) ; les réponses citent les montants exacts. Les règles (conditions, panier de soins, RSA, ASPA, décision du Conseil constitutionnel) ne sont pas des séries : elles sont dans « À savoir » et « Ce qu'on entend », d'après service-public.gouv.fr et le Conseil constitutionnel, ajoutés aux sources de la page |
| Première édition | À remplir à la publication |

## « À savoir »

1. Selon service-public.gouv.fr, l'AME permet aux étrangers en situation irrégulière d'accéder aux soins. Il faut résider en France depuis plus de 3 mois et ne pas dépasser un plafond de ressources : 10 421 € par an pour une personne seule en métropole. Source : https://www.service-public.gouv.fr/particuliers/vosdroits/F3079 (« L'aide médicale de l'État (AME) est un dispositif permettant aux étrangers en situation irrégulière de bénéficier d'un accès aux soins » ; « Vous devez résider en France depuis plus de 3 mois » ; « Métropole […] Personne seule 10 421 € » ; page « Vérifié le 01 avril 2026 », relue le 09/11/2026 par l'agent qui a saisi la page).
2. Selon service-public.gouv.fr, l'AME prend en charge à 100 % les soins dans la limite des tarifs de la Sécurité sociale. Certains frais en sont exclus, comme les cures thermales ; certains soins non urgents attendent 9 mois après l'admission. Les mineurs restent couverts à 100 % dans tous les cas. Source : même page (« L'AME donne droit à la prise en charge à 100 % de vos soins médicaux et hospitaliers dans la limite des tarifs de la sécurité sociale » ; « Cure thermale. Toutefois, pour les mineurs, les frais médicaux restent pris en charge à 100 % dans tous les cas. » ; « Certains soins et traitements non urgents ne sont pris en charge qu'au bout d'un délai de 9 mois après l'admission à l'AME pour tout nouveau bénéficiaire majeur »).
3. Ces règles sont lues sur service-public.gouv.fr (pages vérifiées entre avril et juin 2026) : les textes de loi n'ont pas pu être ouverts sur Légifrance. Selon le projet annuel de performances 2027, deux décrets du 6 février 2026 renforcent les contrôles. Source : https://www.service-public.gouv.fr (pages F3079, F19778 et F16871) ; Légifrance (CASF L251-1 et L251-2, L262-4 ; CSS, ASPA ; décrets n° 2026-66 et 2026-67) a répondu 403 et 404 à la contre-vérification ; PAP 2027 Santé, https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128269/file/PAP%202027%20-%20Sant%C3%A9.pdf.
4. Selon le projet annuel de performances 2027, les dépenses hospitalières font 65 % de la dépense, pour 15 % des bénéficiaires. Il ne dit pas si les 1 340 M€ comprennent les soins urgents, que la Direction de la Sécurité sociale présente à part (132 M€ en 2024). Source : PAP 2027 Santé (même URL) ; Comptes de la Sécurité sociale, fiche 3.3, https://www.securite-sociale.fr/files/live/sites/SSFR/files/medias/CCSS/2025/3.3%20L%27Aide%20M%C3%A9dicale%20de%20l%27Etat.pdf (soins urgents, 132 M€ en 2024, selon la contre-vérification).

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/stateMedicalAid.json` (clé `claims`, français et anglais). Source de chaque chiffre de la réponse :

1. « On entend que l'AME coûte des milliards et offre des soins gratuits illimités aux clandestins. » 454 111 bénéficiaires fin 2025 et 1 340 M€ en 2025 : PAP 2027 Santé (« Au 31 décembre 2025, le nombre de bénéficiaires de l'AME de droit commun a baissé de -2,4 % … atteignant les 454 111 bénéficiaires » ; « pour atteindre 1 340 M€ en 2025 »). 0,3 % en 2024 : Comptes de la Sécurité sociale, fiche 3.3 (« Les dépenses de l'AME ont ainsi représenté 0,3% du total des dépenses de l'État pour cette dernière année. »). 100 %, exclusions et 9 mois : service-public.gouv.fr, F3079.
2. « On entend que les immigrés touchent le minimum vieillesse dès leur arrivée. » 10 ans et situations listées : service-public.gouv.fr, https://www.service-public.gouv.fr/particuliers/vosdroits/F16871 (« Avoir de façon continue depuis au moins 10 ans un titre de séjour autorisant à travailler » ; « Être réfugié Être apatride Bénéficier de la protection subsidiaire »). La liste d'exceptions de la page est plus longue que celle de la réponse.
3. « On entend qu'il suffit d'une loi pour réserver les aides aux Français ou imposer 5 ans de résidence. » Décision du 11 avril 2024, 5 ans ou 30 mois : Conseil constitutionnel, https://www.conseil-constitutionnel.fr/decision/2024/20246RIP.htm (cons. 13 : « … portent une atteinte disproportionnée à ces exigences. Elles sont donc contraires à la Constitution. » ; cons. 12 : une durée « ne saurait être telle qu'elle prive de garanties légales » ces exigences). La réponse dit que la décision portait sur une proposition de loi référendaire, pas sur une loi votée.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après son rapport `verify-immigration.md` : PDF du PAP Santé et des Comptes de la Sécurité sociale re-téléchargés, pages de service-public.gouv.fr et du Conseil constitutionnel rouvertes. Aucun écart de valeur.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, bénéficiaires | 454 111 (fin 2025) ; 465 208 (fin 2024) | Idem ; 32 679 en outre-mer ; 323 799 (71 %) remboursés au dernier trimestre | https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128269/file/PAP%202027%20-%20Sant%C3%A9.pdf | Conforme. Source : copie du PAP déposée à l'Assemblée |
| Dépense d'AME | 1,34 Md€ (2025) | « pour atteindre 1 340 M€ en 2025 » ; 65 % hospitalier pour 15 % des bénéficiaires | même PDF | Conforme, avec réserve : la page ne dit ni si les soins urgents sont compris, ni que le montant dépasse les crédits votés (affirmations de la recherche non retrouvées, non reprises) |
| Crédits 2027 | 1,2083 Md€ (prévision) | « 02 – Aide médicale de l'État 1 208 300 000 » ; programme 183 : 1 216,3 M€, égal à la LFI 2026 | même PDF ; PLF n° 3210 | Conforme, avec réserve : projet de loi non voté ; une « sous-budgétisation » n'est pas démontrée par les pages lues, la page n'en dit rien |
| Part des dépenses de l'État | 0,3 % (2024) | « 0,3% du total des dépenses de l'État pour cette dernière année » (1 256 M€) | https://www.securite-sociale.fr/files/live/sites/SSFR/files/medias/CCSS/2025/3.3%20L%27Aide%20M%C3%A9dicale%20de%20l%27Etat.pdf | Conforme, avec réserve : année 2024 ; la fiche 2026 n'a pas été trouvée |
| Conditions et panier | plus de 3 mois ; 10 421 € ; exclusions ; 9 mois | Idem, « Vérifié le 01 avril 2026 » | https://www.service-public.gouv.fr/particuliers/vosdroits/F3079 | Conforme, avec réserve : service-public, Légifrance non ouvert ; texte en vigueur au 09/11/2026 non confronté |
| RSA | 5 ans de titre | Idem (vérifié le 01/04/2026) | https://www.service-public.gouv.fr/particuliers/vosdroits/F19778 | Conforme, avec réserve : idem |
| ASPA | 10 ans continus | Idem (vérifié le 23/06/2026) ; liste d'exceptions plus longue | https://www.service-public.gouv.fr/particuliers/vosdroits/F16871 | Conforme, avec réserve : idem |
| Décision n° 2024-6 RIP | contraire à la Constitution | Idem (cons. 12 et 13) | https://www.conseil-constitutionnel.fr/decision/2024/20246RIP.htm | Conforme. Décision sur une proposition de loi référendaire |

**Conclusion.** Aucun chiffre du fichier n'est faux. La dépense de 2025 et les crédits de 2027 sont de nature différente ; la part des dépenses de l'État est de 2024.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus. Inaccessibles à la contre-vérification : Légifrance, ameli.fr, budget.gouv.fr (rapport annuel de performances 2025), la fiche AME des Comptes de la Sécurité sociale 2026 (introuvable).

## Réserves

- Le texte de loi des conditions (CASF L251-1 et L251-2), du RSA (L262-4) et de l'ASPA n'a pas été lu : les règles viennent de service-public.gouv.fr, dans leur version vérifiée d'avril à juin 2026.
- On ne sait pas si les 1 340 M€ de 2025 comprennent les soins urgents (132 M€ en 2024, présentés à part par la DSS ; dotation de 70 M€ pour 2027 dans le PAP), ni comment ils se comparent aux crédits votés pour 2025.
- Le « 14 % de déboutés parmi les bénéficiaires » (Sénat, au conditionnel) et le coût « 1,3 Md€ en 2024 » sont écartés par la recherche.

## Mises à jour

**09/11/2026** : le bloc « Ce qu'on entend » ne garde que les fausses vérités que les chiffres de la page démentent (décision du PO) : affirmations retirées : « On entend que les étrangers touchent le RSA dès leur arrivée. » ; reformulées : « On entend que les immigrés touchent le minimum vieillesse sans avoir jamais cotisé. » devient « On entend que les immigrés touchent le minimum vieillesse dès leur arrivée. ».

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert les documents.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande, lues le 12/11/2026 :
  - Gouvernement, document cité depuis budget.gouv.fr : Licence Ouverte 2.0 (« licence ouverte Etalab 2.0 »), mention de la source et de sa date de dernière mise à jour, contenus de tiers et photos exclus (https://www.budget.gouv.fr/mentions-legales, lues le 12/11/2026). Le PAP 2027 « Santé » y est la même édition (104 pages, créé le 30/09/2026), cité en citation seule depuis l'Assemblée nationale jusqu'au 12/11/2026 (décision du PO) ; les fichiers des deux sites n'ont pas été comparés ;
  - citation seule : Direction de la Sécurité sociale, DILA (service-public.gouv.fr), Conseil constitutionnel (chiffres cités avec leur source, aucun fichier redistribué).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
