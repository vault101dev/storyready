# StoryReady 🎯

**AI-powered behavioral interview story coach for FAANG and Tier-1 company interviews.**

StoryReady coaches you through crafting compelling STAR-format behavioral stories, maps them to leadership principles, preps you for every follow-up question, and helps you build a complete interview story portfolio — just like working with a dedicated FAANG interview coach.

Live at: **[vault101dev.github.io/storyready](https://vault101dev.github.io/storyready)**

---

## What It Does

You share a rough experience. StoryReady coaches you through it and returns:

- **Refined Response** — A polished, conversational version of your story aligned with FAANG expectations
- **STAR Breakdown** — Situation, Task, Action, Result structured and ready to use
- **Leadership Principles** — Which principles your story demonstrates (Strong vs. Moderate), with proof points
- **Follow-Up Questions** — Every probe the interviewer is likely to ask, with coaching on how to answer
- **Question Mapping** — Other interview questions your story can answer, with pivot tips

---

## Key Features

**Story Building**
- 15 pre-loaded interview questions covering all major FAANG behavioral categories
- Custom question support — type any question you're preparing for
- Multi-turn AI coaching conversation that strengthens your story before generating output
- Retry on failed generation — no lost work if the API times out

**Portfolio**
- Save completed stories to a persistent portfolio in your browser
- Expand each story with a tabbed interface: STAR Format / Leadership Principles / Follow-Up Questions / Other Questions
- Select individual stories or all stories for download
- Per-story cost tracking and total portfolio spend display

**Download Formats**
All downloads are generated client-side — no server, no uploads. Paragraph breaks and multi-line cell content are preserved automatically.

| Format | Notes |
|--------|-------|
| Text (.txt) | Plain text with section headers and paragraph breaks |
| Word (.docx) | Fully formatted with headings, bold labels, proper paragraph spacing |
| Google Docs | Downloads as .docx; one-click upload to Google Docs converts it automatically |
| CSV (.csv) | One row per story, multi-line cells for long-form content |
| Excel (.xlsx) | Styled spreadsheet with bold navy header row and wrap-text cells |
| Google Sheets | Downloads as .xlsx; upload to Google Sheets converts it automatically |

**Model Picker**
Choose your Claude model in the API key settings. Pricing displayed per model so you know exactly what you're spending before you start.

| Model | Input | Output | Best for |
|-------|-------|--------|----------|
| Claude Opus 4.8/4.7/4.6 | $15/M | $75/M | Highest quality output |
| Claude Sonnet 4.6 *(default)* | $3/M | $15/M | Best balance of quality and cost |
| Claude Haiku 4.5 | $0.80/M | $4/M | Fastest and cheapest |

**Multi-Session Support**
- Start a story, leave mid-conversation, start another — all sessions persist independently
- In Progress / Completed status badges on the question selection screen
- Resume any in-progress story exactly where you left off
- All sessions stored in your browser's localStorage — no account required

---

## API Key Setup

StoryReady is **bring-your-own-key** — each user connects their own Anthropic API key, stored only in their browser's `localStorage` and sent directly to Anthropic. The key never touches a server and is never visible to anyone else.

**Why this matters:**
- ✅ No cost exposure for the app owner — every user pays for their own usage
- ✅ No API key sitting in a public GitHub repo
- ✅ Works immediately on GitHub Pages with zero backend

**To get started:**
1. Open the app and click **🔑 Connect Key**
2. Get a free API key at [console.anthropic.com](https://console.anthropic.com) → API Keys → Create Key
3. Paste it in and choose your model — that's it

New Anthropic accounts include free starting credits. A typical story session costs $0.01–$0.05 with Sonnet 4.6.

---

## Interview Questions Covered

- Risk and failure
- Ethical dilemmas and integrity
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
- Custom questions (type any question)

---

## Tech Stack

- **React 18** via CDN — no build step
- **Babel Standalone** — JSX transpilation in the browser
- **Anthropic Claude API** — story coaching and refinement
- **Hand-rolled DOCX/XLSX generators** — valid ZIP + WordprocessingML/SpreadsheetML built entirely in vanilla JS, no npm packages; schema-validated against the official OOXML spec and round-trip tested through LibreOffice
- **Pure CSS** — custom dark design system, no framework
- **Single HTML file** — deploy anywhere static hosting is available

---

## Deployment

### GitHub Pages (live)
This app is deployed at [vault101dev.github.io/storyready](https://vault101dev.github.io/storyready).

To deploy your own fork:
1. Fork this repo
2. Go to **Settings → Pages → Source → main branch / root**
3. Your app will be live at `https://yourusername.github.io/storyready` within a few minutes

Make sure the repository is **public** — GitHub Pages requires a public repo on the free plan.

### Run Locally
```bash
cd storyready
python3 -m http.server 8000
# then open http://localhost:8000
```

Opening `index.html` directly via `file://` will not work — the browser blocks API calls and certain script behaviors under the file protocol. Serve it over `http://` instead.

---

## Analytics

This app uses Google Analytics (GA4) to track page views and session behavior. No personally identifiable information is collected. API keys are never logged or transmitted to any analytics endpoint.

---

## Built By

Built as a demonstration of AI-assisted product development. Conceived, designed, and built in collaboration with Claude (Anthropic) as a coding and product partner.

---

## License

MIT — use freely, fork freely, build on it.
