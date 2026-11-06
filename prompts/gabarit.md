# Gabarit de prompt des illustrations

Pour les essais comme pour les images finales, dans ChatGPT (ChatGPT Images, le générateur d'images d'OpenAI). La première série a été faite avec le modèle GPT Sol 6.1 en effort « light » et ChatGPT Images 2.5. Chaque image a sa fiche, `prompts/<catégorie>/<id-de-la-carte>.md`, sur le modèle de [`modele-fiche.md`](modele-fiche.md), et l'image validée est rangée à part, en `illustrations/<catégorie>/<id-de-la-carte>.webp`. La catégorie est le `kind` de la carte dans le moteur du jeu (`polemic`, `crisis`…), que la fiche donne à sa ligne « Carte ». Les 36 fiches de la première série (30 et 31/10, 01/11/2026) montrent ces règles à l'œuvre, essais écartés compris.

La direction artistique fait foi dans le ticket #159 du dépôt de l'app. Ce gabarit en reprend ce qu'il faut pour écrire un prompt, avec les leçons de la première série.

## Remplir le prompt

1. **La scène**, tirée du texte de la carte : un seul moment, un geste ou une réaction, en France, en 2027.
   - Le personnage principal est dans le tiers gauche ou droit de l'image, le visage au-dessus de la mi-hauteur.
   - Les détails sont ceux de 2027 : smartphones, caméras, écrans, véhicules électriques.
   - **Le décor que l'histoire demande, esquissé.** Un hangar de matériel de meeting est plein, un QG a ses bureaux et ses écrans : les objets qui disent où l'on est et ce qui se passe restent, nommés dans le prompt. Ceux qui ne font que remplir tombent (la plante, le pot à crayons, le tableau, les rayonnages colorés). Tous sont esquissés au crayon avec un lavis léger, jamais finis : c'est le rendu fini qui tire vers la photo plus que le nombre d'objets, et [`oldTweet`](polemic/oldTweet.md), chargée, reste un dessin (PO, 04/11/2026). Le même jour, la règle de « trois ou quatre objets au plus » avait donné un premier essai de régénération trop dépouillé, et le PO l'a abandonnée ([`inflatedInvoices`](affair/inflatedInvoices.md)).
