# `paralysedCountry` · Pays paralysé

**À générer.** L'illustration d'une fin de campagne, pas d'une carte : l'écran de fin « Pays paralysé » (Mitchnsun/moi-president#205), quand la crise des milices va au bout de ses trois jours. Elle sert telle quelle en clair et en sombre.

![Pays paralysé](../../illustrations/endings/paralysedCountry.webp)

| Champ | Valeur |
| --- | --- |
| Carte | Aucune : la fin `paralysed`, catégorie `endings` (Fins de campagne). L'app la lit sous l'identifiant `paralysedCountry` (`constants/Illustrations.ts`) |
| Style | Reportage dessiné |
| Ton | Tendu |
| Date | À remplir |
| Outil | À remplir |
| Conversation | À remplir |
| Format rendu | À remplir : export en 1290 × 726 px, WebP de qualité 75 |
| Fichier d'origine | Image de ChatGPT, chez le PO |
| Première édition | À remplir |

## Texte de l'écran

> **Pays paralysé**
>
> Les milices ont paralysé le pays : le président sortant a suspendu l'élection en invoquant l'article 16 et reste à l'Élysée. Personne n'est élu.

## Le moment choisi

Le dimanche matin où le premier tour aurait dû avoir lieu. Devant une école de briques rouges d'une ville moyenne du Nord, transformée en bureau de vote, la grille est fermée par une chaîne ; derrière elle, les urnes transparentes et les isoloirs sont empilés, jamais servis. Une affichette officielle, illisible, est scotchée à la grille. La rue est vide ; au loin, un véhicule blindé de gendarmerie barre le carrefour. Le candidat du joueur est venu voir : au premier plan, ses tracts mouillés sur le trottoir. Personne ne pose. Pas de violence, pas de milicien, pas de blessé : l'élection qui n'a pas lieu.

## Prompt complet

Dans une nouvelle conversation, avec [`primeTime.webp`](../../illustrations/media/primeTime.webp) comme seule image de référence :

```
Use the attached image as the style reference and copy its drawing: a realistic reportage drawing made on the spot for a newspaper, with quick, nervous pencil lines, often drawn twice, ink hatching in the shadows, transparent watercolour washes that spill a little over the lines, and the warm paper showing through. Not the same scene and not the same people: never reuse the face or the hair of the woman in the reference.
Like in the reference, the setting can be full when the story needs it, with the things that say where we are and what is happening, but each one is sketched with a few pencil lines and a light wash, never rendered or finished, and the drawing gets looser and paler towards the edges until it fades into the bare paper.
This must look like a drawing made by hand on paper by a press illustrator, halfway between a quick sketch and a realistic picture: never a photograph, a film poster or a digital painting, and never a cartoon, a comic strip, a caricature or a children's book illustration. Continuous lines, never dotted or dashed outlines; no uniform texture, speckles or hatching filter laid over the picture; no glossy highlights, no smooth gradients, in the sky and on the walls too. Colour can be rich in places, on a piece of clothing, a light or a flag, but it stays transparent and within the palette below. The fade into the paper at the edges stays narrow, without a wide white margin. No blur and no depth-of-field effect: everything, the foreground included, is drawn sharp, like a sketch made on the spot.
People are drawn from life with realistic anatomy and proportions, like in the reference: faces shaped with pencil lines, hatching and light washes, a little more finished than the background but never photographic (no photographic skin, no airbrushed or digital-painting look). Expressions stay natural and restrained: no exaggerated grins, no wide-open mouths, no rubbery or cartoonish faces.

Editorial illustration, landscape 16:9 (1536 × 864 px), the scene filling the frame, with only a light fade into the paper at the edges. A Sunday morning in 2027, in a mid-sized town of northern France with red-brick houses: the day the first round of the presidential election should have taken place, and will not. A red-brick primary school that should have been a polling station: its iron gate is closed with a heavy chain and a padlock, a small official notice taped to it, unreadable. Behind the gate, in the school yard, transparent ballot boxes and folded voting booths are stacked, unused, under a tarpaulin. A French flag hangs limp above the school door. The player's candidate stays off-camera: in the foreground, only a few of the candidate's rain-soaked leaflets on the wet pavement, with no face and nothing readable on them. In the left third, the school caretaker, a stocky woman in her fifties of North African origin, with short greying curly hair, a padded jacket and a ring of keys in her hand, stands by the gate and looks at the viewer with a tired, worried face, her face above mid-height. Across the empty street, an elderly man of West African origin, tall and thin, in a long coat and a flat cap, holds his voter card in his hand and looks at the chained gate. Far away, at the end of the street, a gendarmerie armoured vehicle blocks the crossroads, two gendarmes beside it, small and sketched. The street is otherwise empty, shutters half closed. No crowd, no fighting, no weapon raised, no injured person, no militia: only an election that does not happen. Nothing on the notice, the leaflets, the boxes or the vehicle is readable.

Style: Reportage drawing made on the spot, like a press illustrator or courtroom sketch artist: pencil and ink with loose watercolour washes, lively unfinished lines, white paper showing through.

Palette: navy #13203F, vellum #F5EFE1, gold #A9802A, brick #B5523B, ochre #D9A441, sage #8FA58A, slate #5E7186, sand #DCC8A4, warm grey #8C8279; use 4 to 6 of them, subtle warm paper grain.

Tone: tense and silent, a grey morning after rain, cold light, long soft shadows.

Constraints: realistic proportions, natural expressions, never cartoonish or caricatured faces, drawn like the rest of the illustration and never photographic; people of varied ages, genders, origins and body types, each with a distinct face and haircut (no two people alike), drawn with respect and never as a joke; each person's age, build and look plausible for their role and the scene, no stereotype tying an origin or a gender to a role; anatomically correct hands with exactly five fingers, few hands visible; no readable text anywhere (the notice, the leaflets, the ballot boxes and the vehicle stay unreadable); no captions or speech bubbles; no logos or political party colours; no recognisable real person, no lookalike of a real politician; no explicit violence, no weapon pointed; no photographic rendering, no blur or bokeh, no dotted outlines, no texture or hatching filter over the picture, no oil-paint texture, no wide white margin or frame (a light fade into the paper at the edges is fine).

Format: if 16:9 is not available, make 1536 × 1024 and keep the top 80 px and the bottom 80 px free of anything important (faces, hands, the main action): they will be cropped.
```

## Décisions prises sur cette image

- Une fin, pas une carte : elle est rangée dans `endings`, que `yarn kit:build` reconnaît avec les cartes du deck (`ENDING_ILLUSTRATIONS`, `constants/Illustrations.ts` de l'app). Sans elle, l'écran de fin s'ouvre sur son verdict, comme sans le kit.
- Les règles de fiction de la crise (#205) : les milices sont des groupes anonymes, jamais le Rassemblement Hexagonal ni ses figures, et l'image n'en montre aucune ; le président sortant n'apparaît pas.

## Essais écartés

Aucun pour l'instant.

## Retouches

Aucune.

## Relecture

À faire par le PO.

- [ ] Aucun texte lisible : affichette, tracts, urnes, véhicule.
- [ ] Aucun sosie d'une personne réelle.
- [ ] Le candidat du joueur est hors champ ; ses tracts n'ont ni visage ni texte.
- [ ] Mains, visages et foules sans défaut visible à 343 px de large.
- [ ] Aucune couleur ni aucun logo de parti. Drapeau seulement pour signaler l'école. Des personnes variées par l'âge, le corps, l'origine et la coiffure.
- [ ] En 3:2 : rien d'important dans les 80 px du haut et du bas.
- [ ] Lisible sur l'écran de fin, en clair et en sombre.
