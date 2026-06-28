# HO2 Sample 3 — Consultant

## What you'll build
A first-contact page that answers a prospect's questions before you've even replied. It
shows your areas of expertise, how you work, the results you get for clients, and an
**"Ask Me Anything"** section that handles the usual pricing-and-process questions. This
folder already contains a finished example (Priya Nair, an operations & automation
consultant) — open it, see it working, then make it yours.

## Use it with your Claude.ai subscription
No API key needed. Just your normal Claude.ai login.

1. Open **`index.html`** from this folder in your browser to see the finished example page.
2. Open **Claude.ai** in another tab (your subscription — no API key, no billing).
3. Paste **the example prompt below** and fill in your own expertise and results. Claude
   will write your expertise descriptions, client-result lines, and prospect answers.
4. Open `index.html` in a text editor, replace the example text with what Claude wrote,
   and save.
5. Refresh the page in your browser to see your version.
6. (Optional) For a live link, push to GitHub and turn on **Settings → Pages** on `main`.

## The example prompt
Copy this into Claude.ai and fill in the parts in CAPITALS:

```
I'm an independent consultant building a one-page website to capture and answer leads. Help me write the content.

About my consulting:
- Name: YOUR NAME
- What I help clients with: e.g. operations & automation for small businesses
- My three main areas of expertise: LIST THEM
- How I work (my steps): e.g. discovery audit, design & build, handover & support
- Two or three real client results with numbers if possible: e.g. cut order-processing time 60%

Please give me:
1. A one-line tagline for the top of the page.
2. A short description for each of my three expertise areas.
3. A punchy one-line result for each client outcome (include the number).
4. Clear answers to these three prospect questions, two or three sentences each:
   - "How much do you charge and how is it priced?"
   - "What does working with you actually look like?"
   - "Do you work with small or early-stage businesses?"

Keep it professional, specific, and reassuring.
```

## Make it your own
- Replace the client results with your own — real numbers build trust fast.
- Adjust the "How I Work" steps to match your real process.
- Change the colour by editing `--color` near the top of `index.html`.
