Sounny's WebPlotDigitizer (Fork)
=================================

This is Sounny's fork of WebPlotDigitizer, a web-based tool to extract numerical data from plot images. Supports XY, Polar, Ternary diagrams, and Maps. This open source tool is used by thousands and [cited in over 600 published articles](https://scholar.google.com/scholar?as_vis=1&q=WebPlotDigitizer&hl=en&as_sdt=0,44). Visit https://automeris.io/WebPlotDigitizer for the original project.
Quick start
1. Open `index.html` in a modern browser (Chrome, Edge, Safari, Firefox), or serve the folder with any static HTTP server.
2. Click “Load sample” to try it instantly, or use “Load image/PDF” to select your own file.
3. Use the left tree to switch between Image, Axes, Datasets, and Measurements. The right-hand zoom pane helps with precise clicks.

Notes
- PDF import works via PDF.js (loaded from a CDN). Multi-page PDFs enable a Page selector in the top bar.
- Project resume from .tar archives is disabled in this static build.

UI tweaks in this fork
- A modernized top bar with Load sample and Help.
- Minimal popups and page relabel controls are built-in (no templating).

Maintenance notes
- The historical `app/` folder (templates/build scripts) is not used in this fork. All runtime files live at the repository root for static hosting.
![WebPlotDigitizer Screenshot](screenshot.png?raw=true "WebPlotDigitizer")


Sample image
- A small sample image (`start.png`) is included; “Load sample” uses this so you can test immediately.
Contact & Resources
-------------------

To report issues, use GitHub Issues on this repository. For general inquiries or contributions, visit https://sounny.github.io or contact the maintainer via GitHub.

License
-------

WebPlotDigitizer is distributed under [GNU AGPL v3](https://www.gnu.org/licenses/agpl-3.0.en.html). Sounny's fork is also distributed under the same license.

Stable Versions & Running
-------------------------

The master branch in this repository is for development of Sounny's fork and may be unstable. To access stable releases of the original WebPlotDigitizer, visit: https://github.com/ankitrohatgi/WebPlotDigitizer/releases

This version runs on vanilla JavaScript and can be opened in any modern web browser by loading `index.html`.
Contributing & Agents Memory
---------------------------

To contribute to Sounny's fork, please refer to the [developer guidelines](DEVELOPER_GUIDELINES.md). All agents (human or automated) should log changes, ideas, and decisions in the [Agents Memory](agents.md) to provide context for future contributors.
