# Next.js fitness app starter with a free exercise database

A small Next.js 16 app that lists, filters and shows 700+ exercises from the free
[RepDB exercise dataset](https://github.com/RepDB/exercise-dataset): illustrations,
target muscles, equipment, instructions and MET values in English, German and
Spanish. Fork it as the exercise library of your workout app.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FRepDB%2Frepdb-example-nextjs&project-name=repdb-fitness-starter&repository-name=repdb-fitness-starter)

No environment variables, no API key, no external API. The exercise JSON and
WebP images are vendored, so the Vercel deploy works as is.

Want motion? The catalog page shows one looping exercise animation from RepDB
Standard; more are in the
[animation gallery](https://repdb.co/exercise-animations/?utm_source=github-nextjs).

## Features

- Static-rendered exercise list with filter by body part, equipment, difficulty
- Detail page per exercise with flat start/peak (or single-pose) frames,
  instructions, muscle data, equipment icon, and MET value
- EN / DE / ES locale switch (translates the exercise data — UI is EN-only)
- Paid-tier preview on the catalog page: a looping animation — the exact clip
  shown on repdb.co — badged "Standard tier preview", linking to pricing

## Run

```bash
npm install
npm run dev
```

Open <http://localhost:3000>.

## Build

```bash
npm run build
npm run start
```

## What's vendored where

```
src/data/exercises.json        # the public flat-edition bundle (every free exercise, EN/DE/ES), imported as a module
public/images/flat/*.webp      # flat WebP (start/peak pairs + single-pose "main")
public/images/muscles/*.webp   # muscle icons
public/images/equipment/*.webp # equipment icons
public/images/samples/*.webp   # 1 paid-tier looping animation (Standard-tier preview)
LICENSE-free.md                # RepDB Free Tier License for the bundle data & images
LICENSE                        # MIT for the example code
```

The `public/images/samples/` files are paid-tier preview assets: looping
animations, the exact clips shown on repdb.co. The gallery list is derived at
build time from the `.webp` files present there (see `src/lib/samples.ts`) —
no hardcoded list.

## Data & license

This demo uses the RepDB **free tier**: every fully illustrated exercise in
the current catalog with flat-style images, under the
[RepDB Free Tier License](LICENSE-free.md).

**Attribution required.** Keep a visible link — "Exercise data by RepDB
(repdb.co)" — in your app's credits, README, or footer.

**No generative-AI derivation.** The images may not be used as input, reference,
or conditioning material for generative models (image-to-image, style transfer,
fine-tuning, or similar). See term 5 of [LICENSE-free.md](LICENSE-free.md).

**No redistribution as a dataset** — in-app use only.

For French content, classic images, transparent backgrounds, animations, a female
character add-on, 1024px assets, and a commercial license without attribution, see
<https://repdb.co/pricing?utm_source=github-nextjs>.

> Exercise data & images: RepDB (https://repdb.co)

## Sister demos

- [**exercise-dataset**](https://github.com/RepDB/exercise-dataset) — the raw dataset (JSON + WebP), browsable [live viewer](https://exercise-dataset.com/)
- [repdb-example-react-native](https://github.com/RepDB/repdb-example-react-native)
- [repdb-example-flutter](https://github.com/RepDB/repdb-example-flutter)

## License

MIT for the example code (`LICENSE`). Bundle data & images under the
[RepDB Free Tier License](LICENSE-free.md). PRs welcome — accessibility
improvements especially.
