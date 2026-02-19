
# Givex Info 1

Details to provide if `type` is **givex**.

## Structure

`GivexInfo1`

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
  "currencyCode": "currencyCode0",
  "password": "password4",
  "paymentFlow": "Ecommerce",
  "username": "username0"
}
```

