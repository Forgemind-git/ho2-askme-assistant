# HO2 Sample 4 — Speaker / Creator

## What you'll build
A bio page that handles booking questions for you. It shows your speaking topics, past
events, booking info, and an **"Ask Me Anything"** section that answers what event
organisers always ask. This folder already contains a finished example (Jordan Blake, a
keynote speaker on AI productivity) — open it, see it working, then make it yours.

## Use it with your Claude.ai subscription
No API key needed. Just your normal Claude.ai login.

1. Open **`index.html`** from this folder in your browser to see the finished example page.
2. Open **Claude.ai** in another tab (your subscription — no API key, no billing).
3. Paste **the example prompt below** and fill in your own topics and events. Claude will
   write your topic descriptions, event blurbs, and organiser answers.
4. Open `index.html` in a text editor, replace the example text with what Claude wrote,
   and save.
5. Refresh the page in your browser to see your version.
6. (Optional) For a live link, push to GitHub and turn on **Settings → Pages** on `main`.

## The example prompt
Copy this into Claude.ai and fill in the parts in CAPITALS:

```
I'm a speaker and creator building a one-page bio site to make booking me easier. Help me write the content.

About me:
- Name: YOUR NAME
- What I speak about: MY MAIN THEME
- My three signature talk topics: LIST THEM
- A few past events (name, year, city, audience size): LIST THEM
- My booking details: formats (keynote/workshop/virtual), rough fee range, where I travel from

Please give me:
1. A one-line tagline for the top of the page.
2. A short, exciting description for each of my three talk topics.
3. A one-line summary for each past event.
4. Friendly, helpful answers to these three organiser questions, two or three sentences each:
   - "Do you speak virtually or only in person?"
   - "Can you tailor your talk to our industry?"
   - "What topics and dates are you available for?"

Keep it energetic and professional, like a speaker's press kit.
```

## Make it your own
- Swap in your real talks and the events you've actually spoken at.
- Update the booking info (fee range, formats, travel) so it's accurate.
- Change the colour by editing `--color` near the top of `index.html`.
