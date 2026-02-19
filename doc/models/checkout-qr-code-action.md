
# Checkout Qr Code Action

## Structure

`CheckoutQrCodeAction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `expires_at` | `String` | Optional | Expiry time of the QR code. |
| `payment_data` | `String` | Optional | Encoded payment data. |
| `payment_method_type` | `String` | Optional | Specifies the payment method. |
| `qr_code_data` | `String` | Optional | The contents of the QR code as a UTF8 string. |
| `type` | `String` | Required, Constant | **qrCode**<br><br>**Value**: `'qrCode'` |
| `url` | `String` | Optional | Specifies the URL to redirect to. |

## Example (as JSON)

```json
{
  "type": "qrCode",
  "expiresAt": "expiresAt8",
  "paymentData": "paymentData4",
  "paymentMethodType": "paymentMethodType4",
  "qrCodeData": "qrCodeData4",
  "url": "url6"
}
```

