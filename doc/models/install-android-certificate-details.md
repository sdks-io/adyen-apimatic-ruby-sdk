
# Install Android Certificate Details

## Structure

`InstallAndroidCertificateDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate_id` | `String` | Optional | The unique identifier of the certificate to be installed. |
| `type` | [`Type37`](../../doc/models/type-37.md) | Optional | Type of terminal action: Install an Android certificate.<br><br>**Default**: `Type37::INSTALLANDROIDCERTIFICATE` |

## Example (as JSON)

```json
{
  "type": "InstallAndroidCertificate",
  "certificateId": "certificateId6"
}
```

