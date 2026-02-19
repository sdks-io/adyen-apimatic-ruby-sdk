
# Blik

## Structure

`Blik`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blik_code` | `String` | Optional | BLIK code consisting of 6 digits. |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `recurring_detail_reference` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `stored_payment_method_id` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` |
| `type` | [`Type11`](../../doc/models/type-11.md) | Optional | **blik** |

## Example (as JSON)

```json
{
  "blikCode": "blikCode4",
  "checkoutAttemptId": "checkoutAttemptId2",
  "recurringDetailReference": "recurringDetailReference6",
  "sdkData": "sdkData4",
  "storedPaymentMethodId": "storedPaymentMethodId0"
}
```

