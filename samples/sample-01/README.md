# HO2 Sample 1 — Digital Marketer AI Page

## What you'll build
A polished personal "Ask Me" page for a digital marketer (the example is Alex Rivera, a B2B
SaaS marketer). It introduces the role, shows how they use AI day-to-day, and includes an
**Ask Me** section with worked example answers about ad copy, campaign analysis, and content
repurposing — plus a button that opens Claude.ai so visitors can keep chatting live. It's a
single self-contained `index.html`: HTML, CSS, and a little JavaScript, no build step.

## Use it with your Claude.ai subscription
No API key needed. This page runs entirely in the browser and uses your normal Claude.ai
login for the "chat live" part.

1. Open **`index.html`** in your browser to see the finished page and its example answers.
2. Open **Claude.ai** in another tab (your subscription — no API key, no billing, no terminal).
3. Paste **the example prompt below** into Claude.ai and fill in your own details. Claude
   will write your About section and a set of strong sample answers.
4. Open `index.html` in a text editor (Notepad, TextEdit, or VS Code) and replace the
   example name, About cards, and Q&A pairs with what Claude gave you. Save.
5. Refresh the browser to see your version. The "Open claude.ai to chat live" button already
   points visitors to your subscription — nothing else to wire up.

## The example prompt
Copy this into Claude.ai and fill in the parts in CAPITALS:

```
I'm building a personal "Ask Me" web page that shows how I use AI as a digital marketer. Help me write the content.

About me:
- Name: YOUR NAME
- Role: e.g. Digital Marketer at a B2B SaaS company
- The marketing work I do: e.g. demand gen, paid media, content strategy
- The main ways I use AI: e.g. ad copy variations, analysing campaign CSV exports, repurposing one blog into many formats

Please give me:
1. A two-sentence intro for the "About Me" section.
2. Four short "how I use AI" cards (a title + two sentences each).
3. Helpful, specific sample answers to these three visitor questions:
   - "How do I improve my Google Ads CTR?"
   - "Write me a LinkedIn ad for a SaaS free trial."
   - "What's a good content repurposing workflow?"

Keep it practical and confident, the way a real marketer would explain their craft.
```

## Make it your own
- Edit the four About cards to match your actual AI workflows and niche (B2B, e-commerce, influencer).
- Replace the three sample Q&A pairs with the questions people really ask you.
- Swap the colour palette via the CSS variables at the top of `<style>` to match your brand.

## Optional — automate it with the API (advanced)
You do **not** need this for the course. The page works fully on your Claude.ai subscription.
If you later want the Ask Me box to answer live from your own server instead of linking out
to Claude.ai, you could add a small backend that calls the Anthropic API with a key kept
server-side. That's an advanced extra and is never required to finish this hands-on.
