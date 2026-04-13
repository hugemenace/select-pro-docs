# Select Hierarchy

Select objects related to the active object (or all selected objects) by traversing the scene's parent-child hierarchy. Use the **Direction** property to control which part of the hierarchy is targeted — from immediate children or parents, to the entire connected family tree.

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Extend Selection | N/A | `True` | Extend the current selection instead of replacing it |
| Direction | N/A | `Children` | Which part of the hierarchy to select (see below) |

### Direction Options

| Option | Description |
| :--- | :--- |
| Children | Select the direct children of the target object(s) |
| Siblings | Select objects that share the same parent, excluding the target itself |
| Descendants | Select all objects in the subtree below the target, recursively |
| Parent | Select the immediate parent of the target object(s) |
| Ancestors | Select all objects up the chain from the target to the root |
| Root | Select the top-most object in the hierarchy |
| Family | Select every object connected to the target — parents, children, and all their descendants |

## Execution Modes

Hold down these keys when executing the operator to change its default behaviour.

| Key | Description |
| :--- | :--- |
| SHIFT | Use all selected objects instead of just the active object |
