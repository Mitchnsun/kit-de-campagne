# Gabarit de prompt des illustrations

Pour les essais comme pour les images finales, dans ChatGPT (ChatGPT Images, le générateur d'images d'OpenAI). La première série a été faite avec le modèle GPT Sol 6.1 en effort « light » et ChatGPT Images 2.5. Chaque image a sa fiche, `prompts/<catégorie>/<id-de-la-carte>.md`, sur le modèle de [`modele-fiche.md`](modele-fiche.md), et l'image validée est rangée à part, en `illustrations/<catégorie>/<id-de-la-carte>.webp`. La catégorie est le `kind` de la carte dans le moteur du jeu (`polemic`, `crisis`…), que la fiche donne à sa ligne « Carte ». Les 36 fiches de la première série (30 et 31/10, 01/11/2026) montrent ces règles à l'œuvre, essais écartés compris.

La direction artistique fait foi dans le ticket #159 du dépôt de l'app. Ce gabarit en reprend ce qu'il faut pour écrire un prompt, avec les leçons de la première série.

## Remplir le prompt

1. **La scène**, tirée du texte de la carte : un seul moment, un geste ou une réaction, en France, en 2027.
   - Le personnage principal est dans le tiers gauche ou droit de l'image, le visage au-dessus de la mi-hauteur.
   - Les détails sont ceux de 2027 : smartphones, caméras, écrans, véhicules électriques. **Un décor allégé** : plus la scène accumule d'objets, plus le générateur tire vers la photo ([`inflatedInvoices`](affair/inflatedInvoices.md)).
2. **Les personnages, chacun décrit** : âge, corps, visage, coupe de cheveux, origine quand elle compte.
   - **Des corps variés selon le contexte**, pas seulement minces : corpulent, trapu, rond, grand, petit, sec. Sans consigne, le générateur fait des gens minces ([`factoryClosure`](crisis/factoryClosure.md)).
   - **Des visages et des coupes tous différents**, nommés un par un : sans cela, les visages se ressemblent d'une image à l'autre ([`riots`](crisis/riots.md)).
   - **Pas deux personnages semblables dans une image** (deux hommes âgés à moustache blanche, [`ghostAssistants`](affair/ghostAssistants.md)), **ni un personnage qui reprend les traits d'une autre carte** (la reporter de [`firstContact`](farFetched/firstContact.md) recopiait la rappeuse de [`starEndorsement`](breakthrough/starEndorsement.md)).
   - **Pas de profil type d'un titulaire de fonction connu** : un sénateur âgé, corpulent, aux cheveux blancs, au Sénat, évoque un président du Sénat ([`sponsorshipBank`](sponsorships/sponsorshipBank.md)). Un journaliste d'investigation à moustache et lunettes évoque un journaliste réel ([`ghostAssistants`](affair/ghostAssistants.md)).
3. **Dire où regarde chacun.** Quand la scène réagit au candidat, le personnage principal le regarde, c'est-à-dire regarde le spectateur, et les témoins aussi, sans poser ; les autres continuent ce qu'ils font. Sans cette consigne, tout le monde regarde l'objectif comme pour une photo de groupe, ou plus personne ([`marketGaffe`](polemic/marketGaffe.md)). Quand personne ne doit regarder le spectateur, l'écrire (« Nobody looks at the viewer »).
4. **Le candidat du joueur n'a ni visage ni genre.** Il est hors champ, la scène vue de sa place, avec un objet à lui au premier plan (sa tasse, ses tracts, le bord de son parapluie). Toute image de lui dans la scène, affiche, tract ou double numérique, n'a ni visage, ni cheveux, ni vêtement genré : pas de costume-cravate ([`sloganMeme`](buzz/sloganMeme.md)), une silhouette de lumière sans traits ([`aiDouble`](farFetched/aiDouble.md)), ou pas d'image du tout ([`stateAlgorithm`](farFetched/stateAlgorithm.md), [`mayorsCandidate`](sponsorships/mayorsCandidate.md)).
5. **Ce qui est permis** (PO, 30 et 31/10/2026) :
   - les ressemblances avec ce qui existe : interfaces, habillages de chaîne, monuments, modèles d'avions réels ;
   - les drapeaux tricolore et européen, l'écharpe tricolore et la Marianne, pour signaler un bâtiment officiel ou un élu ;
   - un léger fondu du dessin dans le papier aux bords et dans les coins, sans large marge blanche (PO, 01/11/2026, [`firstContact`](farFetched/firstContact.md)).
6. **Ce qui reste interdit** : tout texte lisible ; un logo ou une couleur de parti ; un parti ou une association nommés ou reconnaissables ; un sosie d'une personne réelle ; le portrait d'un président réel au mur ; un vaisseau, un ordinateur ou un extraterrestre tiré d'un film connu.
7. **Le style** : pour le moment, **toutes les cartes sont en reportage dessiné** (décision du 30/10/2026). Le trait cherche l'équilibre entre l'esquisse de [`oldTweet`](polemic/oldTweet.md) et le fini de [`marketGaffe`](polemic/marketGaffe.md). L'affiche lithographique et la BD semi-réaliste restent décrites dans #159, pour une image qui les demanderait plus tard.
8. **Le ton** : observateur par défaut, sinon ironique, tendu ou chaleureux selon l'événement (lignes plus bas), adapté à la scène et à sa lumière.
9. **Ne jamais nommer un artiste ou un dessinateur vivant** : le style se décrit, il ne s'emprunte pas.

