# Select Similar Name

Select objects with names similar to the active object (or all selected objects). Names are compared after optionally stripping common affixes (e.g. `.001`, `_high`/`_low`, `L.`/`R.`), and similarity is measured using Levenshtein distance — allowing fuzzy matching beyond exact name equality.

![Contiguous Edge Path](../../_media/similar-name.avif ':class=avif')

## Properties

| Property | Shortcut | Default | Description |
| :--- | :--- | :--- | :--- |
| Ignore Common Affixes | N/A | `True` | Strip common naming conventions (`.001`, `_high`/`_low`, `L.`/`R.`, etc.) before comparing names |
| Similarity Score | N/A | `0` | Maximum Levenshtein distance allowed for a name to be considered a match. `0` requires an exact match after affix stripping |

## Execution Modes

Hold down these keys when executing the operator to change its default behaviour.

| Key | Description |
| :--- | :--- |
| SHIFT | Use all selected objects instead of just the active object |
