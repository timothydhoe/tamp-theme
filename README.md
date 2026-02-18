# Tamp

**A collection of dark themes for VS Code and Vim.**
*Built for the long-distance developer. Focused. Lived-in. Tactical.*

**Tamp** is born from the intersection of architectural design, 70s retro-futurism, and the ritual of a perfect extraction. It moves away from the neon "gamer" aesthetic of modern editors toward a palette that feels grounded, material, and permanent.

---

## The collection

### Vanguard Outpost
**The Night-Ops Terminal.**
A deep purple-maroon atmosphere designed for high-focus deep work. By using a "nebula-shadow" background instead of pure black, it reduces ocular vibration, making your code feel like a stable holographic projection.

- **Palette:** Deep Plum, Ion Blue, and Muted Zinc.

- **Best for:** Systems architecture and midnight refactors.


### Lunar Lobby
**Retro-Futurist Hospitality.**
Inspired by the monolithic architecture and cinematic warmth of Arctic Monkeys' Tranquility Base Hotel & Casino. This is the "signature blend" of the collection—rich terracotta, oxidized sage, and vintage ochre.

- **Palette:** Roasted Bean, Terracotta, Sage Lounge, and Vintage Ochre.

- **Best for:** Creative coding and long-form development

### Space Rumours
**Luminance as Logic.**
A monochromatic study inspired by the stark, legendary contrast of the Rumours album cover. By stripping away hue, it forces your brain to parse code through light and shadow alone. A masterclass in visual hierarchy.

- **Palette:** 12 shades of Slate, Ash, and Bone.

- **Best for:** Minimalists and those who find color distracting.

---

## Design Philosophy

The **Tamp** collection follows three strict principles:

1. **Chromatic Distance:** Colors are chosen not just because they look good, but because they are functionally distinct. You recognize a "Function" by its temperature, not just its color.

2. **The Extraction Rule:** Like a perfect espresso, we’ve "tamped" the noise. Comments and punctuation recede into the background, leaving only the "crema"—the vital logic of your code—on top.

3. **Matte Finish:** High-vibrancy "neon" purples and greens have been replaced with matte, organic tones to prevent eye strain during 8+ hour sessions.

---

## Recommended Setup

To get the intended "boutique" look, we recommend the following configuration:

**Font:** [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) or [Operator Mono]() (for those gorgeous italics).

**Line Height:** 1.6 — Give your code room to breathe.

**Cursive Italics:** Enabled for comments and docstrings.


```json
{
  "editor.fontFamily": "'JetBrains Mono', monospace",
  "editor.fontSize": 14,
  "editor.lineHeight": 22,
  "editor.fontStyle": "italic",
  "editor.tokenColorCustomizations": {
    "textMateRules": [
      {
        "scope": ["comment", "string.quoted.docstring"],
        "settings": { "fontStyle": "italic" }
      }
    ]
  }
}
```

---

## Contributing

If you'd like to help port **Tamp** to other platforms (iTerm2, Alacritty, Obsidian), feel free to open a PR. Let's keep the extraction perfect.