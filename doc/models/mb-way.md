
# Mb Way

## Structure

`MbWay`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `shopper_email` | `String` | Required | - |
| `telephone_number` | `String` | Required | - |
| `type` | [`Type31`](../../doc/models/type-31.md) | Optional | **mbway**<br><br>**Default**: `Type31::MBWAY` |

## Example (as JSON)

```json
{
  "shopperEmail": "shopperEmail4",
  "telephoneNumber": "telephoneNumber4",
  "type": "mbway",
  "checkoutAttemptId": "checkoutAttemptId8",
  "sdkData": "sdkData8"
}
```

