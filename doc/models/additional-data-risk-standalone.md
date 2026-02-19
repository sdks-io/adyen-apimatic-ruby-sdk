
# Additional Data Risk Standalone

## Structure

`AdditionalDataRiskStandalone`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pay_pal_country_code` | `String` | Optional | Shopper's country of residence in the form of ISO standard 3166 2-character country codes. |
| `pay_pal_email_id` | `String` | Optional | Shopper's email. |
| `pay_pal_first_name` | `String` | Optional | Shopper's first name. |
| `pay_pal_last_name` | `String` | Optional | Shopper's last name. |
| `pay_pal_payer_id` | `String` | Optional | Unique PayPal Customer Account identification number. Character length and limitations: 13 single-byte alphanumeric characters. |
| `pay_pal_phone` | `String` | Optional | Shopper's phone number. |
| `pay_pal_protection_eligibility` | `String` | Optional | Allowed values:<br><br>* **Eligible** — Merchant is protected by PayPal's Seller Protection Policy for Unauthorized Payments and Item Not Received.<br><br>* **PartiallyEligible** — Merchant is protected by PayPal's Seller Protection Policy for Item Not Received.<br><br>* **Ineligible** — Merchant is not protected under the Seller Protection Policy. |
| `pay_pal_transaction_id` | `String` | Optional | Unique transaction ID of the payment. |
| `avs_result_raw` | `String` | Optional | Raw AVS result received from the acquirer, where available. Example: D |
| `bin` | `String` | Optional | The Bank Identification Number of a credit card, which is the first six digits of a card number. Required for [tokenized card request](https://docs.adyen.com/online-payments/tokenization). |
| `cvc_result_raw` | `String` | Optional | Raw CVC result received from the acquirer, where available. Example: 1 |
| `risk_token` | `String` | Optional | Unique identifier or token for the shopper's card details. |
| `three_d_authenticated` | `String` | Optional | A Boolean value indicating whether 3DS authentication was completed on this payment. Example: true |
| `three_d_offered` | `String` | Optional | A Boolean value indicating whether 3DS was offered for this payment. Example: true |
| `token_data_type` | `String` | Optional | Required for PayPal payments only. The only supported value is: **paypal**. |

## Example (as JSON)

```json
{
  "PayPal.CountryCode": "PayPal.CountryCode0",
  "PayPal.EmailId": "PayPal.EmailId0",
  "PayPal.FirstName": "PayPal.FirstName4",
  "PayPal.LastName": "PayPal.LastName0",
  "PayPal.PayerId": "PayPal.PayerId8"
}
```

