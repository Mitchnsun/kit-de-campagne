# Gabarit de la ressemblance voulue

Le PO peut prêter à un personnage les traits d'une personne réelle, un proche ou lui-même, d'après une photo. Ce gabarit donne les prompts pour le faire, en deux étapes, tels qu'ils ont marché sur la première série (huit cartes, en bas de page). Il ne remplace pas le [gabarit de prompt](gabarit.md) : la scène s'écrit comme d'habitude, ce gabarit n'y ajoute que la ressemblance.

Comme partout dans le kit, les explications sont en français et les prompts en anglais. Dans les prompts, les crochets marquent ce qui est à remplir ou à choisir.

## Avant de commencer

- **L'accord de la personne**, confirmé par le PO, avant que l'image entre dans ce dépôt.
- **Rien de privé dans ce dépôt.** Ni la photo, ni le portrait dessiné de l'étape 1. La fiche ne nomme personne : « une photo de famille du PO », ou « un portrait dessiné du PO » quand c'est lui.
- **Le rôle s'adapte à la personne, jamais l'inverse.** Sa silhouette, son visage, sa coiffure et ses lunettes restent les siens.
  - Retirer de la scène ce qui la contredirait : la lanceuse d'alerte n'est plus « corpulente » et ne porte plus de lunettes ([`whistleblower`](breakthrough/whistleblower.md)), l'ingénieur perd sa queue de cheval ([`stateAlgorithm`](farFetched/stateAlgorithm.md)).
  - Changer plutôt l'âge du rôle : le doctorant devient un astronome de la soixantaine ([`comet`](farFetched/comet.md)).
  - La variété des corps et des âges passe par les autres personnages. Aucun d'eux ne doit ressembler à la personne : l'adjoint devient une adjointe, pour ne pas avoir deux hommes de la soixantaine côte à côte ([`sponsorThreatened`](sponsorships/sponsorThreatened.md)).
- **Jamais la photo jointe à la scène.** Jointe directement, elle est recopiée et le visage ressort photographique au milieu du dessin ([`ministerResigns`](crisis/ministerResigns.md), [`donorsDinner`](support/donorsDinner.md)). D'où les deux étapes : un portrait dessiné d'après la photo, puis la scène avec ce portrait.
- **Une même personne peut servir plusieurs cartes**, avec le même portrait (accepté par le PO, [`firstContact`](farFetched/firstContact.md)).

## Choisir la photo

- **Le visage net et bien éclairé**, de face ou de trois quarts, sans lunettes de soleil ni main devant.
- **Le personnage aura l'âge de la photo.** Choisir une photo de l'âge voulu, ou adapter le rôle à cet âge.
- **Une photo de groupe convient.** Désigner la personne par sa place dans la photo, et demander d'ignorer les autres ([`donorsDinner`](support/donorsDinner.md)).
- **Les accessoires de la photo** (un collier, une cravate) passent dans le dessin si le prompt ne dit rien. Les retirer, ou les garder, en le disant : « without the necklace » ([`whistleblower`](breakthrough/whistleblower.md)), « a wide navy tie like in the photograph » ([`ministerResigns`](crisis/ministerResigns.md)).

## Étape 1 : le portrait dessiné

Dans une nouvelle conversation, avec deux images jointes, dans cet ordre : [`primeTime.webp`](../illustrations/media/primeTime.webp) pour le style, puis la photo.

```
Use the first attached image as the style reference: the same pencil and ink drawing with loose watercolour washes and warm paper grain. Never reuse the face or the hair of the woman in the reference.
The second attached image is a photograph. Draw a new portrait of [this man / this woman / the man with white hair on the right of the photograph], as a press illustrator or courtroom sketch artist would draw a quick likeness from life: head and shoulders, three-quarter view, with [a calm, serious / a warm, smiling] expression, in [plain clothes, e.g. a plain dark top without the necklace], on plain warm paper with no background.[ Ignore the other people in the photograph.]
Do not trace or copy the photograph. Redraw the face from scratch and keep only what makes [him / her] recognisable: the shape of the face, [the hair: colour, length, texture and hairline], the eyebrows, the eyes, the nose and the mouth[, the smile, the beard, the glasses]. Everything is drawn with ink outlines, hatching and flat watercolour washes, realistic and drawn from life like the faces in the reference image, never a caricature. No photographic skin, no photographic lighting, no detail taken over from the photo's texture.
Format: square, 1024 × 1024 px.
```

