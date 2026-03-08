# Changelog

All notable changes to Disco Editor are listed here.

---

## [1.1.0] — 2026-03-08

### Fixed
- Zoom shortcuts (`Ctrl++` / `Ctrl+-` / `Ctrl+0`) were broken due to hidden menu bar — replaced with a direct `webContents` input handler

### Added
- **Undo / Redo** — `Ctrl+Z` / `Ctrl+Shift+Z` (or `Ctrl+Y`) with toolbar buttons; history is per-session and clears on dialogue load
- **Search highlighting** — matching text highlighted inline across all language rows when search field has 3+ characters; editable BE textareas get a subtle tint
- **Persist working directory** — selected folder is saved to config and restored on next launch
- **Restore last session** — last opened dialogue and focused node are saved and restored when the app starts

---

## [1.0.0] — 2026-03-08

Initial public release.

### Features
- Tree view of dialogue nodes with collapsible branches
- English and Polish shown alongside Belarusian for context
- Inline editing of Belarusian text with `Enter` / `Escape` / `Shift+Enter`
- `Tab` / `Shift+Tab` to move between BE fields
- `↑` / `↓` / `←` / `→` keyboard navigation across nodes
- `Ctrl+S` to save the entire dialogue to disk
- Node count display (visible / total)
- Global search across all dialogue files (opens results in a new tab)
- Filter nodes by text within the current dialogue
- Alternates (variant lines) shown and editable inline
- Git panel: create branch, commit, push, open pull request
- GitHub token setup for PR creation
- Electron desktop app with Windows installer
