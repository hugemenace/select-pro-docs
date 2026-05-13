# Smart Edge Select

Automatically dispatch to the most appropriate edge selection operator based on the active edge's context. The operator inspects the active edge and runs:

- **Select Similar Connected Edges** — if the active edge has any marks (seam, sharp, crease, or bevel weight)
- **Select Edge Boundary** — if the active edge is naked (one linked face), or if its two adjacent faces meet at a sharp angle (≥ 30°)
- **Select Edge Loop** — if the active edge is on a quad-continuation (follows quads two steps in either direction)
- **Select Contiguous Edge Path** — otherwise

This operator is primarily used as a double-click option in Edit Mesh Mode via the Keymap preferences.
