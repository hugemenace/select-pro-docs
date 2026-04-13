# Select Similar Face Islands

Select mesh islands with similar properties to the island containing the active face. Similarity is measured using bounding box volume and structural complexity (a combined measure of vertex, edge, and face counts). Filters are applied in order of specificity so the most distinctive metric narrows the candidates first.

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Volume Similarity | N/A | `0%` | How strictly bounding box volumes must match. Higher values require a closer volume match |
| Maximum Volume Factor | N/A | `10` | Upper bound on how much larger or smaller a candidate island's volume can be relative to the reference. `0` disables this limit |
| VEF Similarity | N/A | `100%` | How strictly the structural complexity (vertex × edge × face count) must match. Higher values require a closer structural match |
| Only Exact Islands | N/A | `False` | Skip similarity checks and select only the exact island(s) associated with the active face |

## Execution Modes

Hold down these keys when executing the operator to change its default behaviour.

| Key | Description |
| :--- | :--- |
| SHIFT | Use all selected faces as island candidates instead of just the active face |
