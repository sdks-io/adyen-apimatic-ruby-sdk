
# File 1

For `authType` **wpa-eap** or **wpa2-eap**. The root certificate from the CA that signed the certificate of the RADIUS server that is part of your wireless network.

## Structure

`File1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | `String` | Required | The certificate content converted to a Base64-encoded string. |
| `name` | `String` | Required | The name of the certificate. Must be unique across Wi-Fi profiles. |

## Example (as JSON)

```json
{
  "data": "data6",
  "name": "name6"
}
```

