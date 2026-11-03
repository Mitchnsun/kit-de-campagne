# `growthProjections` · Projections (partie de la page « PIB et croissance »)

**Vérifiée le 03/11/2026** : double vérification sur le web, sans écart sur les chiffres (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `growthProjections`, partie de la page composite `growth` (« PIB et croissance »), dossier « Économie et fiscalité » (`economy`), page de type série, ticket #25 de l'app (statut `planned`) ; l'autre partie est `gdpGrowth`, les comptes nationaux de l'Insee (PO, 03/11/2026 : un volet à part) |
| Données | `briefings/manual/growthProjections.json`, saisi à la main le 2026-11-03 d'après les chiffres relevés par le PO sur banque-france.fr, que les scripts ne peuvent pas lire |
| Sources | Banque de France, « Projections macroéconomiques intermédiaires – Septembre 2026 », mises en ligne le 15/09/2026, https://www.banque-france.fr/fr/publications-et-statistiques/publications/projections-macroeconomiques-intermediaires-septembre-2026 ; PDF : https://www.banque-france.fr/system/files/2026-09/Projections_macroeconomiques_Septembre_2026.pdf ; en anglais : « Macroeconomic interim projections – September 2026 » ; citation seulement (conditions de réutilisation non trouvées) |
| Séries | `gdpGrowth` : croissance annuelle du PIB, 2026 à 2028, 3 points ; `hicp` : inflation annuelle moyenne mesurée par l'IPCH, 2026 à 2028, 3 points ; toutes les années au statut `projection` |
| Chiffre clé | 0,4 % de croissance en 2026, sans tendance (une projection) |
| Règles | Le scénario de base seulement, hypothèses de l'Eurosystème arrêtées au 19/08/2026. L'inflation hors énergie et alimentation (1,6 / 2,3 / 1,9 %) est dans une note, pas dans une série |
| Première édition | à venir (l'indicateur est `planned`) |

## « À savoir »

1. Ce sont des projections, les chiffres du scénario de base, construit sur les hypothèses de l'Eurosystème arrêtées au 19 août 2026. Source : la publication, relevée par le PO ; la page anglaise de la Banque de France (résumé) donne le même gel au 19 août.
2. Par rapport à juin 2026, la croissance de 2026 est abaissée de 0,1 point (0,5 % à 0,4 %), 2027 et 2028 ne changent pas ; l'inflation de 2026 est abaissée de 0,2 point (2,5 % à 2,3 %). Source : la publication (PO) ; Daf-Mag et Franceinfo pour la croissance, la page anglaise de la Banque de France (résumé) pour l'inflation.
3. L'inflation projetée est celle de l'IPCH, l'un des deux indices de la page Inflation ; hors énergie et alimentation : 1,6 % en 2026, 2,3 % en 2027 et 1,9 % en 2028. Source : la publication (PO) ; Daf-Mag.

## Double vérification

Faite le 03/11/2026 par un agent Claude (modèle Sonnet) qui cherche sur le web, sans le site de la Banque de France (404 et 403 aux requêtes directes ; ses pages ne sont lues que par des résumés de l'outil de recherche).

| Élément | Valeur du fichier | Valeur trouvée | Source (URL) | Verdict |
| --- | --- | --- | --- | --- |
| PIB 2026 / 2027 / 2028 | 0,4 / 0,9 / 1,2 % | 0,4 / 0,9 / 1,2 % | Daf-Mag (lu) ; Franceinfo (lu, 2026 seulement) ; page anglaise de la Banque de France et son message sur X (résumés) | Conforme |
| IPCH 2026 / 2027 / 2028 | 2,3 / 1,9 / 1,6 % | 2,3 / 1,9 / 1,6 % | Daf-Mag (lu) ; page anglaise de la Banque de France et toutsurmesfinances (résumés) | Conforme |
| Hors énergie et alimentation (note) | 1,6 / 2,3 / 1,9 % | 1,6 / 2,3 / 1,9 % | Daf-Mag (lu) ; 2028 dans cette seule source | Conforme |
| Révisions par rapport à juin | PIB −0,1 / 0 / 0 ; IPCH −0,2 / +0,2 / −0,1 | identiques | Daf-Mag et Franceinfo (PIB) ; page anglaise (résumé) et différence des deux éditions (IPCH) | Conforme |
| Édition de juin | PIB 0,5 / 0,9 / 1,2 ; IPCH 2,5 / 1,7 / 1,7 | identiques | page anglaise de juin (résumé) | Conforme |
| Intitulé « intermédiaires », mise en ligne le 15/09/2026, gel au 19/08/2026 | | identiques | page anglaise (résumé) ; Franceinfo (15/09) | Conforme |

Points d'attention, sans effet sur les chiffres : la date de l'édition de juin (16 ou 17 juin selon les résumés) ; la projection de septembre précède l'IPCH de septembre publié par l'Insee (3,4 % sur un an), plus haut que sa trajectoire. Une nouvelle édition remplacera ces chiffres.

**Conclusion.** Les six valeurs saisies et la note sont conformes ; seules les conditions de réutilisation de la Banque de France n'ont pas été trouvées, d'où « citation seulement ».

**Pages consultées** le 03/11/2026 :
- https://www.daf-mag.fr/fonction-finance-1242/gouvernance-strategie-2125/croissance-la-banque-de-france-abaisse-sa-prevision-a-04-en-2026-27368
- https://www.franceinfo.fr/economie/croissance/la-banque-de-france-abaisse-legerement-sa-prevision-de-croissance-pour-2026-mais-souligne-que-l-economie-francaise-fait-preuve-de-resilience_8194166.html
- https://www.banque-france.fr/en/publications-and-statistics/publications/macroeconomic-interim-projections-september-2026 (résumé)
- https://www.banque-france.fr/en/publications-and-statistics/publications/macroeconomic-projections-june-2026 (résumé)
- https://www.toutsurmesfinances.com/actualites/a/inflation-la-banque-de-france-abaisse-sa-prevision-2026-mais-releve-celle-de-2027 (résumé)
- https://www.banque-france.fr/fr/mentions-legales (403)

## Mises à jour

Aucune.

## Relecture

- [x] Les chiffres clés et quelques points de chaque série recoupés ailleurs que dans la source.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [ ] La licence de chaque source vérifiée, et la mention qu'elle demande (non trouvée : citée seulement).
- [x] Aucune donnée interne du jeu, aucun sondage d'intention de vote pour 2027.
- [ ] Relue par le PO.
