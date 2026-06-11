# ÌTÀN — Atlas of African Peoples

*ìtàn (Yorùbá): history; the telling of what happened.*

A living atlas of African history organized the way it should be — around **peoples**, not colonial borders. The Yoruba before Nigeria. The Zulu before the colony. Kingdoms, migrations, timelines, and art, told from the ground up.

**Live site:** https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/

## How it works

Nothing on the site is written by us, and nothing is hardcoded. Every word, image, and date is fetched live from open archives at the moment you ask:

- **Wikipedia REST API** — summaries, deep-dive history/culture sections, and imagery for every profile
- **Wikidata SPARQL** — structured data: kingdom founding and dissolution dates (which power the timelines) and the live discovery query behind the "All Peoples" index

The codebase contains only the lens: a 12-entry routing registry (names, map pin positions, article pointers), the UI, and the fetch layer.

## Features

- **Semi-3D continent navigation** — Africa rendered as depth-stacked layers in CSS 3D space, tilting with your pointer; twelve featured peoples pinned across every region
- **Featured profiles** — Yoruba, Igbo, Hausa, Ashanti, Wolof, Zulu, Shona, Amhara, Oromo, Swahili, Amazigh, Tuareg — each with live-fetched prose, a kingdoms gallery, and a Wikidata-driven timeline
- **The long roll** — a live SPARQL query discovers every ethnic group the archive knows as indigenous to Africa (300+), searchable, each opening a dynamically built profile
- **Design rooted in the continent** — adire indigo palette, ochre and clay accents, textile pattern bands generated in code, museum-catalog typography

## Tech

- Single static `index.html` — vanilla JS, no framework, no build step, no backend, no API keys
- Hash-based routing, in-memory response caching, graceful offline/error states
- CSS 3D transforms only (no WebGL) — runs smoothly on mid-range mobile
- Respects `prefers-reduced-motion`; keyboard-accessible pins and navigation

## Run it locally

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
# open index.html in a browser — that's the whole stack
```

## Deploy

GitHub Pages: Settings → Pages → Deploy from a branch → `main` / root.

## Roadmap

- [ ] localStorage caching for instant repeat visits
- [ ] Region filtering on the All Peoples index
- [ ] More featured profiles (one-line registry change each)
- [ ] Cross-people connections: trade routes, migrations, conflicts

## Authors

The idea belongs to two of us:

- **Israel Adigun** — Software Developer · Computer Science, University of Wisconsin–Milwaukee
- **Afolabi Raheem Kehinde** — Medical graduate · Kursk State Medical University

## Content & licensing

All text and imagery are served live from [Wikipedia](https://en.wikipedia.org) and [Wikidata](https://www.wikidata.org) under **CC BY-SA 4.0**. ÌTÀN stores nothing and rewrites nothing — the record speaks for itself.

App code: MIT.
