# Select Edge Boundary

Flood-fill select connected boundary edges of the same type — naked (open border), convex, or concave — starting from the active edge. The boundary type is detected automatically from the active edge. An angle tolerance allows variation along the boundary to accommodate slightly uneven geometry.

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Angle Tolerance | N/A | `60°` | Maximum angle deviation allowed along the boundary. Higher values allow less uniform edges to be included |
| Only Loops | N/A | `False` | Ignore edges that are not part of a closed loop |

## Execution Modes

Hold down these keys when executing the operator to change its default behaviour.

| Key | Description |
| :--- | :--- |
| SHIFT | Use all selected edges as starting points instead of just the active edge |
| ALT | Only select edges which are part of a closed loop |
