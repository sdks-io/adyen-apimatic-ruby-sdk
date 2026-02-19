
# Risk Data

## Structure

`RiskData`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `client_data` | `String` | Optional | Contains client-side data, like the device fingerprint, cookies, and specific browser settings.<br><br>**Constraints**: *Maximum Length*: `5000` |
| `custom_fields` | `Hash[String, String]` | Optional | Any custom fields used as part of the input to configured risk rules. |
| `fraud_offset` | `Integer` | Optional | An integer value that is added to the normal fraud score. The value can be either positive or negative. |
| `profile_reference` | `String` | Optional | The risk profile to assign to this payment. When left empty, the merchant-level account's default risk profile will be applied. |

## Example (as JSON)

```json
{
  "clientData": "clientData4",
  "customFields": {
    "key0": "customFields2"
  },
  "fraudOffset": 28,
  "profileReference": "profileReference2"
}
```

