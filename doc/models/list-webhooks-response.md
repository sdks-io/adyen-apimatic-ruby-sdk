
# List Webhooks Response

## Structure

`ListWebhooksResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `links` | [`PaginationLinks1`](../../doc/models/pagination-links-1.md) | Optional | Pagination references. |
| `account_reference` | `String` | Optional | Reference to the account. |
| `data` | [`Array[Webhook]`](../../doc/models/webhook.md) | Optional | The list of webhooks configured for this account. |
| `items_total` | `Integer` | Required | Total number of items. |
| `pages_total` | `Integer` | Required | Total number of pages. |

## Example (as JSON)

```json
{
  "_links": {
    "first": {
      "href": "href2"
    },
    "last": {
      "href": "href2"
    },
    "next": {
      "href": "href4"
    },
    "prev": {
      "href": "href8"
    },
    "self": {
      "href": "href0"
    }
  },
  "accountReference": "accountReference2",
  "data": [
    {
      "_links": {
        "company": {
          "href": "href2"
        },
        "generateHmac": {
          "href": "href6"
        },
        "merchant": {
          "href": "href6"
        },
        "self": {
          "href": "href0"
        },
        "testWebhook": {
          "href": "href6"
        }
      },
      "acceptsExpiredCertificate": false,
      "acceptsSelfSignedCertificate": false,
      "acceptsUntrustedRootCertificate": false,
      "accountReference": "accountReference2",
      "active": false,
      "communicationFormat": "json",
      "type": "type0",
      "url": "url4"
    },
    {
      "_links": {
        "company": {
          "href": "href2"
        },
        "generateHmac": {
          "href": "href6"
        },
        "merchant": {
          "href": "href6"
        },
        "self": {
          "href": "href0"
        },
        "testWebhook": {
          "href": "href6"
        }
      },
      "acceptsExpiredCertificate": false,
      "acceptsSelfSignedCertificate": false,
      "acceptsUntrustedRootCertificate": false,
      "accountReference": "accountReference2",
      "active": false,
      "communicationFormat": "json",
      "type": "type0",
      "url": "url4"
    },
    {
      "_links": {
        "company": {
          "href": "href2"
        },
        "generateHmac": {
          "href": "href6"
        },
        "merchant": {
          "href": "href6"
        },
        "self": {
          "href": "href0"
        },
        "testWebhook": {
          "href": "href6"
        }
      },
      "acceptsExpiredCertificate": false,
      "acceptsSelfSignedCertificate": false,
      "acceptsUntrustedRootCertificate": false,
      "accountReference": "accountReference2",
      "active": false,
      "communicationFormat": "json",
      "type": "type0",
      "url": "url4"
    }
  ],
  "itemsTotal": 90,
  "pagesTotal": 204
}
```

