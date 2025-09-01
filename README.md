# Simple Playlist Extractor

The **Simple Playlist Extractor** is a lightweight tool for extracting and filtering labels from JW Library playlist files (`.jwlplaylist` or `.jwlibrary`).

## Features

- **Drag & Drop** or choose a file with a clean dotted drop zone.
- **Deep teal accent strip** and minimal UI.
- **Filters**:
  - **All**: Show everything.
  - **Filtered**: Hide common headings (Title, Subheading, Q, R, Review).
  - **Custom**: Match by prefix or exact text.
- **Checklist Mode**:
  - Toggle to show results as checkboxes.
  - State persistence via `localStorage`.
- **Diagnostics Pill**:
  - Displays detected label count and source tables.
  - Rightâ€‘aligned, elegant styling.
- **Clipboard Button**:
  - **Checklist ON** â†’ copies only checked items.
  - **Checklist OFF** â†’ copies all visible rows.
  - Visual feedback with âœ… checkmark.

## Usage

1. Open `simple_playlist_extractor.html` in your browser.
2. Drag and drop a `.jwlplaylist` / `.jwlibrary` file, or use **Choose File**.
3. Click **Extract** to parse and view results.
4. Use filters or checklist mode to refine results.
5. Copy results with the clipboard button.

## Technical Notes

- Built with **TailwindCSS** for styling.
- Uses **JSZip** to read compressed JW Library files.
- Uses **sql.js** (SQLite compiled to WebAssembly) to query embedded databases.
- All data processing runs **entirely in the browser**. No server required.

## Baseline Behavior

This repository locks the following as baseline for all future changes:

- Deep teal accent color (`bg-teal-700`).
- Dotted gray border file drop zone.
- Alternating row colors in results table (half width, left aligned).
- Diagnostics pill always visible before results.
- Clipboard logic (checked only vs all) is fixed.
