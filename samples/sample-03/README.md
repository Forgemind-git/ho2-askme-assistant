# HO2 Sample 3 — Product Pre-Sales: "Ask Before You Buy"

## What you'll build
An **AI-powered Claude Artifact** that answers the questions a buyer asks *before* they book a
demo. It's a pre-sales page grounded in your real **plans, limits, integrations and policies**,
with an **Ask Me** box that answers questions **live** — "which plan do I need for three stores?",
"do you integrate with WooCommerce?", "what happens if we cancel?" — from your published facts,
never invented. You build it by chatting with Claude, then publish it and share the link. This
folder's `index.html` is a finished, working example (Northwind Analytics, a product-analytics
tool for small e-commerce teams) you can open, read, and copy.

**Who can use it live:** anyone with a Claude account. It is **not** an anonymous public bot —
when a visitor sends a question they're prompted to sign in to their **own** Claude account, and
the usage counts against *their* account. Replace "a prospect just asks and gets an answer"
in your head with "anyone with a Claude account can ask it live."

## Use it with your Claude.ai subscription
No API key needed. This runs on your normal Claude.ai login.

1. In Claude.ai, turn on **Settings → Capabilities → "AI-powered artifacts"** (one-time).
2. Start a new chat and paste **the example prompt below**, filled in with your real plans and prices.
3. Claude builds the page as an **Artifact** on the right. Ask it in the chat to tweak wording,
   colours or which questions show — until it reads like your product.
4. Click **Publish** on the artifact to get a shareable link. Put that link on your pricing page,
   in outbound emails, or wherever buyers keep asking the same five questions.
5. Anyone with a Claude account who opens the link can ask your page questions live (they sign
   in to their own account first).

> **One caveat to know:** Anthropic changed how `window.claude.complete` behaves on 2025-07-31.
> If live answers ever stop working, open the artifact inside claude.ai and confirm the current
> way to call Claude from an artifact — the feature may have shifted since this was written.

## The example prompt
Copy this into Claude.ai and fill in the parts in CAPITALS:

```
Build me a single-file HTML "Ask-Me" Claude Artifact that answers pre-sales questions about my
product, so buyers get a straight answer instead of waiting on a demo call.

It should be a clean product page with: the product name and a one-line description, a short
About with who it's for, a Pricing & policy section (the real plans with their real limits),
an integrations list (including what I do NOT support), and an "Ask Me" box.

The Ask Me box must answer LIVE using window.claude.complete(prompt) — no API key. Hardcode my
real plans, limits, integrations and policies into the page as the grounding, and instruct the
assistant to answer ONLY from that grounding, warm and specific, 2–4 sentences, quoting the real
plans, prices and limits exactly, and to say "I don't have that detail — the team can confirm it
for you" instead of inventing anything. It must never invent a plan, a price, an integration or a
policy. If window.claude.complete isn't available, show a friendly note telling the visitor to
open it as a Claude Artifact and sign in.

My details:
- Product: NAME — what it does, one line
- Who it's for (and who it's NOT for): DESCRIBE
- Plans (name → price → the real limits and what's included), 2–4 of them: DESCRIBE EACH
- Integrations I support, and the ones I don't: LIST BOTH
- Refunds / cancellation: THE REAL POLICY
- Security: where the data lives, what's on which plan

Give me three good starter questions a buyer would ask, as clickable chips.
```

## Make it your own
- Swap the grounding: everything in the `PROFILE` string (and the visible About / Pricing) is
  yours to edit. Keep it truthful — the assistant can only be as honest as the material.
- Change the accent colour via `--accent` at the top of the `<style>` block.
- Edit the three suggested questions to match what buyers actually ask you.

## How it works (30-second version)
The page hardcodes your real plans, limits and policies and calls `window.claude.complete(prompt)`
at runtime. That API is provided by Claude to published artifacts — it runs on the **viewer's**
Claude subscription, so there's no key and no server. Grounding = your published facts pasted into
the prompt with a firm "answer only from this" instruction, so quoted prices and limits stay right.

## Optional — automate it with the API (advanced)
You do **not** need this for the course. If you later want the page to answer without the
viewer needing a Claude account, you'd host it yourself and call the Anthropic API with a key
kept server-side. That's a separate, paid path and is never required to finish this hands-on.
