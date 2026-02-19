
# Fund Origin

## Structure

`FundOrigin`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `billing_address` | [`Address3`](../../doc/models/address-3.md) | Optional | The address where to send the invoice. |
| `shopper_email` | `String` | Optional | The email address of the person funding the money. |
| `shopper_name` | [`Name1`](../../doc/models/name-1.md) | Optional | The name of the person funding the money. |
| `telephone_number` | `String` | Optional | The phone number of the person funding the money. |
| `wallet_identifier` | `String` | Optional | The unique identifier of the wallet where the funds are coming from. |

## Example (as JSON)

```json
{
  "billingAddress": {
    "city": "city8",
    "country": "country6",
    "houseNumberOrName": "houseNumberOrName0",
    "postalCode": "postalCode6",
    "stateOrProvince": "stateOrProvince0",
    "street": "street2"
  },
  "shopperEmail": "shopperEmail4",
  "shopperName": {
    "firstName": "firstName2",
    "lastName": "lastName6"
  },
  "telephoneNumber": "telephoneNumber2",
  "walletIdentifier": "walletIdentifier4"
}
```

