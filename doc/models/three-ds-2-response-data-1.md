
# Three Ds 2 Response Data 1

Response of the 3D Secure 2 authentication.

## Structure

`ThreeDs2ResponseData1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `acs_challenge_mandated` | `String` | Optional | - |
| `acs_operator_id` | `String` | Optional | - |
| `acs_reference_number` | `String` | Optional | - |
| `acs_signed_content` | `String` | Optional | - |
| `acs_trans_id` | `String` | Optional | - |
| `acs_url` | `String` | Optional | - |
| `authentication_type` | `String` | Optional | - |
| `card_holder_info` | `String` | Optional | - |
| `cavv_algorithm` | `String` | Optional | - |
| `challenge_indicator` | `String` | Optional | - |
| `ds_reference_number` | `String` | Optional | - |
| `ds_trans_id` | `String` | Optional | - |
| `exemption_indicator` | `String` | Optional | - |
| `message_version` | `String` | Optional | - |
| `risk_score` | `String` | Optional | - |
| `sdk_ephem_pub_key` | `String` | Optional | - |
| `three_ds_server_trans_id` | `String` | Optional | - |
| `trans_status` | `String` | Optional | - |
| `trans_status_reason` | `String` | Optional | - |

## Example (as JSON)

```json
{
  "acsChallengeMandated": "acsChallengeMandated0",
  "acsOperatorID": "acsOperatorID0",
  "acsReferenceNumber": "acsReferenceNumber0",
  "acsSignedContent": "acsSignedContent6",
  "acsTransID": "acsTransID0"
}
```

