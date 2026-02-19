
# Givex Info

## Structure

`GivexInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `currency_code` | `String` | Required | The three-character ISO currency code, such as **EUR**. |
| `password` | `String` | Required | The password provided by the acquirer. |
| `payment_flow` | [`PaymentFlow`](../../doc/models/payment-flow.md) | Required | The sales channel used for the payment. |
| `username` | `String` | Required | The username provided by the acquirer. |

## Example (as JSON)

```json
{
  "currencyCode": "currencyCode2",
  "password": "password6",
  "paymentFlow": "Ecommerce",
  "username": "username8"
}
```

