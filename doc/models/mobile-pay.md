
# Mobile Pay

## Structure

`MobilePay`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `type` | [`Type32`](../../doc/models/type-32.md) | Optional | **mobilepay**<br><br>**Default**: `Type32::MOBILEPAY` |

## Example (as JSON)

```json
{
  "type": "mobilepay",
  "checkoutAttemptId": "checkoutAttemptId0",
  "sdkData": "sdkData6"
}
```

