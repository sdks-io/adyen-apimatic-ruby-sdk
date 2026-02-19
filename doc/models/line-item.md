
# Line Item

## Structure

`LineItem`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount_excluding_tax` | `Integer` | Optional | Item amount excluding the tax, in [minor units](https://docs.adyen.com/development-resources/currency-codes/#minor-units). |
| `amount_including_tax` | `Integer` | Optional | Item amount including the tax, in [minor units](https://docs.adyen.com/development-resources/currency-codes/#minor-units). |
| `brand` | `String` | Optional | Brand of the item. |
| `color` | `String` | Optional | Color of the item. |
| `description` | `String` | Optional | Description of the line item.<br><br>**Constraints**: *Maximum Length*: `10000` |
| `id` | `String` | Optional | ID of the line item. |
| `image_url` | `String` | Optional | Link to the picture of the purchased item. |
| `item_category` | `String` | Optional | Item category, used by the payment methods PayPal and Ratepay. |
| `manufacturer` | `String` | Optional | Manufacturer of the item. |
| `marketplace_seller_id` | `String` | Optional | Marketplace seller id. |
| `product_url` | `String` | Optional | Link to the purchased item. |
| `quantity` | `Integer` | Optional | Number of items. |
| `receiver_email` | `String` | Optional | Email associated with the given product in the basket (usually in electronic gift cards). |
| `size` | `String` | Optional | Size of the item. |
| `sku` | `String` | Optional | Stock keeping unit. |
| `tax_amount` | `Integer` | Optional | Tax amount, in [minor units](https://docs.adyen.com/development-resources/currency-codes/#minor-units). |
| `tax_percentage` | `Integer` | Optional | Tax percentage, represented as a [basis point](https://en.wikipedia.org/wiki/Basis_point) integer. For example:<br><br>- **530** for 5.3% (five point three percent)<br>- **2100** for 21% (twenty-one percent) |
| `upc` | `String` | Optional | Universal Product Code. |

## Example (as JSON)

```json
{
  "amountExcludingTax": 36,
  "amountIncludingTax": 146,
  "brand": "brand0",
  "color": "color0",
  "description": "description6"
}
```

