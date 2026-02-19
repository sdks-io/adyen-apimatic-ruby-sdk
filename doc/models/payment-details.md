
# Payment Details

## Structure

`PaymentDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `type` | [`Type38`](../../doc/models/type-38.md) | Optional | The payment method type. |

## Example (as JSON)

```json
{
  "checkoutAttemptId": "checkoutAttemptId2",
  "sdkData": "sdkData4",
  "type": "molpay_boost"
}
```

