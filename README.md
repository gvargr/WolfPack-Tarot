# WolfPack Tarot Prompt Library

**Part of the [WolfPack Suite](https://github.com/gvargr) — AI image prompt tools for Stable Diffusion.**

> Live at **[gvargr.github.io/WolfPack-Tarot](https://gvargr.github.io/WolfPack-Tarot/)**

---

## Overview

A standalone browser tool that generates Stable Diffusion image prompts by combining character descriptions with randomly drawn tarot cards. Three cards are drawn from a full 78-card deck and paired with three characters in a spread — producing ready-to-paste positive and negative prompt sets for each card.

No install, no dependencies, no server required. Open the file in a browser and use it.

---

## Features

- **Full 78-card deck** — all 22 Major Arcana and 56 Minor Arcana (Cups, Wands, Swords, Pentacles, Ace through King)
- **Reversed cards** — 25% chance per draw; adds shadowed and disrupted imagery to the prompt
- **Four spread types** — Past / Present / Future, Situation / Action / Outcome, What I Know / Don't Know / Need to Know, The Seeker / The Journey / The Destination
- **Three character slots** — each independently set to Custom OC (paste any tag string or full prompt) or Random (22 anime archetypes with reroll)
- **Model-aware output** — quality prefix tags and art style language adapt to the selected checkpoint family
- **Suit-specific style conditioning** — Cups, Wands, Swords, and Pentacles each have distinct visual language per model
- **Content rating system** — per-card rating tiers on random slots (see below)
- **Age gate** — displayed on first load per session; confirms 18+ before access

---

## Supported Checkpoint Families

| Selection | Quality Prefix | Style |
|-----------|---------------|-------|
| Illustrious / NoobAI-XL | `masterpiece, best quality, very aesthetic, absurdres` | Ornate, jewel tones, detailed linework |
| Pony Diffusion | `score_9, score_8_up ...` | Vivid anime, glowing effects |
| Anima / AnimaPencil | `masterpiece, best quality, ultra-detailed, illustration` | Pencil sketch, classical inking |

---

## Content Rating Tiers

The global SFW / NSFW toggle controls which tiers are available. Ratings are set per character slot and only apply to Random mode — Custom OC prompts use whatever tags you provide.

| Rating | Mode | Description |
|--------|------|-------------|
| PG | SFW | Fully clothed, family safe, no skin |
| PG-R | SFW | Suggestive, closer to ecchi — midriff, thighs, form-fitting. No nudity |
| R | NSFW | Cleavage, implied nipples, covered. Large male genitals implied through clothing. No full nudity |
| X | NSFW | Full nudity and explicit content. Character type rolled at draw: Standard (60%), Femboy (20%), Futanari (20%) |

> **All characters are fictional and intended to represent adults aged 18 or over.**

---

## Random Archetype Pool

22 anime archetypes available in Random mode:

Shrine Maiden, Battle Mage, Dark Knight, Forest Elf, Demon Hunter, Sea Witch, Scholar, Assassin, Idol, Vampire Noble, Alchemist, Celestial Knight, Kunoichi, Pirate Captain, Spirit Medium, Berserker, Witch, Catgirl Knight, Empress, Wandering Swordsman, Oracle, Fallen Angel

---

## Repository Structure

```plaintext
WolfPack-Tarot/
├── index.html                      # Redirect to current version
├── wolfpack-tarot-v1_1_0.html      # Main application
└── README.md
```

When a new version is released, the versioned file is added and `index.html` is updated to point to it. Old versions remain accessible directly via their filename.

---

## Usage

### Via GitHub Pages

Open [gvargr.github.io/WolfPack-Tarot](https://gvargr.github.io/WolfPack-Tarot/) in any modern browser.

### Local

```bash
# Clone the repo
git clone https://github.com/gvargr/WolfPack-Tarot.git
cd WolfPack-Tarot

# Serve locally (required for clipboard on non-secure HTTP)
python3 -m http.server 8080
```

Then open `http://localhost:8080` in your browser. The tool works on the same local network, so you can access it from a phone or tablet at `http://<your-machine-ip>:8080`.

> On macOS or Windows, the WolfPack Suite launcher scripts from the main suite repo can also serve this directory.

---

## How to Use

1. **Select a checkpoint family** — matches the output tags to your SD model
2. **Toggle SFW / NSFW** — unlocks rating tiers on random character slots
3. **Select a spread** — sets the positional labels on each result card
4. **Set up three character slots** — paste a Custom OC prompt or use Random with an archetype and rating
5. **Draw Three Cards** — three cards are drawn, each paired with a character
6. **Copy the prompts** — positive and negative prompt blocks per card, paste into A1111, SwarmUI, or any compatible frontend

---

## Compatibility

- **Browsers:** Chrome, Firefox, Safari (desktop and mobile)
- **Models:** Illustrious / NoobAI-XL, Pony Diffusion, Anima / AnimaPencil
- **Frontends:** A1111, SwarmUI, ComfyUI (manual paste), Forge
- **Context:** Works over local network for mobile access — no internet required after page load

---

## WolfPack Suite

This tool is part of the WolfPack Suite, a collection of standalone HTML prompt tools for Stable Diffusion.

| Tool | Description |
|------|-------------|
| [WolfPack Prompt Builder](https://github.com/gvargr/WolfPack-Prompt-Builder) | 115 characters across 33 franchises, outfits, poses, environments |
| [WolfPack OC Builder](https://github.com/gvargr/WolfPack-Prompt-Builder) | Custom character creator with localStorage persistence |
| [WolfPack Gacha](https://github.com/gvargr/WolfPack-Gacha) | Waifu and Husbando collector card generator |
| WolfPack Tarot | Tarot-driven prompt library (this repo) |

---

## Credits

Danbooru tag data in the suite sourced from the [SwarmUI Prompt Builder Extension](https://github.com/jtreminio/SwarmUI-PromptBuilderExtension) by Juan Treminio. Used with thanks.

---

## License

Personal and creative use. Not for commercial redistribution.
