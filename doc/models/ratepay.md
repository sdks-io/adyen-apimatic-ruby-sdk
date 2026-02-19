
# Ratepay

*This model accepts additional fields of type Object.*

## Structure

`Ratepay`

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
| `type` | [`Type42`](../../doc/models/type-42.md) | Required | **ratepay**<br><br>**Default**: `Type42::RATEPAY` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "ratepay",
  "billingAddress": "billingAddress6",
  "checkoutAttemptId": "checkoutAttemptId4",
  "deliveryAddress": "deliveryAddress4",
  "personalDetails": "personalDetails6",
  "recurringDetailReference": "recurringDetailReference8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

