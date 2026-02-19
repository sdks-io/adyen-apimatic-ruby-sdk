
# Masterpass

## Structure

`Masterpass`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `funding_source` | [`FundingSource`](../../doc/models/funding-source.md) | Optional | The funding source that should be used when multiple sources are available. For Brazilian combo cards, by default the funding source is credit. To use debit, set this value to **debit**. |
| `masterpass_transaction_id` | `String` | Required | The Masterpass transaction ID. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `type` | [`Type30`](../../doc/models/type-30.md) | Optional | **masterpass**<br><br>**Default**: `Type30::MASTERPASS` |

## Example (as JSON)

```json
{
  "masterpassTransactionId": "masterpassTransactionId0",
  "type": "masterpass",
  "checkoutAttemptId": "checkoutAttemptId4",
  "fundingSource": "credit",
  "sdkData": "sdkData2"
}
```

