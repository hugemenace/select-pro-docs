# Preferences

## General

### Menu Settings

| Setting | Description |
| :--- | :--- |
| **Enable global pinned items** | Show All, None, and Invert selection operators at the top of the menu |
| **Keep all mode specific selection tools in a submenu** | Collapse mode-specific Blender selection tools into a submenu instead of showing them inline |
| **Show options menu** | Show the Options entry at the bottom of the menu |
| **Enable right-click context menu integration** | Add Select Pro to Blender's right-click context menu in Object and Edit Mesh modes. Requires a reload to take effect |
| **Enable the sidebar / N-panel** | Show the Select Pro panel in the sidebar (N-panel). Requires a reload to take effect |

### Prediction Settings

| Setting | Description |
| :--- | :--- |
| **Enable context-aware predictions** | Show predicted selection operators in the menu based on the current context |
| **The maximum number of predictions to show** | Cap on how many predicted operators appear in the menu |
| **Enable automatic prediction skipping** | Automatically reduce prediction thresholds when predictions take too long, to keep menu response times fast |
| **Max prediction time (ms)** | If predictions exceed this duration, the threshold for the current mode is reduced automatically. Only applies when automatic skipping is enabled |
| **Show predictions skipped notice** | Show an info label in the menu when predictions have been skipped |
| **Force mode submenu expansion on predictions skip** | Expand the mode-specific selection submenu inline when predictions are skipped |
| **Max objects before skipping predictions** | Predictions are skipped in Object Mode when the view layer exceeds this object count |
| **Max polygons before skipping predictions** | Predictions are skipped in Edit Mesh Mode when the active mesh exceeds this polygon count |
| **Max curve points before skipping predictions** | Predictions are skipped in Edit Curve Mode when the total control point count exceeds this value |
| **Max bones before skipping predictions** | Predictions are skipped in Edit Armature and Pose Mode when the bone count exceeds this value |

### Modal Settings

| Setting | Description |
| :--- | :--- |
| **Modal Speed Control Key** | Modifier key that slows down modal operators when held (`Shift` or `Ctrl`) |
| **Complete on Mouse Release** | Finish modal operations when the left mouse button is released instead of when it is clicked |
| **Modal Operator Sensitivity** | Controls how fast modal operators respond to mouse movement. Higher values are more sensitive |
| **Modal Step Distance** | Mouse distance in pixels required to trigger one selection step in modal operators |

## Keymap

Contains the customisable keybinds for each supported mode. See [Shortcuts](/getting-started/shortcuts) for an overview.

### Double-Click Operators

| Setting | Description |
| :--- | :--- |
| **Enable Double-Click in Object Mode** | Enable double-click operator dispatch in Object Mode. Requires a reload to take effect |
| **Object** | Operator to run when double-clicking an object in Object Mode |
| **Enable Double-Click in Edit Mesh Mode** | Enable double-click operator dispatch in Edit Mesh Mode. Requires a reload to take effect |
| **Vertex** | Operator to run when double-clicking a vertex in Edit Mesh Mode |
| **Edge** | Operator to run when double-clicking an edge in Edit Mesh Mode |
| **Face** | Operator to run when double-clicking a face in Edit Mesh Mode |
| **Enable Double-Click in Edit Curve Mode** | Enable double-click operator dispatch in Edit Curve Mode. Requires a reload to take effect |
| **Curve** | Operator to run when double-clicking a control point in Edit Curve Mode |
| **Enable Double-Click in Edit Armature Mode** | Enable double-click operator dispatch in Edit Armature Mode. Requires a reload to take effect |
| **Armature** | Operator to run when double-clicking a bone in Edit Armature Mode |
| **Enable Double-Click in Pose Mode** | Enable double-click operator dispatch in Pose Mode. Requires a reload to take effect |
| **Pose** | Operator to run when double-clicking a bone in Pose Mode |
| **Remember Double-Click operator settings** | Save and restore operator properties between double-click invocations for the current session |
| **Use Right Mouse Double-Click Select** | Adjust double-click detection to work correctly when Blender's right-click select is enabled. Requires a reload to take effect |
