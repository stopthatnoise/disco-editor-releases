# Changelog

All notable changes to Disco Editor are listed here.

---

## [1.2.0] — 2026-03-08

### Changed
- **Major codebase refactoring** — split monolithic `server.mjs` (2010 lines) into modular structure: backend modules in `lib/`, frontend assets in `public/`. Server is now a 284-line routing layer. No functionality changes
- **Renamed to Disco Editor** — unified branding across all files, window title, and UI (was "Disco BE Editor" / "Рэдактар BE")
- **Installer filename** — now `Disco-Editor-Setup-1.2.0.exe` instead of `Disco.Editor.Setup.1.0.0.exe`

### Added
- **App icon** — custom icon for Electron window, GNOME taskbar, and Windows installer
- **About modal** — version, description, and repository links accessible via `?` button in the top bar

### Fixed
- Global search modal was visible behind other modals due to CSS specificity issue

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