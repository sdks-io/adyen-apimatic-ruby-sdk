
# Checkout Bank Transfer Action

## Structure

`CheckoutBankTransferAction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_number` | `String` | Optional | The account number of the bank transfer. |
| `bank_code` | `String` | Optional | The bank code of the bank transfer. |
| `beneficiary` | `String` | Optional | The name of the account holder. |
| `bic` | `String` | Optional | The BIC of the IBAN. |
| `branch_code` | `String` | Optional | The branch code of the bank transfer. |
| `download_url` | `String` | Optional | The url to download payment details with. |
| `iban` | `String` | Optional | The IBAN of the bank transfer. |
| `payment_method_type` | `String` | Optional | Specifies the payment method. |
| `reference` | `String` | Optional | The transfer reference. |
| `routing_number` | `String` | Optional | The routing number of the bank transfer. |
| `shopper_email` | `String` | Optional | The e-mail of the shopper, included if an e-mail was sent to the shopper. |
| `sort_code` | `String` | Optional | The sort code of the bank transfer. |
| `total_amount` | [`Amount10`](../../doc/models/amount-10.md) | Optional | The amount of the bank transfer. |
| `type` | `String` | Required, Constant | The type of the action.<br><br>**Value**: `'bankTransfer'` |
| `url` | `String` | Optional | Specifies the URL to redirect to. |

## Example (as JSON)

```json
{
  "type": "bankTransfer",
  "accountNumber": "accountNumber4",
  "bankCode": "bankCode8",
  "beneficiary": "beneficiary6",
  "bic": "bic0",
  "branchCode": "branchCode0"
}
```

