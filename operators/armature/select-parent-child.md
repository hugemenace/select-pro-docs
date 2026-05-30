# Select Parent/Child

Walk up or down the bone hierarchy from the current selection. Move the mouse away from the starting point to walk toward children, and toward it to walk toward parents. Works in both Edit Armature and Pose mode.

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Steps | N/A | `0` | Number of steps to walk (positive walks to children, negative walks to parents) |
| Extend Selection | `E` | `False` | Select the full chain from the starting bone to the destination instead of only the destination |
| All Descendants | `A` | `False` | Follow all child branches instead of only the first (no effect when walking to parents) |
| Flip Direction | `F` | `False` | Flip the walk direction so positive steps walk to parents instead of children |

## Interactive Controls

These keys can be pressed while the operator is running to change its behaviour.

| Key | Description |
| :--- | :--- |
| `E` | Toggle **Extend Selection** |
| `A` | Toggle **All Descendants** |
| `F` | Toggle **Flip Direction** |
| `LMB` / `Enter` | Confirm and apply the selection |
| `RMB` / `Esc` | Cancel and restore the original selection |
