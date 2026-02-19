
# Pse Latam

*This model accepts additional fields of type Object.*

## Structure

`PseLatam`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `bank` | `String` | Required | The shopper's bank. |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `client_type` | `String` | Required | The client type. |
| `identification` | `String` | Required | The identification code. |
| `identification_type` | `String` | Required | The identification type. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `type` | [`Type40`](../../doc/models/type-40.md) | Optional | The payment method type. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "bank": "bank4",
  "checkoutAttemptId": "checkoutAttemptId2",
  "clientType": "clientType4",
  "identification": "identification4",
  "identificationType": "identificationType8",
  "sdkData": "sdkData4",
  "type": "pse_payulatam",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

