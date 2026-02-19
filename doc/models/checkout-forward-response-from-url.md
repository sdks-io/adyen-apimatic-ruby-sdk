
# Checkout Forward Response From Url

## Structure

`CheckoutForwardResponseFromUrl`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `String` | Optional | The body of the response Adyen received from the third party, in string format. |
| `headers` | `Hash[String, String]` | Optional | The HTTP headers of the response Adyen received from the third party. |
| `status` | `Integer` | Optional | The HTTP status of the response Adyen received from the third party. |

## Example (as JSON)

```json
{
  "body": "body0",
  "headers": {
    "key0": "headers7",
    "key1": "headers8",
    "key2": "headers9"
  },
  "status": 152
}
```

