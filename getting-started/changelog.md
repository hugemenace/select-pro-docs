# Changelog

## 0.5.2 — 2026-04-07

### Features

- Add additional scene tokens for object dimensions, volumes, and materials, and update object predictions accordingly
- Add an option to remember double-click operator settings for the current session (enabled by default)
- Add an option to remove Select Pro's customisation panel from Blender's sidebar (N-Panel)
- Add an options menu to quickly reset double-click operator defaults or reset the predictions cache
- Add interactive grow/shrink selection operator and associated prediction
- Add option to switch modal speed control key from SHIFT to CTRL and also to complete on mouse release instead of press
- Add selection ALL/SUBSET tokens and improve associated predictions
- Add select grow/shrink to the double-click operator options

### Bug Fixes

- Ensure the keymaps in the Select Pro preferences window retain their modifications on reload
- Fix error in contiguous path when traversing non-manifold edges (3+ faces)

## 0.4.5 — 2026-03-30

### Features

- Add native module integration for increased prediction, menu, and operator performance

### Bug Fixes

- Ensure the BMesh selection cache is flushed on cancelling the select vertices by proximity modal operator
- Ensure the predict menu doesn't open in mixed-mode contexts (e.g., bone selection active while in weight paint mode)

## 0.4.4 — 2026-03-21

### Features

- Add custom predictions support and associated configuration panel (available via the 3D viewport sidebar / N panel)
- Add double-click bounded edge path, face surface (predictive/bounded), and linked island options
- Add exact face island selection to similar islands operator and associated prediction
- Add linked island option to the select linked sub menu
- Add option to enable/disable double-click selection in object and edit mesh mode
- Add option to enable/disable global pinned items (all, none, invert)
- Add option to expand/collapse the mode specific sub-menus
- Add prediction and double-click support for Edit Armature Mode
- Add prediction and double-click support for Edit Curve Mode
- Add prediction and double-click support for Pose Mode
- Add restore keybinds button to preferences
- Add select similar face direction operator and associated prediction
- Allow for easy keybind updates from Select Pro's preferences
- Ensure that the adjust last operation panel appears for all SP operators executed via the double-click binding
- Rewrite the core contiguous path algorithm for more robust path selection across tris, quads, and ngons
- Simplify face surface prediction and double-click behaviour

### Bug Fixes

- Add the force_only_active property to all SP operators to solve double-click vs prediction selection issues
- Ensure all operators flush the mode-specific bmesh selection after completion
- Ensure that the double-click "Do Nothing" option passes through the event for other keybinds to handle

## 0.3.0 — 2026-03-03

### Features

- Add double-click keybinding and associated context-aware operator dispatch (configurable in preferences)
- Add edge strip (partial ring loop) prediction
- Add edge strip to the edit mesh select loops sub menu
- Add mirror prediction for faces (previously only vertices and edges)
- Add multi-select support to the Select Vertices by Proximity operator
- Add prediction for faces with similar surface area
- Add prediction for select more across vertices, edges, and faces
- Add select similar objects by name operator and associated prediction
- Add select similar sub-menu for volume, dimensions, and name operators
- Add SHIFT-key selection extension to Hierarchy, Similar Name, and Similar Size operators
- Add UV island prediction for selected faces in edit mode

### Bug Fixes

- Ensure all, none, and invert options are prefixed for non-English locales to support existing tap-patterns

## 0.2.0 — 2026-02-17

### Features

- Add multi-path selection support to the Contiguous Edge Path operator
- Add multi-path selection support to the Select Connected Similar Edges operator
- Add multi-path selection support to the Select Edge Boundary operator
- Add multi-surface selection support to the Select Face Surface operator
- Add object mode Select Similar Size (by volume or dimensions) operator and associated predictions
- Add option to append Select Pro to Blender's object and edit mode context menus (via preferences)
- Add prediction for objects with shared data blocks
- Add Select Vertices by Proximity operator and associated predictions
- Add support for Blender 5.1's new Edge Loop and Ring operators
- Adjust base operator weights for cameras, types, and surfaces
- Improve object hierarchy family selector predictions
- Improve prediction sorting (score > operator > label)

### Bug Fixes

- Ensure that active object material mutation invalidates the object context cache
- Ensure that objects excluded from the view layer are ignored during prediction
- Ensure that selected edges with marks can invalidate the edit mesh context cache
- Ensure that the "Only Loops" option for Select Similar Connected and Boundary edges works reliably and is turned off by default
- Fix the broken Only Active Object option on the Select Hierarchy operator