À remplir :

| Crochet | Ce qu'on y met |
| --- | --- |
| La personne | « this man » ou « this woman » quand elle est seule sur la photo ; sinon sa place et un trait qui la distingue (« the man with white hair on the right of the photograph ») |
| L'expression | Celle du rôle : calme et sérieuse, chaleureuse, inquiète. Elle peut changer dans la scène |
| Les vêtements | Simples et neutres : la scène habillera le personnage. Dire ce qu'on retire de la photo |
| Ce qui la rend reconnaissable | La forme du visage et la coiffure toujours, puis ce qui compte chez elle : le sourire, les sourcils, la barbe, les lunettes |
| « Ignore the other people » | Seulement pour une photo de groupe |

Si la silhouette compte pour le rôle (une carrure, une grande taille), on peut demander un portrait à mi-corps : remplacer « head and shoulders, three-quarter view » par « half-length, from the head to the waist, three-quarter view, keeping [his / her] build ». Cela n'a pas encore été essayé.

### Plusieurs portraits d'un coup

Le PO peut faire tous les portraits d'une série dans une seule conversation (04/11/2026) : la référence de style d'abord, puis les photos, numérotées dans l'ordre où elles sont jointes. Le prompt nomme chaque personne par sa photo et sa place, et demande une image carrée par personne, l'une après l'autre. Si le générateur n'en fait qu'une par réponse, on écrit « next » pour la suivante. Une même personne sur deux photos donne deux portraits : le PO garde le meilleur.

```
Use the first attached image as the style reference: the same pencil and ink drawing with loose watercolour washes and warm paper grain. Never reuse the face or the hair of the woman in the reference.
The other attached images are photographs, numbered in the order they are attached: photo 1 is the second attached image, photo 2 the third, and so on. Draw [N] separate portraits, each one as its own square image, 1024 × 1024 px, in this order:
1. [The person, e.g. the man on the left of photo 1]: [what makes him or her recognisable], [expression], in [plain clothes].
2. …
For each portrait: draw a new likeness as a press illustrator or courtroom sketch artist would from life, head and shoulders, three-quarter view, at the same age as in the photograph, on plain warm paper with no background. Ignore everyone else in the photographs. Do not trace or copy the photographs: redraw each face from scratch and keep only what makes the person recognisable: the shape of the face, the hair (colour, length, texture and hairline), the eyebrows, the eyes, the nose, the mouth, the smile and the beard. Everything is drawn with ink outlines, hatching and flat watercolour washes, realistic and drawn from life like the faces in the reference image, never a caricature. No photographic skin, no photographic lighting, no detail taken over from the photos' texture, no readable text anywhere, nothing from the prints on the clothes.
If you can only make one image per answer, make portrait 1 now, then the next one each time I write "next".
```

## Vérifier le portrait

Avant la scène, le PO vérifie deux choses.

1. **Le portrait est dessiné** : trait d'encre, hachures et lavis, comme les visages de `primeTime`. Un portrait déjà photographique donne une scène où le visage l'est aussi ([`whistleblower`](breakthrough/whistleblower.md)).
2. **Il est ressemblant**, aux yeux du PO, et si possible de la personne.

Si le rendu est trop photographique, envoyer ce message dans la même conversation. Il reprend le message de correction des scènes ; il n'a pas encore été essayé sur un portrait :

```
Keep the same person, the same pose and the same likeness, but draw the portrait much more simply, like the faces in the first attached image: a quick sketch on warm paper, ink outlines, a few hatching strokes and flat watercolour washes, plenty of white paper showing through; no photographic skin, no realistic wrinkles or pores, no photographic lighting, no smooth shading.
```

