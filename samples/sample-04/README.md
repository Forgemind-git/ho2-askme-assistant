# Sample 04 — HR Professional AI Page

## Problem Statement

You are an **HR Business Partner**. You use Claude to draft job descriptions, policy documents, and 1:1 prep notes.

This sample shows how to build a personal "Ask Me" page that introduces your HR expertise and gives colleagues, hiring managers, and job seekers an AI assistant pre-scoped to HR policies, performance management, and hiring topics.

## What this page does

- **About Me section** — introduces your role and lists specific ways you use AI to accelerate HR work
- **Ask Me section** — a live chat widget backed by the Claude API, pre-prompted to answer questions about HR policies, performance management, and hiring

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
   > **Security note:** For a public GitHub Pages site, do not commit a real API key. Use a backend proxy or serverless function instead.
5. Save, commit, and push.

## Local preview

Open `index.html` directly in your browser — no build step needed.

## Customisation tips

- Update the name, jurisdiction (country/region), and company size context so Claude's HR advice is relevant.
- Edit the About Me cards to reflect your specific HR specialisms (e.g., Learning & Development, Talent Acquisition, Compensation & Benefits).
- Adjust `SYSTEM_PROMPT` to include your industry, employment law jurisdiction, and any compliance frameworks you work within.
- Swap the amber/orange colour palette via CSS variables to match your employer brand.
