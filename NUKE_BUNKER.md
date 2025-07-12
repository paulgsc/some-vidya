
---

# 🧪 **Search Poison Checklist**

> A toolkit to prevent unwanted search traffic from “normie” behavior while keeping your videos functional for yourself.

---

## 🏷️ **Title Poisoning (High Priority)**

### ✅ DO:

* Use vague, poetic, numeric, or symbolic titles:

  * `#83 - event horizon loops (devlog)`
  * `S4E19 - feedback decay spiral`
* Use neutral metadata words like: `log`, `archive`, `raw`, `dump`, `stream`, `pulse`, `trace`, `fractal`, etc.
* Use internal codes: `[#ws]` instead of “websocket”, `[#tok]` instead of “tokio”

### ❌ AVOID:

* **Any keyword** that looks like:

  * Tech tutorial queries (`websocket`, `obs`, `debug`, `ai`, `python`, `error fix`)
  * Product names (`obs`, `vscode`, `nodejs`)
  * User intent verbs (`how to`, `fix`, `explain`, `setup`)
  * Direct mentions of major frameworks, tools, or concepts
* Question formats: `"How does X work?"` will immediately rank in search

---

## 📦 **Description Hardening (Medium Priority)**

### ✅ DO:

* Put internal tags at bottom in structured format:

```md
--- metadata ---
tags: [#obs, #ws, #dbg]
notes: reconnect crash loop in tokio
context: raw stream, internal ref
----------------
```

* Prefer your own **shorthand tags** (`#dbg`, `#tsync`) over canonical terms
* If you must mention tools, do so **deep in the description**, never at top

### ❌ AVOID:

* Putting "normal" keywords in the **first 2 lines** of the description (they’re indexed more heavily)
* Phrases that look like help content: `in this video, I’ll show you how...`

---

## 🖼️ **Thumbnail Design (Optional but Helpful)**

### ✅ DO:

* Use abstract visuals, static color swatches, timestamp overlays, or blurred text
* Optionally: use no custom thumbnail at all (forces default, neutral frames)

### ❌ AVOID:

* Faces
* Logos (OBS, React, AI stuff)
* Screenshots with readable code
* Anything resembling a “tutorial snapshot” (e.g. a UI in mid-click)

---

## 🔒 **Tags & Hashtags (Low Priority, but Worthwhile)**

YouTube says tags have minimal effect, but:

### ✅ DO:

* Use **non-keyword tags**: `meta-log`, `no-index`, `internal-ref`
* Use meaningless hashtags: `#x43`, `#looptrace`, `#nofeed`

### ❌ AVOID:

* `#obs`, `#ai`, `#websocket`, `#javascript` — these still get scraped
* Tutorial / coding hashtags: they may still push you into unwanted buckets

---

## 🛠️ **Other Tactics**

### ✅ DO:

* **Unlist videos** not meant for discovery, but include them in public **playlists**
* Add a **"private channel note"** at the start of the description like:

  > `Note: This is a raw devlog, not intended for general search traffic.`

### ❌ AVOID:

* Adding videos to generic playlists (`WebSocket Tutorials`, `OBS Fixes`)
* Enabling **auto-caption translation** if your speech contains hot keywords (they get indexed!)

---

## 🗃️ Optional: External Index Strategy

Build a local or cloud-based index (e.g., Notion, Obsidian, markdown repo) that tracks:

```md
## #83 - event horizon loops (devlog)
Date: 2025-07-12
Tags: [#obs, #ws, #tok]
Summary: testing reconnect logic, hit crash on reconnect edge.
URL: https://youtube.com/watch?v=abc123
```

Then you can **fully poison your channel metadata** on YouTube, and **rely on the external index** for retrieval.

---

## ☢️ TL;DR – "Poison Pill" Title Template

```txt
#84 - [abstract phrase] (devlog)
```

```md
--- metadata ---
tags: [#ws, #dbg, #obs]
context: livestream debug trace
summary: websocket reconnect problem
```

---