Si la ressemblance se perd, régénérer dans une nouvelle conversation plutôt que corriger : un visage se corrige mal ([`primeTime`](media/primeTime.md)).

## Garder le portrait

- **Hors de ce dépôt**, chez le PO, à côté de la photo.
- **Il resservira** pour toute autre carte avec la même personne. Le portrait de [`pundit`](attack/pundit.md) a servi pour [`firstContact`](farFetched/firstContact.md), celui de [`comet`](farFetched/comet.md) pour [`sponsorThreatened`](sponsorships/sponsorThreatened.md).
- **Le PO peut fournir un portrait dessiné de lui-même** : on passe alors directement à l'étape 2 ([`stateAlgorithm`](farFetched/stateAlgorithm.md)).

## Étape 2 : la scène

Dans une nouvelle conversation, avec deux images jointes, dans cet ordre : [`primeTime.webp`](../illustrations/media/primeTime.webp) pour le style, puis le portrait dessiné. La scène s'écrit avec le [gabarit de prompt](gabarit.md), avec quatre changements :

1. la première ligne dit « the first attached image » ;
2. la ligne de la ressemblance vient en deuxième ;
3. dans la scène, le personnage est « the man (the woman) from the portrait », avec son âge, ses vêtements, son geste et son regard, mais sans corps, visage ni coiffure qui contrediraient le portrait ;
4. les contraintes disent « apart from [le rôle], no recognisable real person ».

Le prompt complet, à copier :

```
Use the first attached image as the style reference and copy its drawing: a realistic reportage drawing made on the spot for a newspaper, with quick, nervous pencil lines, often drawn twice, ink hatching in the shadows, transparent watercolour washes that spill a little over the lines, and the warm paper showing through. Not the same scene and not the same people: never reuse the face or the hair of the woman in the reference.
Like in the reference, the setting can be full when the story needs it, with the things that say where we are and what is happening, but each one is sketched with a few pencil lines and a light wash, never rendered or finished, and the drawing gets looser and paler towards the edges until it fades into the bare paper.
Use the second attached image, a drawn portrait, only as the likeness reference for [the role, e.g. the mayor]: give [him / her] this [man's / woman's] features, [the hair, e.g. short grey-white hair] and [light stubble / a short beard / clean-shaven], and draw [his / her] face with the same ink lines and washes as the other people in the scene. Keep the likeness through the drawing, never through photographic detail.
This must look like a drawing made by hand on paper by a press illustrator, halfway between a quick sketch and a realistic picture: never a photograph, a film poster or a digital painting, and never a cartoon, a comic strip, a caricature or a children's book illustration. Continuous lines, never dotted or dashed outlines; no uniform texture, speckles or hatching filter laid over the picture; no glossy highlights, no smooth gradients, in the sky and on the walls too. Colour can be rich in places, on a piece of clothing, a light or a flag, but it stays transparent and within the palette below. The fade into the paper at the edges stays narrow, without a wide white margin. No blur and no depth-of-field effect: everything, the foreground included, is drawn sharp, like a sketch made on the spot.
People are drawn from life with realistic anatomy and proportions, like in the reference: faces shaped with pencil lines, hatching and light washes, a little more finished than the background but never photographic (no photographic skin, no airbrushed or digital-painting look). Expressions stay natural and restrained, even in laughter or tears: no exaggerated grins, no wide-open mouths full of teeth, no rubbery or cartoonish faces.

Editorial illustration, landscape 16:9 (1536 × 864 px), the scene filling the frame, with only a light fade into the paper at the edges. [SCENE, written with the prompt template. The character with the likeness: "In the right (or left) third, [the role], the [man / woman] from the portrait, in [his / her] [sixties], in [clothes], [action], looking at the viewer, [his / her] face above mid-height." The other people described one by one, none of them like the person from the portrait. Nothing on [the objects of the scene] is readable.]

Style: Reportage drawing made on the spot, like a press illustrator or courtroom sketch artist: pencil and ink with loose watercolour washes, lively unfinished lines, white paper showing through.

Palette: navy #13203F, vellum #F5EFE1, gold #A9802A, brick #B5523B, ochre #D9A441, sage #8FA58A, slate #5E7186, sand #DCC8A4, warm grey #8C8279; use 4 to 6 of them, subtle warm paper grain.

Tone: [observant / ironic / tense / warm, with the light that goes with it]

Constraints: realistic proportions, natural expressions, never cartoonish or caricatured faces, drawn like the rest of the illustration and never photographic; people of varied ages, genders, origins and body types (heavy, stocky, round, tall, short, wiry, not only slim), each with a distinct face and haircut (no two people alike), drawn with respect and never as a joke; anatomically correct hands with exactly five fingers, few hands visible, the others in pockets, behind objects or out of frame; no readable text anywhere ([the objects of the scene] stay unreadable); no captions or speech bubbles; no logos or political party colours; apart from [the role], no recognisable real person and no lookalike of a real politician [or of the trade in the scene]; no explicit violence; no photographic rendering, no blur or bokeh, no dotted outlines, no texture or hatching filter over the picture, no oil-paint texture, no wide white margin or frame (a light fade into the paper at the edges is fine).

Format: if 16:9 is not available, make 1536 × 1024 and keep the top 80 px and the bottom 80 px free of anything important (faces, hands, the main action): they will be cropped.
```

