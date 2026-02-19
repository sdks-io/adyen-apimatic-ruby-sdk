
# Stored Payment Method

## Structure

`StoredPaymentMethod`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cashtag` | `String` | Optional | Cash App issued cashtag for recurring payment |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `customer_id` | `String` | Optional | Cash App issued customerId for recurring payment |
| `grant_id` | `String` | Optional | Cash App issued grantId for one time payment |
| `on_file_grant_id` | `String` | Optional | Cash App issued onFileGrantId for recurring payment |
| `recurring_detail_reference` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. |
| `request_id` | `String` | Optional | Cash App request id |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `stored_payment_method_id` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` |
| `subtype` | `String` | Optional | The payment method subtype. |
| `type` | [`Type14`](../../doc/models/type-14.md) | Optional | cashapp<br><br>**Default**: `Type14::CASHAPP` |

## Example (as JSON)

```json
{
  "type": "cashapp",
  "cashtag": "cashtag0",
  "checkoutAttemptId": "checkoutAttemptId8",
  "customerId": "customerId6",
  "grantId": "grantId0",
  "onFileGrantId": "onFileGrantId0"
}
```

