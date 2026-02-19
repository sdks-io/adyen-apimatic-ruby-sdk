
# Event Url

## Structure

`EventUrl`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `event_local_urls` | [`Array[Url]`](../../doc/models/url.md) | Optional | One or more local URLs to send event notifications to when using Terminal API. |
| `event_public_urls` | [`Array[Url]`](../../doc/models/url.md) | Optional | One or more public URLs to send event notifications to when using Terminal API. |

## Example (as JSON)

```json
{
  "eventLocalUrls": [
    {
      "encrypted": false,
      "password": "password4",
      "url": "url4",
      "username": "username0"
    },
    {
      "encrypted": false,
      "password": "password4",
      "url": "url4",
      "username": "username0"
    },
    {
      "encrypted": false,
      "password": "password4",
      "url": "url4",
      "username": "username0"
    }
  ],
  "eventPublicUrls": [
    {
      "encrypted": false,
      "password": "password8",
      "url": "url8",
      "username": "username4"
    },
    {
      "encrypted": false,
      "password": "password8",
      "url": "url8",
      "username": "username4"
    },
    {
      "encrypted": false,
      "password": "password8",
      "url": "url8",
      "username": "username4"
    }
  ]
}
```

