
# Checkout Three Ds 2 Action

## Structure

`CheckoutThreeDs2Action`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorisation_token` | `String` | Optional | A token needed to authorise a payment. |
| `payment_data` | `String` | Optional | Encoded payment data. |
| `payment_method_type` | `String` | Optional | Specifies the payment method. |
| `subtype` | `String` | Optional | A subtype of the token. |
| `token` | `String` | Optional | A token to pass to the 3DS2 Component to get the fingerprint. |
| `type` | `String` | Required, Constant | **threeDS2**<br><br>**Value**: `'threeDS2'` |
| `url` | `String` | Optional | Specifies the URL to redirect to. |

## Example (as JSON)

```json
{
  "type": "threeDS2",
  "authorisationToken": "authorisationToken0",
  "paymentData": "paymentData8",
  "paymentMethodType": "paymentMethodType8",
  "subtype": "subtype8",
  "token": "token0"
}
```

