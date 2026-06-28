# HO2 Sample 3 — Teacher AI Page

## What you'll build
A polished personal "Ask Me" page for a teacher (the example is Ms. Priya Sharma, a
secondary-school science teacher). It shows her teaching approach, how she uses AI to plan
lessons and support different learners, and an **Ask Me** section with worked example answers
for students, parents and fellow educators — plus a button that opens Claude.ai for live
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
I'm building a personal "Ask Me" web page that shows how I use AI as a teacher. Help me write the content.

About me:
- Name: YOUR NAME
- Role: e.g. Secondary School Science Teacher, Years 7–13
- Subjects/curriculum: e.g. UK GCSE Biology, Chemistry, Physics
- The main ways I use AI: e.g. lesson plans, quiz questions, plain-English explainers, differentiation ideas

Please give me:
1. A two-sentence intro for the "About Me" section.
2. Four short "how I use AI" cards (a title + two sentences each).
3. Clear, friendly sample answers to these three visitor questions:
   - "Can you explain photosynthesis simply?"
   - "How do I differentiate for mixed-ability classes?"
   - "Give me a starter activity for Year 9 chemistry."

Keep it warm and practical, written for students, parents and fellow teachers.
```

## Make it your own
- Change the subject specialism (Physics vs Biology), year groups and curriculum (GCSE, IB, AP).
- Replace the sample answers with explanations from topics you actually teach.
- Swap the green palette via the CSS variables at the top of `<style>`.

## Optional — automate it with the API (advanced)
You do **not** need this for the course. The page works fully on your Claude.ai subscription.
If you later want the Ask Me box to answer live from your own server, you could add a small
backend that calls the Anthropic API with a key kept server-side. That's an advanced extra,
never required to finish this hands-on.
