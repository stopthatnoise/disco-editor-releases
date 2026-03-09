# Disco Editor  

  A desktop editor for the Belarusian fan translation of Disco Elysium.

  Built for translators working on the [disco-bel-translation](https://github.com/stopthatnoise/disco-bel-translation) project.

  ---

  ## Download

  Go to the [Releases](https://github.com/stopthatnoise/disco-editor-releases/releases) page and download the latest installer.

  **Supported platforms:** Windows, macOS

  ---

  ## Features

  - Browse and edit dialogue nodes with English and Polish shown as reference
  - Tree view with collapsible nodes and keyboard navigation
  - Global search across all dialogue files
  - Git integration — create branches, commit, push, and open pull requests directly from the editor
  - Auto-saves to JSON files on disk

  ---

  ## Installation

  ### Windows

  1. Download `Disco-Editor-Setup-x.x.x.exe` from the latest release
  2. Run the installer
  3. On first launch, point the editor to your local `dialogues` folder

  ### macOS

  1. Download `Disco-Editor-x.x.x.dmg` from the latest release
  2. Open the DMG and drag **Disco Editor** to your Applications folder
  3. On first launch, macOS may block the app with a *"damaged and can't be opened"* message — this happens because the app is not notarized by Apple

  **To fix this, run the following command in Terminal:**

  ```bash
  xattr -dr com.apple.quarantine /Applications/Disco\ Editor.app
  ```

  Then launch the app normally.

  Alternatively, go to **System Settings → Privacy & Security** and click **Open Anyway** shortly after the blocked launch attempt.

  ---

  ## Usage

  See the full documentation in the [Manual](https://github.com/stopthatnoise/disco-editor-releases/blob/main/MANUAL.md).
