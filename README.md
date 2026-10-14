# SPORTS COMPLEX · Play now

A small 3D sports complex to explore: an F1 track for experience, a stadium for achievements and a rally hall for skills.

Built with F1 · Soccer · Badminton · Table tennis. Part of [Shreyansh Sharan's portfolio](https://shreyanshsharan.com/), split into its own site.

```bash
npm install
npm run dev      # http://localhost:5173
npm run build    # production build in dist/
npm run lint     # oxlint
```

The site is a single page: `#/` is the game's menu, and the same query parameters the portfolio used still work
(for example `#/?auto=...` to skip the menu, `#/?join=CODE` for an invite link).

## Controls

- `W` `A` `S` `D` walk · mouse to look · `Shift` run · `Space` jump
- `E` use a glowing pad (enter a venue, get in the car, start a game) · `E`/`Esc` leave it
- Car: `W`/`S` throttle and brake · `A`/`D` steer · `R` back on track
- Penalties: aim with the mouse · hold `LMB` for power, release to shoot
- Rallies: `A`/`D` move · `LMB` or `Space` hit as the ring turns green
- `Esc` frees the mouse; again to leave the complex

## Ads and gear

Optional AdSense and Amazon affiliate IDs come from environment variables (see `.env.example`). Leave them empty and
no ad or shop code loads.
