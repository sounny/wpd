Sounny's WebPlotDigitizer (Static Vanilla JS Fork)
==================================================

This is Sounny's fork of WebPlotDigitizer, a web-based tool to extract numerical data from plot images. It supports XY, Polar, Ternary, and Map axes. WebPlotDigitizer is used by thousands and is [cited in 600+ publications](https://scholar.google.com/scholar?as_vis=1&q=WebPlotDigitizer&hl=en&as_sdt=0,44). For the original project, visit https://automeris.io/WebPlotDigitizer.

![WebPlotDigitizer Screenshot](screenshot.png?raw=true "WebPlotDigitizer")

## Live demo

- GitHub Pages (if enabled): https://sounny.github.io/wpd/
	- If the link returns 404, enable GitHub Pages in the repository settings (Pages → Deploy from branch → `master` → `/ (root)`).

## Quick start

1. Open `index.html` in a modern browser (Chrome, Edge, Safari, Firefox), or serve the folder with any static HTTP server.
2. Click “Load sample” to try it instantly, or use “Load image/PDF” to select your own file.
3. Use the left tree to switch between Image, Axes, Datasets, and Measurements. The right-hand zoom pane helps with precise clicks.

Tip: Some browsers restrict web workers over the `file://` scheme. If PDF import fails when opening `index.html` directly, serve via HTTP (for example, with Python's simple server) and retry.

## Features in this fork

- Static, framework-free build that runs from a single `index.html` (GitHub Pages friendly).
- PDF import via PDF.js (loaded from a CDN). Multi-page PDFs enable a Page selector in the top bar.
- Non-blocking Help and Start sidebars with quick instructions.
- “Load sample” for instant testing and “Export CSV” for easy data export.
- Light theme by default with modernized styles.

## Notes

- Project resume from `.tar` archives is disabled in this static build (no bundler or Node services).
- You may see a benign `GET /log` 404 in the browser console; it's from an analytics stub and can be ignored on static hosting.

## Project structure

- `index.html` — Main entry point; includes all scripts and UI.
- `styles.css`, `widgets.css` — Core styles.
- `javascript/` — Application logic (controllers, services, widgets, tools).
- `images/` — Built-in icons and sample assets.
- `start.png` — Small sample image used by “Load sample”.
- `screenshot.png` — Screenshot for this README.
- `app/` — Historical folder for templates/build scripts; not used in this fork.

## Troubleshooting

- PDF import fails or worker error in console: serve the folder via HTTP instead of opening with `file://` and try again.
- UI doesn’t update after a change: hard refresh (Cmd+Shift+R) to bypass cache.
- 404 for `/log`: expected on static hosting; safe to ignore.

## Stable versions of the original

The `master` branch here tracks active development of this static fork. For stable releases of the original WebPlotDigitizer, see: https://github.com/ankitrohatgi/WebPlotDigitizer/releases

## Contributing & agents memory

- Read the [Developer Guidelines](DEVELOPER_GUIDELINES.md).
- Log significant changes, ideas, and decisions in [agents.md](agents.md) to maintain context for future contributors.

## License

WebPlotDigitizer is distributed under the [GNU AGPL v3](https://www.gnu.org/licenses/agpl-3.0.en.html). This fork is also distributed under the same license.

## Contact & resources

- Issues: use GitHub Issues on this repository.
- Info and updates: https://sounny.github.io
