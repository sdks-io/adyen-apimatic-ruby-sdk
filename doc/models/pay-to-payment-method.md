
# Pay to Payment Method

*This model accepts additional fields of type Object.*

## Structure

`PayToPaymentMethod`

## Inherits From

[`ShopperIdPaymentMethod`](../../doc/models/shopper-id-payment-method.md)

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `shopper_reference` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `256` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "payTo",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  },
  "shopperReference": "shopperReference2"
}
```

