# Select Along Axis

Select all connected lattice points along the chosen axes, starting from the current selection. Each selected point is used as a seed, and points sharing its row along the enabled axes are added to the selection.

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| X | N/A | `False` | Extend the selection along the lattice U (X) axis |
| Y | N/A | `False` | Extend the selection along the lattice V (Y) axis |
| Z | N/A | `True` | Extend the selection along the lattice W (Z) axis |
| Direction | N/A | `Both` | Which way to extend the selection along the enabled axes (see below) |

### Direction Options

| Option | Description |
| :--- | :--- |
| Positive | Select points in the positive axis direction only |
| Negative | Select points in the negative axis direction only |
| Both | Select points in both axis directions |
