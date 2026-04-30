# Select Edge Boundary

Flood-fill select all connected boundary edges starting from the active edge. The edge type is detected automatically — wire edges (no faces) select all connected wire edges, naked edges (one face) select all connected naked edges, and surface edges (two faces) select all connected edges meeting the minimum face angle threshold.

![Contiguous Edge Path](../../_media/boundary-edges.avif ':class=avif')

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Minimum Angle | N/A | `30°` | Minimum face angle required for an edge to be included. Only applies to surface edges |
| Use Smart Surface | N/A | `False` | Limit selection to the boundary on the surface under the cursor, falling back to the surface most aligned with the viewport camera. Only applies to surface edges |
