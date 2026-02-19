
# E Banking Finland

## Structure

`EBankingFinland`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `issuer` | `String` | Optional | The Ebanking Finland issuer value of the shopper's selected bank. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `type` | `String` | Required, Constant | **ebanking_FI**<br><br>**Value**: `'ebanking_FI'` |

## Example (as JSON)

```json
{
  "type": "ebanking_FI",
  "checkoutAttemptId": "checkoutAttemptId4",
  "issuer": "issuer8",
  "sdkData": "sdkData2"
}
```

