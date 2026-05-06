# FKNG MARK / Launch Engine Demo

Interactive public demo for **FKNG MARK**, a product-first marketing engine for moving product ideas through research, strategy, content, publishing, metrics, and a 48-hour decision loop.

Live demo: https://ulayuga.github.io/launch-engine-demo/

## What This Demo Shows

- Product workspace layout and operator navigation.
- Product candidate screening flow.
- Research, ICP, positioning, and channel strategy surfaces.
- VK, Telegram, OK, and article content review screens.
- Publication calendar, metrics, and final decision flow.
- A safe AI generation endpoint without exposing backend secrets in this public repository.

## What The Private Core Does

The production FKNG MARK repository runs the real backend:

- Next.js operator app with PostgreSQL and Drizzle.
- pg-boss worker queues for research, publishing, metrics, and decisions.
- LLM-backed competitor research and structured strategy/content generation.
- Publication adapters for VK, Telegram, OK, and Dzen/RSS paths.
- Click tracking, search metric ingestion, aggregation windows, and T+48 decision artifacts.
- Operational dashboards for products, brands, review queue, prompts, calendar, portfolio, errors, settings, and health.

## Public / Private Split

This repository is public by design. It contains the static demo shell only.

The production core stays private because it contains live infrastructure assumptions, operational scripts, channel integration wiring, and credential names. No live channel tokens or production secrets belong in this demo repository.

## Run Locally

Open `index.html` directly or serve the folder with any static file server:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080`.
