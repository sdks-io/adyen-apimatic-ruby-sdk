
# Android Certificate

## Structure

`AndroidCertificate`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Optional | The description that was provided when uploading the certificate. |
| `extension` | `String` | Optional | The file format of the certificate, as indicated by the file extension. For example, **.cert** or **.pem**. |
| `id` | `String` | Required | The unique identifier of the certificate. |
| `name` | `String` | Optional | The file name of the certificate. For example, **mycert**. |
| `not_after` | `DateTime` | Optional | The date when the certificate stops to be valid. |
| `not_before` | `DateTime` | Optional | The date when the certificate starts to be valid. |
| `status` | `String` | Optional | The status of the certificate. |

## Example (as JSON)

```json
{
  "description": "description8",
  "extension": "extension4",
  "id": "id8",
  "name": "name8",
  "notAfter": "2016-03-13T12:52:32.123Z",
  "notBefore": "2016-03-13T12:52:32.123Z"
}
```

