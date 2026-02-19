
# Affirm

## Structure

`Affirm`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `type` | [`Type1`](../../doc/models/type-1.md) | Optional | **affirm**<br><br>**Default**: `Type1::AFFIRM` |

## Example (as JSON)

```json
{
  "type": "affirm",
  "checkoutAttemptId": "checkoutAttemptId6",
  "sdkData": "sdkData0"
}
```

