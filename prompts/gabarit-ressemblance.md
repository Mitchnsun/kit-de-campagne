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

Dans une nouvelle conversation, avec deux images jointes, dans cet ordre : [`oldTweet.webp`](../illustrations/polemic/oldTweet.webp) pour le style, puis la photo.

```
Use the first attached image as the style reference: the same pencil and ink drawing with loose watercolour washes and warm paper grain.
The second attached image is a photograph. Draw a new portrait of [this man / this woman / the man with white hair on the right of the photograph], as a press illustrator or courtroom sketch artist would draw a quick likeness from life: head and shoulders, three-quarter view, with [a calm, serious / a warm, smiling] expression, in [plain clothes, e.g. a plain dark top without the necklace], on plain warm paper with no background.[ Ignore the other people in the photograph.]
Do not trace or copy the photograph. Redraw the face from scratch and keep only what makes [him / her] recognisable: the shape of the face, [the hair: colour, length, texture and hairline], the eyebrows, the eyes, the nose and the mouth[, the smile, the beard, the glasses]. Everything is drawn with ink outlines, hatching and flat watercolour washes, simplified like the faces in the reference image. No photographic skin, no photographic lighting, no detail taken over from the photo's texture.
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

## Vérifier le portrait

Avant la scène, le PO vérifie deux choses.

1. **Le portrait est dessiné** : trait d'encre, hachures et lavis, comme les visages de `oldTweet`. Un portrait déjà photographique donne une scène où le visage l'est aussi ([`whistleblower`](breakthrough/whistleblower.md)).
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

Dans une nouvelle conversation, avec deux images jointes, dans cet ordre : [`oldTweet.webp`](../illustrations/polemic/oldTweet.webp) pour le style, puis le portrait dessiné. La scène s'écrit avec le [gabarit de prompt](gabarit.md), avec quatre changements :

1. la première ligne dit « the first attached image » ;
2. la ligne de la ressemblance vient en deuxième ;
3. dans la scène, le personnage est « the man (the woman) from the portrait », avec son âge, ses vêtements, son geste et son regard, mais sans corps, visage ni coiffure qui contrediraient le portrait ;
4. les contraintes disent « apart from [le rôle], no recognisable real person ».

Le prompt complet, à copier :

```
Use the first attached image as the style reference: the same pencil and ink drawing with loose watercolour washes and warm paper grain. Not the same scene.
Use the second attached image, a drawn portrait, only as the likeness reference for [the role, e.g. the mayor]: give [him / her] this [man's / woman's] features, [the hair, e.g. short grey-white hair] and [light stubble / a short beard / clean-shaven], and draw [his / her] face with the same ink lines and washes as the other people in the scene. Keep the likeness through the drawing, never through photographic detail.
This must look like a drawing made by hand on paper, never like a photograph or a film poster: the people are drawn with ink lines and flat washes, not modelled; the background is only suggested with a few pencil lines and light, transparent washes, so that the warm paper shows through; the drawing may fade lightly into the bare paper at the edges and in the corners, as on a sketchbook page, the fade staying narrow, without a wide white margin. Lighter and less saturated than a painting: no dense colour, no glossy highlights, no hatching filter laid over a finished image. No blur and no depth-of-field effect: everything, the foreground included, is drawn sharp with ink lines, like a sketch made on the spot.
Faces are drawn exactly like the clothes and the background: ink outlines, a few hatching strokes and flat watercolour washes for the skin, with the same level of detail as the rest of the drawing. No photographic skin, no realistic wrinkles or pores, no airbrushed or digital-painting look on the faces.

Editorial illustration, landscape 16:9 (1536 × 864 px), the scene filling the frame, with only a light fade into the paper at the edges. [SCENE, written with the prompt template. The character with the likeness: "In the right (or left) third, [the role], the [man / woman] from the portrait, in [his / her] [sixties], in [clothes], [action], looking at the viewer, [his / her] face above mid-height." The other people described one by one, none of them like the person from the portrait. Nothing on [the objects of the scene] is readable.]

Style: Reportage drawing made on the spot, like a press illustrator or courtroom sketch artist: pencil and ink with loose watercolour washes, lively unfinished lines, white paper showing through.

