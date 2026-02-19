
# Upi Payment Method

*This model accepts additional fields of type Object.*

## Structure

`UpiPaymentMethod`

## Inherits From

[`ShopperIdPaymentMethod`](../../doc/models/shopper-id-payment-method.md)

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `virtual_payment_address` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "upi_collect",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  },
  "virtualPaymentAddress": "virtualPaymentAddress4"
}
```

