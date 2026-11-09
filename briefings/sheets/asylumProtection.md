# `asylumProtection` · Asile : décisions et protection (saisi à la main)

**Vérifiée le 09/11/2026** : double vérification sur le web, aucun écart numérique ; réserves de lecture (taux calculés d'après Eurostat, deux valeurs de 2024 dans le rapport de l'Ofpra, formule du taux synthétique non publiée), reprises dans « À savoir » et ci-dessous. La licence des sources n'a pas été vérifiée (voir « Relecture »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `asylumProtection`, dossier « Immigration » (`immigration`), page de type comparaison |
| Données | `briefings/manual/asylumProtection.json`, saisi à la main le 2026-11-09 depuis les rapports d'activité 2025 de l'Ofpra et de la CNDA, le rapport au Parlement 2025 de la DGEF et l'API d'Eurostat, d'après la recherche contre-vérifiée du 09/11/2026 (`final-immigration.json`) |
| Sources | Ofpra, « Rapport d'activité 2025 » (page du 27/07/2026 et PDF) ; CNDA, « Rapport d'activité 2025 » (PDF créé le 26/03/2026) ; ministère de l'Intérieur (DGEF), « Les étrangers en France 2025 – Rapport au Parlement » (PDF créé le 28/09/2026) ; Eurostat, `migr_asydcfsta` (mis à jour le 28/10/2026), `migr_asyappctza` (03/09/2026) et `tps00001` (27/10/2026) ; Gouvernement, « Projet annuel de performances 2027, mission Immigration, asile et intégration » (copie de l'Assemblée nationale, PDF créé le 29/09/2026). Licence « citation seule » pour l'Ofpra, la CNDA, la DGEF et le PAP (en français seulement), réutilisation libre avec mention de la source pour Eurostat |
| Séries | `ofpraRate` : taux de protection de l'Ofpra, %, 2024 et 2025, 2 points ; `cndaRate` : taux de protection de la CNDA, %, 2024 et 2025, 2 points ; `syntheticRate` : taux synthétique de protection publié par la DGEF, %, 2025, 1 point |
| Valeurs par catégorie | `applicantsPer100k` (2025, provisoire) : primo-demandeurs d'asile pour 100 000 habitants, France 169, UE 149, **calculé** ; `firstInstancePositive` (2025) : part des décisions positives en première instance, France 40,0 %, UE 39,1 %, **calculé** |
| Chiffre clé | 41,2 % (taux de protection de l'Ofpra, 2025), en hausse (38,8 % en 2024). Choisi parmi les taux publiés : sa formule est publiée et se recalcule (admissions 63 593 / (63 593 + rejets 90 610), clôtures exclues) ; le taux synthétique (52,1 %) n'a pas de formule publiée et le taux de la CNDA ne porte que sur les recours |
| Règles | Saisie à la main. Les taux pour 100 000 habitants et les parts de décisions positives ne sont publiés par aucun producteur : ils sont calculés à partir des chiffres d'Eurostat (FR 116 475 primo-demandeurs, UE 672 350 ; population au 1er janvier 2025 FR 68 882 600, UE 451 284 558, provisoires ; décisions positives FR 60 515 sur 151 125, UE 325 935 sur 833 650), et la page le dit (« calculé ») ; ils vont en valeurs par catégorie, jamais en série. Le rang de la France (3e en volume, 9e sur 27 par habitant) n'est que dans une affirmation, avec « calculé ». 2024 de l'Ofpra : 38,8 % (tableau du rapport et page web), le texte p. 66 écrit 38,9 %. Le taux synthétique n'a qu'un point (2025), seul chiffre du fichier vérifié. L'allocation pour demandeur d'asile (212 € par mois, prévision 2027) n'est que dans une affirmation |
| Première édition | À remplir à la publication |

## « À savoir »

1. Le taux de protection de l'Ofpra rapporte ses décisions d'accord aux accords et aux rejets de l'année : les irrecevabilités sont comptées dans les rejets, les clôtures exclues. Pour 2024, le rapport de l'Ofpra écrit 38,8 % dans son tableau et 38,9 % dans son texte. Source : Ofpra, rapport d'activité 2025, https://www.ofpra.gouv.fr/sites/default/files/2026-07/Rapport%20d%27activit%C3%A9%202025%20Ofpra.pdf (« Le taux de protection de l'Ofpra s'est établi à 41,2 %, contre 38,8 % en 2024 » ; tableau « Taux d'admission Ofpra 41,2 % 38,8 % » ; texte p. 66 : 38,9 %).
2. La CNDA juge les recours contre les rejets de l'Ofpra : en 2025, 12 391 décisions de protection sur 53 086 décisions. Selon elle, la part des rejets de l'Ofpra contestés devant elle est passée de 84 % à 87 %. Source : CNDA, rapport d'activité 2025, https://www.cnda.fr/Media/mediatheque-cnda/documents/rapports-d-activite/rapport-d-activite-2025 (« En 2025, le taux de protection de la Cour s'établit à 23,3 % contre 21,3 % en 2024, avec 12 391 décisions de protection » ; « Le taux de recours contre les décisions de rejet … est passé de 84 % à 87 % »).
3. Le taux synthétique de 52,1 % est publié par la DGEF, qui ne détaille pas sa formule : il réunit les protections accordées par l'Ofpra et par la CNDA, soit 78 782 personnes protégées en 2025 (78 783 selon l'Ofpra). Source : DGEF, rapport au Parlement 2025, https://www.immigration.interieur.gouv.fr/sites/dgef/files/medias/documents/2026-10/INTV2623196X_Rapport%20au_Parlement_2025_28sept2026.pdf (« Au total, 78 782 personnes ont obtenu une protection internationale en 2025 (+ 12,1 % en un an), portant le taux global de protection à 52,1 % »).
4. Les rapports pour 100 000 habitants et les parts de décisions positives sont calculés d'après Eurostat, qui ne les publie pas. La part calculée pour la France (40,0 %) et le taux de l'Ofpra (41,2 %) ne reposent pas sur le même décompte des décisions. Source : API Eurostat, `migr_asyappctza`, `migr_asydcfsta` et `tps00001` (valeurs dans « Règles ») ; la différence de décompte se lit dans les chiffres (Eurostat : 60 515 positives sur 151 125 ; Ofpra : 63 593 admissions et 90 610 rejets), ce n'est pas une phrase de la source.