## Le prompt

Avec [`oldTweet.webp`](../illustrations/polemic/oldTweet.webp) comme seule image de référence, dans une nouvelle conversation. Les trois premières lignes tiennent le rendu dessiné : sans elles, le générateur revient à une photo ou à une peinture numérique sous un filtre de hachures.

```
Use the attached image as the style reference: the same pencil and ink drawing with loose watercolour washes and warm paper grain. Not the same scene.
This must look like a drawing made by hand on paper, never like a photograph or a film poster: the people are drawn with ink lines and flat washes, not modelled; the background is only suggested with a few pencil lines and light, transparent washes, so that the warm paper shows through; the drawing may fade lightly into the bare paper at the edges and in the corners, as on a sketchbook page, the fade staying narrow, without a wide white margin. Lighter and less saturated than a painting: no dense colour, no glossy highlights, no hatching filter laid over a finished image. No blur and no depth-of-field effect: everything, the foreground included, is drawn sharp with ink lines, like a sketch made on the spot.
Faces are drawn exactly like the clothes and the background: ink outlines, a few hatching strokes and flat watercolour washes for the skin, with the same level of detail as the rest of the drawing. No photographic skin, no realistic wrinkles or pores, no airbrushed or digital-painting look on the faces.

Editorial illustration, landscape 16:9 (1536 × 864 px), the scene filling the frame, with only a light fade into the paper at the edges. [SCENE: the event as a single moment in a French setting in 2027. The player's candidate stays off-camera: in the foreground, only [an object of the candidate's]. In the right (or left) third, the main character, [age, body, face, haircut, clothes], [action], looking at the viewer [or not], their face above mid-height. Around: each person described the same way, with where they look. Nothing on [the objects of the scene] is readable.]

Style: Reportage drawing made on the spot, like a press illustrator or courtroom sketch artist: pencil and ink with loose watercolour washes, lively unfinished lines, white paper showing through.

Palette: navy #13203F, vellum #F5EFE1, gold #A9802A, brick #B5523B, ochre #D9A441, sage #8FA58A, slate #5E7186, sand #DCC8A4, warm grey #8C8279; use 4 to 6 of them, subtle warm paper grain.

Tone: [observant / ironic / tense / warm, with the light that goes with it]

Constraints: realistic proportions, expressive but not caricatured faces, drawn like the rest of the illustration and never photographic; people of varied ages, genders, origins and body types (heavy, stocky, round, tall, short, wiry, not only slim), each with a distinct face and haircut (no two people alike), drawn with respect and never as a joke; anatomically correct hands with exactly five fingers, few hands visible, the others in pockets, behind objects or out of frame; no readable text anywhere ([the objects of the scene] stay unreadable); no captions or speech bubbles; no logos or political party colours; no recognisable real person, no lookalike of a real politician [or of the trade in the scene]; no explicit violence; no photographic rendering, no blur or bokeh, no hatching filter over a finished digital painting, no oil-paint texture, no wide white margin or frame (a light fade into the paper at the edges is fine).

Format: if 16:9 is not available, make 1536 × 1024 and keep the top 80 px and the bottom 80 px free of anything important (faces, hands, the main action): they will be cropped.
```

## Une ressemblance voulue

Le PO peut prêter à un personnage les traits d'un proche, ou les siens, d'après une photo (première série : [`ministerResigns`](crisis/ministerResigns.md), [`donorsDinner`](support/donorsDinner.md), [`pundit`](attack/pundit.md), [`whistleblower`](breakthrough/whistleblower.md), [`firstContact`](farFetched/firstContact.md), [`stateAlgorithm`](farFetched/stateAlgorithm.md), [`comet`](farFetched/comet.md), [`sponsorThreatened`](sponsorships/sponsorThreatened.md)).

- **L'accord de la personne**, confirmé par le PO, avant d'ajouter l'image au dépôt.
- **Ni la photo ni le portrait dessiné ne vont dans ce dépôt.** La fiche dit seulement « photo de famille du PO » ou « portrait dessiné du PO », sans nom.
- **On ne change ni la silhouette, ni le visage, ni la coiffure de la personne réelle** : la description du personnage perd « corpulent », les lunettes ou la queue de cheval qu'elle avait ([`whistleblower`](breakthrough/whistleblower.md), [`stateAlgorithm`](farFetched/stateAlgorithm.md)). On adapte plutôt le rôle à son âge, et la variété des corps passe par les autres personnages.
- **En deux étapes**, jamais la photo jointe à la scène : jointe directement, la photo est recopiée et le visage ressort photographique ([`donorsDinner`](support/donorsDinner.md), [`pundit`](attack/pundit.md)).

