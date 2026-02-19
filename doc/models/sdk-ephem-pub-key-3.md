
# Sdk Ephem Pub Key 3

The `sdkEphemPubKey` value as received from the 3D Secure 2 SDK.
Required for `deviceChannel` set to **app**.

## Structure

`SdkEphemPubKey3`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `crv` | `String` | Optional | The `crv` value as received from the 3D Secure 2 SDK. |
| `kty` | `String` | Optional | The `kty` value as received from the 3D Secure 2 SDK. |
| `x` | `String` | Optional | The `x` value as received from the 3D Secure 2 SDK. |
| `y` | `String` | Optional | The `y` value as received from the 3D Secure 2 SDK. |

## Example (as JSON)

```json
{
  "crv": "crv2",
  "kty": "kty2",
  "x": "x0",
  "y": "y8"
}
```

