
# Checkout Order Response 1

Contains updated information regarding the order in case order information was provided in the request.

## Structure

`CheckoutOrderResponse1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | [`Amount11`](../../doc/models/amount-11.md) | Optional | The initial amount of the order. |
| `expires_at` | `String` | Optional | The expiry date for the order. |
| `order_data` | `String` | Optional | The encrypted order data. |
| `psp_reference` | `String` | Required | The `pspReference` that belongs to the order. |
| `reference` | `String` | Optional | The merchant reference for the order. |
| `remaining_amount` | [`Amount12`](../../doc/models/amount-12.md) | Optional | The updated remaining amount. |

## Example (as JSON)

```json
{
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "expiresAt": "expiresAt0",
  "orderData": "orderData6",
  "pspReference": "pspReference6",
  "reference": "reference0",
  "remainingAmount": {
    "currency": "currency6",
    "value": 156
  }
}
```

