# Agents Memory

This document serves as a memory for all agents (human or automated) working on this repository. Please log below any significant changes, ideas, or decisions made during development to provide context for future contributors.

## Change Log

- Date: 2025-08-11
  - **Automated Agent**: index.html — Added PDF.js via CDN and configured worker. Restored canonical init flow (wpd.initApp) and removed temporary simplified init. Added minimal DOM required by controllers/widgets: popups (shadow, message/ok-cancel), page navigation and relabel popup, basic sidebars, and essential i18n strings.
  - **Automated Agent**: Smoke test — Served locally over HTTP; default image loads; a benign 404 to /log remains from analytics stub in services/log.js (safe to ignore on static hosting).
  - **Automated Agent**: UI — Modernized top bar (brand, Load sample, Help), consistent button styles, refined popups; added Help modal with quick steps. README updated with Quick start and sample image notes.

- Date: 2025-08-19
  - **Automated Agent**: Added touch event handling in `graphicsWidget` to support drawing on touch devices (iOS).

- Date: YYYY-MM-DD
  - **Agent**: Description of change

- Date: 2025-07-24
  - **Agent**: Created `agents.md` for agent memory.
  - **Agent**: Updated `README.md` to reflect Sounny’s fork, link to https://sounny.github.io, and note vanilla JS.
  - **Agent**: Corrected typos across project files (`DEVELOPER_GUIDELINES.md`, `script_examples/README.md`).
  - **Agent**: Created root `index.html` to redirect to `app/index.html`.
  - **Agent**: Pruned build tooling, back-end code, examples, docs, and templates to minimal static frontend.
- Date: 2025-07-24
  - **Automated Agent**: Replaced missing LFS image pointers with small placeholder PNGs and updated `index.html` to use the SVG crosshair. Ensured app loads without Git LFS.
- Date: 2025-07-26
  - **Automated Agent**: Removed remaining Git LFS pointer images and unused placeholder directories (`app`, `script_examples`, `images/icon`).

## Ideas and Notes

- Idea: 
- Note:
