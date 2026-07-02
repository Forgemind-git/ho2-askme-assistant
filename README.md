# HO2 — "Ask-Me" AI Assistant · **starter (copy-and-use)**

> Hands-on portfolio project · **Week 2** · **Solo** · module M5. Part of the **ForgeMind AI — AI Productivity Essentials** course.
>
> **You're on the `starter` branch.** Every sample here is a **finished, working
> template** with example grounding already filled in. Don't start from a blank page —
> pick the one closest to you, swap in your real details where it says **EDIT HERE**,
> and publish.

## What you'll ship

A shareable **AI-powered Claude Artifact** that answers questions about *you* **live**,
grounded only in your real information — no code you host, **no API key**. It runs on the
Claude account of whoever is viewing it.

## The one template, five ready examples

`samples/sample-01 … sample-05` are five copy-and-use versions of the same template, one per
situation. Open the one that fits, then make it yours:

| Sample | For you if… |
|--------|-------------|
| **01 · Job seeker** | you're job-hunting and want recruiters to get real answers about your experience |
| **02 · Freelancer portfolio** | you want one link that tells the real story behind each project |
| **03 · Freelancer leads** | prospects ask the same questions about your services, pricing and process |
| **04 · Speaker / creator** | event organisers keep asking what you speak about and whether you fit |
| **05 · Career changer** | your old job titles don't signal the role you want next |

## Use it with your Claude.ai subscription (no API key)

1. In Claude.ai, turn on **Settings → Feature preview → "Create AI-powered artifacts"** (one-time).
2. Open a sample's `index.html` here to see the finished example, and its `README.md` for the
   ready-to-copy prompt.
3. **Two ways to make it yours — pick one:**
   - **Prompt Claude:** paste the sample's example prompt into a new chat with *your* details.
     Claude rebuilds the page as an Artifact you can refine in the chat.
   - **Edit the file:** open the sample's `index.html`, find the big **`EDIT HERE`** banner in
     the script, and replace the `PROFILE` text (and the visible About/cards) with your own.
4. Click **Publish** on the artifact to get a shareable link. Paste it into the sample's README
   where it says `[paste your published artifact share link here]`, and onto your CV / LinkedIn.

## Who can use it live (the honest bit)

To use the live AI in a **shared** artifact, a viewer needs their **own Claude account** — when
they ask a question they're prompted to sign in, and the usage counts against *their* account.
It is **not** an anonymous public bot. So: *anyone with a Claude account can ask it live.*

> **One caveat:** Anthropic changed how `window.claude.complete` behaves on **2025-07-31**. The
> template uses the documented `window.claude.complete(prompt: string): Promise<string>` API. If
> live answers ever stop working, open your artifact inside claude.ai and confirm the current way
> to call Claude — the feature may have shifted since this was written.

## Make it your own

- Swap the `PROFILE` grounding and the visible About / project cards for your real material.
- Change the accent colour via `--accent` at the top of the `<style>` block.
- Edit the three suggested question chips to match what people actually ask you.

## Optional — automate it with the API (advanced)

You do **not** need this for the course. `window.claude.complete` runs on the viewer's Claude
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
