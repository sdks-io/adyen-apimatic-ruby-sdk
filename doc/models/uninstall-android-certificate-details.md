
# Uninstall Android Certificate Details

*This model accepts additional fields of type Object.*

## Structure

`UninstallAndroidCertificateDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate_id` | `String` | Optional | The unique identifier of the certificate to be uninstalled. |
| `type` | [`Type71`](../../doc/models/type-71.md) | Optional | Type of terminal action: Uninstall an Android certificate.<br><br>**Default**: `Type71::UNINSTALLANDROIDCERTIFICATE` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "UninstallAndroidCertificate",
  "certificateId": "certificateId6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

