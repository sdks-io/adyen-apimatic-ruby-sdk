
# Doku

## Structure

`Doku`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `first_name` | `String` | Required | The shopper's first name. |
| `last_name` | `String` | Required | The shopper's last name. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `shopper_email` | `String` | Required | The shopper's email. |
| `type` | [`Type19`](../../doc/models/type-19.md) | Required | **doku** |

## Example (as JSON)

```json
{
  "checkoutAttemptId": "checkoutAttemptId4",
  "firstName": "firstName6",
  "lastName": "lastName2",
  "sdkData": "sdkData2",
  "shopperEmail": "shopperEmail8",
  "type": "doku_bni_va"
}
```

