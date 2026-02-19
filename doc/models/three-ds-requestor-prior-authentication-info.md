
# Three Ds Requestor Prior Authentication Info

## Structure

`ThreeDsRequestorPriorAuthenticationInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `three_ds_req_prior_auth_data` | `String` | Optional | Data that documents and supports a specific authentication process. Maximum length: 2048 bytes. |
| `three_ds_req_prior_auth_method` | [`ThreeDsReqPriorAuthMethod`](../../doc/models/three-ds-req-prior-auth-method.md) | Optional | Mechanism used by the Cardholder to previously authenticate to the 3DS Requestor. Allowed values:<br><br>* **01** — Frictionless authentication occurred by ACS.<br>* **02** — Cardholder challenge occurred by ACS.<br>* **03** — AVS verified.<br>* **04** — Other issuer methods.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `2` |
| `three_ds_req_prior_auth_timestamp` | `String` | Optional | Date and time in UTC of the prior cardholder authentication. Format: YYYYMMDDHHMM<br><br>**Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12` |
| `three_ds_req_prior_ref` | `String` | Optional | This data element provides additional information to the ACS to determine the best approach for handing a request. This data element contains an ACS Transaction ID for a prior authenticated transaction. For example, the first recurring transaction that was authenticated with the cardholder. Length: 30 characters.<br><br>**Constraints**: *Minimum Length*: `36`, *Maximum Length*: `36` |

## Example (as JSON)

```json
{
  "threeDSReqPriorAuthData": "threeDSReqPriorAuthData2",
  "threeDSReqPriorAuthMethod": "03",
  "threeDSReqPriorAuthTimestamp": "threeDSReqPriorAuthTimestamp0",
  "threeDSReqPriorRef": "threeDSReqPriorRef2"
}
```

