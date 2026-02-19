
# Stored Payment Method 2

## Structure

`StoredPaymentMethod2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `bank_account_number` | `String` | Optional | The bank account number (without separators). |
| `bank_location_id` | `String` | Optional | The location id of the bank. The field value is `nil` in most cases. |
| `brand` | `String` | Optional | The brand of the card. |
| `expiry_month` | `String` | Optional | The two-digit month when the card expires |
| `expiry_year` | `String` | Optional | The last two digits of the year the card expires. For example, **22** for the year 2022. |
| `holder_name` | `String` | Optional | The unique payment method code. |
| `iban` | `String` | Optional | The IBAN of the bank account. |
| `id` | `String` | Optional | A unique identifier of this stored payment method. |
| `label` | `String` | Optional | The shopper’s issuer account label |
| `last_four` | `String` | Optional | The last four digits of the PAN. |
| `name` | `String` | Optional | The display name of the stored payment method. |
| `network_tx_reference` | `String` | Optional | Returned in the response if you are not tokenizing with Adyen and are using the Merchant-initiated transactions (MIT) framework from Mastercard or Visa.<br><br>This contains either the Mastercard Trace ID or the Visa Transaction ID. |
| `owner_name` | `String` | Optional | The name of the bank account holder. |
| `shopper_email` | `String` | Optional | The shopper’s email address. |
| `supported_recurring_processing_models` | `Array[String]` | Optional | The supported recurring processing models for this stored payment method. |
| `supported_shopper_interactions` | `Array[String]` | Optional | The supported shopper interactions for this stored payment method. |
| `type` | `String` | Optional | The type of payment method. |

## Example (as JSON)

```json
{
  "bankAccountNumber": "bankAccountNumber2",
  "bankLocationId": "bankLocationId4",
  "brand": "brand6",
  "expiryMonth": "expiryMonth6",
  "expiryYear": "expiryYear4"
}
```

