
# Invalid Field

*This model accepts additional fields of type Object.*

## Structure

`InvalidField`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | The field that has an invalid value. |
| `value` | `String` | Required | The invalid value. |
| `message` | `String` | Required | Description of the validation error. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "name": "name8",
  "value": "value0",
  "message": "message2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

