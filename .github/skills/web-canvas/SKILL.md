---
name: web-canvas
description: Creates a local interactive web design canvas when users want to explore and adjust a web application's visual design before implementation.
---

# Web canvas

Create a lightweight, local design canvas that lets the user compare and adjust
the visual direction of a web application.

## Workflow

1. Inspect the application's existing framework, styles, design tokens, and
   accessibility requirements. Ask which screens, brand constraints, and
   devices matter.
2. Propose the canvas scope and output location before editing. Reuse the
   existing toolchain; do not add a framework or dependency only for the
   canvas.
3. Build representative components and states, not a disconnected mood board.
   Include controls for relevant choices such as color, typography, spacing,
   radius, density, elevation, and component variants.
4. Keep changes in the browser preview and expose the selected values as
   readable design tokens. Avoid sending source code or content to external
   services.
5. Provide keyboard-operable controls, visible focus, useful labels, sufficient
   contrast, responsive layouts, and reduced-motion behavior.
6. Run the repository's existing checks and launch the canvas using an existing
   local development or preview command. Give the user the local URL and short
   interaction instructions.
7. Ask the user to compare options and record their choices. Iterate in small
   steps.
8. Before applying the chosen direction to production code, summarize the
   selected tokens and components and obtain explicit approval.

Keep the canvas isolated and easy to remove unless the user asks to integrate
it. Do not overwrite an existing application or claim that an aesthetic choice
has been approved without user confirmation.
