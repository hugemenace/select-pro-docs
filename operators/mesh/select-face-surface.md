# Select Face Surface

Flood-fill select a face surface starting from the active face. By default, the surface is bounded by marked edges (seams, sharps, creases, or bevel weights). Alternatively, enable **Use Prediction** to ignore edge marks and instead determine surface boundaries from face attribute similarity — normal direction, area, perimeter, and corner angles.

![Contiguous Edge Path](../../_media/face-surface.avif ':class=avif')

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Boundary Type | N/A | `Any` | The edge mark type to stop at when flood-filling. Has no effect when **Use Prediction** is enabled (see below) |
| Use Prediction | N/A | `False` | Ignore edge marks and use face attribute similarity to determine the extent of the surface |
| Normal Angle Threshold | N/A | `20°` | Maximum angle difference between face normals. Only applies in **Prediction** mode |
| Area Range | N/A | `10×` | Maximum area multiplier between faces (`1.0` = identical, `2.0` = up to 2× bigger or smaller). Only applies in **Prediction** mode |
| Perimeter Range | N/A | `10×` | Maximum perimeter multiplier between faces. Only applies in **Prediction** mode |
| Corner Angle Threshold | N/A | `65°` | Maximum difference in average internal corner angles between faces. Only applies in **Prediction** mode |
| Fill Gaps | N/A | `True` | After the predictive flood fill, select any unselected faces surrounded on 2+ sides by selected faces that are within the normal angle threshold. Only applies in **Prediction** mode |

### Boundary Type Options

| Option | Description |
| :--- | :--- |
| Any | Stop at any marked edge |
| Crease | Stop at edges marked as creases |
| Bevel | Stop at edges with bevel weight |
| Seam | Stop at edges marked as seams |
| Sharp | Stop at edges marked as sharp |

## Execution Modes

Hold down these keys when executing the operator to change its default behaviour.

| Key | Description |
| :--- | :--- |
| SHIFT | Use all selected faces as starting points instead of just the active face |
