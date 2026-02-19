
# Validate Shopper Id Response

*This model accepts additional fields of type Object.*

## Structure

`ValidateShopperIdResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reason` | `String` | Optional | Reason for the result. |
| `result` | [`Result1`](../../doc/models/result-1.md) | Optional | Result of the validation. Ex: valid, invalid, unknown |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "reason": "reason8",
  "result": "INVALID",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

