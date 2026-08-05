# Changelog — Discovery Hub

Format based on [Keep a Changelog](https://keepachangelog.com/). The current version is shown in the app footer.

## [1.2.0] — 2026-08-05

### Added
- **Welcome is now its own page** (separate from the Dashboard), with a sidebar entry; the app opens here when no project has been started yet.
- **Interview media options (Steps 3 & 5):** besides live recording, you can now **upload an MP3** or **upload photos of handwritten notes** — useful when an interviewee declines to be recorded. Attachments are saved in JSON backups and referenced in the TNA Package.

### Changed
- Vietnamese UI: "Training Needs Analysis" → "Phân tích nhu cầu đào tạo"; reworded the welcome heading/description.
- Empty/silent recordings (<1 KB) are rejected with a clear message instead of appearing "saved".
- Clearer warnings when opened via `file://` (microphone & auto-transcript need `http://localhost` or https) and when auto-transcript fails due to network.

### Fixed
- **Security:** interview notes/transcripts and operational-data fields are now sanitized on input, import, and render — prevents stored-XSS via imported JSON files.
- Recording controls (Pause/Stop) no longer disappear if the page re-renders mid-recording.
- Released audio/image object URLs between renders (fixed a memory leak).
- Re-importing a file no longer creates duplicate/colliding record IDs.
- Step 2 progress now updates live while editing operational-data content.
- Removed dead code/CSS; internal cleanup.

---

## [1.1.0] — 2026-07-30

### Added
- First-run **welcome / empty state** with a one-click sample project (Auréa Bay) and a "sample data" banner so you can explore before starting.
- Contextual empty-state hints on each step (method guidance shown where data is missing).

### Changed
- Unified color system (single source of design tokens) and consistent step numbering (Screening + Steps 1–5).

### Fixed
- **Save reliability:** when browser storage is full, the app now shows a **"Save failed"** state with a rescue banner (Export JSON / free up space) instead of silently claiming "Saved"; early warning as the storage limit approaches.
- Microphone-denied state now shows an inline explanation with a **Retry** button.
- Import shows a result summary and distinguishes "not a valid JSON file" from "not a Discovery Hub file".

### Removed
- Removed unused/legacy features and dead code (AI-extract view, insight-capture / RCA workspace, redundant steps and documents).

---

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
