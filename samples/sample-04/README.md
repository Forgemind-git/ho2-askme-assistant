# HO2 Sample 4 — Brand Voice: "Can We Say That?"

## What you'll build
An **AI-powered Claude Artifact** that stops the wrong claim reaching a customer. It's an internal
brand guide grounded in your real **tone, positioning, approved claims and banned claims**, with an
**Ask Me** box that answers **live** — "how do we describe the product?", "can we say 'clinically
proven'?", "are we allowed to name a competitor?" — from the actual guidelines, never invented.
Anyone writing copy, in-house or freelance, can check a line *before* they publish it. You build it
by chatting with Claude, then publish it and share the link. This folder's `index.html` is a
finished, working example (Lumen Skincare, a D2C skincare brand) you can open, read, and copy.

**Who can use it live:** anyone with a Claude account. It is **not** an anonymous public bot —
when a teammate sends a question they're prompted to sign in to their **own** Claude account, and
the usage counts against *their* account. Replace "a writer just asks and gets an answer"
in your head with "anyone with a Claude account can ask it live."

## Use it with your Claude.ai subscription
No API key needed. This runs on your normal Claude.ai login.

1. In Claude.ai, turn on **Settings → Capabilities → "AI-powered artifacts"** (one-time).
2. Start a new chat and paste **the example prompt below**, filled in with your real guidelines.
3. Claude builds the page as an **Artifact** on the right. Ask it in the chat to tweak wording,
   colours or which questions show — until it reads like your brand.
4. Click **Publish** on the artifact to get a shareable link. Share it with everyone who writes
   copy — agency, freelancers, social, support.
5. Anyone with a Claude account who opens the link can ask it questions live (they sign
   in to their own account first).

> **One caveat to know:** Anthropic changed how `window.claude.complete` behaves on 2025-07-31.
> If live answers ever stop working, open the artifact inside claude.ai and confirm the current
> way to call Claude from an artifact — the feature may have shifted since this was written.

## The example prompt
Copy this into Claude.ai and fill in the parts in CAPITALS:

```
Build me a single-file HTML "Ask-Me" Claude Artifact that acts as our brand voice guide, so
anyone writing copy can check whether a claim is approved before they publish it.

It should be a clean internal-guide page with: the brand name and a one-line description, a short
About explaining why the guide exists, our positioning line, our tone, an APPROVED claims list
(exact wording) and a BANNED claims list (with why), and an "Ask Me" box.

The Ask Me box must answer LIVE using window.claude.complete(prompt) — no API key. Hardcode our
real guidelines into the page as the grounding, and instruct the assistant to answer ONLY from
that grounding, warm and specific, 2–4 sentences, quoting approved and banned claims exactly as
written. If a claim is banned it must say so plainly and offer the closest approved wording
instead. It must never approve wording that is not in the guide — if the answer isn't there it
says "That is not covered in the guide — check with brand before you publish." If
window.claude.complete isn't available, show a friendly note telling the visitor to open it as a
Claude Artifact and sign in.

Our details:
- Brand: NAME — what we sell, one line
- Why this guide exists: DESCRIBE
- Positioning: the one line we want people to remember
- Tone: how we sound — and how we never sound
- Approved claims (the exact wording anyone may publish): LIST THEM
- Banned claims (never publish, and why — e.g. regulatory risk): LIST THEM
- Competitors: named, or never named?

Give me three good starter questions a copywriter would ask, as clickable chips.
```

## Make it your own
- Swap the grounding: everything in the `PROFILE` string (and the visible Voice & claims section)
  is yours to edit. Keep it truthful — a guide that overstates what's approved is worse than none.
- Change the accent colour via `--accent` at the top of the `<style>` block.
- Edit the three suggested questions to match what your writers actually get stuck on.

## How it works (30-second version)
The page hardcodes your real guidelines and calls `window.claude.complete(prompt)` at runtime.
That API is provided by Claude to published artifacts — it runs on the **viewer's** Claude
subscription, so there's no key and no server. Grounding = your approved and banned claims pasted
into the prompt with a firm "answer only from this, never approve anything else" instruction.

## Optional — automate it with the API (advanced)
You do **not** need this for the course. If you later want the page to answer without the
viewer needing a Claude account, you'd host it yourself and call the Anthropic API with a key
kept server-side. That's a separate, paid path and is never required to finish this hands-on.
