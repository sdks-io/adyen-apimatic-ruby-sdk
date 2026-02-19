
# Google Pay 3

## Structure

`GooglePay3`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `funding_source` | [`FundingSource`](../../doc/models/funding-source.md) | Optional | The funding source that should be used when multiple sources are available. For Brazilian combo cards, by default the funding source is credit. To use debit, set this value to **debit**. |
| `google_pay_token` | `String` | Required | The `token` that you obtained from the [Google Pay API](https://developers.google.com/pay/api/web/reference/response-objects#PaymentData) `PaymentData` response.<br><br>**Constraints**: *Maximum Length*: `5000` |
| `recurring_detail_reference` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `stored_payment_method_id` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` |
| `three_ds_2_sdk_version` | `String` | Optional | Required for mobile integrations. Version of the 3D Secure 2 mobile SDK.<br><br>**Constraints**: *Maximum Length*: `12` |
| `type` | [`Type22`](../../doc/models/type-22.md) | Optional | **paywithgoogle**<br><br>**Default**: `Type22::PAYWITHGOOGLE` |

## Example (as JSON)

```json
{
  "googlePayToken": "googlePayToken6",
  "type": "paywithgoogle",
  "checkoutAttemptId": "checkoutAttemptId0",
  "fundingSource": "prepaid",
  "recurringDetailReference": "recurringDetailReference4",
  "sdkData": "sdkData6",
  "storedPaymentMethodId": "storedPaymentMethodId8"
}
```

