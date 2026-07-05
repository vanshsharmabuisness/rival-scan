# 🕵️ RivalScan

**Side-by-side competitor intelligence, powered by Firecrawl.**

RivalScan scrapes the homepage, pricing page, and blog of one or two competitor domains in parallel, scores each on a transparency/content/clarity rubric, and produces a scored verdict with a concrete growth opportunity.

## What it does

- Scrapes `/`, `/pricing`, and `/blog` for up to **two domains simultaneously**, 6 requests running in parallel
- Scores each domain 0–100 on: pricing transparency, content publishing velocity, and homepage messaging clarity
- Renders the two domains as side-by-side report cards plus an animated comparison bar
- Generates a written verdict identifying who's ahead and why, and proposes a specific fast-follow demo idea that exploits the gap — either via a built-in rules engine or, optionally, an LLM (any OpenAI-compatible key)
- Works in single-domain mode too if you only want one report

## Run it

No install, no backend, no build step.

```
open index.html
```

## Stack

- Vanilla HTML / CSS / JS
- Firecrawl `/v1/scrape` REST API, called concurrently across both domains
- Optional: any OpenAI-compatible chat completions endpoint for the verdict

## Privacy

Runs entirely client-side. Nothing is stored or sent anywhere except directly to Firecrawl (and optionally your LLM provider).
