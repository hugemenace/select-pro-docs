# Select Vertices by Proximity

Interactively select vertices within a radius of the active vertex. Move the mouse away from the starting point to increase the radius and toward it to decrease it. Can optionally restrict selection to vertices that are topologically connected to the origin.

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Only Connected | `C` | `False` | Select only vertices within the radius that are reachable via connected edges from the origin vertex |

## Execution Modes

Hold down these keys when executing the operator to change its default behaviour.

| Key | Description |
| :--- | :--- |
| SHIFT | Use all selected vertices as starting points instead of just the active vertex |

## Interactive Controls

These keys can be pressed while the operator is running to change its behaviour.

| Key | Description |
| :--- | :--- |
| `C` | Toggle **Only Connected** |
| `LMB` / `Enter` | Confirm and apply the selection |
| `RMB` / `Esc` | Cancel and restore the original selection |
