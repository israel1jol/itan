# ÌTÀN — Atlas of African Peoples

*ìtàn (Yorùbá): history; the telling of what happened.*

A living atlas of African history organized the way it should be — around **peoples**, not colonial borders. The Yoruba before Nigeria. The Zulu before the colony. And it doesn't just tell the history — it turns every people's story into a playable expedition.

## How it works

Nothing on the site is written by us, and nothing is hardcoded. Every word, image, date — and every quiz question — is generated live from open archives at the moment you ask:

- **Wikipedia REST API** — summaries, deep-dive history/culture sections, and imagery for every profile and artifact card
- **Wikidata SPARQL** — kingdom founding and dissolution dates (powering the timelines, Time Machine, and quiz engine) and the live discovery query behind the "All Peoples" index

The codebase contains only the lens: a 12-entry routing registry (names, map pin positions, article pointers), the UI, the game systems, and the fetch layer.

## The Expedition System

Every featured people's page is a four-chapter quest with XP, ranks (Wanderer 🌱 → Pathfinder 🧭 → Chronicler 📜 → Griot 👑), badges, synthesized sound effects, and a completion celebration:

1. **The Story** — live-fetched history with glowing *artifact words* hidden in the text; tap to open live fact cards and collect them into your satchel
2. **The Time Machine** — drag a year dial and watch kingdoms rise and fall in real time, then answer time riddles generated from live dates
3. **The Builders** — kingdom gallery, interactive timeline ("lasted 412 years!"), and a memory-match game built from fetched imagery
4. **The Lightning Round** — 45 seconds of rapid-fire questions forged from the archive

Finish all four and the expedition completes — then there are eleven more peoples waiting on the map.

## Features

- **Semi-3D continent navigation** — Africa as depth-stacked layers in CSS 3D space, tilting with your pointer; region-colored pins with touch-friendly preview chips on mobile
- **Twelve featured peoples** — Yoruba, Igbo, Hausa, Ashanti, Wolof, Zulu, Shona, Amhara, Oromo, Swahili, Amazigh, Tuareg — spanning every region of the continent
- **The long roll** — a live SPARQL query discovers 300+ peoples indigenous to Africa, searchable, each opening a dynamically built profile
- **Quiz mode** — a standalone 8-question quiz with streaks, confetti, and explanations, plus per-people quick quizzes
- **Social sharing** — quiz scores, lightning results, and expedition completions share to X, WhatsApp, Facebook, or the native share sheet
- **Two themes, one continent** — "Night over the continent" (dark) and "Savanna noon" (light), following the device's setting automatically
- **Design rooted in the continent** — sunset-and-earth palette, six region color identities, museum-catalog typography

## Tech

- Single static `index.html` — vanilla JS, no framework, no build step, no backend, no API keys, no audio files (sound is synthesized with the Web Audio API)
- Hash-based routing, in-memory response caching, graceful offline/error states
- CSS 3D transforms only (no WebGL) — runs smoothly on mid-range mobile
- Respects `prefers-reduced-motion` and `prefers-color-scheme`; keyboard-accessible throughout

## Run it locally

```bash
git clone https://github.com/israel1jol/itan.git
cd itan
# open index.html in a browser
```

## Roadmap

- [ ] Persistent XP, ranks, and explored progress across visits
- [ ] Region filtering on the All Peoples index
- [ ] More featured expeditions (one-line registry change each)
- [ ] Cross-people connections: trade routes, migrations, conflicts
- [ ] Multiplayer lightning rounds

## Authors

The idea belongs to two of us:

- **Israel Adigun** — Software Developer · Computer Science, University of Wisconsin–Milwaukee
- **Afolabi Raheem Kehinde** — Medical graduate · Kursk State Medical University

## Content & licensing

All text and imagery are served live from [Wikipedia](https://en.wikipedia.org) and [Wikidata](https://www.wikidata.org) under **CC BY-SA 4.0**. ÌTÀN stores nothing and rewrites nothing — the record speaks for itself.

App code: MIT.
