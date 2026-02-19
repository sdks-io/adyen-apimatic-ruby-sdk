
# Klarna

## Structure

`Klarna`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `billing_address` | `String` | Optional | The address where to send the invoice. |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `delivery_address` | `String` | Optional | The address where the goods should be delivered. |
| `personal_details` | `String` | Optional | Shopper name, date of birth, phone number, and email address. |
| `recurring_detail_reference` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `stored_payment_method_id` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` |
| `subtype` | `String` | Optional | The type of flow to initiate. |
| `type` | [`Type29`](../../doc/models/type-29.md) | Required | **klarna**<br><br>**Default**: `Type29::KLARNA` |

## Example (as JSON)

```json
{
  "type": "klarna",
  "billingAddress": "billingAddress8",
  "checkoutAttemptId": "checkoutAttemptId6",
  "deliveryAddress": "deliveryAddress6",
  "personalDetails": "personalDetails8",
  "recurringDetailReference": "recurringDetailReference0"
}
```

