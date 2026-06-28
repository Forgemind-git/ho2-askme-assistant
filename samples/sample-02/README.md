# HO2 Sample 2 — Data Analyst AI Page

## What you'll build
A polished personal "Ask Me" page for a data analyst (the example is Jordan Kim, an
e-commerce analyst). It introduces the role, shows how they use AI for SQL, KPI reading and
exec summaries, and includes an **Ask Me** section with worked example answers — plus a
button that opens Claude.ai so visitors can keep chatting live. It's a single self-contained
`index.html`: HTML, CSS, and a little JavaScript, no build step.

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
I'm building a personal "Ask Me" web page that shows how I use AI as a data analyst. Help me write the content.

About me:
- Name: YOUR NAME
- Role: e.g. Data Analyst specialising in e-commerce
- My stack: e.g. PostgreSQL, Looker, Python
- The main ways I use AI: e.g. drafting SQL, spotting trends in chart data, turning raw numbers into exec summaries

Please give me:
1. A two-sentence intro for the "About Me" section.
2. Four short "how I use AI" cards (a title + two sentences each).
3. Helpful, specific sample answers to these three visitor questions:
   - "Write a SQL query to find top 10 customers by LTV."
   - "What does a sudden drop in conversion rate mean?"
   - "How do I write an exec summary from raw data?"

Keep it clear and business-focused, the way a real analyst explains insights to non-technical stakeholders.
```

## Make it your own
- Edit the About cards to match your own tech stack (BigQuery instead of PostgreSQL, Tableau instead of Looker).
- Replace the sample SQL and answers with examples from your own industry.
- Swap the teal palette via the CSS variables at the top of `<style>`.

## Optional — automate it with the API (advanced)
You do **not** need this for the course. The page works fully on your Claude.ai subscription.
If you later want the Ask Me box to answer live from your own server, you could add a small
backend that calls the Anthropic API with a key kept server-side. That's an advanced extra,
never required to finish this hands-on.
