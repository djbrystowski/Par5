# Warmer 🔥

A two-player "guess who I'm thinking of" game.

One player thinks of a person (famous, or someone you both know). The other guesses people one at a time, and the picker scores each guess 0–100 for how close it is. Keep going until they get it, then swap.

- **Play with a friend (live):** create a game, choose who picks first, and send one invite link. Once your friend joins, both phones update live. No sign-up. The picker's answer stays on their phone and is only sent when it's revealed.
- **Play on one phone:** pass-and-play with a "pass the phone" screen so nobody peeks.

It's a single static file (`index.html`). Live games are stored in a Supabase project (`warmer`): one `games` table that the site can only reach through three functions (`create_game`, `get_game`, `save_game` with a version check). Updates arrive through Supabase Realtime, with a 3-second refresh as a fallback. One-phone games stay in the browser (localStorage).
