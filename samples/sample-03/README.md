# Sample 03 — Teacher AI Page

## Problem Statement

You are a **Secondary school Science teacher**. You use Claude to create lesson plans, quiz questions, and plain-English explainers for complex topics.

This sample shows how to build a personal "Ask Me" page that showcases your teaching philosophy and gives students, parents, and fellow educators an AI assistant pre-scoped to science education topics.

## What this page does

- **About Me section** — introduces your role and explains how you use AI to design better lessons and support diverse learners
- **Ask Me section** — a live chat widget backed by the Claude API, pre-prompted to answer questions about science education, lesson design, and study tips

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
   > **Security note:** For a public GitHub Pages site, do not commit a real API key. Instead, use a backend proxy or serverless function (Netlify Functions, Cloudflare Workers, etc.) to keep your key server-side.
5. Save, commit, and push. GitHub Pages will publish your site within a few minutes.

## Local preview

No build step needed. Open `index.html` directly in your browser:

```bash
open index.html   # macOS
xdg-open index.html  # Linux
```

## Customisation tips

- Change the teacher's name, subject specialisation (e.g., Physics vs. Biology), and year groups.
- Edit the About Me cards to reflect your own teaching methods and AI workflows.
- Adjust `SYSTEM_PROMPT` to steer Claude toward your specific curriculum (e.g., UK GCSE, IB, AP Sciences) or grade level.
- The green palette can be swapped via the CSS variables at the top of `<style>`.
- Add a "Resources" section with links to lesson plan templates or revision guides.
