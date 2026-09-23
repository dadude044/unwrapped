# Unwrapped

**The tools these apps charge $70–135/month for, minus the wrapper.**

Resume.io, CoverPaste, Coverler, LinkedIn "AI optimizer" tools, and $25–70/mo case-interview coaches are, underneath, a prompt wrapped in a subscription. This is that prompt, run for free, using an AI model you provide the key for yourself.

**Live demo:** `https://dadude044.github.io/unwrapped/` *(fill in once Pages is enabled — see Step 4 below)*

---

## What's inside

One HTML file, no build step, no backend, no database. Five tools:

| # | Tool | What it does |
|---|------|---------------|
| 01 | Resume | Tightens rough bullets into quantified, resume-ready lines |
| 02 | Cover letter | Turns your background + a job description into a specific 3-paragraph letter |
| 03 | LinkedIn | Writes a headline + About section tuned for recruiter search |
| 04 | Case prep | Runs a live, turn-by-turn mock consulting case interview |
| 05 | Price check | Shows what each tool above would cost as a paid subscription |

Everything runs client-side. Your browser talks directly to Google's Gemini API using a key you get yourself. This project's server never sees your key, your resume, or anything you type, because this project has no server.

## Setup (for anyone using the live site)

1. **Get a free Gemini API key** — go to [aistudio.google.com/apikey](https://aistudio.google.com/apikey), sign in with any Google account, click **Create API key**. No credit card needed for this step.
2. **Paste it into the site** — open the live demo link above, paste your key into the field at the top labeled *YOUR GEMINI API KEY*. It's saved only in your own browser (`localStorage`), never sent anywhere but Google.
3. **Open the menu (☰, top left)** and pick a tool.

The site itself walks through all of this in more detail on its own "Start Here" pages, this is just the short version.

### Usage limits

Every visitor uses their *own* key, so there's no shared pool to run out of. Per person: **500 requests/day, 15/minute** on Gemini's free tier (verify current numbers at [aistudio.google.com](https://aistudio.google.com) → Usage, they can change). The site cools each button down for 4 seconds after a click so normal use won't trip the per-minute cap.

## Running it yourself instead of using the hosted link

Clone or download this repo, then just open `index.html` in any browser. No install, no dependencies, no server to run.

```bash
git clone https://github.com/YOUR-USERNAME/unwrapped.git
cd unwrapped
open index.html   # or double-click it
```

## Publishing your own copy on GitHub Pages (free hosting)

1. Create a new **public** repository on GitHub.
2. Upload `index.html` and this `README.md` (drag-and-drop works fine on github.com, no command line needed).
3. Go to the repo's **Settings → Pages**.
4. Under **Build and deployment**, set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
5. GitHub gives you a live URL after a minute or two, usually `https://YOUR-USERNAME.github.io/REPO-NAME/`.

That's it, no server to pay for, no build pipeline. GitHub Pages hosting is free for public repos.

## A note on what this is

This is a personal, open-source developer project, a demonstration of calling Google's Gemini API from a static page with a user-supplied key, shared for other developers to read and adapt. It is not a commercial product. Google's Gemini API terms restrict use to developers building for "professional or business purposes, not for consumer use" — if you fork this and put it in front of a general audience at scale, that's worth reading yourself: [ai.google.dev/gemini-api/terms](https://ai.google.dev/gemini-api/terms).

Not affiliated with Resume.io, CoverPaste, Coverler, LinkedIn, or any case-prep tool named on the site's Price Check page.

## License

Do whatever you want with this code. No warranty, use at your own risk, especially around the legal note above.
