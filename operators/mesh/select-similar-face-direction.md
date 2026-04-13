# Select Similar Face Direction

Select faces whose normals point in a similar direction to the active face. An angle tolerance defines a cone around the reference normal — any face whose normal falls within that cone is selected. Mirroring options allow the selection to include faces pointing in the opposite direction along one or more axes.

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Angle Tolerance | N/A | `5°` | Maximum angle deviation from the reference normal for a face to be selected |
| Mirror X | ALT | `False` | Also select faces with normals flipped across the object X axis |
| Mirror Y | ALT | `False` | Also select faces with normals flipped across the object Y axis |
| Mirror Z | ALT | `False` | Also select faces with normals flipped across the object Z axis |

## Execution Modes

Hold down these keys when executing the operator to change its default behaviour.

| Key | Description |
| :--- | :--- |
| SHIFT | Use all selected faces as references instead of just the active face |
| ALT | Enable mirrored selection across all object axes (X, Y, and Z) |
