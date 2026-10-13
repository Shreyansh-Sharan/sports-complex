# Deploying SPORTS COMPLEX

This folder is a complete repository: an initial commit is already made on `main`.

## 1. Create the GitHub repository

Create an empty repository called **sports-complex** under **Shreyansh-Sharan** (no README, no licence, no .gitignore), then:

```bash
git remote add origin git@github.com:Shreyansh-Sharan/sports-complex.git
git push -u origin main
```

## 2. Enable GitHub Pages

Settings → Pages → Build and deployment → Source: **GitHub Actions**. The workflow in
`.github/workflows/deploy.yml` builds on every push to `main` and publishes `dist/`. The site appears at

    https://shreyansh-sharan.github.io/sports-complex/

(`base: './'` in `vite.config.ts` keeps asset paths relative, so it also works from a custom domain or Vercel.)

Ads and affiliate IDs are optional repository variables: Settings → Secrets and variables → Actions → Variables
(`VITE_ADSENSE_CLIENT`, `VITE_ADSENSE_SLOT_LOBBY`, `VITE_ADSENSE_SLOT_SIDE`, `VITE_H5_GAME_ADS`, `VITE_AMAZON_TAG`,
`VITE_AMAZON_DOMAIN`).

## 3. Point the portfolio at it

In the portfolio repository, `site/src/data/gameLinks.ts` lists this URL. Once the site is live, set
`GAMES_EXTERNAL = true` there and the portfolio's Play button opens it in a new tab.

## Vercel instead

`vercel.json` is included (SPA rewrite, immutable `/assets`). Import the repository in Vercel with the default
Vite settings.
