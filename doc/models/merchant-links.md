
# Merchant Links

## Structure

`MerchantLinks`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `api_credentials` | [`LinksElement`](../../doc/models/links-element.md) | Optional | - |
| `mself` | [`LinksElement6`](../../doc/models/links-element-6.md) | Required | Link to the resource itself. |
| `users` | [`LinksElement`](../../doc/models/links-element.md) | Optional | - |
| `webhooks` | [`LinksElement`](../../doc/models/links-element.md) | Optional | - |

## Example (as JSON)

```json
{
  "apiCredentials": {
    "href": "href8"
  },
  "self": {
    "href": "href0"
  },
  "users": {
    "href": "href8"
  },
  "webhooks": {
    "href": "href8"
  }
}
```

