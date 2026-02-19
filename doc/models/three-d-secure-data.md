
# Three D Secure Data

## Structure

`ThreeDSecureData`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authentication_response` | [`AuthenticationResponse`](../../doc/models/authentication-response.md) | Optional | In 3D Secure 2, this is the `transStatus` from the challenge result. If the transaction was frictionless, omit this parameter. |
| `cavv` | `String` | Optional | The cardholder authentication value (base64 encoded, 20 bytes in a decoded form). |
| `cavv_algorithm` | `String` | Optional | The CAVV algorithm used. Include this only for 3D Secure 1. |
| `challenge_cancel` | [`ChallengeCancel`](../../doc/models/challenge-cancel.md) | Optional | Indicator informing the Access Control Server (ACS) and the Directory Server (DS) that the authentication has been cancelled. For possible values, refer to [3D Secure API reference](https://docs.adyen.com/online-payments/3d-secure/api-reference#mpidata). |
| `directory_response` | [`DirectoryResponse`](../../doc/models/directory-response.md) | Optional | In 3D Secure 2, this is the `transStatus` from the `ARes`. |
| `ds_trans_id` | `String` | Optional | Supported for 3D Secure 2. The unique transaction identifier assigned by the Directory Server (DS) to identify a single transaction. |
| `eci` | `String` | Optional | The electronic commerce indicator. |
| `risk_score` | `String` | Optional | Risk score calculated by Directory Server (DS). Required for Cartes Bancaires integrations. |
| `three_ds_version` | `String` | Optional | The version of the 3D Secure protocol. |
| `token_authentication_verification_value` | `String` | Optional | Network token authentication verification value (TAVV). The network token cryptogram. |
| `trans_status_reason` | `String` | Optional | Provides information on why the `transStatus` field has the specified value. For possible values, refer to [our docs](https://docs.adyen.com/online-payments/3d-secure/api-reference#possible-transstatusreason-values). |
| `xid` | `String` | Optional | Supported for 3D Secure 1. The transaction identifier (Base64-encoded, 20 bytes in a decoded form). |

## Example (as JSON)

```json
{
  "authenticationResponse": "Y",
  "cavv": "cavv6",
  "cavvAlgorithm": "cavvAlgorithm4",
  "challengeCancel": "02",
  "directoryResponse": "N"
}
```

