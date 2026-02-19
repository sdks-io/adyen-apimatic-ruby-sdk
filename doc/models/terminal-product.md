
# Terminal Product

## Structure

`TerminalProduct`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Optional | Information about items included and integration options. |
| `id` | `String` | Optional | The unique identifier of the product. |
| `items_included` | `Array[String]` | Optional | A list of parts included in the terminal package. |
| `name` | `String` | Optional | The descriptive name of the product. |
| `price` | [`TerminalProductPrice2`](../../doc/models/terminal-product-price-2.md) | Optional | The price of the product. |

## Example (as JSON)

```json
{
  "description": "description6",
  "id": "id6",
  "itemsIncluded": [
    "itemsIncluded9"
  ],
  "name": "name6",
  "price": {
    "currency": "currency2",
    "value": 203.04
  }
}
```

