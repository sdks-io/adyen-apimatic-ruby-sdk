
# Checkout Sdk Action

## Structure

`CheckoutSdkAction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `payment_data` | `String` | Optional | Encoded payment data. |
| `payment_method_type` | `String` | Optional | Specifies the payment method. |
| `sdk_data` | `Hash[String, String]` | Optional | The data to pass to the SDK. |
| `type` | [`Type17`](../../doc/models/type-17.md) | Required | The type of the action. |
| `url` | `String` | Optional | Specifies the URL to redirect to. |

## Example (as JSON)

```json
{
  "paymentData": "paymentData4",
  "paymentMethodType": "paymentMethodType4",
  "sdkData": {
    "key0": "sdkData3",
    "key1": "sdkData4"
  },
  "type": "sdk",
  "url": "url6"
}
```

