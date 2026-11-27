# Audiotheca website

Interactive showcase site, live at https://chrisjrovira.com/Audiotheca/, for [Audiotheca](https://github.com/cephyrixzyth/Audiotheca), the self-hosted audio library dedupe and routing engine.

It is a static site with no build step: `index.html`, `styles.css`, `app.js` and `assets/`.

## What's on the page

- **Dry-scan demo**: a toy library runs through the real phases (walk, identify, archive peek, dedupe, plan routes, report). Phases can be skipped, keepers picked, investigation items resolved, and a live run approved to see the reorganized tree.
- **Product tour**: tabbed real screenshots of every workspace station, with a lightbox.
- **Walkthrough player**: the 12 documentation videos.
- **Audio preview**: a Web Audio loop player with waveform, tempo and pitch controls.
- **Theme gallery**: the app's 22 built-in themes, which re-skin the page.
- **Install**: Unraid steps, a Docker command builder that generates secrets in the browser, Windows portable and source instructions.
- **Staged rollout**, safety guarantees and FAQ.

## Run locally

```sh
python -m http.server 8000
# open http://localhost:8000
```

## Publishing

The live copy is served from the `Audiotheca/` folder of [cephyrixzyth/chrisjrovira.com](https://github.com/cephyrixzyth/chrisjrovira.com) at https://chrisjrovira.com/Audiotheca/. After changing this repo, copy `index.html`, `styles.css`, `app.js` and `assets/` into that folder and open a PR there.

This repo can also be published on its own with GitHub Pages (Settings → Pages → Deploy from a branch → `main` / root). `.nojekyll` is included.

## Assets

Screenshots, videos, logo and theme room art come from the Audiotheca repo (`docs/assets/` and `ui/public/`). Screenshots were converted to WebP. To refresh them, re-run `python scripts/capture_doc_assets.py` in Audiotheca and copy them over.
