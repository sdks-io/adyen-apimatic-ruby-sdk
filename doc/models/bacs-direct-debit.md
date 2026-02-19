
# Bacs Direct Debit

## Structure

`BacsDirectDebit`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `bank_account_number` | `String` | Optional | The bank account number (without separators). |
| `bank_location_id` | `String` | Optional | The bank routing number of the account. |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `holder_name` | `String` | Optional | The name of the bank account holder. |
| `recurring_detail_reference` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `stored_payment_method_id` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` |
| `transfer_instrument_id` | `String` | Optional | The unique identifier of your user's verified transfer instrument, which you can use to top up their balance accounts. |
| `type` | [`Type8`](../../doc/models/type-8.md) | Optional | **directdebit_GB**<br><br>**Default**: `Type8::DIRECTDEBIT_GB` |

## Example (as JSON)

```json
{
  "type": "directdebit_GB",
  "bankAccountNumber": "bankAccountNumber8",
  "bankLocationId": "bankLocationId2",
  "checkoutAttemptId": "checkoutAttemptId4",
  "holderName": "holderName4",
  "recurringDetailReference": "recurringDetailReference8"
}
```

