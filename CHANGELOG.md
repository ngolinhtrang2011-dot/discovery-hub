# Changelog — Discovery Hub

Format based on [Keep a Changelog](https://keepachangelog.com/). The current version is shown in the app footer.

## [1.0.0] — 2026-07-25

🎉 **First public release.**

### Features
- **Step 0 — Go/No-Go Screening:** 7 screening questions with an automatic verdict (GO / GO WITH CONDITIONS / NO-GO) and alternative recommendations when the project doesn't fit Action Mapping
- **Step 1 — Business Goal:** goal defined as Metric + Baseline → Target + Deadline, with sponsor and confirmation status
- **Step 2 — Operational Data:** Data Request List with file attachments (complaint logs, mystery shopper reports, QA scores...)
- **Step 3 — Staff & Manager Interviews** and **Step 5 — SME Interviews:** notes, live audio recording, automatic transcription (Chrome/Edge + internet), and a Scenario Bank capturing real incidents as raw material for practice design
- **Step 4 — Learner Profile:** who the performers are and their real working conditions
- **TNA Package export:** a single `.md` file containing all collected data plus embedded AI analysis instructions — direct input for generating an Action Map
- **Progress dashboard** + "Ready to map" indicator (requires Screening GO + completed Goal + operational and interview data present)
- **Bilingual Vietnamese–English UI** with instant switching, preference saved
- **Responsive across 3 device classes:** smartphone / tablet / desktop — usable for note-taking during live interviews
- **Autosave** (localStorage) + **JSON Export/Import** for backups and merging data from multiple collectors
- **Data management:** "Start new project" (full wipe with pre-delete backup prompt) and per-section deletion
- Print-ready documents (A4/PDF) generated automatically from collected data

### Release notes
- Automatic transcription is supported on Chrome/Edge with an internet connection only; other browsers can still record audio and paste transcripts later
- All data is stored locally in the browser — export JSON after every working session

---

## Development history (internal, pre-release)

### [0.4.0] — 07/2026
- Repositioned the tool to focus purely on **TNA data collection**; analysis work (gap classification, root cause) moved to the AI-assisted Action Mapping stage
- Removed pain-point tagging at data entry and the RCA analysis workspace
- Removed Step 6 (Constraints) & Step 7 (Commitments) — streamlined to Steps 0–5
- Added interview recording + automatic transcription
- Added file attachments for the Data Request List (IndexedDB)
- Added TNA Package export
- Added Next/Back navigation between steps

### [0.3.0] — 07/2026
- Added Step 0 — Go/No-Go Screening with automatic verdict logic

### [0.2.0] — 07/2026
- Added bilingual Vietnamese–English UI (i18n dictionary, VI/EN toggle)
- Responsive layout across 3 breakpoints: smartphone / tablet / desktop

### [0.1.0] — 07/2026
- Initial build: data collection flow based on the 7-step pre-Action-Mapping checklist (*Map It* — Cathy Moore), autosave, JSON export/import, print-ready documents

---

*Discovery Hub — designed by Trang Ngo, CPTD. Bug reports and feature requests: see Contributing & feedback in the README.*
