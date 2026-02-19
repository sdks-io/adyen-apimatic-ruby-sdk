
# Android Pay

## Structure

`AndroidPay`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `type` | [`Type5`](../../doc/models/type-5.md) | Optional | **androidpay**<br><br>**Default**: `Type5::ANDROIDPAY` |

## Example (as JSON)

```json
{
  "type": "androidpay",
  "checkoutAttemptId": "checkoutAttemptId2",
  "sdkData": "sdkData4"
}
```

