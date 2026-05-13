# Select Similar Element

Select mesh elements (vertices, edges, or faces) whose local geometry matches the shape of the active element. The comparison is topology- and geometry-based — the operator analyses the surrounding structure and spatial layout to find elements with a matching local form.

Works in Vertex, Edge, and Face select modes.

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Tolerance | N/A | `0.001` | Maximum allowed deviation when comparing elements. Higher values allow looser matches |
| Check Connected | N/A | `2` | How many topology steps outward to include in the shape comparison (`0` = shape only, `1` = immediate neighbours, `2+` = expanding rings) |
| Only Active Element | N/A | `True` | Use only the active element's component as the seed; when disabled, all selected components are used |

## Execution Modes

Hold down these keys when executing the operator to change its default behaviour.

| Key | Description |
| :--- | :--- |
| SHIFT | Sets **Only Active Element** to `False` |
