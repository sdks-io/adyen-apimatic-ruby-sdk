
# Service Error Exception

*This model accepts additional fields of type Object.*

## Structure

`ServiceErrorException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `additional_data` | `Hash[String, String]` | Optional | Contains additional information about the payment. Some data fields are included only if you select them first. Go to **Customer Area** > **Developers** > **Additional data**. |
| `error_code` | `String` | Optional | The error code mapped to the error message. |
| `error_type` | `String` | Optional | The category of the error. |
| `message` | `String` | Optional | A short explanation of the issue. |
| `psp_reference` | `String` | Optional | The PSP reference of the payment. |
| `status` | `Integer` | Optional | The HTTP response status. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "additionalData": {
    "key0": "additionalData0"
  },
  "errorCode": "errorCode6",
  "errorType": "errorType0",
  "message": "message0",
  "pspReference": "pspReference8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

