
# Validate Shopper Id Request

*This model accepts additional fields of type Object.*

## Structure

`ValidateShopperIdRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_account` | `String` | Required | The merchant account identifier, with which you want to process the transaction.<br><br>**Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1000` |
| `payment_method` | [`ShopperIdPaymentMethod1`](../../doc/models/shopper-id-payment-method-1.md) | Required | paymentMethod |
| `shopper_email` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `300` |
| `shopper_ip` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `15` |
| `shopper_reference` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `256` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "merchantAccount": "merchantAccount8",
  "paymentMethod": {
    "type": "ShopperIdPaymentMethod1",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "shopperEmail": "shopperEmail0",
  "shopperIP": "shopperIP4",
  "shopperReference": "shopperReference4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

