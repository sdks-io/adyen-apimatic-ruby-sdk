
# List Stores Response

## Structure

`ListStoresResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `links` | [`PaginationLinks1`](../../doc/models/pagination-links-1.md) | Optional | Pagination references. |
| `data` | [`Array[Store]`](../../doc/models/store.md) | Optional | List of stores |
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
  "data": [
    {
      "_links": {
        "self": {
          "href": "href0"
        }
      },
      "address": {
        "city": "city6",
        "country": "country0",
        "line1": "line18",
        "line2": "line20",
        "line3": "line38",
        "postalCode": "postalCode8"
      },
      "businessLineIds": [
        "businessLineIds4"
      ],
      "description": "description0",
      "externalReferenceId": "externalReferenceId8"
    }
  ],
  "itemsTotal": 122,
  "pagesTotal": 84
}
```

