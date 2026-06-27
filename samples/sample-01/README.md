# Sample 01 — Digital Marketer AI Page

## Problem Statement

You are a **Digital Marketer at a SaaS company**. You use Claude to draft ad copy, analyse campaign data, and repurpose content across platforms.

This sample shows how to build a personal "Ask Me" page that introduces your role and gives visitors an interactive AI assistant pre-scoped to marketing topics.

## What this page does

- **About Me section** — introduces your role and lists specific ways you use AI in your day-to-day marketing work
- **Ask Me section** — a live chat widget backed by the Claude API, pre-prompted to answer questions about marketing strategy and campaign ideas

## Files

| File | Purpose |
|------|---------|
| `index.html` | Complete self-contained single-file app — HTML + CSS + JS |

## How to deploy to GitHub Pages

1. **Fork or copy** this folder to your own GitHub repository.
2. Go to **Settings → Pages** in your repo.
3. Under *Source*, select **Deploy from a branch**, choose `main`, and set the folder to `/` (or the subfolder containing `index.html`).
4. **Add your Anthropic API key** — open `index.html` and replace the placeholder:
   ```js
   const ANTHROPIC_API_KEY = 'YOUR_ANTHROPIC_API_KEY_HERE';
   ```
   > **Security note:** For a public GitHub Pages site, do not commit a real API key. Instead, use a backend proxy, a Cloudflare Worker, or a service like Netlify Functions to keep the key server-side. The placeholder is for local/demo use only.
5. Save, commit, and push. GitHub Pages will publish your site within a few minutes.

## Local preview

No build step needed. Just open `index.html` directly in your browser:

```bash
open index.html   # macOS
xdg-open index.html  # Linux
```

Add your API key in the file first, then type a marketing question in the Ask Me box.

## Customisation tips

- Change the name, photo placeholder colour, and role in the hero section.
- Edit the bullet points in the About section to reflect your actual AI workflows.
- Adjust `SYSTEM_PROMPT` in the `<script>` block to steer Claude toward your specific marketing niche (e.g., B2B SaaS, e-commerce, influencer marketing).
- Swap the CSS colour variables at the top of `<style>` to match your personal brand.