### Si le visage ressort plus fini que les autres

Le générateur soigne souvent le visage ressemblant plus que le reste. Dans le message de correction ou le prompt revu (voir « Quand le rendu dérive » dans le [gabarit](gabarit.md)), ajouter à la ligne des visages qu'il est dessiné aussi simplement qu'un autre personnage de la scène. Le prompt revu de [`firstContact`](farFetched/firstContact.md), qui a donné l'image retenue, le demandait, avec un rendu plus léger :

```
[the role]'s face is drawn as simply as [other people of the scene, e.g. the gendarmes]' faces.
```

## Dans la fiche

Les phrases à reprendre, sans nom ni rien qui désigne la personne :

- **« Prompt complet »** : « En deux étapes, pour que la scène ne voie jamais la photo de famille. » Puis une sous-section par étape :
  - **Étape 1** : « Dans une nouvelle conversation, avec deux images jointes : `primeTime.webp` pour le style, puis une photo de famille du PO. Le portrait obtenu n'est pas dans ce dépôt. »
  - **Étape 2** : « Dans une nouvelle conversation, avec deux images jointes : `primeTime.webp` pour le style, puis le portrait dessiné de l'étape 1 pour la ressemblance de [rôle]. »
  - **Avec un portrait déjà fait**, une seule étape : « … puis le portrait dessiné déjà fait pour [`<carte>`](../<catégorie>/<carte>.md), d'après une photo de famille du PO, pour la ressemblance de [rôle]. »
- **« Décisions prises sur cette image »** : « **[Le rôle] reprend les traits d'une photo de famille fournie par le PO**, avec l'accord de la personne, confirmé par le PO (JJ/MM/AAAA). Ni la photo ni le portrait dessiné ne sont dans ce dépôt. » Puis ce que le rôle a changé pour suivre la personne : l'âge, la silhouette, un autre personnage modifié pour ne pas lui ressembler.
- **« Relecture »** : « Aucun sosie d'une personne réelle, hors la ressemblance voulue de [rôle]. »

## La première série

