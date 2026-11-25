# `institutionsRules` · Les institutions en chiffres

**Vérifiée le 25/11/2026** : chaque citation relue par script dans une copie ouverte du texte, chaque compte du territoire relevé dans les fichiers de l'Insee (section « Double vérification »).

| Champ | Valeur |
| --- | --- |
| Indicateur | `institutionsRules`, dossier « Institutions » (`institutions`), page de règles (`chart: 'rules'`, nature `law`), ticket #541 de l'app. Elle reprend l'encadré « Au-delà de l'élection » de `presidentialRules` (PO, 25/11/2026 : déplacé, pas doublé) |
| Données | `briefings/manual/institutionsRules.json`, saisi à la main le 2026-11-25 ; les règles `deputies`, `senators`, `ripMembers`, `ripVoters` et `rip2019` viennent de `presidentialRules.json`, inchangées |
| Sources | Conseil constitutionnel, « Constitution du 4 octobre 1958 », texte intégral en vigueur à jour de la révision du 8 mars 2024 ; « Décision n° 2019-1 RIP du 9 mai 2019 » ; « Décision n° 2019-1-8 RIP du 26 mars 2020 », https://www.conseil-constitutionnel.fr/decision/2020/201918RIP.htm ; « L'histoire du référendum sous la Ve République », mise à jour le 11/02/2020, https://www.conseil-constitutionnel.fr/la-constitution/l-histoire-du-referendum-sous-la-ve-republique ; Insee, « Code officiel géographique au 1er janvier 2026 », mis à jour le 24/02/2026, https://www.insee.fr/fr/information/8740222 (fichiers `v_commune_2026.csv`, `v_departement_2026.csv`, `v_region_2026.csv`) |
| Règles | Les comptes du territoire sont ceux de l'Insee (`valueSource`), sous l'article 72 de la Constitution, qui nomme les collectivités : aucune loi ne dit 18 régions. Les référendums : le compte du Conseil, neuf sur le fondement des articles 11 et 89 ; son tableau en a dix avec celui de 1958, dit dans les notes. Le CGCT et le code électoral n'ont été lus que dans des copies non officielles (droit.org) : rien n'en est cité dans le fichier, seulement dans une note (326 sénateurs) |
| Chiffre clé | 577 députés au plus (Constitution, art. 24) |
| Première édition | La prochaine édition du kit |

## Les comptes du territoire

Comptés dans les fichiers du COG 2026 par l'agent de recherche : communes de type COM, 34 875 ; départements, 101 lignes ; régions, 18 lignes (13 de métropole, Corse comprise, et Guadeloupe, Martinique, Guyane, La Réunion, Mayotte, devenue Département-Région de Mayotte, code 976R, au 1er janvier 2026).

## « À savoir »

1. Liste des décisions RIP du Conseil, https://www.conseil-constitutionnel.fr/les-decisions/type/RIP : 2019-1 (conforme), 2021-2, 2022-3, 2023-4, 2023-5, 2024-6, 2026-7 (non conformes) ; 2019-1-8, cons. 5 et 6.
2. « L'histoire du référendum sous la Ve République » (« Neuf référendums ») et le « Tableau récapitulatif des référendums de la Vème République » (dix lignes ; 2005 : non à 54,67 %).
3. Constitution, art. 24 ; code électoral, art. LO 119 (« Le nombre des députés est de cinq cent soixante-dix-sept. ») et LO 274 (« Le nombre des sénateurs élus dans les départements est de trois cent vingt-six. »), lus dans la copie de codes.droit.org, non officielle (Légifrance en 403) ; les autres sièges : LO 438-1, LO 473, LO 500, LO 527, LO 555 et les Français établis hors de France (Sénat).
4. COG 2026, ci-dessus ; note de la page : « Entre le 2 janvier 2025 et le 1er janvier 2026, aucune commune nouvelle n'a vu le jour en raison de la tenue des élections municipales en mars 2026. »

## Double vérification

Faite le 25/11/2026 par un agent Claude (modèle Sonnet), citations vérifiées par script dans les copies enregistrées (rapport `research/briefings-quiz-2026-11/verification-textes.md` de l'app), après une première recherche (`verification-regles.md`, § 5) : même RIP de 2019 (1 093 030 sur 4 717 396), mêmes comptes de l'Insee. Les règles reprises de `presidentialRules` avaient été vérifiées pour #443. L'article 72 relu par l'agent principal dans la copie de la Constitution.

## Mises à jour

Aucune.

## Relecture

- [x] Chaque citation relue dans une copie ouverte.
- [x] Chaque « À savoir » soutenu par une source, en français et en anglais.
- [x] La licence de chaque source vérifiée, et la mention qu'elle demande.
- [ ] Une révision de la Constitution postérieure au 8 mars 2024, ou un référendum après 2020 : non cherchés au-delà des pages du Conseil.