Palette: navy #13203F, vellum #F5EFE1, gold #A9802A, brick #B5523B, ochre #D9A441, sage #8FA58A, slate #5E7186, sand #DCC8A4, warm grey #8C8279; use 4 to 6 of them, subtle warm paper grain.

Tone: [observant / ironic / tense / warm, with the light that goes with it]

Constraints: realistic proportions, expressive but not caricatured faces, drawn like the rest of the illustration and never photographic; people of varied ages, genders, origins and body types (heavy, stocky, round, tall, short, wiry, not only slim), each with a distinct face and haircut (no two people alike), drawn with respect and never as a joke; anatomically correct hands with exactly five fingers, few hands visible, the others in pockets, behind objects or out of frame; no readable text anywhere ([the objects of the scene] stay unreadable); no captions or speech bubbles; no logos or political party colours; apart from [the role], no recognisable real person and no lookalike of a real politician [or of the trade in the scene]; no explicit violence; no photographic rendering, no blur or bokeh, no hatching filter over a finished digital painting, no oil-paint texture, no wide white margin or frame (a light fade into the paper at the edges is fine).

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
  - **Étape 1** : « Dans une nouvelle conversation, avec deux images jointes : `oldTweet.webp` pour le style, puis une photo de famille du PO. Le portrait obtenu n'est pas dans ce dépôt. »
  - **Étape 2** : « Dans une nouvelle conversation, avec deux images jointes : `oldTweet.webp` pour le style, puis le portrait dessiné de l'étape 1 pour la ressemblance de [rôle]. »
  - **Avec un portrait déjà fait**, une seule étape : « … puis le portrait dessiné déjà fait pour [`<carte>`](../<catégorie>/<carte>.md), d'après une photo de famille du PO, pour la ressemblance de [rôle]. »
- **« Décisions prises sur cette image »** : « **[Le rôle] reprend les traits d'une photo de famille fournie par le PO**, avec l'accord de la personne, confirmé par le PO (JJ/MM/AAAA). Ni la photo ni le portrait dessiné ne sont dans ce dépôt. » Puis ce que le rôle a changé pour suivre la personne : l'âge, la silhouette, un autre personnage modifié pour ne pas lui ressembler.
- **« Relecture »** : « Aucun sosie d'une personne réelle, hors la ressemblance voulue de [rôle]. »

## La première série

| Carte | Rôle | Comment | Ce qu'on en retient |
| --- | --- | --- | --- |
| [`ministerResigns`](crisis/ministerResigns.md) | Le secrétaire d'État | Photo jointe à la scène, avant la méthode | Le visage ressort presque photographique |
| [`donorsDinner`](support/donorsDinner.md) | L'hôte | Photo de groupe jointe à la scène, la personne désignée par sa place | Rendu très réaliste, gardé par le PO ; c'est ce qui a mené aux deux étapes |
| [`pundit`](attack/pundit.md) | L'éditorialiste | Les deux étapes, au premier essai | La méthode de référence ; le portrait a resservi |
| [`whistleblower`](breakthrough/whistleblower.md) | La lanceuse d'alerte | Les deux étapes ; le rôle perd « corpulente » et les lunettes | Le visage reste presque photographique : vérifier le portrait avant la scène |
| [`firstContact`](farFetched/firstContact.md) | Le général | Le portrait de `pundit` | À l'essai 2, le visage était plus fini que les autres ; le prompt revu le demande aussi simple que ceux des gendarmes |
| [`stateAlgorithm`](farFetched/stateAlgorithm.md) | L'ingénieur | Un portrait dessiné fourni par le PO : l'étape 2 seule | Le rôle perd « corpulent » et la queue de cheval ; un autre personnage devient corpulent |
| [`comet`](farFetched/comet.md) | Un astronome | Les deux étapes ; le doctorant devient un astronome de la soixantaine | Le rôle suit l'âge de la personne |
| [`sponsorThreatened`](sponsorships/sponsorThreatened.md) | Le maire | Le portrait de `comet` | L'adjoint devient une adjointe, pour ne pas avoir deux hommes de la soixantaine côte à côte |