Les quatre points en anglais disent la même chose que le français.

## Ce qu'on entend

Chaque affirmation est dans `briefings/notes/asylumProtection.json` (clé `claims`, français et anglais). Source de chaque chiffre de la réponse :

1. « On entend que 90 % des demandeurs d'asile sont déboutés. » 41,2 % : Ofpra, rapport d'activité 2025. 23,3 % : CNDA, rapport d'activité 2025. 52,1 % : DGEF, rapport au Parlement 2025. Le « 90 % » vient d'un article de presse que la contre-vérification n'a pas rouvert.
2. « On entend que la France accueille le plus de demandeurs d'asile d'Europe et accorde l'asile plus facilement que les autres. » 3e en volume (ES 141 055 provisoire, IT 128 655, FR 116 475, DE 113 235) et 9e sur 27 par habitant : rangs calculés à partir de `migr_asyappctza` et `tps00001`. 169 et 149 pour 100 000 habitants : calculés. 40,0 % et 39,1 % : calculés à partir de `migr_asydcfsta`. Le mot « calculé » est dans la réponse.
3. « On entend que les demandeurs d'asile touchent plus qu'un retraité. » 65 944 allocataires en moyenne par mois et 212 € par mois et par personne en 2027 : PAP 2027, mission Immigration, asile et intégration (« L'allocation serait versée à 65 944 individus en moyenne par mois en 2027, pour un montant moyen de 212 € par mois et par individu. »). Prévision budgétaire, dite comme telle ; le barème réglementaire n'a pas été confirmé. La réponse ne compare pas ce montant à une pension, faute de chiffre de la page.

## Double vérification

Faite le 09/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, d'après son rapport `verify-immigration.md` : PDF de l'Ofpra, de la CNDA, de la DGEF et du PAP re-téléchargés, API d'Eurostat réinterrogée, rangs et ratios recalculés. Aucun écart de valeur.

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| Chiffre clé, taux de l'Ofpra | 41,2 % (2025) ; 38,8 % (2024) | 41,2 % ; 38,8 % au tableau et sur la page web, 38,9 % au texte p. 66 ; 63 593 / (63 593 + 90 610) = 41,2 % | https://www.ofpra.gouv.fr/sites/default/files/2026-07/Rapport%20d%27activit%C3%A9%202025%20Ofpra.pdf | Conforme, avec réserve : deux valeurs de 2024 dans le rapport ; irrecevabilités (15 338) comptées dans les rejets |
| Taux de la CNDA | 23,3 % (2025) ; 21,3 % (2024) | 12 391 / 53 086 = 23,34 % ; « de 84 % à 87 % » lu | https://www.cnda.fr/Media/mediatheque-cnda/documents/rapports-d-activite/rapport-d-activite-2025 | Conforme. La date de publication n'est pas lisible ; le PDF est créé le 26/03/2026 |
| Taux synthétique | 52,1 % (2025) | 52,1 % ; 78 782 personnes protégées (+12,1 %) | https://www.immigration.interieur.gouv.fr/sites/dgef/files/medias/documents/2026-10/INTV2623196X_Rapport%20au_Parlement_2025_28sept2026.pdf | Conforme, avec réserve : formule de la DGEF non retrouvée, non recalculé ; 78 783 selon l'Ofpra |
| Décisions positives, 1re instance | 40,0 % (FR) ; 39,1 % (UE) | 60 515 / 151 125 = 40,04 % ; 325 935 / 833 650 = 39,10 % | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/migr_asydcfsta?geo=FR&geo=EU27_2020&time=2025&citizen=TOTAL&sex=T&age=TOTAL | Conforme, avec réserve : taux calculé ; les positives de l'UE comprennent des statuts humanitaires nationaux (86 575) |
| Primo-demandeurs pour 100 000 habitants | 169 (FR) ; 149 (UE) | 169,1 (rang 9) ; 149,0 ; volumes ES 141 055 (p), IT 128 655, FR 116 475, DE 113 235 | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/migr_asyappctza?time=2025&citizen=TOTAL&sex=T&age=TOTAL&applicant=FRST | Conforme, avec réserve : taux calculé ; Espagne provisoire ; population provisoire |
| Allocation pour demandeur d'asile | 212 € par mois, 65 944 allocataires (2027, dans l'affirmation 3) | Idem | https://www.assemblee-nationale.fr/dyn/contenu/visualisation/1128237/file/PAP%202027%20-%20Immigration%20asile%20et%20int%C3%A9gration.pdf | Conforme, avec réserve : prévision 2027 |

