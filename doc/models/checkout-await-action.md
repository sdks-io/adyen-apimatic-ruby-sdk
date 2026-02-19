
# Checkout Await Action

## Structure

`CheckoutAwaitAction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `payment_data` | `String` | Optional | Encoded payment data. |
| `payment_method_type` | `String` | Optional | Specifies the payment method. |
| `type` | `String` | Required, Constant | **await**<br><br>**Value**: `'await'` |
| `url` | `String` | Optional | Specifies the URL to redirect to. |

## Example (as JSON)

```json
{
  "type": "await",
  "paymentData": "paymentData8",
  "paymentMethodType": "paymentMethodType8",
  "url": "url0"
}
```

