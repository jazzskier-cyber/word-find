# Word Find for the web

A browser edition of the cozy Godot Word Find game. It uses the same six collections, starter-friendly difficulty settings, rounded visual style, hints, and colorful found-word ribbons. It runs independently in a browser.

## Play locally

From the `games/` repository root:

```sh
npm run dev --workspace=word-find
```

Open the local URL printed by Vite. Choose a collection and a difficulty, then drag through letters. On a phone, touch and slide. The starter board is 8×8 with four short words placed across or down. The highest web difficulty uses a 10×10 board with eight words so the letters stay touchable on narrow phones.

Completing a board gives pocket points: 400, 600, or 800 base points by difficulty, plus up to 300 points for finishing sooner, minus 100 points per hint. The game never shows a countdown. Personal bests are stored in the current browser for each difficulty. In the [published game](https://www.ai-made.games/games/word-find-6b0682c6/playing), each completed puzzle also submits its score to the [Pocket points leaderboard](https://www.ai-made.games/games/word-find-6b0682c6/leaderboard?board=4929e772-be77-40ce-9427-bdcdc43a6739). The leaderboard keeps each player's best score across all three difficulties. A failed submission can be retried from the completion card.

## Build

```sh
npm run build --workspace=word-find
npm run preview --workspace=word-find
```

The static site is generated in `apps/word-find/dist/` with relative asset paths, so it can be hosted from a subdirectory. The repository root build still targets Cloud Garden.

Word Find's source build needs its own repository root for hosts that run `npm ci` and `npm run build` at the top level. A static host can serve `apps/word-find/dist/` directly.

When this folder is copied to a dedicated Word Find repository, run `npm ci`, `npm run build`, and `npm run preview` from that repository root.

The included Fredoka font is licensed under the SIL Open Font License. See `assets/fonts/OFL.txt`.
