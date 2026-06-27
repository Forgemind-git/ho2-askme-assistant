# Sample 02 — Data Analyst AI Page

## Problem Statement

You are a **Data Analyst specialising in e-commerce**. You use Claude to write SQL queries, interpret chart data, and generate executive summaries from raw numbers.

This sample shows how to build a personal "Ask Me" page that introduces your analytical expertise and gives visitors an AI assistant pre-scoped to data analysis, SQL, and business insights topics.

## What this page does

- **About Me section** — introduces your role and lists specific ways you use AI to accelerate data work
- **Ask Me section** — a live chat widget backed by the Claude API, pre-prompted to answer questions about data analysis, SQL queries, and business insights

## Files

| File | Purpose |
|------|---------|
| `index.html` | Complete self-contained single-file app — HTML + CSS + JS |

## How to deploy to GitHub Pages

1. **Fork or copy** this folder to your own GitHub repository.
2. Go to **Settings → Pages** in your repo.
3. Under *Source*, select **Deploy from a branch**, choose `main`, and set the folder to the subfolder containing `index.html`.
4. **Add your Anthropic API key** — open `index.html` and replace the placeholder:
   ```js
   const ANTHROPIC_API_KEY = 'YOUR_ANTHROPIC_API_KEY_HERE';
   ```
   > **Security note:** For a public GitHub Pages site, do not commit a real API key. Instead, route the API call through a backend proxy or serverless function (Netlify Functions, Cloudflare Workers, etc.).
5. Save, commit, and push. GitHub Pages will publish your site within a few minutes.

## Local preview

No build step needed. Just open `index.html` directly in your browser:

```bash
open index.html   # macOS
xdg-open index.html  # Linux
```

Add your API key in the file first, then ask a SQL or data analysis question.

## Customisation tips

- Update the name, avatar emoji, and role description in the hero section.
- Edit the About Me cards to match your own tech stack (e.g., BigQuery instead of PostgreSQL, Tableau instead of Looker).
- Modify `SYSTEM_PROMPT` to add your specific database dialect preferences, industry context (e-commerce, fintech, healthcare), or output formatting requirements.
- Change CSS colour variables at the top of `<style>` — the teal palette is easy to swap for any brand colour.
