# Sample 05 — Product Manager AI Page

## Problem Statement

You are a **Product Manager at a fintech startup**. You use Claude to write PRDs, user stories, and competitor analysis briefs.

This sample shows how to build a personal "Ask Me" page that demonstrates your product thinking and gives visitors an AI assistant pre-scoped to product strategy, feature prioritisation, and user stories.

## What this page does

- **About Me section** — introduces your role and describes how you use AI throughout the product development lifecycle
- **Ask Me section** — a live chat widget backed by the Claude API, pre-prompted to answer questions about product strategy, feature prioritisation, and user stories

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
   > **Security note:** For a public GitHub Pages site, do not commit a real API key. Use a backend proxy or serverless function to keep your key server-side.
5. Save, commit, and push.

## Local preview

Open `index.html` directly in your browser — no build step needed.

## Customisation tips

- Update the name, company stage (Series A, growth, etc.), and product domain (payments, lending, investing).
- Edit the About Me cards to reflect your specific PM workflows and frameworks (OKRs, RICE, Jobs-to-be-Done, etc.).
- Adjust `SYSTEM_PROMPT` to include your product domain, tech stack awareness, and preferred output formats (Confluence template, Notion doc, etc.).
- Swap the indigo/blue palette via CSS variables at the top of `<style>`.
