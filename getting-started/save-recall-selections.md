# Save & Recall Selections

Save named snapshots of the current selection and restore them at any time. Saved selections are stored in the project file and work in Object Mode, Edit Mesh, Edit Armature, Edit Curve, and Pose Mode — they persist across sessions and will still be available after closing and reopening the file.

Access the feature via **Manage Selections** in the main Select Pro menu. It can be disabled in [Preferences](/getting-started/preferences).

## Saving a Selection

Select the elements you want to save, then open the menu and choose **Manage Selections → Save Current Selection**. A dialog appears with a pre-filled name based on the current selection (e.g. *Selection (3 Faces)*). Edit the name or confirm as-is.

## Recalling a Selection

Saved selections appear as entries under **Manage Selections**. Click any entry to restore it, replacing the current selection.

Hold **Shift** when clicking to add the saved selection to the current selection instead of replacing it.

After recalling, the **Adjust Last Operation** panel (**`F9`**) exposes a **Boolean** property with full control over how the saved and current selections are combined:

| Option | Description |
| :--- | :--- |
| **None** | Replace the current selection with the saved one |
| **Union** | Add the saved selection to the current selection |
| **Difference** | Remove saved elements from the current selection |
| **Difference (Reverse)** | Keep only saved elements not in the current selection |
| **Intersection** | Keep only elements present in both selections |

## Clearing Saved Selections

**Manage Selections → Clear Saved Selections** removes all saved selections for the current mode and element type. A confirmation prompt appears before anything is deleted.
