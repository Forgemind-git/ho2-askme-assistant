# HO2 Sample 5 — Career Changer: "Reframe My Experience"

## What you'll build
An **AI-powered Claude Artifact** for the hardest hiring problem a career changer faces: your
old job titles don't signal the role you're targeting, so recruiters bounce off before they see
the fit. This page fixes that. It's a personal page grounded in your **real** past experience,
with an **Ask Me** box that answers the question everyone's really asking — "why are you
qualified for *this*?" — **live**, by reframing what you actually did toward the target role,
never inventing experience you don't have. You build it by chatting with Claude, then publish it
and share the link. This folder's `index.html` is a finished, working example — Sofia Reyes, a
science teacher of 7 years moving into UX research — that you can open, read, and copy.

**Who can use it live:** anyone with a Claude account. It is **not** an anonymous public bot —
when a visitor sends a question they're prompted to sign in to their **own** Claude account, and
the usage counts against *their* account. Replace "a recruiter just asks and gets an answer" in
your head with "anyone with a Claude account can ask it live."

## Use it with your Claude.ai subscription
No API key needed. This runs on your normal Claude.ai login.

1. In Claude.ai, turn on **Settings → Feature preview → "Create AI-powered artifacts"** (one-time).
2. Start a new chat and paste **the example prompt below**, filled in with your real details.
3. Claude builds the page as an **Artifact** on the right. Ask it in the chat to tweak wording,
   colours or which questions show — until it feels like you.
4. Click **Publish** on the artifact to get a shareable link. Put that link on your CV / LinkedIn.
5. Anyone with a Claude account who opens the link can ask your page questions live (they sign
   in to their own account first).

> **One caveat to know:** Anthropic changed how `window.claude.complete` behaves on 2025-07-31.
> If live answers ever stop working, open the artifact inside claude.ai and confirm the current
> way to call Claude from an artifact — the feature may have shifted since this was written.

## The example prompt
Copy this into Claude.ai and fill in the parts in CAPITALS:

```
Build me a single-file HTML "Ask-Me" Claude Artifact that helps me change careers.

My problem: my old job titles don't signal my target role, but my real skills do. The page's
job is to answer "why are you qualified for this?" by REFRAMING my genuine past experience
toward the target role — honestly, never fabricating titles or experience I don't have.

The page should be a clean personal page with: my name and a "OLD ROLE → TARGET ROLE" line, a
short honest About paragraph (the bridge between the two), an "Experience, reframed" section of
3–4 cards, and an "Ask Me" box. Each card has: the ORIGINAL context as a kicker, the
transferable skill as the title, what I really did as the description, and a "Reads as: <target-
role equivalent>" line that does the reframing.

The Ask Me box must answer LIVE using window.claude.complete(prompt) — no API key. Hardcode my
real details into the page as the grounding, and instruct the assistant to answer ONLY from
that grounding, in the first person as me, warm and specific, 2–4 sentences. When asked why I'm
qualified, it must REFRAME my real past experience toward the target role using only the
grounding — and it must NEVER invent job titles, employers, dates or experience I don't have.
If asked about gaps, be honest about them. If the answer isn't in the grounding, say "I don't
have that detail" instead of guessing. If window.claude.complete isn't available, show a
friendly note telling the visitor to open it as a Claude Artifact and sign in.

My details:
- Name: YOUR NAME
- Old role → target role: e.g. Science teacher (7 years) → UX Researcher
- The honest bridge: one paragraph on what genuinely carries over
- Experience to reframe (original context → what I really did → how it reads for the target
  role), 3–4 of these: DESCRIBE EACH
- New skills/methods I've learned for the target role, and any honest gaps I'm still working on

Give me three good starter questions a recruiter would ask a career changer, as clickable chips
(e.g. "Why are you qualified for this role?", "How does your old field transfer?", "Have you
done real work in the new field?").
```

## Make it your own
- Swap the grounding: everything in the `PROFILE` string (and the visible About/Experience
  cards) is yours to edit. Keep it truthful — the reframing only works if the underlying facts
  are real, and the honest gaps keep it credible.
- Change the accent colour via `--accent` at the top of the `<style>` block (this example uses
  an ochre / amber identity).
- Edit the three suggested questions and the "Reads as:" lines to match your own transition.

## How it works (30-second version)
The page hardcodes your real record and calls `window.claude.complete(prompt)` at runtime.
That API is provided by Claude to published artifacts — it runs on the **viewer's** Claude
subscription, so there's no key and no server. Grounding = your facts pasted into the prompt
with a firm "answer only from this, reframe don't fabricate" instruction, so the reframing stays
tethered to what you actually did.

## Optional — automate it with the API (advanced)
You do **not** need this for the course. If you later want the page to answer without the
viewer needing a Claude account, you'd host it yourself and call the Anthropic API with a key
kept server-side. That's a separate, paid path and is never required to finish this hands-on.
