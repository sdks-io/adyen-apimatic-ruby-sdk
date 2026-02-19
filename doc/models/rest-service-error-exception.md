
# Rest Service Error Exception

*This model accepts additional fields of type Object.*

## Structure

`RestServiceErrorException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `detail` | `String` | Required | A human-readable explanation specific to this occurrence of the problem. |
| `error_code` | `String` | Required | A code that identifies the problem type. |
| `instance` | `String` | Optional | A unique URI that identifies the specific occurrence of the problem. |
| `invalid_fields` | [`Array[InvalidField]`](../../doc/models/invalid-field.md) | Optional | Detailed explanation of each validation error, when applicable. |
| `request_id` | `String` | Optional | A unique reference for the request, essentially the same as `pspReference`. |
| `response` | `Object` | Optional | JSON response payload. |
| `status` | `Integer` | Required | The HTTP status code. |
| `title` | `String` | Required | A short, human-readable summary of the problem type. |
| `type` | `String` | Required | A URI that identifies the problem type, pointing to human-readable documentation on this problem type. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "detail": "detail8",
  "errorCode": "errorCode8",
  "instance": "instance8",
  "invalidFields": [
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
  "requestId": "requestId4",
  "response": {
    "key1": "val1",
    "key2": "val2"
  },
  "status": 158,
  "title": "title8",
  "type": "type2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

