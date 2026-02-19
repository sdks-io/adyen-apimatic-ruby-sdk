
# Visa Checkout

*This model accepts additional fields of type Object.*

## Structure

`VisaCheckout`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `funding_source` | [`FundingSource`](../../doc/models/funding-source.md) | Optional | The funding source that should be used when multiple sources are available. For Brazilian combo cards, by default the funding source is credit. To use debit, set this value to **debit**. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `type` | [`Type49`](../../doc/models/type-49.md) | Optional | **visacheckout**<br><br>**Default**: `Type49::VISACHECKOUT` |
| `visa_checkout_call_id` | `String` | Required | The Visa Click to Pay Call ID value. When your shopper selects a payment and/or a shipping address from Visa Click to Pay, you will receive a Visa Click to Pay Call ID. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "visacheckout",
  "visaCheckoutCallId": "visaCheckoutCallId0",
  "checkoutAttemptId": "checkoutAttemptId8",
  "fundingSource": "credit",
  "sdkData": "sdkData8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