**Étape 1, le portrait dessiné**, dans une nouvelle conversation, avec `oldTweet.webp` puis la photo. Adapter la deuxième phrase (« this man », « this woman », l'expression, les vêtements) :

```
Use the first attached image as the style reference: the same pencil and ink drawing with loose watercolour washes and warm paper grain.
The second attached image is a family photograph. Draw a new portrait of this man, as a press illustrator or courtroom sketch artist would draw a quick likeness from life: head and shoulders, three-quarter view, on plain warm paper with no background.
Do not trace or copy the photograph. Redraw the face from scratch and keep only what makes him recognisable: the shape of the face, the hairline and the wavy hair, the eyebrows, the nose and the smile. Everything is drawn with ink outlines, hatching and flat watercolour washes, simplified like the faces in the reference image. No photographic skin, no photographic lighting, no detail taken over from the photo's texture.
Format: square, 1024 × 1024 px.
```

Vérifier le portrait avant la scène : s'il est déjà photographique, le régénérer, sinon la scène le sera aussi ([`whistleblower`](breakthrough/whistleblower.md)). Un portrait réussi resservira pour d'autres cartes ([`pundit`](attack/pundit.md), [`firstContact`](farFetched/firstContact.md)).

**Étape 2, la scène**, dans une nouvelle conversation, avec `oldTweet.webp` puis le portrait. Ajouter cette ligne en deuxième position, remplacer « Use the attached image » par « Use the first attached image », décrire le personnage comme « the man (the woman) from the portrait », et ajouter « apart from [le personnage], » devant « no recognisable real person » :

```
Use the second attached image, a drawn portrait, only as the likeness reference for [the character]: give him (her) this man's (woman's) features, [hair] and [beard], and draw his (her) face with the same ink lines and washes as the other people in the scene. Keep the likeness through the drawing, never through photographic detail.
```

## Les lignes de ton

| Ton | Quand | Ligne à coller, à adapter à la scène |
| --- | --- | --- |
| Observateur (par défaut) | La plupart des événements | `Tone: observant and neutral, late-morning daylight.` |
| Ironique | Gaffes, buzz, polémiques légères | `Tone: gently ironic, postures slightly exaggerated but never the faces, soft light.` |
| Tendu | Crises, affaires, attaques | `Tone: tense, dusk palette, colder light, hard shadows.` |
| Chaleureux | Soutiens, coups de projecteur | `Tone: warm, soft afternoon sun, light warm colours.` |

## Quand le rendu dérive

Le générateur revient souvent à une photo, à une peinture numérique sous un filtre de hachures, à une affiche de film ou à un premier plan flou. Dans l'ordre :

1. **Un message de correction, dans la même conversation**, qui garde la scène et ne change que le rendu (il a suffi pour [`starEndorsement`](breakthrough/starEndorsement.md) et [`ghostAssistants`](affair/ghostAssistants.md)) :

   ```
   Keep the same scene, the same people, the same places and the same poses, but match the rendering of the reference image much more closely: a quick reportage drawing on warm paper, pencil and ink lines, loose watercolour washes, plenty of white paper showing through, lighter and less saturated overall; no photographic rendering, no hatching filter over a finished digital painting; every face is drawn like the clothes, with an ink outline, a few hatching strokes and flat watercolour washes. Everything else stays the same: nothing readable, exactly five fingers on every visible hand.
   ```

   Chaque changement ajouté au message (un personnage, un décor) augmente le risque que tout le reste bouge.
2. **Si le rendu ne bouge pas : renvoyer le prompt revu en entier, dans la même conversation**, sans rejoindre d'image. Il garde la composition, ou la refait de près, et change le rendu ([`inflatedInvoices`](affair/inflatedInvoices.md), [`firstContact`](farFetched/firstContact.md), [`comet`](farFetched/comet.md)).
3. **En dernier recours, une nouvelle conversation** avec le prompt revu : la composition est perdue.

Pour changer un visage, régénérer plutôt que corriger ([`primeTime`](media/primeTime.md)).

## Après la génération

1. Garder le fichier d'origine (PNG) hors du dépôt, et noter dans la fiche où il est rangé.
2. Relire l'image en zoomant : les mains, tout ce qui pourrait porter du texte (journaux, enseignes, plans, tampons, formulaires), les sosies possibles, et toute image du candidat.
3. Remplir la fiche : le prompt complet et les messages envoyés ensuite, les décisions, les essais écartés, la relecture.
4. Exporter en `illustrations/<catégorie>/<id-de-la-carte>.webp`, sans recadrage, en 1290 × 726 px pour une image en 16:9 (1290 × 860 px si elle est restée en 3:2 : c'est l'app qui recadre), **en WebP de qualité 75, même au-delà de 180 Ko** (PO, 31/10/2026, [`starEndorsement`](breakthrough/starEndorsement.md)) : les images de la première série font de 110 à 255 Ko.

   ```python
   from PIL import Image
   im = Image.open(png).convert('RGB').resize((1290, 726), Image.LANCZOS)
   im.save('illustrations/<catégorie>/<id>.webp', 'WEBP', quality=75, method=6)
   ```