| Carte | Rôle | Comment | Ce qu'on en retient |
| --- | --- | --- | --- |
| [`ministerResigns`](crisis/ministerResigns.md) | Le secrétaire d'État | Photo jointe à la scène, avant la méthode | Le visage ressort presque photographique ; régénérée le 04/11/2026 avec son propre portrait dessiné, fait d'après la même photo |
| [`donorsDinner`](support/donorsDinner.md) | L'hôte | Photo de groupe jointe à la scène, la personne désignée par sa place | Rendu très réaliste, gardé par le PO ; c'est ce qui a mené aux deux étapes |
| [`pundit`](attack/pundit.md) | L'éditorialiste | Les deux étapes, au premier essai | La méthode de référence ; le portrait a resservi |
| [`whistleblower`](breakthrough/whistleblower.md) | La lanceuse d'alerte | Les deux étapes ; le rôle perd « corpulente » et les lunettes | Le visage reste presque photographique : vérifier le portrait avant la scène |
| [`firstContact`](farFetched/firstContact.md) | Le général | Le portrait de `pundit` | À l'essai 2, le visage était plus fini que les autres ; le prompt revu le demande aussi simple que ceux des gendarmes |
| [`stateAlgorithm`](farFetched/stateAlgorithm.md) | L'ingénieur | Un portrait dessiné fourni par le PO : l'étape 2 seule | Le rôle perd « corpulent » et la queue de cheval ; un autre personnage devient corpulent |
| [`comet`](farFetched/comet.md) | Un astronome | Les deux étapes ; le doctorant devient un astronome de la soixantaine | Le rôle suit l'âge de la personne |
| [`sponsorThreatened`](sponsorships/sponsorThreatened.md) | Le maire | Le portrait de `comet` | L'adjoint devient une adjointe, pour ne pas avoir deux hommes de la soixantaine côte à côte |
| [`podcast`](media/podcast.md) | L'animatrice | Un portrait dessiné fourni par le PO : l'étape 2 seule (04/11/2026) | Le rôle prend les cheveux longs et ondulés du portrait ; la présentatrice de `primeTime`, gardée telle quelle, s'en distingue par ses cheveux lissés au brushing |
| [`womensDay`](rendezvous/womensDay.md) | La porte-parole | Un portrait dessiné fourni par le PO : l'étape 2 seule (04/11/2026) | Le rôle prend l'âge et les cheveux courts et bouclés du portrait ; la syndicaliste et l'étudiante gardent des coupes distinctes |
| [`taxReturn`](rendezvous/taxReturn.md) | La journaliste et le jeune reporter | Deux portraits dessinés fournis par le PO, joints ensemble à la scène : l'étape 2 seule (04/11/2026) | Le prompt dit quelle image va à quel rôle, dans l'ordre où elles sont jointes |
| [`cobbledClassic`](chance/cobbledClassic.md) | Le coureur vainqueur | Un portrait dessiné fourni par le PO, peut-être la même personne que le reporter de `taxReturn` : l'étape 2 seule (04/11/2026) | Le rôle passe du lointain au premier plan, casque à la main, pour qu'on voie le visage |
| [`filmAward`](chance/filmAward.md) | Le maire | Un portrait dessiné fourni par le PO, la même personne que le secrétaire d'État de `ministerResigns`, avec son accord : l'étape 2 seule (04/11/2026) | Le rôle perd les cheveux gris et les lunettes pour suivre le portrait |
| [`factoryInvite`](field/factoryInvite.md) | Le directeur d'usine | Un portrait dessiné fourni par le PO : l'étape 2 seule (05/11/2026) | Le rôle perd les lunettes et prend les cheveux blancs du portrait ; poli mais pressé |
| [`creuseSurgery`](field/creuseSurgery.md) | La médecin qui part | Un portrait dessiné fourni par le PO : l'étape 2 seule (05/11/2026) | Le portrait sourit, la scène la veut émue : le prompt le dit en toutes lettres ; elle passe au premier plan pour qu'on voie son visage |
| [`blackFriday`](polemic/blackFriday.md) | Le jeune militant écologiste | Un portrait dessiné fourni par le PO : l'étape 2 seule (05/11/2026) | Le rôle perd la barbe rousse et le bonnet pour suivre le portrait |
| [`clockChange`](buzz/clockChange.md) | L'horloger à la retraite | Un portrait dessiné fourni par le PO : l'étape 2 seule (05/11/2026) | Le rôle perd le bouc et l'origine écrite pour suivre le portrait ; le portrait sourit, la bouche ouverte, le prompt la veut à peine ouverte |
