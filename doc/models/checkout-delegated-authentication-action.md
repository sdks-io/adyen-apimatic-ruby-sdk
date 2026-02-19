
# Checkout Delegated Authentication Action

## Structure

`CheckoutDelegatedAuthenticationAction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorisation_token` | `String` | Optional | A token needed to authorise a payment. |
| `payment_data` | `String` | Optional | Encoded payment data. |
| `payment_method_type` | `String` | Optional | Specifies the payment method. |
| `token` | `String` | Optional | A token to pass to the delegatedAuthentication component. |
| `type` | `String` | Required, Constant | **delegatedAuthentication**<br><br>**Value**: `'delegatedAuthentication'` |
| `url` | `String` | Optional | Specifies the URL to redirect to. |

## Example (as JSON)

```json
{
  "type": "delegatedAuthentication",
  "authorisationToken": "authorisationToken4",
  "paymentData": "paymentData2",
  "paymentMethodType": "paymentMethodType2",
  "token": "token4",
  "url": "url4"
}
```

