
# Payment Method

## Structure

`PaymentMethod`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `apps` | [`Array[PaymentMethodUpiApps]`](../../doc/models/payment-method-upi-apps.md) | Optional | A list of apps for this payment method. |
| `brand` | `String` | Optional | Brand for the selected gift card. For example: plastix, hmclub. |
| `brands` | `Array[String]` | Optional | List of possible brands. For example: visa, mc. |
| `configuration` | `Hash[String, String]` | Optional | The configuration of the payment method. |
| `funding_source` | [`FundingSource9`](../../doc/models/funding-source-9.md) | Optional | The funding source of the payment method. |
| `group` | [`PaymentMethodGroup2`](../../doc/models/payment-method-group-2.md) | Optional | The group where this payment method belongs to. |
| `input_details` | [`Array[InputDetail]`](../../doc/models/input-detail.md) | Optional | All input details to be provided to complete the payment with this payment method. |
| `issuers` | [`Array[PaymentMethodIssuer]`](../../doc/models/payment-method-issuer.md) | Optional | A list of issuers for this payment method. |
| `name` | `String` | Optional | The displayable name of this payment method. |
| `promoted` | `TrueClass \| FalseClass` | Optional | Indicates whether this payment method should be promoted or not. |
| `type` | `String` | Optional | The unique payment method code. |

## Example (as JSON)

```json
{
  "apps": [
    {
      "id": "id6",
      "name": "name6"
    },
    {
      "id": "id6",
      "name": "name6"
    },
    {
      "id": "id6",
      "name": "name6"
    }
  ],
  "brand": "brand8",
  "brands": [
    "brands5",
    "brands6"
  ],
  "configuration": {
    "key0": "configuration0"
  },
  "fundingSource": "credit"
}
```

