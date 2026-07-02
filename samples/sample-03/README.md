# HO2 Sample 3 — Freelancer: "Ask About Working With Me"

## What you'll build
An **AI-powered Claude Artifact** that stops leads going cold while they wait for a reply. It's a
freelancer first-contact page grounded in your real **services, pricing and process**, with an
**Ask Me** box that answers prospect questions **live** — "how much is a landing page?", "what's
your process?", "do you offer retainers?" — from your actual details, never invented. You build it
by chatting with Claude, then publish it and share the link. This folder's `index.html` is a
finished, working example (Priya Nair, a freelance conversion copywriter) you can open, read, and copy.

**Who can use it live:** anyone with a Claude account. It is **not** an anonymous public bot —
when a visitor sends a question they're prompted to sign in to their **own** Claude account, and
the usage counts against *their* account. Replace "a prospect just asks and gets an answer"
in your head with "anyone with a Claude account can ask it live."

## Use it with your Claude.ai subscription
No API key needed. This runs on your normal Claude.ai login.

1. In Claude.ai, turn on **Settings → Feature preview → "Create AI-powered artifacts"** (one-time).
2. Start a new chat and paste **the example prompt below**, filled in with your real services and prices.
3. Claude builds the page as an **Artifact** on the right. Ask it in the chat to tweak wording,
   colours or which questions show — until it feels like your business.
4. Click **Publish** on the artifact to get a shareable link. Put that link in your bio, proposals,
   or wherever leads first find you.
5. Anyone with a Claude account who opens the link can ask your page questions live (they sign
   in to their own account first).

> **One caveat to know:** Anthropic changed how `window.claude.complete` behaves on 2025-07-31.
> If live answers ever stop working, open the artifact inside claude.ai and confirm the current
> way to call Claude from an artifact — the feature may have shifted since this was written.

## The example prompt
Copy this into Claude.ai and fill in the parts in CAPITALS:

```
Build me a single-file HTML "Ask-Me" Claude Artifact that answers questions from prospects
so leads don't go cold waiting for my reply.

It should be a clean personal page with: my name and what I do, a short About with a "how I
work" note, a Services section (2–4 cards, each with what's included and a "From: PRICE" line),
a small facts row about my process, and an "Ask Me" box.

The Ask Me box must answer LIVE using window.claude.complete(prompt) — no API key. Hardcode
my real services, prices and process into the page as the grounding, and instruct the assistant
to answer ONLY from that grounding, in the first person as me, warm and specific, 2–4 sentences,
quoting my real prices and process steps, and to say "I don't have that detail — happy to confirm
on a call" instead of inventing anything. If window.claude.complete isn't available, show a
friendly note telling the visitor to open it as a Claude Artifact and sign in. Do NOT add any
contact or email-capture form — just answer questions honestly.

My details:
- Name: YOUR NAME
- What I do: e.g. freelance conversion copywriter for SaaS & e-commerce
- Services (name → what's included → From price), 2–4 of them: DESCRIBE EACH
- My process, step by step: e.g. discovery call, proposal in 2 days, 50% deposit, draft in a week
- Availability: e.g. usually booking ~2 weeks out
- Who I'm a good fit for (and who I'm not): DESCRIBE

Give me three good starter questions a prospect would ask, as clickable chips.
```

## Make it your own
- Swap the grounding: everything in the `PROFILE` string (and the visible About/Services) is
  yours to edit. Keep it truthful — the assistant can only be as honest as the material.
- Change the accent colour via `--accent` at the top of the `<style>` block.
- Edit the three suggested questions to match what prospects actually ask you.

## How it works (30-second version)
The page hardcodes your real services, prices and process and calls `window.claude.complete(prompt)`
at runtime. That API is provided by Claude to published artifacts — it runs on the **viewer's**
Claude subscription, so there's no key and no server. Grounding = your details pasted into the
prompt with a firm "answer only from this" instruction, so quoted prices stay accurate.

## Optional — automate it with the API (advanced)
You do **not** need this for the course. If you later want the page to answer without the
viewer needing a Claude account, you'd host it yourself and call the Anthropic API with a key
kept server-side. That's a separate, paid path and is never required to finish this hands-on.