2. **Les personnages, chacun décrit** : âge, corps, visage, coupe de cheveux, origine quand elle compte.
   - **Des corps variés selon le contexte**, pas seulement minces : corpulent, trapu, rond, grand, petit, sec. Sans consigne, le générateur fait des gens minces ([`factoryClosure`](crisis/factoryClosure.md)).
   - **Des origines variées, nommées une par une**, autant que le contexte le permet : la France de 2027 n'est pas faite que de personnes blanches. Sans origine écrite dans le prompt, le générateur dessine surtout des personnes blanches, et la consigne générale des contraintes ne suffit pas. Dans une scène de groupe, au moins deux ou trois personnages d'origines différentes, y compris aux premiers rôles (le maire, l'éleveur, la journaliste), pas seulement parmi les figurants (PO, 04/11/2026, [`charityMarathon`](rendezvous/charityMarathon.md)).
   - **Des lieux et des régions variés.** Pas toujours le village et son église, ni des immeubles haussmanniens hors de Paris : le générateur y revient sans consigne, les deux tiers de la série s'y ressemblent. Selon la carte, une ville moyenne, une banlieue, une grande ville, la montagne, la mer, les Outre-mer, et surtout une région nommée avec son architecture : colombages et toits pentus d'Alsace, granit et ardoise de Bretagne, brique rouge du Nord et de Lille, brique rose de Toulouse, façades ocre et tuiles de Provence, maisons blanches aux volets rouges du Pays basque, pierre blonde de Bordeaux, chalets de Savoie, immeubles pastel de Lyon ou de Nice, cases créoles des Antilles. Une carte qui laisse le choix prend une région qui n'a pas encore servi (PO, 04/11/2026, [`easterWeekend`](rendezvous/easterWeekend.md)).
   - **Des visages et des coupes tous différents**, nommés un par un : sans cela, les visages se ressemblent d'une image à l'autre ([`riots`](crisis/riots.md)).
   - **Pas deux personnages semblables dans une image** (deux hommes âgés à moustache blanche, [`ghostAssistants`](affair/ghostAssistants.md)), **ni un personnage qui reprend les traits d'une autre carte** (la reporter de [`firstContact`](farFetched/firstContact.md) recopiait la rappeuse de [`starEndorsement`](breakthrough/starEndorsement.md)).
   - **Pas de profil type d'un titulaire de fonction connu** : un sénateur âgé, corpulent, aux cheveux blancs, au Sénat, évoque un président du Sénat ([`sponsorshipBank`](sponsorships/sponsorshipBank.md)). Un journaliste d'investigation à moustache et lunettes évoque un journaliste réel ([`ghostAssistants`](affair/ghostAssistants.md)).
3. **Dire où regarde chacun.** Quand la scène réagit au candidat, le personnage principal le regarde, c'est-à-dire regarde le spectateur, et les témoins aussi, sans poser ; les autres continuent ce qu'ils font. Sans cette consigne, tout le monde regarde l'objectif comme pour une photo de groupe, ou plus personne ([`marketGaffe`](polemic/marketGaffe.md)). Quand personne ne doit regarder le spectateur, l'écrire (« Nobody looks at the viewer »).
4. **Le candidat du joueur n'a ni visage ni genre.** Il est hors champ, la scène vue de sa place, avec un objet à lui au premier plan (sa tasse, ses tracts, le bord de son parapluie). Toute image de lui dans la scène, affiche, tract ou double numérique, n'a ni visage, ni cheveux, ni vêtement genré : pas de costume-cravate ([`sloganMeme`](buzz/sloganMeme.md)), une silhouette de lumière sans traits ([`aiDouble`](farFetched/aiDouble.md)), ou pas d'image du tout ([`stateAlgorithm`](farFetched/stateAlgorithm.md), [`mayorsCandidate`](sponsorships/mayorsCandidate.md)).
5. **Ce qui est permis** (PO, 30 et 31/10/2026) :
   - les ressemblances avec ce qui existe : interfaces, habillages de chaîne, monuments, modèles d'avions réels ;
   - les drapeaux tricolore et européen, l'écharpe tricolore et la Marianne, pour signaler un bâtiment officiel ou un élu ;
   - un léger fondu du dessin dans le papier aux bords et dans les coins, sans large marge blanche (PO, 01/11/2026, [`firstContact`](farFetched/firstContact.md)) ;
   - **les candidats parodiés du jeu, vus de dos** : leur silhouette, leur coupe et leur allure peuvent rappeler la personne réelle qu'ils parodient, jamais leur visage (PO, 04/11/2026, [`televisedDebate`](breakthrough/televisedDebate.md)).
6. **Ce qui reste interdit** : tout texte lisible ; un logo ou une couleur de parti ; un parti ou une association nommés ou reconnaissables ; un sosie d'une personne réelle ; le portrait d'un président réel au mur ; un vaisseau, un ordinateur ou un extraterrestre tiré d'un film connu.
7. **Le style** : pour le moment, **toutes les cartes sont en reportage dessiné** (décision du 30/10/2026). Le trait est celui de [`primeTime`](media/primeTime.md), la référence depuis le 04/11/2026 : un dessin de reportage plus propre et plus calme que celui d'[`oldTweet`](polemic/oldTweet.md), aux contours nets, aux lavis clairs et chauds, le papier très visible. Le PO l'a préférée après deux essais avec elle ([`privateJet`](polemic/privateJet.md), [`ruralMayors`](support/ruralMayors.md)) ; les douze images régénérées avant, avec `oldTweet` (traits de crayon nerveux et repassés, hachures d'encre), restent telles quelles. C'est un dessin de reportage de presse, entre l'esquisse et le réalisme : des gens dessinés d'après nature, aux proportions et aux visages réalistes, aux expressions naturelles, jamais une BD ni une caricature. [`inflatedInvoices`](affair/inflatedInvoices.md), [`rivalLeak`](attack/rivalLeak.md) et [`televisedDebate`](breakthrough/televisedDebate.md) tiennent cet équilibre ; le premier essai de [`danceVideo`](buzz/danceVideo.md) a basculé dans la BD, avec des visages hilares et des corps caoutchouteux (PO, 04/11/2026). Les couleurs peuvent être un peu plus saturées par endroits, un vêtement, une lumière, un drapeau, en restant transparentes et dans la palette de l'app (PO, 04/11/2026, après [`danceVideo`](buzz/danceVideo.md), juste mais pâle). L'affiche lithographique et la BD semi-réaliste restent décrites dans #159, pour une image qui les demanderait plus tard.
8. **Le ton** : observateur par défaut, sinon ironique, tendu ou chaleureux selon l'événement (lignes plus bas), adapté à la scène et à sa lumière.
9. **Ne jamais nommer un artiste ou un dessinateur vivant** : le style se décrit, il ne s'emprunte pas.

## Le prompt

Avec [`primeTime.webp`](../illustrations/media/primeTime.webp) comme seule image de référence, dans une nouvelle conversation (PO, 04/11/2026, après [`privateJet`](polemic/privateJet.md) et [`ruralMayors`](support/ruralMayors.md)). Avant elle, [`oldTweet.webp`](../illustrations/polemic/oldTweet.webp) a servi pour les douze premières régénérations du 04/11/2026, et [`mayorsCandidate.webp`](../illustrations/sponsorships/mayorsCandidate.webp) le temps d'un essai, sorti trop dépouillé ([`inflatedInvoices`](affair/inflatedInvoices.md)). La présentatrice de `primeTime` évoque le type des présentatrices du journal du soir : la première ligne interdit de reprendre son visage ou sa coiffure, pour qu'elle ne passe pas aux autres cartes. Jamais une image qui porte une ressemblance voulue, comme [`sponsorThreatened`](sponsorships/sponsorThreatened.md) : la référence peut passer ses visages à l'image. Les quatre premières lignes tiennent le rendu dessiné : la première décrit le trait attendu, la deuxième garde le décor esquissé quand il est chargé, la troisième ferme les dérives des deux côtés (photo, peinture numérique, pointillés et filtre de texture d'un côté ; BD, caricature et livre pour enfants de l'autre) et la quatrième garde des gens réalistes aux expressions naturelles, même dans le rire ou les larmes. Jusqu'au 04/11/2026, la quatrième demandait des visages « exactement comme les vêtements », en aplats : sur les scènes joyeuses, elle tirait vers la BD. Le prompt ne nomme pas le fichier : une ligne qui demandait le titre de la carte comme nom (« Factures gonflées.png ») n'a rien changé au téléchargement ([`inflatedInvoices`](affair/inflatedInvoices.md), 04/11/2026), et elle a été retirée.

```
Use the attached image as the style reference and copy its drawing: a realistic reportage drawing made on the spot for a newspaper, with quick, nervous pencil lines, often drawn twice, ink hatching in the shadows, transparent watercolour washes that spill a little over the lines, and the warm paper showing through. Not the same scene and not the same people: never reuse the face or the hair of the woman in the reference.
Like in the reference, the setting can be full when the story needs it, with the things that say where we are and what is happening, but each one is sketched with a few pencil lines and a light wash, never rendered or finished, and the drawing gets looser and paler towards the edges until it fades into the bare paper.
This must look like a drawing made by hand on paper by a press illustrator, halfway between a quick sketch and a realistic picture: never a photograph, a film poster or a digital painting, and never a cartoon, a comic strip, a caricature or a children's book illustration. Continuous lines, never dotted or dashed outlines; no uniform texture, speckles or hatching filter laid over the picture; no glossy highlights, no smooth gradients, in the sky and on the walls too. Colour can be rich in places, on a piece of clothing, a light or a flag, but it stays transparent and within the palette below. The fade into the paper at the edges stays narrow, without a wide white margin. No blur and no depth-of-field effect: everything, the foreground included, is drawn sharp, like a sketch made on the spot.
People are drawn from life with realistic anatomy and proportions, like in the reference: faces shaped with pencil lines, hatching and light washes, a little more finished than the background but never photographic (no photographic skin, no airbrushed or digital-painting look). Expressions stay natural and restrained, even in laughter or tears: no exaggerated grins, no wide-open mouths full of teeth, no rubbery or cartoonish faces.

Editorial illustration, landscape 16:9 (1536 × 864 px), the scene filling the frame, with only a light fade into the paper at the edges. [SCENE: the event as a single moment in a French setting in 2027. The player's candidate stays off-camera: in the foreground, only [an object of the candidate's]. In the right (or left) third, the main character, [age, body, face, haircut, clothes], [action], looking at the viewer [or not], their face above mid-height. Around: each person described the same way, with where they look. Nothing on [the objects of the scene] is readable.]

Style: Reportage drawing made on the spot, like a press illustrator or courtroom sketch artist: pencil and ink with loose watercolour washes, lively unfinished lines, white paper showing through.

Palette: navy #13203F, vellum #F5EFE1, gold #A9802A, brick #B5523B, ochre #D9A441, sage #8FA58A, slate #5E7186, sand #DCC8A4, warm grey #8C8279; use 4 to 6 of them, subtle warm paper grain.

Tone: [observant / ironic / tense / warm, with the light that goes with it]

Constraints: realistic proportions, natural expressions, never cartoonish or caricatured faces, drawn like the rest of the illustration and never photographic; people of varied ages, genders, origins and body types (heavy, stocky, round, tall, short, wiry, not only slim), each with a distinct face and haircut (no two people alike), drawn with respect and never as a joke; anatomically correct hands with exactly five fingers, few hands visible, the others in pockets, behind objects or out of frame; no readable text anywhere ([the objects of the scene] stay unreadable); no captions or speech bubbles; no logos or political party colours; no recognisable real person, no lookalike of a real politician [or of the trade in the scene]; no explicit violence; no photographic rendering, no blur or bokeh, no dotted outlines, no texture or hatching filter over the picture, no oil-paint texture, no wide white margin or frame (a light fade into the paper at the edges is fine).

Format: if 16:9 is not available, make 1536 × 1024 and keep the top 80 px and the bottom 80 px free of anything important (faces, hands, the main action): they will be cropped.
```

## Une ressemblance voulue

Le PO peut prêter à un personnage les traits d'une personne réelle, un proche ou lui-même, d'après une photo, avec son accord. Jamais la photo jointe à la scène : d'abord un portrait dessiné d'après la photo, puis la scène avec ce portrait. Ni la photo ni le portrait ne vont dans ce dépôt. Les prompts des deux étapes, les règles et les huit cartes de la première série sont dans le [gabarit de la ressemblance voulue](gabarit-ressemblance.md).

## Les lignes de ton

| Ton | Quand | Ligne à coller, à adapter à la scène |
| --- | --- | --- |
| Observateur (par défaut) | La plupart des événements | `Tone: observant and neutral, late-morning daylight.` |
| Ironique | Gaffes, buzz, polémiques légères | `Tone: gently ironic, postures slightly exaggerated but never the faces, soft light.` |
| Tendu | Crises, affaires, attaques | `Tone: tense, dusk palette, colder light, hard shadows.` |
| Chaleureux | Soutiens, coups de projecteur | `Tone: warm, soft afternoon sun, light warm colours.` |

## Quand le rendu dérive

Le générateur revient souvent à une photo, à une peinture numérique sous un filtre de hachures, à une affiche de film ou à un premier plan flou. Dans l'ordre :

1. **Un message de correction, dans la même conversation**, qui garde la scène et ne change que le rendu (il a suffi pour [`starEndorsement`](breakthrough/starEndorsement.md), [`ghostAssistants`](affair/ghostAssistants.md) et [`familyJob`](affair/familyJob.md), où il ajoutait : « Every outline is a continuous pencil or ink line: no dotted or dashed outlines anywhere, and no mottled or speckled texture laid over the furniture ») :

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
