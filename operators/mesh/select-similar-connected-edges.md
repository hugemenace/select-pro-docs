# Select Similar Connected Edges

Flood-fill selects all edges connected to the active edge that share the same mark type — crease, bevel weight, seam, or sharp. The property to match can be detected automatically from the active edge, or set manually. Optionally restrict the result to edges that form closed loops.

![Select Similar Connected Edges](../../_media/similar-edges.avif ':class=avif')

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Auto Detect Property | N/A | `True` | Automatically detect which property to match from the active edge. Detection order: Seam → Sharp → Crease → Bevel |
| Property | N/A | `Crease` | Edge property to match when **Auto Detect Property** is disabled (see below) |
| Only Loops | N/A | `False` | Ignore edges that are not part of a closed loop |
| Tolerance | N/A | `0.0001` | Maximum difference allowed when comparing float properties (Crease and Bevel). Has no effect on Seam or Sharp |
| Only Active Edge | N/A | `True` | Use only the active edge as the starting point; when disabled, all selected edges are used |

### Property Options

| Option | Description |
| :--- | :--- |
| Crease | Match edges with the same crease value |
| Bevel | Match edges with the same bevel weight |
| Seam | Match edges marked as a UV seam |
| Sharp | Match edges marked as sharp |

## Execution Modes

Hold down these keys when executing the operator to change its default behaviour.

| Key | Description |
| :--- | :--- |
| SHIFT | Sets **Only Active Edge** to `False` |
| ALT | Sets **Only Loops** to `True` |
