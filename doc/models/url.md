
# Url

## Structure

`Url`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `encrypted` | `TrueClass \| FalseClass` | Optional | Indicates if the message sent to this URL should be encrypted. |
| `password` | `String` | Optional | The password for authentication of the notifications. |
| `url` | `String` | Optional | The URL in the format: http(s)://domain.com. |
| `username` | `String` | Optional | The username for authentication of the notifications. |

## Example (as JSON)

```json
{
  "encrypted": false,
  "password": "password6",
  "url": "url6",
  "username": "username2"
}
```

