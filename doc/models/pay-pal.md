
# Pay Pal

## Structure

`PayPal`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `order_id` | `String` | Optional | The unique ID associated with the order. |
| `payee_preferred` | `String` | Optional | IMMEDIATE_PAYMENT_REQUIRED or UNRESTRICTED |
| `payer_id` | `String` | Optional | The unique ID associated with the payer. |
| `payer_selected` | `String` | Optional | PAYPAL or PAYPAL_CREDIT |
| `recurring_detail_reference` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `stored_payment_method_id` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` |
| `subtype` | [`Subtype`](../../doc/models/subtype.md) | Optional | The type of flow to initiate. |
| `type` | `String` | Required, Constant | **paypal**<br><br>**Value**: `'paypal'` |

## Example (as JSON)

```json
{
  "type": "paypal",
  "checkoutAttemptId": "checkoutAttemptId2",
  "orderID": "orderID0",
  "payeePreferred": "payeePreferred6",
  "payerID": "payerID2",
  "payerSelected": "payerSelected2"
}
```

