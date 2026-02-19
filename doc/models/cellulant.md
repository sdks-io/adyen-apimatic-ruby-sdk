
# Cellulant

## Structure

`Cellulant`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `issuer` | `String` | Optional | The Cellulant issuer. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `type` | [`Type15`](../../doc/models/type-15.md) | Optional | **Cellulant**<br><br>**Default**: `Type15::CELLULANT` |

## Example (as JSON)

```json
{
  "type": "cellulant",
  "checkoutAttemptId": "checkoutAttemptId0",
  "issuer": "issuer4",
  "sdkData": "sdkData6"
}
```

