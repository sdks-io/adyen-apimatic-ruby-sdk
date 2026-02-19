
# Sepa Direct Debit

*This model accepts additional fields of type Object.*

## Structure

`SepaDirectDebit`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `due_date` | `String` | Optional | The date that the the shopper's bank account is charged. |
| `iban` | `String` | Required | The International Bank Account Number (IBAN). |
| `owner_name` | `String` | Required | The name of the bank account holder. |
| `recurring_detail_reference` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `stored_payment_method_id` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` |
| `transfer_instrument_id` | `String` | Optional | The unique identifier of your user's verified transfer instrument, which you can use to top up their balance accounts. |
| `type` | [`Type45`](../../doc/models/type-45.md) | Optional | **sepadirectdebit**<br><br>**Default**: `Type45::SEPADIRECTDEBIT` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "iban": "iban4",
  "ownerName": "ownerName4",
  "type": "sepadirectdebit",
  "checkoutAttemptId": "checkoutAttemptId6",
  "dueDate": "dueDate6",
  "recurringDetailReference": "recurringDetailReference0",
  "sdkData": "sdkData0",
  "storedPaymentMethodId": "storedPaymentMethodId4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

