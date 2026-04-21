# Select Similar Faces by Direction

Interactively select faces whose normals point in a similar direction to the active face. Move the mouse away from the starting point to increase the angle tolerance and toward it to decrease it. Mirroring options allow the selection to include faces pointing in the opposite direction along one or more axes.

![Contiguous Edge Path](../../_media/similar-face-direction.avif ':class=avif')

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Angle Tolerance | N/A | `5°` | Maximum angle deviation from the reference normal for a face to be selected |
| Mirror X | `X` | `False` | Also select faces with normals flipped across the object X axis |
| Mirror Y | `Y` | `False` | Also select faces with normals flipped across the object Y axis |
| Mirror Z | `Z` | `False` | Also select faces with normals flipped across the object Z axis |
| Connected Only | `C` | `False` | Only select faces connected to the active face(s) that match the criteria |

## Execution Modes

Hold down these keys when executing the operator to change its default behaviour.

| Key | Description |
| :--- | :--- |
| SHIFT | Use all selected faces as references instead of just the active face |
| ALT | Enable mirrored selection across all object axes (X, Y, and Z) |

## Interactive Controls

These keys can be pressed while the operator is running to change its behaviour.

| Key | Description |
| :--- | :--- |
| `X` | Toggle **Mirror X** |
| `Y` | Toggle **Mirror Y** |
| `Z` | Toggle **Mirror Z** |
| `C` | Toggle **Connected Only** |
| `LMB` / `Enter` | Confirm and apply the selection |
| `RMB` / `Esc` | Cancel and restore the original selection |
