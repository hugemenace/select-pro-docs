# Shortcuts

## Main Menu

| Shortcut | Description | Customisable |
| :--- | :--- | :--- |
| **`A`** | Open the Select Pro menu | **Yes** |

The main menu is available in Object Mode, Edit Mesh, Edit Curve, Edit Armature, and Pose Mode. The shortcut can be changed in **Preferences → Keymap**.

## Double-Click Operators

When double-clicking an element in the viewport, Select Pro can automatically run a configurable operator based on the current mode and element type.

| Mode | Element | Default Operator |
| :--- | :--- | :--- |
| Object | Object | Select Similar Size (Volume) |
| Edit Mesh | Vertex | Select Vertices by Proximity |
| Edit Mesh | Edge | Select Contiguous Edge Path |
| Edit Mesh | Face | Select Face Surface (Predictive) |
| Edit Curve | Point | Select Linked (Spline) |
| Edit Armature | Bone | Select Linked (Chain) |
| Pose | Bone | Select Linked (Chain) |

Double-click operators can be enabled, disabled, and reconfigured per mode in **Preferences → Keymap**.

## Modal Operators

Some operators are interactive and controlled by mouse movement. Each modal operator has its own set of interactive controls documented on its operator page.

| Key | Description |
| :--- | :--- |
| **`LMB`** / **`Enter`** | Confirm and apply the current operation |
| **`RMB`** / **`Esc`** | Cancel and restore the original selection |
