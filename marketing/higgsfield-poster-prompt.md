# Higgsfield Image Prompt — Shree Fabrics Raksha Bandhan Poster

**Model:** `nano_banana_pro` (routes to nano_banana_2) — chosen because it is the strongest option for rendering readable text inside an image.
**Aspect ratio:** `4:5` — the tallest format Instagram allows in the feed, so it occupies the most screen height as people scroll. Use `9:16` for Story/WhatsApp Status and `1:1` only if you specifically need a square.
**Resolution:** `4k` → outputs **3712 × 4608 px**. Worth it: the extra pixels sharpen the small text (the phone number especially), and it gives you room to print the poster or crop it without softening. Takes ~40s vs ~15s for `1k`.
**Count:** 2–4 variants per run — text rendering is a lottery, so always generate several and pick the one where the spelling is clean.

### Size reference

| Aspect ratio | Resolution setting | Output pixels | Use for |
|---|---|---|---|
| `4:5` | `4k` | 3712 × 4608 | **Instagram/Facebook feed — the default** |
| `9:16` | `4k` | 3392 × 6016 approx. | Story, Reel cover, WhatsApp Status |
| `1:1` | `4k` | 4096 × 4096 approx. | Profile grid, square print |
| any | `1k` | ~1024 on the long edge | Quick draft to check the layout before committing to 4K |

---

## The Prompt

```
A premium Indian festive sale poster for a fabric store, tall vertical 4:5 portrait format, photorealistic product photography blended with elegant graphic design.

LAYOUT (top to bottom, using the full height of the tall frame):
- Top: an ornate gold mandala arch with hanging marigold garlands and small gold bells framing the top of the composition.
- Below the arch, small elegant gold serif text: "SHREE FABRICS" with a thin decorative gold rule underneath.
- Upper middle, headline in large elegant gold serif capitals: "RAKSHA BANDHAN SALE"
- Center of the frame, the single dominant element of the whole poster, in very large bold cream and gold letters with a subtle glow: "UP TO 50% OFF"
- Beneath that, a clean single line of smaller cream text: "Suit Sets | Dress Material | Silk | Cotton | Georgette"
- Lower third: the clothing arrangement.
- Bottom strip: a gold banner ribbon containing dark maroon text: "Call / WhatsApp +91 82958 86667"

VISUALS: the lower third displays UNSTITCHED PUNJABI SALWAR SUIT SETS, also called dress material sets. Each set is a neatly folded three piece coordinated group: a rectangular folded kurta top fabric, a matching folded salwar bottom fabric placed beside it, and a long embroidered dupatta scarf folded in a soft zigzag on top with its embroidered end and tassel trim visible. Four or five such suit sets are arranged in an overlapping fan across the lower third in rich jewel tones - deep maroon, emerald green, royal blue, saffron, magenta - each with delicate gold thread embroidery, floral block prints, and decorative borders. Behind them, two complete stitched salwar kameez suits hang on wooden hangers, each showing a knee length kurta with churidar pants and a draped dupatta over the shoulder. A delicate red and gold rakhi thread with beads rests on top of the front suit set. Scattered marigold petals and tiny diyas glowing warmly in the corners.

STYLE: deep maroon and gold color palette, luxurious festive Indian aesthetic, soft warm cinematic lighting, gold foil texture accents, subtle bokeh, high contrast so text is crisply readable, ultra detailed, sharp focus, 4K commercial advertising quality, clean uncluttered composition with generous vertical breathing space between each element.

CRITICAL - NO SAREES: absolutely no sarees anywhere in this image. No six yard draped saree, no saree pallu falling over a shoulder, no long single continuous drape of cloth, no saree mannequin display, no rolled fabric bolts. The garments must clearly read as salwar suit sets and dress material - separate kurta piece plus bottom piece plus dupatta - not as sarees.

IMPORTANT: fill the entire tall vertical frame edge to edge with the design, no letterboxing, no white borders, no empty dead space at top or bottom. All text must be spelled exactly as written, perfectly legible, correctly kerned English typography. No extra words, no gibberish text, no watermarks, no human faces.
```

---

## Why the prompt is built this way

| Technique | Reason |
|---|---|
| Explicit top-to-bottom layout list | Stops the model from inventing its own composition and burying the discount |
| Text in `"quotes"` | Signals to the model which strings are literal copy to render |
| "the dominant element of the whole poster" on 50% OFF | Forces visual hierarchy — the offer must read at thumbnail size |
| "high contrast so text is crisply readable" | Prevents gold-on-gold text that disappears |
| "no gibberish text, no watermarks, no human faces" | Image models love adding fake text and faces; faces also risk looking uncanny |
| "generous vertical breathing space" | Leaves room to crop for Stories without cutting words |
| "using the full height of the tall frame" + "fill the entire frame edge to edge, no letterboxing" | Tall formats tempt the model to render a square design with empty bands above and below — this forces it to use the whole canvas |
| The suit sets described **part by part** (kurta piece + salwar piece + dupatta) | "Suits" alone is ambiguous to an image model — it may render Western business suits or default to sarees. Naming the three pieces is what makes it render actual dress material |
| The `CRITICAL - NO SAREES` block | "Indian festive fabric shop" is so strongly associated with sarees in training data that the model reaches for them by default. Listing the specific saree cues to avoid (pallu, six-yard drape, rolled bolts) works better than just "no sarees" |

---

## Variations to try

**Story format (9:16)** — change `tall vertical 4:5 portrait format` to `extra tall vertical 9:16 format` and add:
`leave the top 20 percent and bottom 15 percent of the frame free of text for Instagram Story UI.`

**Emotional / lifestyle version** — replace the VISUALS block with:
`a warm candid moment of a sister tying a red and gold rakhi onto her brother's wrist, shot from behind and to the side so no faces are visible, she wears a vivid magenta silk saree with gold zari border, soft window light, shallow depth of field.`

**Minimal / modern version** — replace the STYLE block with:
`clean minimal design, cream and deep maroon palette, lots of negative space, single thin gold line accents, modern editorial typography, flat lay of three folded fabrics on a plain cream backdrop, soft even studio lighting.`

---

## Checklist before posting any generated poster

- [ ] **Phone number reads exactly `+91 82958 86667`** — this is the single most common thing AI image models garble. Zoom in and check every digit.
- [ ] **The garments read as suit sets, not sarees** — look for a separate top piece, bottom piece and dupatta. If you see one long continuous drape or a pallu over a shoulder, the model has slipped back to sarees; regenerate.
- [ ] "RAKSHA BANDHAN" and "SHREE FABRICS" are spelled correctly
- [ ] "50%" shows the percent sign, not a stray character
- [ ] No invented extra words floating in the background
- [ ] Text is readable when shrunk to thumbnail size

If any text is wrong, regenerate rather than posting — or fix the text layer in Canva over the generated background, which is the most reliable route for a poster carrying a phone number.
