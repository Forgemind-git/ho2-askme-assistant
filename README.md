# HO2 — "Ask-Me" AI Assistant

> Hands-on portfolio project · **Week 2** · **Solo** · module M5. Part of the **ForgeMind AI — AI Productivity Essentials** course.

## Goal

**Done when:** you have a shareable **AI-powered Claude Artifact** that answers questions about you
**live**, grounded in your real information — not a page of pre-written answers.

## What it is

A Claude **Artifact** (a single-file page Claude builds for you inside a chat) that:

- hardcodes *your* real About / projects / skills as its grounding, and
- calls Claude at runtime with the built-in **`window.claude.complete(prompt)`** API to answer
  visitor questions **from that material only** — no API key, no server, no code you host.

You build it by prompting Claude, then click **Publish** to get a link you can share.

## Who can actually use it live (read this — it's the honest bit)

- To **build** it, you must turn on **Settings → Feature preview → "Create AI-powered artifacts"**
  in Claude.ai (one-time).
- To **use the live AI in a shared artifact**, a viewer needs their **own Claude account** — when
  they ask a question they're prompted to sign in, and the usage counts against **their** account.
  It is **not** an anonymous public bot. So the honest framing is *"anyone with a Claude account
  can ask it live,"* not *"a recruiter just asks and gets an answer."*

> **One caveat:** Anthropic changed how `window.claude.complete` behaves on **2025-07-31**. Write to
> the documented `window.claude.complete(prompt: string): Promise<string>` API (the samples do), and
> if live answers ever stop working, open your artifact inside claude.ai and confirm the current way
> to call Claude — the feature may have shifted since this was written.

## What to ship

The artifact code (a single `index.html`) + your grounding filled in + this README with your
**published share link** pasted in.

## Pick a problem statement

Choose **one** — each maps to a fully-built example in `samples/` you can open and copy:

1. You are job-hunting and tired of recruiters skimming past your CV. Build an AI-powered Claude Artifact — an "Ask-Me" chat grounded in your experience, projects and skills — so anyone with a Claude account can ask "have you led a team?" or "do you know React?" and get an accurate answer from your real material. Success: a published artifact link where three sample questions answer correctly, live.

2. As a freelancer with a scattered portfolio, you want one link that sells your work. Build an AI-powered Claude Artifact that explains each project, the problem it solved and the decisions behind it, grounded only in your own write-ups. Success: a shared artifact where a Claude-using visitor can ask about any project and get the real story, not invented detail.

3. You freelance and lose leads to slow replies. Build an AI-powered Claude Artifact grounded in your services, pricing and process that answers a prospect's questions about working with you. Success: a published artifact where test questions about your pricing and process are answered accurately from your own content.

4. You are a speaker and creator fielding the same booking questions over and over. Build an AI-powered Claude Artifact grounded in your talks, topics and background so event organisers can ask what you speak about and whether you fit their event. Success: a shared artifact that answers three organiser questions correctly from your real material.

5. You are switching careers and your old titles do not signal your new target role. Build an AI-powered Claude Artifact grounded in your past experience that reframes it toward the role you want, answering "why are you qualified for this?". Success: a published artifact that convincingly reframes three of your past roles toward the target.

## Use it with your Claude.ai subscription

No API key needed.

1. Open the landing page `index.html` (or view it on GitHub Pages) to browse the five examples.
2. Open the README of the sample closest to your situation and copy its **example prompt**.
3. In Claude.ai, enable **Settings → Feature preview → "Create AI-powered artifacts"**.
4. Paste the prompt into a new chat with **your own details** filled in. Claude builds your page
   as an Artifact — refine it in the chat until it sounds like you.
5. Click **Publish** on the artifact, copy the link, and paste it into your README.

## How to use this repo

- `index.html` — landing page linking the five worked examples.
- `samples/sample-01 … sample-05` — five complete reference artifacts (one per problem statement),
  each with its own README + example prompt.
- On the **`starter`** branch you'll find a copy-and-use template with example grounding already
  filled in — clone it, swap in your details, publish.

## Optional — automate it with the API (advanced)

You do **not** need this for the course. `window.claude.complete` runs on the *viewer's* Claude
account, so there's no key. If you later want a page that answers without the viewer needing a
Claude account, you'd host it yourself and call the Anthropic API with a key kept server-side —
a separate, paid path that is never required to finish this hands-on.

---

*HO2 · Solo · ForgeMind AI Course · module M5 (Week 2)*


## 💡 Use your Claude.ai Pro plan wisely

The Pro plan has a usage limit that resets every few hours. A few habits make it stretch — and
keep a mistake from burning your whole session:

- **Use the example prompt** in each sample's README — it's already written and tested. Don't
  reinvent it.
- **One clear prompt** beats lots of vague back-and-forth. Say what you want, with an example, in
  a single message.
- **Start a new chat when you switch tasks.** Long chats re-read every earlier message and use up
  your limit faster.
- **Don't paste big files over and over.** Paste once, then refer back to it.
- **If something works, keep it.** Tweak it rather than regenerate from scratch.
- **Using Claude Code or Cowork?** This repo's `CLAUDE.md` makes Claude follow these same rules
  automatically, and `SKILL.md` is a reusable "token-wise" skill.

If you do hit the limit, it resets after a few hours — nothing you've saved is lost.
