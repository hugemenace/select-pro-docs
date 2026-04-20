# Custom Predictions — Examples

The examples below show common customisation scenarios. Each example is a complete, minimal JSON file that can be loaded directly via the config panel.

For the full list of available modes, op sets, and op IDs, use **Generate Custom Config** in the N-panel to produce a copy of the default prediction set — this is the best reference for IDs and structure.

---

## Boost an Existing Prediction's Score

Increase the score of the **Similar Volume** prediction in Object Mode so it appears higher in the list.

```json
{
  "__VERSION__": 1,
  "__NAME__": "Boost Similar Volume",
  "OBJECT": {
    "SP_SIMILAR_SIZE": {
      "VOLUME": {
        "score": 500
      }
    }
  }
}
```

Only the `score` field is needed — all other fields are inherited from the default entry.

---

## Change a Prediction's Label

Rename the **Similar Volume** prediction to something shorter.

```json
{
  "__VERSION__": 1,
  "__NAME__": "Rename Predictions",
  "OBJECT": {
    "SP_SIMILAR_SIZE": {
      "VOLUME": {
        "text": "Similar Volume",
        "prediction_text": "Same Volume"
      }
    }
  }
}
```

`text` controls the label in the full menu and should generally match the operator's name as Blender presents it. `prediction_text` is a free alias shown when the entry appears as a prediction — use it to give the operator a more descriptive or contextual label that reflects how it's been configured or what it predicts.

---

## Add a New Prediction

### Surface an Existing Operator as a Prediction

Some operators already exist in the default set but have no `match_tokens`, so they never appear as predictions. You can give them tokens to surface them in context.

The example below adds match tokens to the existing **Face Perimeter** entry so it appears as a prediction whenever a single face is selected in face mode.

```json
{
  "__VERSION__": 1,
  "__NAME__": "Surface Face Perimeter",
  "EDIT_MESH": {
    "SIMILAR": {
      "FACE_PERIMETER": {
        "match_tokens": [
          ["MESH::IS_FACE_MODE", "SELECTION::SINGLE"]
        ]
      }
    }
  }
}
```

Only `match_tokens` is needed — all other fields are inherited from the existing entry.

### Add a Completely New Operator

To surface an operator that has no entry in the default set at all — such as one from a custom add-on — add a new op set and entry with the required fields.

```json
{
  "__VERSION__": 1,
  "__NAME__": "My Custom Operator",
  "EDIT_MESH": {
    "MY_TOOLS": {
      "MY_CUSTOM_OP": {
        "operator": "mesh.my_custom_operator",
        "text": "My Custom Operator",
        "prediction_text": "Custom Select",
        "icon": "RESTRICT_SELECT_OFF",
        "score": 100,
        "params": {
          "my_param": ["my_value", "str"]
        },
        "match_tokens": [
          "MESH::IS_FACE_MODE"
        ],
        "invoke": false,
        "prediction_invoke": false
      }
    }
  }
}
```

`MY_TOOLS` and `MY_CUSTOM_OP` are arbitrary IDs — use names that are meaningful to you. They just need to be unique within the mode.

---

## Combine Multiple Changes in One File

Multiple modifications can live in a single file.

```json
{
  "__VERSION__": 1,
  "__NAME__": "My Workflow Tweaks",
  "OBJECT": {
    "SP_SIMILAR_SIZE": {
      "VOLUME": {
        "score": 500
      }
    },
    "SP_SIMILAR_NAME": {
      "DEFAULT": {
        "score": 300,
        "prediction_text": "Name Match"
      }
    }
  }
}
```
