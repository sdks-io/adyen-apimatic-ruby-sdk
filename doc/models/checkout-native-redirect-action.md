
# Checkout Native Redirect Action

## Structure

`CheckoutNativeRedirectAction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | `Hash[String, String]` | Optional | When the redirect URL must be accessed via POST, use this data to post to the redirect URL. |
| `method` | `String` | Optional | Specifies the HTTP method, for example GET or POST. |
| `native_redirect_data` | `String` | Optional | Native SDK's redirect data containing the direct issuer link and state data that must be submitted to the /v1/nativeRedirect/redirectResult. |
| `payment_method_type` | `String` | Optional | Specifies the payment method. |
| `type` | `String` | Required, Constant | **nativeRedirect**<br><br>**Value**: `'nativeRedirect'` |
| `url` | `String` | Optional | Specifies the URL to redirect to. |

## Example (as JSON)

```json
{
  "type": "nativeRedirect",
  "data": {
    "key0": "data5"
  },
  "method": "method6",
  "nativeRedirectData": "nativeRedirectData8",
  "paymentMethodType": "paymentMethodType2",
  "url": "url4"
}
```

