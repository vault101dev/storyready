# StoryReady 🎯

**AI-powered behavioral interview story coach for FAANG and Tier-1 company interviews.**

StoryReady coaches job seekers through crafting compelling STAR-format behavioral stories, maps them to leadership principles, and preps you for every follow-up question — just like working with a dedicated FAANG interview coach.

---

## What It Does

You share a rough experience. StoryReady returns:

- **Refined Response** — A polished, conversational version of your story aligned with FAANG expectations
- **STAR Breakdown** — Situation, Task, Action, Result structured and ready to paste into your prep sheet
- **Leadership Principles** — Which principles your story demonstrates (Strong vs. Moderate)
- **Follow-Up Questions** — Every probe question the interviewer is likely to ask, with coaching on how to answer
- **Question Mapping** — Other interview questions your story can answer, with pivot tips

---

## How to Use It

### Option 1: GitHub Pages (Recommended)
1. Fork this repository
2. Go to **Settings → Pages**
3. Set source to **main branch / root**
4. Your app will be live at `https://yourusername.github.io/storyready`

### Option 2: Run Locally
Just open `index.html` in any modern browser. No build step, no dependencies, no server required.

---

## Tech Stack

- **React 18** (via CDN — no build step required)
- **Babel Standalone** (JSX transpilation in browser)
- **Anthropic Claude API** (claude-sonnet-4-6 for story coaching and refinement)
- **Pure CSS** (no framework — custom design system)
- Single HTML file — deploy anywhere

---

## API Key Setup

StoryReady is **bring-your-own-key** — each user connects their own Anthropic API key, which is stored only in their browser's `localStorage` and sent directly from their browser to Anthropic's API. The key never touches a server, and it's never visible to other users.

**Why this matters:**
- ✅ No cost exposure for the app owner — every user pays for their own usage
- ✅ No shared secret sitting in a public GitHub repo
- ✅ Works immediately on GitHub Pages with zero backend

**For users:**
1. Open the app
2. Click "🔑 Connect Key" when prompted
3. Get a free API key at [console.anthropic.com](https://console.anthropic.com) → API Keys → Create Key
4. Paste it in — that's it. New Anthropic accounts include free starting credits.

A typical story session (coaching conversation + full output generation) costs roughly $0.01–$0.05 in API usage.

---

## Features

- 🎯 **15 pre-loaded interview questions** covering all major FAANG behavioral categories
- ✏️ **Custom question support** — type any question
- 🤖 **Multi-turn coaching conversation** — AI asks follow-up questions to strengthen your story before generating output
- 📋 **One-click copy** — copy everything to clipboard
- ⬇️ **Download as text file** — save to your computer and upload to Google Drive
- 📱 **Responsive design** — works on desktop and mobile
- 🌙 **Dark mode** — easy on the eyes during late-night prep sessions

---

## Interview Questions Covered

- Risk and failure
- Ethical dilemmas
- Raising the bar
- Disagreeing with your manager
- Limited resources / frugality
- Ruthless prioritization
- Change management
- Scope creep / requirement volatility
- Data-driven decisions
- Managing a major pivot
- Conflicting team incentives
- Mentoring and developing others
- Compliance and regulatory risk
- Fast decisions with incomplete information
- Custom questions

---

## Built By

Built as a demonstration of AI-assisted product development. This app was conceived, designed, and built using Claude as a collaborative coding partner.

---

## License

MIT — use freely, fork freely, build on it.
