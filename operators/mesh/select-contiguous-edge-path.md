# Select Contiguous Edge Path

Select a contiguous edge path from the active edge by following the most visually straight route through the mesh. The path is determined by direction continuity, face angles, and edge length — automatically navigating bends and corners while stopping where the geometry becomes ambiguous.

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Boundary Angle | N/A | `180°` | Maximum face angle the path is allowed to traverse. Paths will stop at edges whose face angle exceeds this value |
| Ignore Marks | N/A | `True` | Allow the path to cross edges that have marks (seams, sharps, etc.) without stopping |

## Execution Modes

Hold down these keys when executing the operator to change its default behaviour.

| Key | Description |
| :--- | :--- |
| SHIFT | Use all selected edges as starting points instead of just the active edge |
