
# Eft Direct Debit

## Structure

`EftDirectDebit`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `bank_account_number` | `String` | Optional | The bank account number (without separators). |
| `bank_code` | `String` | Optional | The financial institution code. |
| `bank_location_id` | `String` | Optional | The bank routing number of the account. |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `owner_name` | `String` | Optional | The name of the bank account holder.<br>If you submit a name with non-Latin characters, we automatically replace some of them with corresponding Latin characters to meet the FATF recommendations. For example:<br><br>* χ12 is converted to ch12.<br>* üA is converted to euA.<br>* Peter Møller is converted to Peter Mller, because banks don't accept 'ø'.<br>  After replacement, the ownerName must have at least three alphanumeric characters (A-Z, a-z, 0-9), and at least one of them must be a valid Latin character (A-Z, a-z). For example:<br>* John17 - allowed.<br>* J17 - allowed.<br>* 171 - not allowed.<br>* John-7 - allowed.<br><br>> If provided details don't match the required format, the response returns the error message: 203 'Invalid bank account holder name'. |
| `recurring_detail_reference` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `stored_payment_method_id` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` |
| `type` | [`Type25`](../../doc/models/type-25.md) | Optional | **eft**<br><br>**Default**: `Type25::EFT_DIRECTDEBIT_CA` |

## Example (as JSON)

```json
{
  "type": "eft_directdebit_CA",
  "bankAccountNumber": "bankAccountNumber4",
  "bankCode": "bankCode4",
  "bankLocationId": "bankLocationId8",
  "checkoutAttemptId": "checkoutAttemptId0",
  "ownerName": "ownerName8"
}
```

