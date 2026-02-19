
# Riverty

*This model accepts additional fields of type Object.*

## Structure

`Riverty`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `billing_address` | `String` | Optional | The address where to send the invoice. |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `delivery_address` | `String` | Optional | The address where the goods should be delivered. |
| `device_fingerprint` | `String` | Optional | A string containing the shopper's device fingerprint. For more information, refer to [Device fingerprinting](https://docs.adyen.com/risk-management/device-fingerprinting).<br><br>**Constraints**: *Maximum Length*: `5000` |
| `iban` | `String` | Optional | The iban number of the customer<br><br>**Constraints**: *Maximum Length*: `34` |
| `personal_details` | `String` | Optional | Shopper name, date of birth, phone number, and email address. |
| `recurring_detail_reference` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `stored_payment_method_id` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` |
| `subtype` | `String` | Optional | The payment method subtype. |
| `type` | [`Type43`](../../doc/models/type-43.md) | Required | **riverty**<br><br>**Default**: `Type43::RIVERTY` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "riverty",
  "billingAddress": "billingAddress2",
  "checkoutAttemptId": "checkoutAttemptId0",
  "deliveryAddress": "deliveryAddress0",
  "deviceFingerprint": "deviceFingerprint0",
  "iban": "iban8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

