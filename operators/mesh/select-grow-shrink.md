# Select Grow / Shrink

Interactively grow or shrink the current vertex, edge, or face selection. Move the mouse away from the starting point to grow, and toward it to shrink. Works in all mesh edit sub-modes.

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Face Step | `F` | `True` | Grow and shrink through face connections instead of edge connections |
| Avoid Empty Selections | `A` | `True` | Prevent the selection from being shrunk to zero elements |

## Interactive Controls

These keys can be pressed while the operator is running to change its behaviour.

| Key | Description |
| :--- | :--- |
| `F` | Toggle **Face Step** |
| `A` | Toggle **Avoid Empty Selections** |
| `LMB` / `Enter` | Confirm and apply the selection |
| `RMB` / `Esc` | Cancel and restore the original selection |
