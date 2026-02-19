
# Payment Completion Details 1

Use this collection to submit the details that were returned as a result of the `/payments` call.

## Structure

`PaymentCompletionDetails1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `md` | `String` | Optional | A payment session identifier returned by the card issuer.<br><br>**Constraints**: *Maximum Length*: `20000` |
| `pa_req` | `String` | Optional | (3D) Payment Authentication Request data for the card issuer.<br><br>**Constraints**: *Maximum Length*: `20000` |
| `pa_res` | `String` | Optional | (3D) Payment Authentication Response data by the card issuer.<br><br>**Constraints**: *Maximum Length*: `20000` |
| `authorization_token` | `String` | Optional | - |
| `billing_token` | `String` | Optional | PayPal-generated token for recurring payments. |
| `cupsecureplus_smscode` | `String` | Optional | The SMS verification code collected from the shopper. |
| `facilitator_access_token` | `String` | Optional | PayPal-generated third party access token. |
| `one_time_passcode` | `String` | Optional | A random number sent to the mobile phone number of the shopper to verify the payment. |
| `order_id` | `String` | Optional | PayPal-assigned ID for the order. |
| `payer_id` | `String` | Optional | PayPal-assigned ID for the payer (shopper). |
| `payload` | `String` | Optional | Payload appended to the `returnURL` as a result of the redirect.<br><br>**Constraints**: *Maximum Length*: `20000` |
| `payment_id` | `String` | Optional | PayPal-generated ID for the payment. |
| `payment_status` | `String` | Optional | Value passed from the WeChat MiniProgram `wx.requestPayment` **complete** callback. Possible values: any value starting with `requestPayment:`. |
| `redirect_result` | `String` | Optional | The result of the redirect as appended to the `returnURL`.<br><br>**Constraints**: *Maximum Length*: `20000` |
| `result_code` | `String` | Optional | Value you received from the WeChat Pay SDK. |
| `return_url_query_string` | `String` | Optional | The query string as appended to the `returnURL` when using direct issuer links .<br><br>**Constraints**: *Maximum Length*: `20000` |
| `three_ds_result` | `String` | Optional | Base64-encoded string returned by the Component after the challenge flow. It contains the following parameters: `transStatus`, `authorisationToken`.<br><br>**Constraints**: *Maximum Length*: `50000` |
| `threeds_2_challenge_result` | `String` | Optional | Base64-encoded string returned by the Component after the challenge flow. It contains the following parameter: `transStatus`.<br><br>**Constraints**: *Maximum Length*: `50000` |
| `threeds_2_fingerprint` | `String` | Optional | Base64-encoded string returned by the Component after the challenge flow. It contains the following parameter: `threeDSCompInd`.<br><br>**Constraints**: *Maximum Length*: `100000` |
| `vault_token` | `String` | Optional | PayPalv2-generated token for recurring payments. |

## Example (as JSON)

```json
{
  "MD": "MD8",
  "PaReq": "PaReq4",
  "PaRes": "PaRes4",
  "authorization_token": "authorization_token8",
  "billingToken": "billingToken6"
}
```

