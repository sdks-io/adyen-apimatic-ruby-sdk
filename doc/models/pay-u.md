
# Pay U

## Structure

`PayU`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `recurring_detail_reference` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `shopper_notification_reference` | `String` | Optional | The `shopperNotificationReference` returned in the response when you requested to notify the shopper. Used for recurring payment only. |
| `stored_payment_method_id` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` |
| `type` | `String` | Required, Constant | **payu_IN_upi**<br><br>**Value**: `'payu_IN_upi'` |
| `virtual_payment_address` | `String` | Optional | The virtual payment address for UPI. |

## Example (as JSON)

```json
{
  "type": "payu_IN_upi",
  "checkoutAttemptId": "checkoutAttemptId8",
  "recurringDetailReference": "recurringDetailReference2",
  "sdkData": "sdkData8",
  "shopperNotificationReference": "shopperNotificationReference2",
  "storedPaymentMethodId": "storedPaymentMethodId6"
}
```

