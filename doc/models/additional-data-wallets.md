
# Additional Data Wallets

## Structure

`AdditionalDataWallets`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `androidpay_token` | `String` | Optional | The Android Pay token retrieved from the SDK. |
| `masterpass_transaction_id` | `String` | Optional | The Mastercard Masterpass Transaction ID retrieved from the SDK. |
| `payment_token` | `String` | Optional | The Apple Pay token retrieved from the SDK. |
| `paywithgoogle_token` | `String` | Optional | The Google Pay token retrieved from the SDK. |
| `samsungpay_token` | `String` | Optional | The Samsung Pay token retrieved from the SDK. |
| `visacheckout_call_id` | `String` | Optional | The Visa Checkout Call ID retrieved from the SDK. |

## Example (as JSON)

```json
{
  "androidpay.token": "androidpay.token2",
  "masterpass.transactionId": "masterpass.transactionId2",
  "payment.token": "payment.token4",
  "paywithgoogle.token": "paywithgoogle.token0",
  "samsungpay.token": "samsungpay.token0"
}
```

