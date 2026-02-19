
# Pagination Links 1

Pagination references.

## Structure

`PaginationLinks1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `first` | [`LinksElement9`](../../doc/models/links-element-9.md) | Required | The first page. |
| `last` | [`LinksElement10`](../../doc/models/links-element-10.md) | Required | The last page. |
| `mnext` | [`LinksElement11`](../../doc/models/links-element-11.md) | Optional | The next page. Only present if there is a next page. |
| `prev` | [`LinksElement12`](../../doc/models/links-element-12.md) | Optional | The previous page. Only present if there is a previous page. |
| `mself` | [`LinksElement13`](../../doc/models/links-element-13.md) | Required | The current page. |

## Example (as JSON)

```json
{
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
}
```

