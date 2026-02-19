
# Checkout Voucher Action

## Structure

`CheckoutVoucherAction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alternative_reference` | `String` | Optional | The voucher alternative reference code. |
| `collection_institution_number` | `String` | Optional | A collection institution number (store number) for Econtext Pay-Easy ATM. |
| `download_url` | `String` | Optional | The URL to download the voucher. |
| `entity` | `String` | Optional | An entity number of Multibanco. |
| `expires_at` | `String` | Optional | The date time of the voucher expiry. |
| `initial_amount` | [`Amount13`](../../doc/models/amount-13.md) | Optional | The initial amount. |
| `instructions_url` | `String` | Optional | The URL to the detailed instructions to make payment using the voucher. |
| `issuer` | `String` | Optional | The issuer of the voucher. |
| `masked_telephone_number` | `String` | Optional | The shopper telephone number (partially masked). |
| `merchant_name` | `String` | Optional | The merchant name. |
| `merchant_reference` | `String` | Optional | The merchant reference. |
| `pass_creation_token` | `String` | Optional | A Base64-encoded token containing all properties of the voucher. For iOS, you can use this to pass a voucher to Apple Wallet. |
| `payment_data` | `String` | Optional | Encoded payment data. |
| `payment_method_type` | `String` | Optional | Specifies the payment method. |
| `reference` | `String` | Optional | The voucher reference code. |
| `shopper_email` | `String` | Optional | The shopper email. |
| `shopper_name` | `String` | Optional | The shopper name. |
| `surcharge` | [`Amount14`](../../doc/models/amount-14.md) | Optional | The surcharge amount. |
| `total_amount` | [`Amount15`](../../doc/models/amount-15.md) | Optional | The total amount (initial plus surcharge amount). |
| `type` | `String` | Required, Constant | **voucher**<br><br>**Value**: `'voucher'` |
| `url` | `String` | Optional | Specifies the URL to redirect to. |

## Example (as JSON)

```json
{
  "type": "voucher",
  "alternativeReference": "alternativeReference4",
  "collectionInstitutionNumber": "collectionInstitutionNumber2",
  "downloadUrl": "downloadUrl4",
  "entity": "entity4",
  "expiresAt": "expiresAt2"
}
```

