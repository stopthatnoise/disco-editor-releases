# Changelog

All notable changes to Disco Editor are listed here.

---

## [1.3.0] — 2026-03-08

### Added
- **Branch switching** — click the branch name in the git bar to open a list of local branches; click any to switch; warns if there are uncommitted or unsaved changes; reloads the current dialogue after switching
- **Translation diff in commit modal** — shows changed `belarusian` fields as mini-nodes with before/after text and word-level LCS highlighting (changed words marked with coloured backgrounds)
- **Single-file commit toggle** — checkbox in commit modal (on by default) that limits staging to the current dialogue file only; the file list and diff update live when toggled
- **Discard per node** — ↩ button on each diff mini-node reverts that field to the HEAD version without affecting the rest of the file
- **PR Review Comments sidebar** — 💬 Рэв'ю button opens a right sidebar showing all open review threads for the current branch's PR; threads include replies and formatted diff hunks with coloured lines (+/−/@@ syntax highlighting)
- **Auto node-matching** — on sidebar load, each review thread is automatically matched to a node using a multi-level search: `articyId` → `english` → `polish` → `belarusian`; clicking a comment navigates directly to the matched node
- **Reply from sidebar** — textarea under each thread posts replies to GitHub directly from the editor
- **PR button guard** — "Стварыць PR" button is disabled when an open PR already exists for the current branch

### Fixed
- Commit modal discard handler crashed with an unreadable error when the server had not been restarted after an update

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
