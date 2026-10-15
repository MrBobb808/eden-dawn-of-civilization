# EDEN: Dawn of Civilization 🌿

A playable, standalone browser village simulation inspired by the Book of Genesis. Eden currently includes painted procedural scenery, characters, animals, resource interactions, Scripture-led story quests, and settlements.


## Play

The entire game is contained in [`index.html`](index.html). Open the HTML file in a modern desktop browser, or serve this folder with `python3 -m http.server 8000` and open `http://localhost:8000`.

Once GitHub Pages is enabled and has deployed successfully, the intended address for the repository `MrBobb808/eden-dawn-of-civilization` is `https://mrbobb808.github.io/eden-dawn-of-civilization/`. This is a **planned address**, not a verified live link until GitHub Pages reports success.

## Features in current build

- Tap or click to move Adam and interact with the world
- Tend fields, gather fruit, name animals, fish and gather resources
- Follow Genesis 2–4-inspired narrated chapters
- Unlock Cain and Seth settlement locations
- Open a family-tree journal, Scripture journal, inventory, and world map
- Mobile/touch layout and browser save persistence

## Current limitations

This is a playable **prototype**, not yet the finished high-fidelity edition. Full autonomous generational growth, livestock breeding, authentic hand-animated sprite sheets, and independent living village economies are planned rather than finished. See [GAME_DESIGN.md](GAME_DESIGN.md).

## Biblical approach

Core narrative milestones follow Genesis 2–4; daily activities, dialogue, environmental artwork and some timelines are imagined for gameplay. The game identifies itself as an artistic adaptation and not a substitute for reading Scripture.

## Set up GitHub Pages

1. Create a **public** repository with default branch `main`.
2. Place the contents of this package at the repository root (so `index.html` is in the root, not nested under `eden-game/`).
3. Open **Settings → Pages → Build and deployment → Source: GitHub Actions**.
4. The included `.github/workflows/pages.yml` will publish automatically on `main` pushes. Check its status in **Actions**, or run it manually.
5. After it succeeds, open **Settings → Pages → Visit site**.

No paid hosting, API keys, dependencies, or build command required.