# Tamp

**Six cinematic dark themes for VS Code.**  
*Built for the long-distance developer. Focused. Lived-in. Tactical.*

**Tamp** is born from the intersection of architectural design, 70s retro-futurism, and the ritual of a perfect extraction. It moves away from the neon "gamer" aesthetic of modern editors toward a palette that feels grounded, material, and permanent.

Each theme ships in two variants: **Night** for deep focus sessions, and **Day** — a lifted, matte version of the same identity that holds up under bright office light without switching to a light theme.

---

## The Collection

### Lunar Lobby
**Retro-Futurist Hospitality.**

Inspired by the monolithic architecture and cinematic warmth of Arctic Monkeys' *Tranquility Base Hotel & Casino*. Rich terracotta keywords, sage-green functions, and vintage ochre strings. The background is a roasted espresso — dark enough to be a proper dark theme, warm enough to feel like a room rather than a void.

- **Palette:** Roasted Bean · Terracotta · Sage Lounge · Vintage Ochre
- **Night bg:** `#26201E` — deep espresso
- **Day bg:** `#3A3430` — lifted warm matte
- **Best for:** Creative coding and long-form development

---

### Space Rumours
**Luminance as Logic.**

A monochromatic study inspired by the stark, legendary contrast of the *Rumours* album cover. By stripping away hue, it forces your brain to parse code through light and shadow alone — functions are the brightest thing on screen, brackets nearly disappear, comments dissolve into shadow.

The Day variant introduces a single deliberate exception: strings gain a warm bone/ivory tint. One hue. Chosen because it breaks the rule in a way that feels considered rather than accidental.

> **The value scale**
>
> Functions   `#EDE8E0`  ████████████  — the action  
> Methods     `#E0DBD4`  ███████████░  — close behind  
> Keywords    `#D4CFC8`  ██████████░░  — structure  
> Types       `#BEC4C8`  █████████░░░  — classification  
> Variables   `#A4A9AE`  ███████░░░░░  — recede until needed  
> Numbers     `#98A0A6`  ██████░░░░░░  — data, not logic  
> Operators   `#6E7378`  █████░░░░░░░  — connective tissue  
> Brackets    `#585D62`  ████░░░░░░░░  — disappear  
> Comments    `#6E7378`  ███░░░░░░░░░  — shadow  

- **Night:** pure greyscale, luminance only
- **Day:** greyscale + warm bone accent on strings (`#C8BB98`)
- **Best for:** Minimalists and those who find colour distracting

---

### Vanguard Outpost
**The Night-Ops Terminal.**

A deep purple-maroon atmosphere for high-focus deep work. Ion blue functions float against the nebula-shadow background; sage-olive types ground them. Amber strings are the warmest thing on screen — deliberate contrast against the cool violet field.

The Day variant shifts the background toward a dusty rosewood, pulling the temperature slightly warmer for daylight wearability while keeping the plum DNA intact.

- **Palette:** Deep Plum · Ion Blue · Sage Olive · Warm Amber
- **Night bg:** `#2A1C28` — deep purple-maroon
- **Day bg:** `#402E32` — dusty rosewood
- **Best for:** Systems architecture and deep-work sessions

---

## Design Principles

### 1. The Luminance Floor

Every syntax colour sits above a minimum contrast ratio against the background. The floor is calibrated so that the *weakest* meaningful token — variables, parameters — still reads cleanly under daylight glare. Comments sit just below at ~3.0:1: readable, but clearly subordinate to code.

Backgrounds are matte, not black. Pure black causes mirror-glare on glossy screens and forces your pupils to dilate every time you glance between the editor and a browser window. Tamp's darkest background (`#2A1C28`) sits at a perceptual lightness of L\*=12.5 — dark enough to be distinctly dark-themed, light enough to be matte.

### 2. The Extraction Rule

Like a perfect espresso, we've tamped the noise. Operators and punctuation recede into the mid-range. Comments sit in shadow. What rises to the surface — functions, strings, keywords — is the crema: the vital logic of your code.

### 3. Semantic Temperature

Your brain maps colour temperature to meaning before it maps hue to token type. Warm = data (strings, values). Cool = structure (types, interfaces). Neutral = variables. Tamp follows this wiring. You recognise a function by its temperature as much as its colour.

### 4. The 5th Layer

Tamp uses VS Code's semantic token system to express information that TextMate scopes cannot. Same hue, different state:

- **`readonly`** variables are desaturated — locked, not removed
- **`static`** methods are slightly brighter — always present, elevated
- **`async`** functions are italic — they suspend; grammar signals behaviour
- **`abstract`** types are italic and ethereal — cannot be instantiated
- **`deprecated`** symbols fade with strikethrough — dead code recedes
- **`defaultLibrary`** tokens glow slightly brighter — they come from outside your file, already proven

This requires VS Code 1.85+ with `"editor.semanticHighlighting.enabled": true`.

### 5. Monolith UI

The Activity Bar, Sidebar, Tab Bar, and Status Bar share the same deep background with no visible borders. There is no UI chrome competing with your code in peripheral vision. The editor feels like a canvas, not an application window.

---

## Installation

### VS Code Marketplace
Search **Tamp** in the Extensions panel, or install via:
```
ext install tamp-theme.tamp
```

### Manual
1. Clone or download this repo
2. Copy the `themes/` folder and `package.json` into `~/.vscode/extensions/tamp-1.0.0/`
3. Reload the VS Code window (`Cmd/Ctrl+Shift+P` → *Reload Window*)
4. Open the theme picker (`Cmd/Ctrl+K Cmd/Ctrl+T`) and choose any Tamp variant

---

## Recommended Setup

```json
{
  "editor.fontFamily": "'JetBrains Mono', 'Operator Mono', monospace",
  "editor.fontSize": 14,
  "editor.lineHeight": 22,
  "editor.semanticHighlighting.enabled": true,
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

**Font:** [JetBrains Mono](https://www.jetbrains.com/lp/mono/) is the design reference. Operator Mono or Recursive (with italic axis) will make the most of the italic semantic tokens.

**Line height:** 1.6 minimum. Give your code room to breathe.

**Semantic highlighting:** Required for the 5th-layer token states (`readonly`, `async`, `deprecated`, etc.). Enable it — it's off by default in some VS Code builds.

---

## Ports

Tamp exports are available for:

- **VS Code** — primary target, full semantic token support
- **Vim / Neovim** — includes Treesitter and LSP semantic groups
- **iTerm2** — terminal palette
- **Alacritty** — TOML terminal palette

See the `/exports` directory or use the [Tamp Theme Editor](https://github.com/tamp-theme/editor) to generate any format from a customised palette.

---

## Contributing

If you'd like to refine a variant, port to a new platform (Ghostty, Zed, Obsidian), or suggest a fourth identity for the collection, open a PR or issue.

Keep the extraction perfect.
