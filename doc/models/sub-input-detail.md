
# Sub Input Detail

## Structure

`SubInputDetail`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `configuration` | `Hash[String, String]` | Optional | Configuration parameters for the required input. |
| `items` | [`Array[Item]`](../../doc/models/item.md) | Optional | In case of a select, the items to choose from. |
| `key` | `String` | Optional | The value to provide in the result. |
| `optional` | `TrueClass \| FalseClass` | Optional | True if this input is optional to provide. |
| `type` | `String` | Optional | The type of the required input. |
| `value` | `String` | Optional | The value can be pre-filled, if available. |

## Example (as JSON)

```json
{
  "configuration": {
    "key0": "configuration0",
    "key1": "configuration9"
  },
  "items": [
    {
      "id": "id8",
      "name": "name8"
    }
  ],
  "key": "key4",
  "optional": false,
  "type": "type6"
}
```

