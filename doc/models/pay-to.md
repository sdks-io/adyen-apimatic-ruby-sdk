
# Pay To

## Structure

`PayTo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `recurring_detail_reference` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `shopper_account_identifier` | `String` | Optional | The shopper's banking details or payId reference, used to complete payment. |
| `stored_payment_method_id` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` |
| `type` | [`Type36`](../../doc/models/type-36.md) | Optional | **payto**<br><br>**Default**: `Type36::PAYTO` |

## Example (as JSON)

```json
{
  "type": "payto",
  "checkoutAttemptId": "checkoutAttemptId2",
  "recurringDetailReference": "recurringDetailReference6",
  "sdkData": "sdkData4",
  "shopperAccountIdentifier": "shopperAccountIdentifier6",
  "storedPaymentMethodId": "storedPaymentMethodId0"
}
```

