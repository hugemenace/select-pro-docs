# Select Edge Boundary

Select connected boundary edges starting from the active edge. The edge type is detected automatically:

- **Wire edges** (no linked faces) — immediately selects all connected wire edges
- **Naked edges** (one linked face) — immediately selects all connected naked edges
- **Surface edges** (two linked faces) — enters an interactive preview mode where hovering the cursor to either side of the edge highlights that surface's boundary; press `A` to select all connected boundaries regardless of surface side

![Select Edge Boundary](../../_media/boundary-edges.avif ':class=avif')

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| All Boundaries | `A` | `False` | Select all connected boundary edges rather than just the surface boundary under the cursor. Only applies to surface edges |

## Interactive Controls

These keys can be pressed while the operator is running to change its behaviour. Only applies when the active edge is a surface edge.

| Key | Description |
| :--- | :--- |
| `A` | Toggle **All Boundaries** |
| `LMB` / `Enter` | Confirm and apply the selection |
| `RMB` / `Esc` | Cancel and restore the original selection |
