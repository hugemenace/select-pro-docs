# Custom Predictions — Introduction

Select Pro's prediction system analyses the current context and surfaces the most relevant selection operators in the menu. By default, it uses a built-in set of predictions tuned for common workflows — but you can customise this behaviour by loading your own prediction config files.

Custom prediction files are JSON documents that can modify existing predictions (changing scores, labels, or parameters) or add entirely new ones pointing at any Blender operator.

## The Config Panel

The config panel is available in the **3D viewport sidebar** (press `N` to open it) under the **HugeMenace** tab. It manages the list of JSON config files that Select Pro loads when building the prediction set.

### Controls

| Control | Description |
| :--- | :--- |
| **+** | Add a JSON file to the list via the file browser |
| **−** | Remove the selected file from the list |
| **Edit (pencil)** | Replace the selected entry with a different file |
| **Move Up / Move Down** | Change the order files are applied. Files later in the list take precedence when modifying the same entry |
| **Generate Custom Config** | Create a full copy of the default prediction set as a JSON file in Blender's config folder, and add it to the list automatically. Use this as a starting point for edits |
| **Open Config Folder** | Open the folder where Blender stores config files in your file explorer |
| **Reload Predictions** | Reload all scripts to apply changes made to config files on disk |

## Getting Started

The easiest way to start is to click **Generate Custom Config**. This creates a file called `select_pro_custom_predictions.json` in Blender's config folder containing every default prediction. You can then edit it directly, reload, and see the results.

Alternatively, create a minimal JSON file by hand and add only the entries you want to change or add.

## JSON File Structure

A predictions config file is a JSON object with the following top-level structure:

```json
{
  "__VERSION__": 1,
  "__NAME__": "My Custom Predictions",
  "MODE": {
    "OP_SET": {
      "OP_ID": { ... }
    }
  }
}
```

| Key | Required | Description |
| :--- | :--- | :--- |
| `__VERSION__` | Yes | Must be `1`. Files with a mismatched version are skipped |
| `__NAME__` | No | Display name shown in the config panel list |
| Mode keys | No | One or more mode blocks containing operator sets to modify or add |

### Modes

The top-level mode keys correspond to Blender's edit modes:

| Key | Mode |
| :--- | :--- |
| `OBJECT` | Object Mode |
| `EDIT_MESH` | Edit Mesh Mode |
| `EDIT_CURVE` | Edit Curve Mode |
| `EDIT_ARMATURE` | Edit Armature Mode |
| `POSE` | Pose Mode |

### Operator Entry Fields

Each entry under `MODE → OP_SET → OP_ID` is an object with the following fields. When **modifying an existing entry**, only the fields you want to change are required. When **adding a new entry**, `operator`, `text`, and `score` are required.

| Field | Type | Required (new) | Description |
| :--- | :--- | :--- | :--- |
| `operator` | string | Yes | Blender operator ID (e.g. `"object.select_all"`) |
| `text` | string | Yes | Label shown in the menu |
| `score` | integer | Yes | Sort weight — higher scores appear first |
| `icon` | string | No | Blender icon identifier |
| `params` | object | No | Operator parameters (see below) |
| `prediction_text` | string | No | Label shown when the entry appears as a prediction. Defaults to `text` |
| `match_tokens` | array | No | Conditions that must be met for this entry to appear as a prediction (see below) |
| `invoke` | boolean | No | Whether to invoke (rather than execute) the operator from the menu |
| `prediction_invoke` | boolean | No | Whether to invoke the operator when shown as a prediction |

### Parameter Encoding

Each parameter value in `params` is encoded as a 2-element array `[value, "type"]`, where `type` is one of: `"str"`, `"int"`, `"float"`, `"bool"`, `"list"`, `"set"`, `"tuple"`.

```json
"params": {
  "action": ["SELECT", "str"],
  "extend": [true, "bool"]
}
```

### Match Tokens

`match_tokens` is an array where each element is either a **string** (a single token) or an **array of strings** (multiple tokens that must all be present). A prediction is shown if **any** element in the array matches.

```json
"match_tokens": [
  "SELECTION::SUBSET",
  ["SELECTION::NONE", "OBJECTS::HAS_MULTI_OBJECTS"]
]
```

The above would show the prediction if either:
- `SELECTION::SUBSET` is present, **or**
- Both `SELECTION::NONE` **and** `OBJECTS::HAS_MULTI_OBJECTS` are present

See the [Token Reference](/predictions/token-reference) for all available tokens.
