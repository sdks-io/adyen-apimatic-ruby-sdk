
# Default Error Response Entity Exception

Standardized error response following RFC-7807 format

Find out more here: [https://www.rfc-editor.org/rfc/rfc7807](https://www.rfc-editor.org/rfc/rfc7807)

*This model accepts additional fields of type Object.*

## Structure

`DefaultErrorResponseEntityException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `detail` | `String` | Optional | A human-readable explanation specific to this occurrence of the problem. |
| `error_code` | `String` | Optional | Unique business error code. |
| `instance` | `String` | Optional | A URI that identifies the specific occurrence of the problem if applicable. |
| `invalid_fields` | [`Array[InvalidField]`](../../doc/models/invalid-field.md) | Optional | Array of fields with validation errors when applicable. |
| `request_id` | `String` | Optional | The unique reference for the request. |
| `status` | `Integer` | Optional | The HTTP status code. |
| `title` | `String` | Optional | A short, human-readable summary of the problem type. |
| `type` | `String` | Optional | A URI that identifies the validation error type. It points to human-readable documentation for the problem type. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "detail": "detail0",
  "errorCode": "errorCode0",
  "instance": "instance0",
  "invalidFields": [
    {
      "name": "name6",
      "value": "value8",
      "message": "message6",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "name": "name6",
      "value": "value8",
      "message": "message6",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "requestId": "requestId6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

