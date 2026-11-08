# 📊 Text Stats

> Words, reading time, readability, keyword density

![License](https://img.shields.io/badge/license-MIT-blue) ![Privacy](https://img.shields.io/badge/privacy-no%20uploads-black) ![Offline](https://img.shields.io/badge/offline-first-8b5cf6) ![PRs](https://img.shields.io/badge/PRs-welcome-green) ![Pages](https://img.shields.io/github/deployments/Kayforkind/NavigatorsLab-Text-Stats/github-pages?label=Pages&logo=github&event=push) ![Live check](https://img.shields.io/endpoint?url=https%3A%2F%2Fnavigatorslab.com%2Ftools%2Fbadge-textstats.json&cacheSeconds=300)

<h4 align="center">
  &#9654; <a href="https://navigatorslab.com/tools/textstats.html">Open it on navigatorslab.com</a> &mdash; free, no sign-up, nothing uploaded<br>
  <a href="https://navigatorslab.com/Text-Stats">navigatorslab.com/Text-Stats</a> &middot; <a href="https://navigatorslab.com/tools/videos/textstats.mp4">🔊 Watch Narrated Step-by-Step Tutorial Video</a> &middot; <a href="https://navigatorslab.com/tools/videos/notebooklm-overview.mp4">Watch Full Suite Hands-On Video</a><br>
  This repo's Pages site runs the <em>actual tool</em>: <code>demo.html</code>
</h4>

![Text Stats Annotated Live Usage Frame](poster.jpg)

Words, reading time, Flesch reading-ease, keyword density and a sentence-length rhythm histogram.

## 📖 Complete Step-by-Step User Guide

### Step 1: Paste Your Draft, Article, or Script Into the Editor (`Full-Width Text Editor (#textInput)`)
- **How to do it:** Paste or type your essay, documentation page, video script, or speech into `#textInput` (or pass `?text=...` / `?url=data:...` in the URL).
- **Expected result:** All metrics compute instantaneously on every keystroke.

### Step 2: Read Live Word Count, Reading Time & Flesch Grade (`Metric Cards Grid (#cards)`)
- **How to do it:** Review `#cards` for Words, Characters (with/without spaces), Sentences, Paragraphs, Reading Time (`225 wpm`), Speaking Time (`140 wpm`), Average Sentence Length, and Flesch Reading Ease (`0–100` + US Grade Level).
- **Expected result:** Instant readability and length verification.

### Step 3: Audit Top Keyword Density & Overused Terms (`Keyword Frequency Panel (#keywords)`)
- **How to do it:** Examine `#keywords` to see the top content words ranked by count and density percentage (with common English stop-words excluded).
- **Expected result:** Spot repetitive phrasing or verify SEO topic coverage immediately.

### Step 4: Balance Your Pacing with the Sentence-Rhythm Histogram (`Sentence-Rhythm Histogram (#rhythm)`)
- **How to do it:** Inspect `#rhythm`, which plots a bar for each sentence's word count so you can spot monotonous runs or overly dense 40-word sentences.
- **Expected result:** Polished, well-paced prose with verified readability.

## 🎛️ UI Controls, Shortcuts & Parameters Reference

| Control / Shortcut | What It Does |
|---|---|
| `Text Editor (`#textInput`)` | Full-width live textarea that recalculates metrics on every keystroke. |
| `11 Stat Cards (`#cards`)` | Words, characters, sentences, paragraphs, reading/speaking time, and Flesch score. |
| `Keyword Density (`#keywords`)` | Stop-word-filtered top terms with occurrence counts and percentages. |
| `Sentence Rhythm (`#rhythm`)` | Visual bar chart of sentence lengths across your document. |

## 💡 Pro Tips & Real-World Workflows

- 💡 Aim for a **Flesch Reading Ease between 60 and 75** (8th–9th grade level) for technical blog posts and product landing pages so readers scan effortlessly.
- 💡 Recording a YouTube Short or presentation? Check the **Speaking Time (`140 wpm`)** card to verify your script fits inside 60 seconds before recording.
- 💡 AI agents can invoke this analyzer over MCP (`POST /tools/mcp` -> `text_stats`) or via URL deep-link (`textstats.html?text=...`).

## 🧪 Concrete Example: Input → Engine → Output

| Stage | What Happens | Details |
|---|---|---|
| **1. Raw Input** | **Keynote Draft / Fellowship Essay (620 Words)** | Strict 650-word limit; need Flesch reading-ease score, speaking time, keyword density & sentence rhythm |
| **2. On-Device Engine** | **Real-time syllable, lexical density, Flesch-Kincaid & 7-bucket sentence-length histogram analyzer** | Runs 100% client-side in your browser tab under strict `CSP` (`connect-src 'none'`). |
| **3. Verified Output** | **Readability & Rhythm Report + Markdown Table** | 620/650 words (95% goal) · 2.5 min read · Flesch 64.2 (8th–9th grade) · Sentence rhythm histogram + Markdown copy |

```text
Words: 620/650 (95%) | Read: 2.5m | Flesch: 64.2 | Avg Sentence: 14.8 words | Top: privacy (3.2%)
```

- 🔊 **Narrated Step-by-Step Usage Tutorial Video (`36s`):** [`demo.mp4`](./demo.mp4) (also live at [`https://navigatorslab.com/tools/videos/textstats.mp4`](https://navigatorslab.com/tools/videos/textstats.mp4))
- 🎬 **Full Suite Hands-On Video Guide:** [`https://navigatorslab.com/tools/videos/notebooklm-overview.mp4`](https://navigatorslab.com/tools/videos/notebooklm-overview.mp4)

## ✅ What it does

- Words, characters, sentences, reading and speaking time
- Flesch reading-ease with grade level, plus keyword density
- Live sentence-rhythm histogram

## 🚀 Try it in 30 seconds

1. Paste the text
2. Get words, Flesch grade and keyword density
3. Watch the sentence-rhythm histogram

## 📸 Live UI in action

![Text Stats in action](shot.png)

## 🔒 Private by design

- **100% on-device** — files are processed in your browser and **never uploaded** to any server
- **No accounts, no tracking, no cookies, nothing retained** — open the page and work
- **Works offline** once loaded; fully mobile-friendly
- **Free & open source (MIT)** — use it at home, at work, anywhere

## 🤖 Built for humans *and* AI agents

- Deep-linkable via URL parameters — see the [Agent Mode guide](https://navigatorslab.com/tools/agents.html)
- Machine-readable catalog: [llms.txt](https://navigatorslab.com/tools/llms.txt) · [llms-full.txt](https://navigatorslab.com/tools/llms-full.txt)
- MCP endpoint: `POST https://navigatorslab.com/tools/mcp` (tool catalog + deterministic text tools — see the [main repo](https://github.com/Kayforkind/NavigatorsLab-Tools))
- No build step required to *use* any tool — just the URL

## 🛠 Under the hood

Pure TypeScript: Flesch reading-ease, keyword density, rhythm histogram

Third-party components are catalogued in [NOTICE](NOTICE); this repo is MIT-licensed ([LICENSE](LICENSE)).

## 🗂 The NavigatorsLab Tools suite

The full catalog — every tool in the hub with the same zero-upload promise, plus the lab's apps, CLIs and engines:

| Tool | What it does | |
|---|---|---|
| 🛡 Photo Privacy Kit | Strip GPS, camera model and timestamps before posting | [Open](https://navigatorslab.com/tools/exif.html) |
| 🔐 Password Breach Checker | Has this password been breached? — it never leaves your tab | [Open](https://navigatorslab.com/tools/breachcheck.html) |
| 🔍 Metadata & Hidden-Data Checker | See what's really inside a file — then strip it | [Open](https://navigatorslab.com/tools/metadata.html) |
| 🗜 Image Shrinker | Hit “max 2 MB” portal limits without TinyPNG | [Open](https://navigatorslab.com/tools/shrink.html) |
| 📄 Scan & Screenshot Cleaner | Phone photos of documents → clean, straight PDFs | [Open](https://navigatorslab.com/tools/scan.html) |
| ✍ Local E-Sign Pad | Sign this lease tonight — not DocuSign | [Open](https://navigatorslab.com/tools/sign.html) |
| 🧾 Receipts → One PDF | Shoebox of receipt photos → one date-sorted PDF | [Open](https://navigatorslab.com/tools/receipts.html) |
| 🔢 Receipt OCR → CSV | Read totals off receipt photos, export for expenses | [Open](https://navigatorslab.com/tools/ocr.html) |
| 🔳 QR Studio | Generate QR codes and decode QR images — no site sees them | [Open](https://navigatorslab.com/tools/qr.html) |
| 🎧 Audio Trimmer | Cut voice notes and clips on a waveform | [Open](https://navigatorslab.com/tools/audio.html) |
| 🧮 Invoice / Quote Generator | One-person shops: hours in, clean PDF out | [Open](https://navigatorslab.com/tools/invoice.html) |
| 🗂 Batch Rename & Sort | IMG_5847.jpg → 2026-09-05-receipt-home-depot.jpg | [Open](https://navigatorslab.com/tools/rename.html) |
| 🖨 Print-Shop Prep | Exact sizes, bleed, DPI checks, print-ready PDF | [Open](https://navigatorslab.com/tools/printprep.html) |
| 📑 PDF Pages | Reorder, rotate, delete and extract PDF pages | [Open](https://navigatorslab.com/tools/pdfpages.html) |
| 🔬 Text Diff | Compare two texts with word-level highlights | [Open](https://navigatorslab.com/tools/textdiff.html) |
| 🎨 Reimagine | Redesign any HTML page from its own content | [Open](https://navigatorslab.com/reimagine/) |
| **📊 Text Stats** | Words, reading time, readability, keyword density | [Open](https://navigatorslab.com/tools/textstats.html) |
| 📜 PDF Studio | Edit the text inside your PDF — private, free, open source | [Open](https://navigatorslab.com/pdf-studio/) |
| 🩺 Design Health | 18 deterministic design-quality checks for HTML — no LLM, no API key | [Open](https://github.com/Kayforkind/design-health-action) |
| 🔪 Skill Slice | Copy one Read-verified skill folder — a slice, not the pie | [Open](https://github.com/Kayforkind/skill-slice) |
| 🕵 liecatchers | Your agent said Done. Prove it — ten sensors, one RECEIPT.json | [Open](https://github.com/Kayforkind/liecatchers) |
| 📚 Book Guide MCP | Ship improvements with your books — agents cite, run playbooks, learn | [Open](https://github.com/Kayforkind/book-guide-mcp) |
| 📡 Data Insights | Founder intelligence — daily & weekly tech signal briefs | [Open](https://github.com/Kayforkind/data-insights) |
| 🪓 Iron Axe: Legacy | An original side-scrolling beat 'em up — Godot 4 | [Open](https://github.com/Kayforkind/iron-axe-legacy) |

---

<p align="center">
  <b>One hub, twenty-four projects:</b> <a href="https://navigatorslab.com/tools/">https://navigatorslab.com/tools</a><br>
  <b>Source &amp; the whole suite:</b> <a href="https://github.com/Kayforkind/NavigatorsLab-Tools">https://github.com/Kayforkind/NavigatorsLab-Tools</a>
</p>