**Conclusion.** Aucun chiffre du fichier n'est faux. Les taux pour 100 000 habitants, les parts de décisions positives et les rangs sont calculés, et la page le dit.

**Pages consultées** le 09/11/2026 : les documents des URL ci-dessus. Les dates de mise à jour d'Eurostat (28/10/2026, 03/09/2026, 27/10/2026) et les intitulés français des jeux ont été relus dans l'API le 09/11/2026 par l'agent qui a saisi la page ; les valeurs 2025 y sont les mêmes.

## Réserves

- Le taux de 2024 de l'Ofpra est écrit 38,8 % ou 38,9 % selon la page du rapport : le fichier garde 38,8 % (tableau et page web).
- La formule du taux synthétique de la DGEF n'est pas publiée.
- Les chiffres de la DGEF (156 590 décisions de l'Ofpra, 145 211 demandes, provisoires) diffèrent légèrement de ceux de l'Ofpra (156 509 et 145 270) ; ils ne sont pas saisis.
- Le stock de bénéficiaires de la protection (736 534 dans l'annexe du rapport de l'Ofpra, 734 360 dans son texte, une estimation) n'est pas saisi.

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source du script. Il n'y a pas de script : la double vérification a rouvert les documents et l'API.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande. Non vérifiée : le registre dit « citation seule » pour l'Ofpra, la CNDA, la DGEF et le PAP (chiffres cités, aucun fichier redistribué), et la licence d'Eurostat pour ses jeux.
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
