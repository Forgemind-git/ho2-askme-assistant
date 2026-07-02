# HO2 Sample 2 — Freelancer: "Ask My Portfolio"

## What you'll build
An **AI-powered Claude Artifact** that acts as a concierge for your freelance portfolio. Instead
of a scattered set of case studies, it's one page grounded in your real project write-ups —
problem, decision, result — with an **Ask Me** box that answers client questions **live**:
"tell me about the fintech project", "do you do design systems?" — from your actual material,
never invented. You build it by chatting with Claude, then publish it and share the link. This
folder's `index.html` is a finished, working example (Dan Okoye, a freelance product designer)
you can open, read, and copy.

**Who can use it live:** anyone with a Claude account. It is **not** an anonymous public bot —
when a visitor sends a question they're prompted to sign in to their **own** Claude account, and
the usage counts against *their* account. Replace "a client just asks and gets an answer" in
your head with "anyone with a Claude account can ask it live."

## Use it with your Claude.ai subscription
No API key needed. This runs on your normal Claude.ai login.

1. In Claude.ai, turn on **Settings → Feature preview → "Create AI-powered artifacts"** (one-time).
2. Start a new chat and paste **the example prompt below**, filled in with your real projects.
3. Claude builds the page as an **Artifact** on the right. Ask it in the chat to tweak wording,
   colours or which questions show — until it feels like you.
4. Click **Publish** on the artifact to get a shareable link. Put that link in your bio, proposals
   or the top of your portfolio.
5. Anyone with a Claude account who opens the link can ask your portfolio questions live (they
   sign in to their own account first).

> **One caveat to know:** Anthropic changed how `window.claude.complete` behaves on 2025-07-31.
> If live answers ever stop working, open the artifact inside claude.ai and confirm the current
> way to call Claude from an artifact — the feature may have shifted since this was written.

## The example prompt
Copy this into Claude.ai and fill in the parts in CAPITALS:

```
Build me a single-file HTML "Ask-Me" Claude Artifact that acts as a concierge for my freelance
portfolio.

It should be a clean personal page with: my name and role, a short About, a skills list, a
"Projects" section of 3–4 project cards (each with a kicker, title, the problem, and a "Result:"
line), a small facts row, and an "Ask Me" box.

The Ask Me box must answer LIVE using window.claude.complete(prompt) — no API key. Hardcode my
real project write-ups into the page as the grounding, and instruct the assistant to answer ONLY
from that grounding, in the first person as me, warm and specific, 2–4 sentences, and to say
"I don't have that detail" instead of inventing anything. If window.claude.complete isn't
available, show a friendly note telling the visitor to open it as a Claude Artifact and sign in.

My details:
- Name: YOUR NAME
- Role: e.g. Freelance product designer (UX/UI)
- Experience: e.g. 8 years freelance, 40+ projects across onboarding, checkout, design systems
- Skills: e.g. UX/UI, design systems, user research, prototyping, accessibility, Figma
- Projects (kicker → problem → decision → result), 3–4 of them: DESCRIBE EACH
- What I'm looking for: e.g. interesting product work, contract or project-based

Give me three good starter questions a client would ask, as clickable chips, and use a warm
coral accent colour.
```

## Make it your own
- Swap the grounding: everything in the `PROFILE` string (and the visible About/Projects) is
  yours to edit. Keep it truthful — the assistant can only be as honest as your write-ups.
- Change the accent colour via `--accent` at the top of the `<style>` block.
- Edit the three suggested questions to match what clients actually ask you.

## How it works (30-second version)
The page hardcodes your real project write-ups and calls `window.claude.complete(prompt)` at
runtime. That API is provided by Claude to published artifacts — it runs on the **viewer's**
Claude subscription, so there's no key and no server. Grounding = your facts pasted into the
prompt with a firm "answer only from this" instruction.

## Optional — automate it with the API (advanced)
You do **not** need this for the course. If you later want the page to answer without the
viewer needing a Claude account, you'd host it yourself and call the Anthropic API with a key
kept server-side. That's a separate, paid path and is never required to finish this hands-on.
