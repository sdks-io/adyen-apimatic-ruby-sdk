
# Delivery Method

## Structure

`DeliveryMethod`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | [`Amount23`](../../doc/models/amount-23.md) | Optional | The cost of this delivery method. |
| `description` | `String` | Optional | The name of the delivery method as shown to the shopper. |
| `reference` | `String` | Optional | The reference of the delivery method. |
| `selected` | `TrueClass \| FalseClass` | Optional | If you display the PayPal lightbox with delivery methods, set to **true** for the delivery method that is selected. Only one delivery method can be selected at a time. |
| `type` | [`Type18`](../../doc/models/type-18.md) | Optional | The type of the delivery method. |

## Example (as JSON)

```json
{
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "description": "description6",
  "reference": "reference0",
  "selected": false,
  "type": "Shipping"
}
```

