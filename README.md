# Sim Room FC — World Cup 2026 Bracket

Live site: https://simroomfc.github.io/simroomfc-bracket/

This README is for you (or anyone helping maintain the repo). It doesn't show
up on the live site — GitHub just displays it on this repo's code page.

## Updating results

After each Round of 16 video posts:

1. Open `index.html` (edit directly on GitHub, or locally then push).
2. Find the `RESULTS` object near the top of the `<script>` block and add one
   line — match id, score, winner. Example:
   ```js
   m5: { score: "2–1", winner: "Spain" },
   ```
3. Commit. The bracket locks that match, highlights the winner, and
   auto-feeds it into the quarter-final slot — no other edits needed. Fan
   picks made further along the bracket stay put unless they conflict with a
   newly confirmed result.
4. Separately, run `Sim_Room_FC_Cover_Generator.py` locally (or ask Claude to)
   to produce that match's cover image from the same `RESULTS` entry — one
   edit drives both the bracket and the cover.

## Publishing

Commit and push to this repo's `main` branch. GitHub Pages redeploys
automatically within about a minute — no separate upload step.

## Match ID reference

| id | fixture |
|----|---------|
| m1 | Morocco v Canada |
| m2 | France v Paraguay |
| m3 | Brazil v Norway |
| m4 | Mexico v England |
| m5 | Spain v Portugal |
| m6 | Belgium v USA |
| m7 | Egypt v Argentina |
| m8 | Switzerland v Colombia |
