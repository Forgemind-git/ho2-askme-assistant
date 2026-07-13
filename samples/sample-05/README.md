# HO2 Sample 5 — Campaign & Offer Desk: "What's Running Right Now?"

## What you'll build
An **AI-powered Claude Artifact** that becomes the single source of truth for your live promotions.
When several offers run at once, sales, support and social all quote them from memory — and one
wrong end-date, or a code stacked that shouldn't be, costs real money. This page is grounded in
your real **offers, codes, dates, eligibility and exclusions**, with an **Ask Me** box that answers
**live** — "what's running right now?", "can SPRING20 be stacked with the student discount?", "do
outlet items qualify for free delivery?" — from the actual offer sheet, never invented. It will
also tell you when something is **not** running. You build it by chatting with Claude, then publish
it and share the link. This folder's `index.html` is a finished, working example (Rally Sportswear)
you can open, read, and copy.

**Who can use it live:** anyone with a Claude account. It is **not** an anonymous public bot —
when a teammate sends a question they're prompted to sign in to their **own** Claude account, and
the usage counts against *their* account. Replace "the team just asks and gets an answer"
in your head with "anyone with a Claude account can ask it live."

## Use it with your Claude.ai subscription
No API key needed. This runs on your normal Claude.ai login.

1. In Claude.ai, turn on **Settings → Capabilities → "AI-powered artifacts"** (one-time).
2. Start a new chat and paste **the example prompt below**, filled in with your real offer sheet.
3. Claude builds the page as an **Artifact** on the right. Ask it in the chat to tweak wording,
   colours or which questions show — until it matches how your team actually asks.
4. Click **Publish** on the artifact to get a shareable link. Drop it in the sales and support
   channels, and re-publish whenever the offers change.
5. Anyone with a Claude account who opens the link can ask it questions live (they sign
   in to their own account first).

> **One caveat to know:** Anthropic changed how `window.claude.complete` behaves on 2025-07-31.
> If live answers ever stop working, open the artifact inside claude.ai and confirm the current
> way to call Claude from an artifact — the feature may have shifted since this was written.

## The example prompt
Copy this into Claude.ai and fill in the parts in CAPITALS:

```
Build me a single-file HTML "Ask-Me" Claude Artifact that acts as our campaign and offer desk, so
sales, support and social quote our promotions correctly instead of from memory.

It should be a clean internal page with: the brand name and a one-line description, a short About
explaining why one source of truth matters, a "Live offers & terms" section (each offer with its
code, discount, exact dates, whether it stacks, and what it excludes), the delivery and returns
terms, and an "Ask Me" box.

The Ask Me box must answer LIVE using window.claude.complete(prompt) — no API key. Hardcode our
real offer sheet into the page as the grounding, and instruct the assistant to answer ONLY from
that grounding, warm and specific, 2–4 sentences, quoting the real codes, dates, discounts and
exclusions exactly as written. It must never invent an offer, a code, a discount or an exclusion.
If an offer isn't on the sheet it must say "That is not on the offer sheet — treat it as not
running" rather than guessing. If window.claude.complete isn't available, show a friendly note
telling the visitor to open it as a Claude Artifact and sign in.

Our details:
- Brand: NAME — what we sell, one line
- Live offers, 2–4 of them (code → discount → exact start/end → stackable or not → exclusions)
- Stacking rules: what may be combined with what
- Eligibility: who qualifies, and how it's verified
- Delivery and returns: the real terms
- NOT running: the offers people still ask about that are over, or never existed

Give me three good starter questions the team would ask, as clickable chips.
```

## Make it your own
- Swap the grounding: everything in the `PROFILE` string (and the visible Live offers section) is
  yours to edit. Keep it exact — a wrong date here is a wrong date quoted to a customer.
- Keep the **NOT running** list current. It's the half everyone forgets, and it's what stops the
  assistant guessing about an offer that ended last month.
- Change the accent colour via `--accent` at the top of the `<style>` block.

## How it works (30-second version)
The page hardcodes your real offer sheet and calls `window.claude.complete(prompt)` at runtime.
That API is provided by Claude to published artifacts — it runs on the **viewer's** Claude
subscription, so there's no key and no server. Grounding = your codes, dates and exclusions pasted
into the prompt with a firm "answer only from this" instruction, so quoted terms stay accurate.

## Optional — automate it with the API (advanced)
You do **not** need this for the course. If you later want the page to answer without the
viewer needing a Claude account, you'd host it yourself and call the Anthropic API with a key
kept server-side. That's a separate, paid path and is never required to finish this hands-on.
