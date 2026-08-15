# Higgsfield Image Prompt — Shree Fabrics Raksha Bandhan Poster

**Model:** `nano_banana_pro` (routes to nano_banana_2) — chosen because it is the strongest option for rendering readable text inside an image.
**Aspect ratio:** `1:1` for the Instagram feed. Use `9:16` for Story/WhatsApp Status and `16:9` for a Facebook cover.
**Count:** 2–4 variants per run — text rendering is a lottery, so always generate several and pick the one where the spelling is clean.

---

## The Prompt

```
A premium Indian festive sale poster for a fabric store, square format, photorealistic product photography blended with elegant graphic design.

LAYOUT (top to bottom):
- Top center: an ornate gold mandala arch with hanging marigold garlands and small gold bells framing the composition.
- Below the arch, small elegant gold serif text: "SHREE FABRICS" with a thin decorative gold rule underneath.
- Center headline in large elegant gold serif capitals: "RAKSHA BANDHAN SALE"
- Directly below, the dominant element of the whole poster, in very large bold cream and gold letters with a subtle glow: "UP TO 50% OFF"
- Beneath that, a clean single line of smaller cream text: "Silk | Cotton | Georgette | Chiffon | Suit Pieces"
- Bottom strip: a gold banner ribbon containing dark maroon text: "Call / WhatsApp +91 82958 86667"

VISUALS: a beautifully arranged stack of folded luxury sarees and fabric bolts in rich jewel tones - deep maroon, emerald green, royal blue, saffron, magenta - fanned across the lower third with visible silk sheen and gold zari borders. A delicate red and gold rakhi thread with beads rests on top of the fabric stack. Scattered marigold petals and tiny diyas glowing warmly in the corners.

STYLE: deep maroon and gold color palette, luxurious festive Indian aesthetic, soft warm cinematic lighting, gold foil texture accents, subtle bokeh, high contrast so text is crisply readable, ultra detailed, 4K commercial advertising quality, clean uncluttered composition with generous breathing space around the text.

IMPORTANT: all text must be spelled exactly as written, perfectly legible, correctly kerned English typography. No extra words, no gibberish text, no watermarks, no human faces.
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
| "generous breathing space" | Leaves room to crop for Stories without cutting words |

---

## Variations to try

**Story format (9:16)** — change the first line to `vertical poster, 9:16 format` and add:
`leave the top 20 percent and bottom 15 percent of the frame free of text for Instagram Story UI.`

**Emotional / lifestyle version** — replace the VISUALS block with:
`a warm candid moment of a sister tying a red and gold rakhi onto her brother's wrist, shot from behind and to the side so no faces are visible, she wears a vivid magenta silk saree with gold zari border, soft window light, shallow depth of field.`

**Minimal / modern version** — replace the STYLE block with:
`clean minimal design, cream and deep maroon palette, lots of negative space, single thin gold line accents, modern editorial typography, flat lay of three folded fabrics on a plain cream backdrop, soft even studio lighting.`

---

## Checklist before posting any generated poster

- [ ] **Phone number reads exactly `+91 82958 86667`** — this is the single most common thing AI image models garble. Zoom in and check every digit.
- [ ] "RAKSHA BANDHAN" and "SHREE FABRICS" are spelled correctly
- [ ] "50%" shows the percent sign, not a stray character
- [ ] No invented extra words floating in the background
- [ ] Text is readable when shrunk to thumbnail size

If any text is wrong, regenerate rather than posting — or fix the text layer in Canva over the generated background, which is the most reliable route for a poster carrying a phone number.
