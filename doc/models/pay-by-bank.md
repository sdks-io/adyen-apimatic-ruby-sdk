
# Pay by Bank

## Structure

`PayByBank`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `issuer` | `String` | Optional | The PayByBank issuer value of the shopper's selected bank. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `type` | `String` | Required, Constant | **paybybank**<br><br>**Value**: `'paybybank'` |

## Example (as JSON)

```json
{
  "type": "paybybank",
  "checkoutAttemptId": "checkoutAttemptId2",
  "issuer": "issuer6",
  "sdkData": "sdkData4"
}
```

