# HO2 Sample 4 — Speaker / Creator: "Ask My Booking Page"

## What you'll build
An **AI-powered Claude Artifact** that handles your speaker enquiries for you. It's a booking
page grounded in your real talks, topics and background, with an **Ask Me** box that answers
event-organiser questions **live** — "what do you speak about?", "are you a fit for a fintech
conference?", "what do you need on stage?" — from your actual material, never invented. You
build it by chatting with Claude, then publish it and share the link. This folder's `index.html`
is a finished, working example (Marcus Bell, a keynote speaker on practical AI adoption) you can
open, read, and copy.

**Who can use it live:** anyone with a Claude account. It is **not** an anonymous public bot —
when an organiser sends a question they're prompted to sign in to their **own** Claude account,
and the usage counts against *their* account. Replace "an organiser just asks and gets an answer"
in your head with "anyone with a Claude account can ask it live."

## Use it with your Claude.ai subscription
No API key needed. This runs on your normal Claude.ai login.

1. In Claude.ai, turn on **Settings → Feature preview → "Create AI-powered artifacts"** (one-time).
2. Start a new chat and paste **the example prompt below**, filled in with your real details.
3. Claude builds the page as an **Artifact** on the right. Ask it in the chat to tweak wording,
   colours or which questions show — until it feels like you.
4. Click **Publish** on the artifact to get a shareable link. Put that link in your speaker kit,
   your site, or your reply to an enquiry.
5. Anyone with a Claude account who opens the link can ask your page questions live (they sign
   in to their own account first).

> **One caveat to know:** Anthropic changed how `window.claude.complete` behaves on 2025-07-31.
> If live answers ever stop working, open the artifact inside claude.ai and confirm the current
> way to call Claude from an artifact — the feature may have shifted since this was written.

## The example prompt
Copy this into Claude.ai and fill in the parts in CAPITALS:

```
Build me a single-file HTML "Ask-Me" Claude Artifact that helps event organisers book me
as a speaker.

It should be a clean speaker page with: my name and role, a short About / bio, a set of
signature talks (format + title + what the audience leaves with + who it's best for), a few
key facts (events, countries, audience size), and an "Ask Me" box.

The Ask Me box must answer LIVE using window.claude.complete(prompt) — no API key. Hardcode
my real talks and background into the page as the grounding, and instruct the assistant to
answer ONLY from that grounding, in the first person as me, warm and specific, 2–4 sentences.
For fee questions it must say fees depend on format and travel and invite them to ask for a
quote — never invent a number. It must never invent talks or claims, and should say
"I don't have that detail" instead of guessing. If window.claude.complete isn't available,
show a friendly note telling the visitor to open it as a Claude Artifact and sign in.

My details:
- Name: YOUR NAME
- Role: e.g. keynote speaker & workshop host on TOPIC for AUDIENCE
- Background: e.g. 9 years in operations, 60+ events across 12 countries, audiences up to 1,500
- Signature talks (format → title → takeaway → best for), 3–4 of them: DESCRIBE EACH
- AV / format needs: e.g. confidence monitor, stable wifi for live demos, can present remotely
- Fees: don't publish a number — say fees depend on format/travel, ask for a quote
- Travel base + languages: e.g. travels from London, English
- Good fit for / not a fit for: DESCRIBE

Give me three good starter questions an organiser would ask, as clickable chips.
```

## Make it your own
- Swap the grounding: everything in the `PROFILE` string (and the visible About/Signature talks)
  is yours to edit. Keep it truthful — the assistant can only be as honest as the material.
- Change the accent colour via `--accent` at the top of the `<style>` block.
- Edit the three suggested questions to match what organisers actually ask you.

## How it works (30-second version)
The page hardcodes your real record and calls `window.claude.complete(prompt)` at runtime.
That API is provided by Claude to published artifacts — it runs on the **viewer's** Claude
subscription, so there's no key and no server. Grounding = your facts pasted into the prompt
with a firm "answer only from this" instruction (including the "never invent a fee" rule).

## Optional — automate it with the API (advanced)
You do **not** need this for the course. If you later want the page to answer without the
viewer needing a Claude account, you'd host it yourself and call the Anthropic API with a key
kept server-side. That's a separate, paid path and is never required to finish this hands-on.
