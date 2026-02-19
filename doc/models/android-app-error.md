
# Android App Error

## Structure

`AndroidAppError`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error_code` | `String` | Optional | The error code of the Android app with the `status` of either **error** or **invalid**. |
| `terminal_models` | `Array[String]` | Optional | The list of payment terminal models to which the returned `errorCode` applies. |

## Example (as JSON)

```json
{
  "errorCode": "errorCode6",
  "terminalModels": [
    "terminalModels3"
  ]
}
```

