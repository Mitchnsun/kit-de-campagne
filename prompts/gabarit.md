# Gabarit de prompt des illustrations

Pour les essais comme pour les images finales, dans ChatGPT (générateur d'images d'OpenAI). Chaque image a sa fiche, `prompts/<id-de-la-carte>.md`, sur le modèle de [`modele-fiche.md`](modele-fiche.md).

La direction artistique (styles, palette, cadrage, personnages) fait foi dans le ticket #159 du dépôt de l'app. Ce gabarit en reprend ce qu'il faut pour écrire un prompt.

## Remplir le prompt

1. **La scène**, tirée du texte de la carte : un seul moment, un geste ou une réaction, en France, en 2027.
   - Le personnage principal est dans le tiers gauche ou droit de l'image, le visage au-dessus de la mi-hauteur.
   - Les gens autour réagissent. Les détails sont ceux de 2027 : smartphones, caméras, ring lights, écrans, véhicules électriques.
   - **Dire où regarde chacun.** Quand la scène réagit au candidat, le personnage principal le regarde, c'est-à-dire regarde le spectateur. Les témoins (téléphones, caméras, une partie des badauds) visent aussi le spectateur, sans poser, et les autres continuent ce qu'ils font. Sans cette consigne, le générateur fait regarder tout le monde vers l'objectif, comme pour une photo de groupe, ou plus personne (essais de [`marketGaffe`](marketGaffe.md)).
   - **Le candidat du joueur n'a ni visage ni genre** : il est hors champ, la scène vue de sa place, ou c'est une silhouette lointaine, de dos, sans attribut genré marqué.
2. **Le style** : celui de la catégorie de la carte, sauf si la scène en demande un autre. Un changement se note dans la fiche.

   | Catégorie | Style par défaut |
   | --- | --- |
   | Polémique, Opportunité médiatique, Affaire, Attaque | Reportage dessiné |
   | Crise, Coup de projecteur, Buzz, Crise d'équipe | BD semi-réaliste |
   | Offre de soutien, Incroyable | Affiche lithographique |

3. **Le ton** : observateur par défaut, sinon ironique, tendu ou chaleureux selon l'événement (lignes plus bas).
4. **Ne jamais nommer un artiste ou un dessinateur vivant** : le style se décrit, il ne s'emprunte pas.

## Le prompt

```
Editorial illustration, landscape 16:9 (1536 × 864 px). [SCENE: the event as a single moment in a French setting in 2027, the main character in the left or right third with the face above mid-height, the reaction of the people around, saying where each group looks (at the viewer without posing, at each other, or at what they are doing), 2027 details. The player's candidate is off-camera, or a distant gender-neutral silhouette seen from behind.]

Style: [one of]
- Mid-century lithographic poster: large flat shapes, 4 to 5 colours, visible paper grain, bold simplified silhouettes, no outlines.
- Franco-Belgian semi-realistic comic book illustration: clean regular ink line, realistic proportions, flat colours with hard-edged shadows, one dominant light.
- Reportage drawing made on the spot, like a press illustrator or courtroom sketch artist: pencil and ink with loose watercolour washes, lively unfinished lines, white paper showing through.

Palette: navy #13203F, vellum #F5EFE1, gold #A9802A, brick #B5523B, ochre #D9A441, sage #8FA58A, slate #5E7186, sand #DCC8A4, warm grey #8C8279; use 4 to 6 of them, subtle warm paper grain.

Tone: [observant / ironic / tense / warm, with the light that goes with it]

Constraints: realistic proportions, expressive but not caricatured faces, people of varied ages, genders and origins; anatomically correct hands with exactly five fingers, few hands visible, the others in pockets, behind objects or out of frame; no readable text anywhere (signs, banners, price tags and screens stay blank); no captions or speech bubbles; no logos, flags or political party colours; no recognisable real person, no lookalike of a real politician; no explicit violence.

Format: if 16:9 is not available, make 1536 × 1024 and keep the top 80 px and the bottom 80 px free of anything important (faces, hands, the main action): they will be cropped.
```

## Les lignes de ton

| Ton | Quand | Ligne à coller |
| --- | --- | --- |
| Observateur (par défaut) | La plupart des événements | `Tone: observant and neutral, late-morning daylight.` |
| Ironique | Gaffes, buzz, polémiques légères | `Tone: gently ironic, postures slightly exaggerated but never the faces, soft light.` |
| Tendu | Crises, affaires, attaques | `Tone: tense, dusk palette, colder light, hard shadows.` |
| Chaleureux | Soutiens, coups de projecteur | `Tone: warm, soft afternoon sun, light warm colours.` |

## Garder la cohérence

- **Une conversation ChatGPT par style.** On y garde le même prompt, et on ne change que la scène et le ton.
- **Une image de référence** : l'image validée de l'essai de ce style, jointe au message. Reportage dessiné : [`marketGaffe.webp`](marketGaffe.webp). Avec cette ligne : `Use the attached image as the style reference: same line, paper grain and palette, not the same scene.`

## Après la génération

1. Garder le fichier d'origine (PNG) hors du dépôt, et noter dans la fiche où il est rangé.
2. Remplir la fiche : le prompt complet, le modèle, la date, le lien de la conversation, le format rendu, les retouches.
3. Faire la relecture de la fiche avant d'ajouter l'image à une édition.
4. Le format rendu décide de l'export : 1290 × 726 px en 16:9, ou 1290 × 860 px en 3:2, sans recadrage. Dans le cas du 3:2, c'est l'app qui recadre.
