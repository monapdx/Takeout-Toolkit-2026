# Takeout Toolkit 🧰  
**Local-first pipelines for cleaning, transforming, and exploring your exported data**

Takeout Toolkit is a modular collection of **Python-based pipelines** for processing data exports from major platforms like **Gmail, Google Search, Facebook, and ChatGPT**.

It is designed for people who want to:
- Own their data
- Work offline
- Avoid cloud lock-in
- Turn raw exports into something **readable, explorable, and human-scale**

This is not a black-box dashboard.  
It is a **toolkit**.

---

## ✨ What This Is

- A set of **scripted pipelines** that transform messy export files into clean, structured outputs
- A **local-first** workflow (no servers, no uploads, no accounts)
- Designed for **archival, analysis, personal knowledge, and creative reuse**
- Built to be **inspectable, hackable, and remixable**

You can run one pipeline or many.  
You can stop at CSVs or launch a local visual explorer.

---

## 🚫 What This Is Not

- ❌ A hosted SaaS
- ❌ A surveillance or analytics product
- ❌ A single monolithic app
- ❌ A replacement for the original platforms

Your data stays on *your* machine, always.

---

## 📁 Repository Structure

Takeout-Toolkit/
├─ Python/
│ ├─ Gmail/
│ │ ├─ scripts/
│ │ ├─ pipeline.yaml
│ │ └─ README.md
│ │
│ ├─ Search/
│ │ ├─ scripts/
│ │ └─ pipeline.yaml
│ │
│ ├─ Facebook/
│ │ ├─ scripts/
│ │ └─ pipeline.yaml
│ │
│ └─ ChatGPT/
│ ├─ scripts/
│ └─ pipeline.yaml
│
├─ Screenshots/
└─ README.md


Each platform lives in its **own self-contained pipeline**.

---

## 🔌 Supported Pipelines

### 📧 Gmail
- Parses `.mbox` exports
- Extracts headers, metadata, and message structure
- Outputs CSV/JSON suitable for filtering, timelines, and stats

### 🔍 Google Search
- Processes Takeout search history
- Normalizes timestamps and queries
- Produces clean JSON and CSV datasets

### 📘 Facebook
- Parses Timeline HTML exports
- Filters automated app/game posts
- Extracts posts, timestamps, text, and metadata

### 🤖 ChatGPT
- Processes `conversations.json`
- Handles sparse and null nodes safely
- Outputs structured conversation data for analysis or visualization

---

## ▶️ How It Works (High Level)

1. You download your data using **Google Takeout** or platform export tools
2. You point a pipeline at the exported file(s)
3. The pipeline:
   - Validates input
   - Runs scripts in the correct order
   - Writes clean outputs to an `output/` directory
4. (Optional) You launch a **local visual explorer** for browsing the results

---

## 🧪 Example: Running a Pipeline

```bash
cd Python/Gmail
python run_pipeline.py --mbox ~/Downloads/mail.mbox


Each pipeline provides:

--help text

Sensible defaults

Optional flags for filtering and output control

📊 Outputs

Depending on the pipeline, outputs may include:

CSV files (for spreadsheets, pandas, or databases)

JSON files (for web apps and visualizations)

Intermediate artifacts (optional, for debugging)

All outputs are plain files, not databases.

🧠 Design Philosophy

Local-first – no network required

Readable over clever – clarity beats compression

Composable – pipelines are building blocks, not endpoints

Archival-friendly – outputs should still make sense in 10+ years

This toolkit is meant to age well.

🔐 Privacy & Safety

No telemetry

No tracking

No uploads

No credentials required

If you can run Python locally, you can use this.

🛠 Requirements

Python 3.10+

Standard libraries + a small set of well-known dependencies
(listed per-pipeline)

Each pipeline documents its own requirements.

🧩 Who This Is For

People exploring their digital history

Writers, artists, and researchers

Archivists and digital preservation nerds

Anyone who believes your data should be legible to you

📜 License

MIT License
Do whatever you want — just don’t pretend you wrote it.

🧭 Status

This project is actively evolving.
Pipelines may change as formats change.

Expect iteration, not abandonment.

💬 Notes

If something feels clunky, that’s a signal — not a failure.
This toolkit is meant to be shaped to fit your data and your questions.

Fork it. Break it. Make it yours.
