
# Three Ds 2 Result

## Structure

`ThreeDs2Result`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authentication_value` | `String` | Optional | The `authenticationValue` value as defined in the 3D Secure 2 specification. |
| `cavv_algorithm` | `String` | Optional | The algorithm used by the ACS to calculate the authentication value, only for Cartes Bancaires integrations. |
| `challenge_cancel` | [`ChallengeCancel`](../../doc/models/challenge-cancel.md) | Optional | Indicator informing the Access Control Server (ACS) and the Directory Server (DS) that the authentication has been cancelled. For possible values, refer to [3D Secure API reference](https://docs.adyen.com/online-payments/3d-secure/api-reference#mpidata). |
| `ds_trans_id` | `String` | Optional | The `dsTransID` value as defined in the 3D Secure 2 specification. |
| `eci` | `String` | Optional | The `eci` value as defined in the 3D Secure 2 specification. |
| `exemption_indicator` | [`ExemptionIndicator`](../../doc/models/exemption-indicator.md) | Optional | Indicates the exemption type that was applied by the issuer to the authentication, if exemption applied.<br>Allowed values:<br><br>* `lowValue`<br>* `secureCorporate`<br>* `trustedBeneficiary`<br>* `transactionRiskAnalysis` |
| `message_version` | `String` | Optional | The `messageVersion` value as defined in the 3D Secure 2 specification. |
| `risk_score` | `String` | Optional | Risk score calculated by Cartes Bancaires Directory Server (DS). |
| `three_ds_requestor_challenge_ind` | [`ThreeDsRequestorChallengeInd`](../../doc/models/three-ds-requestor-challenge-ind.md) | Optional | Indicates whether a challenge is requested for this transaction. Possible values:<br><br>* **01** — No preference<br>* **02** — No challenge requested<br>* **03** — Challenge requested (3DS Requestor preference)<br>* **04** — Challenge requested (Mandate)<br>* **05** — No challenge (transactional risk analysis is already performed)<br>* **06** — Data Only |
| `three_ds_server_trans_id` | `String` | Optional | The `threeDSServerTransID` value as defined in the 3D Secure 2 specification. |
| `timestamp` | `String` | Optional | The `timestamp` value of the 3D Secure 2 authentication. |
| `trans_status` | `String` | Optional | The `transStatus` value as defined in the 3D Secure 2 specification. |
| `trans_status_reason` | `String` | Optional | Provides information on why the `transStatus` field has the specified value. For possible values, refer to [our docs](https://docs.adyen.com/online-payments/3d-secure/api-reference#possible-transstatusreason-values). |
| `white_list_status` | `String` | Optional | The `whiteListStatus` value as defined in the 3D Secure 2 specification. |

## Example (as JSON)

```json
{
  "authenticationValue": "authenticationValue6",
  "cavvAlgorithm": "cavvAlgorithm0",
  "challengeCancel": "07",
  "dsTransID": "dsTransID0",
  "eci": "eci4"
}
```

