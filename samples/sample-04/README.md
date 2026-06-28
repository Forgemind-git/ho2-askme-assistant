# HO2 Sample 4 — HR Professional AI Page

## What you'll build
A polished personal "Ask Me" page for an HR professional (the example is Sam Okafor, an HR
Business Partner). It introduces the role, shows how they use AI for job descriptions,
policies and 1:1 prep, and includes an **Ask Me** section with worked example answers for
colleagues, hiring managers and job seekers — plus a button that opens Claude.ai for live
chat. It's a single self-contained `index.html`: HTML, CSS, and a little JavaScript, no build
step.

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
I'm building a personal "Ask Me" web page that shows how I use AI as an HR professional. Help me write the content.

About me:
- Name: YOUR NAME
- Role: e.g. HR Business Partner, People & Culture
- My focus areas: e.g. performance management, hiring, onboarding, policy
- Jurisdiction/company size: e.g. UK employment law, 200-person scale-up
- The main ways I use AI: e.g. drafting job descriptions, policy docs, 1:1 prep notes

Please give me:
1. A two-sentence intro for the "About Me" section.
2. Four short "how I use AI" cards (a title + two sentences each).
3. Practical, careful sample answers to these three visitor questions:
   - "How should I handle a performance improvement plan?"
   - "What are best practices for onboarding new hires?"
   - "How do I write a JD that attracts diverse candidates?"

Keep it professional and people-first, and note where local employment law should be checked.
```

## Make it your own
- Update the jurisdiction and company size so the advice reads as relevant to your context.
- Edit the About cards for your specialism (L&D, Talent Acquisition, Comp & Benefits).
- Swap the amber/orange palette via the CSS variables at the top of `<style>`.

## Optional — automate it with the API (advanced)
You do **not** need this for the course. The page works fully on your Claude.ai subscription.
If you later want the Ask Me box to answer live from your own server, you could add a small
backend that calls the Anthropic API with a key kept server-side. That's an advanced extra,
never required to finish this hands-on.
