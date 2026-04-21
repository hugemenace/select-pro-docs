# Select Similar Size

Select objects with sizes similar to the active object (or all selected objects). Size can be compared by overall volume or by individual axis dimensions, with a configurable tolerance to control how closely sizes must match.

![Contiguous Edge Path](../../_media/similar-size.avif ':class=avif')

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Size Method | N/A | `Volume` | How object sizes are compared (see below) |
| Compare X | N/A | `True` | Include the X axis when comparing dimensions. Only applies in **Dimensions** mode |
| Compare Y | N/A | `True` | Include the Y axis when comparing dimensions. Only applies in **Dimensions** mode |
| Compare Z | N/A | `True` | Include the Z axis when comparing dimensions. Only applies in **Dimensions** mode |
| Tolerance | N/A | `25%` | Maximum percentage difference allowed for a size to be considered a match. `0%` requires an exact match |
| Ignore Unapplied Scale | N/A | `False` | Divide dimensions by the object's scale before comparing, so unapplied scale is not factored in |

### Size Method Options

| Option | Description |
| :--- | :--- |
| Volume | Compare objects by their total bounding box volume (X × Y × Z) |
| Dimensions | Compare objects per-axis, using only the axes enabled by **Compare X/Y/Z** |

## Execution Modes

Hold down these keys when executing the operator to change its default behaviour.

| Key | Description |
| :--- | :--- |
| SHIFT | Use all selected objects instead of just the active object |
