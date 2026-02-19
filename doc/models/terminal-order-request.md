
# Terminal Order Request

## Structure

`TerminalOrderRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `billing_entity_id` | `String` | Optional | The identification of the billing entity to use for the order.<br><br>> When ordering products in Brazil, you do not need to include the `billingEntityId` in the request. |
| `customer_order_reference` | `String` | Optional | The merchant-defined purchase order reference. |
| `items` | [`Array[OrderItem]`](../../doc/models/order-item.md) | Optional | The products included in the order. |
| `order_type` | `String` | Optional | Type of order |
| `shipping_location_id` | `String` | Optional | The identification of the shipping location to use for the order. |
| `tax_id` | `String` | Optional | The tax number of the billing entity. |

## Example (as JSON)

```json
{
  "billingEntityId": "billingEntityId6",
  "customerOrderReference": "customerOrderReference8",
  "items": [
    {
      "id": "id8",
      "installments": 204,
      "name": "name8",
      "quantity": 22
    },
    {
      "id": "id8",
      "installments": 204,
      "name": "name8",
      "quantity": 22
    },
    {
      "id": "id8",
      "installments": 204,
      "name": "name8",
      "quantity": 22
    }
  ],
  "orderType": "orderType4",
  "shippingLocationId": "shippingLocationId4"
}
```

