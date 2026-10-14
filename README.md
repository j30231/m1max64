# Local LLM Observatory

Continuously updated comparison of **local LLMs, quantizations, uncensored variants and inference engines** — measured against real Apple Silicon hardware.

🌐 **Live site:** https://j30231.github.io/m1max64/

## What this is

- **Model catalog** — quality benchmarks, best quantization per model, decode speed on M1 Max 64GB
- **Uncensored tracker** — abliterated/uncensored variants with trust notes
- **Engine comparison** — llama.cpp, MLX, oMLX, MTPLX, TensorFold, Strata, Ollama, LM Studio…
- **Decision models** — JEV-35B, Clef-Flash and the new breed of scoring/classification models
- **Updates feed** — changelog including public corrections

## Methodology

Every speed figure is labeled:

- <span style="color:green">**measured**</span> — real benchmark, source linked
- <span style="color:orange">**estimated**</span> — extrapolated, treat with skepticism

We correct ourselves in public. Retractions appear in the updates feed.

## Data

All content lives in `data/*.json`:

| File | Contents |
|---|---|
| `data/meta.json` | Site meta, hardware focus, last update |
| `data/models.json` | Model catalog |
| `data/engines.json` | Inference engines |
| `data/decisions.json` | Decision/scoring models |
| `data/updates.json` | Changelog feed |

`index.html` is a static single-page app that renders these files — no build step, no dependencies.

## Updating

Data is refreshed by automated watch jobs (model releases, benchmarks, X reports).
To update manually, edit `data/*.json` and push — GitHub Pages redeploys automatically.

## Contributing

PRs welcome — especially **measured** M1 Max / Apple Silicon benchmarks with sources.
