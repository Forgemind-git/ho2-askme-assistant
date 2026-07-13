# CLAUDE.md — Ask-Me AI Assistant (HO2)

Guidance for **Claude Code / Claude Cowork** when working in this repo. The student is on the
**Claude.ai Pro plan**, which is usage-limited — work economically so their limit stretches,
*even when they make mistakes*.

## About this project
A personal 'Ask-Me' AI assistant, built as an **AI-powered Claude Artifact** — a single-file page
that answers visitor questions **live** by calling the built-in `window.claude.complete(prompt)` API,
grounded only in the creator's real hardcoded material.
**Primary way to do it:** Claude.ai chat — enable *Settings → Capabilities → "AI-powered
artifacts"*, prompt Claude to build it, then **Publish** for a share link. **No API key needed** —
live answers run on the *viewer's* own Claude account.
The work lives under `samples/sample-01 … sample-05`; each sample has its own `README.md` with a
ready-to-use example prompt. Start from those — they already work.

## Spend tokens wisely (read this first)
- **Plan before you build.** State a 1–3 line plan, then make the whole change in one pass.
- **Use the example prompt in the sample README** instead of writing a new one — it's tested.
- **Don't re-read or re-paste** files already shown in the conversation.
- **Keep replies short** — show only what changed, skip the preamble.
- **Make all related edits at once** — no trial-and-error loops.
- **Ask one clear question when unsure** rather than guessing and redoing the work.
- **Reuse the starter files** — tweak them, don't rebuild from scratch.

## This repo, specifically
- It's the **Ask-Me AI Assistant** hands-on. Single-file Claude Artifacts that DO call an LLM at
  runtime via `window.claude.complete` — but **no API key**: it runs on the viewer's Claude account.
- **Be honest about reach:** a shared artifact's live AI works only for viewers who have their own
  Claude account and sign in; it is not an anonymous public bot. Don't overclaim.
- Note the **2025-07-31** change to `window.claude.complete` behaviour — write to the documented
  `window.claude.complete(prompt: string): Promise<string>` API and tell the student to confirm the
  current call inside claude.ai if it stops working.
- **No API key is required for the course.** Any backend/API-key path is OPTIONAL, costs money, and
  should be ignored unless the student explicitly asks for the advanced path.
- When helping on the `starter` branch, don't restructure the repo or touch `main`.

See `SKILL.md` for the reusable **token-wise** skill that carries these same rules into Claude.ai.
