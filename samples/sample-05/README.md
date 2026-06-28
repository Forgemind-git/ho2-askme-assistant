# HO2 Sample 5 — Product Manager AI Page

## What you'll build
A polished personal "Ask Me" page for a product manager (the example is Maya Chen, a fintech
PM). It shows the role, how they use AI across the product lifecycle, and an **Ask Me**
section with worked example answers about prioritisation, PRDs and measuring success — plus a
button that opens Claude.ai for live chat. It's a single self-contained `index.html`: HTML,
CSS, and a little JavaScript, no build step.

## Use it with your Claude.ai subscription
No API key needed. This page runs entirely in the browser and uses your normal Claude.ai
login for the "chat live" part.

1. Open **`index.html`** in your browser to see the finished page and its example answers.
2. Open **Claude.ai** in another tab (your subscription — no API key, no billing, no terminal).
3. Paste **the example prompt below** into Claude.ai and fill in your own details. Claude
   will write your About section and a set of strong sample answers.
4. Open `index.html` in a text editor and replace the example name, About cards, and Q&A
   pairs with what Claude gave you. Save.
5. Refresh the browser to see your version. The "Open claude.ai to chat live" button already
   points visitors to your subscription.

## The example prompt
Copy this into Claude.ai and fill in the parts in CAPITALS:

```
I'm building a personal "Ask Me" web page that shows how I use AI as a product manager. Help me write the content.

About me:
- Name: YOUR NAME
- Role: e.g. Product Manager at a fintech startup
- My product domain: e.g. payments / lending / investing
- Frameworks I use: e.g. RICE, OKRs, Jobs-to-be-Done
- The main ways I use AI: e.g. drafting PRDs, user stories, competitor briefs

Please give me:
1. A two-sentence intro for the "About Me" section.
2. Four short "how I use AI" cards (a title + two sentences each).
3. Sharp, specific sample answers to these three visitor questions:
   - "How do I prioritise a feature backlog?"
   - "What's the best way to write a PRD?"
   - "How do I measure if a feature was successful?"

Keep it crisp and outcome-focused, the way a strong PM communicates.
```

## Make it your own
- Update the company stage (Series A, growth) and product domain (payments, lending, investing).
- Edit the About cards to reflect your real PM workflows and frameworks.
- Swap the indigo/blue palette via the CSS variables at the top of `<style>`.

## Optional — automate it with the API (advanced)
You do **not** need this for the course. The page works fully on your Claude.ai subscription.
If you later want the Ask Me box to answer live from your own server, you could add a small
backend that calls the Anthropic API with a key kept server-side. That's an advanced extra,
never required to finish this hands-on.
