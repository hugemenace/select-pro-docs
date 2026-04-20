# Introduction

## Unified Selection Menu

Select Pro unifies all of Blender's built-in selection methods and a suite of custom operators into a single predictive menu, accessible in Object Mode, Edit Mesh, Edit Curve, Edit Armature, and Pose Mode.

Press **`A`** in any supported mode to open the menu. Select Pro can also be added to Blender's right-click context menu via [Preferences](/getting-started/preferences).

## Smart Predictions

When the menu opens, Select Pro analyses the current context — the active object or element, the current selection, and the surrounding geometry — and surfaces the most relevant selection operators at the top of the menu. Predictions update automatically as your selection changes, so the right tools are always front and centre.

Predictions can be enabled, disabled, and tuned in [Preferences](/getting-started/preferences).

## Custom Operators

Select Pro adds a set of advanced selection operators not available in Blender by default. These are fully integrated into the menu and work alongside built-in tools.

**Object Mode**
- [Select Hierarchy](/operators/object/select-hierarchy) — select related objects by traversing the parent-child hierarchy
- [Select Similar Name](/operators/object/select-similar-name) — select objects with similar names using affix stripping and fuzzy matching
- [Select Similar Size](/operators/object/select-similar-size) — select objects with similar dimensions or volume

**Edit Mesh Mode**
- [Select Connected Similar Edges](/operators/mesh/select-connected-similar-edges) — flood-fill select edges sharing the same mark type
- [Select Contiguous Edge Path](/operators/mesh/select-contiguous-edge-path) — select an edge path by visual continuity
- [Select Edge Boundary](/operators/mesh/select-edge-boundary) — select connected boundary edges of the same type
- [Select Face Surface](/operators/mesh/select-face-surface) — flood-fill select a face surface bounded by edge marks or face attributes
- [Select Grow / Shrink](/operators/mesh/select-grow-shrink) — interactively grow or shrink the current selection
- [Select Similar Face Direction](/operators/mesh/select-similar-face-direction) — select faces pointing in a similar direction
- [Select Similar Face Islands](/operators/mesh/select-similar-face-islands) — select mesh islands with similar structure and volume
- [Select Vertices by Proximity](/operators/mesh/select-vertices-by-proximity) — interactively select vertices within a radius

## Double-Click Operators

Select Pro can run a configurable operator whenever you double-click an element in the viewport. The default operator varies by mode and element type — for example, double-clicking an edge in Edit Mesh Mode runs Select Contiguous Edge Path by default.

Double-click operators can be enabled, disabled, and reconfigured per mode in [Preferences](/getting-started/preferences).

## Modal Operators

Some Select Pro operators are interactive — they respond to mouse movement in real time rather than executing immediately. Move the mouse to adjust the result, then confirm or cancel. See the individual operator pages for their available interactive controls.

## Operator Settings

Select Pro operators executed via the **double-click** binding remember their settings between uses. Properties are saved when you confirm an operation and restored the next time the operator runs — so once you've dialled in settings like direction, tolerance, or size method, they'll stick for the session. Operators executed from the predictive menu do not use this behaviour. This can be disabled in [Preferences](/getting-started/preferences).

All operators also support Blender's **Adjust Last Operation** panel (accessible via **`F9`** or the bottom-left corner of the viewport after execution), letting you tweak properties after the fact.

## Quick Actions Menu

The **Options...** entry at the bottom of the Select Pro menu opens a Quick Actions menu with two utilities:

- **Reset Double-Click Defaults** — restores all double-click operator properties to their default values
- **Reset Prediction Cache** — clears the cached predictions, forcing a fresh analysis on next menu open
