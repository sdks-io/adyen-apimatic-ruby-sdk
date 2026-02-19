
# Store Location 1

The address of the store.

## Structure

`StoreLocation1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `String` | Optional | The name of the city. |
| `country` | `String` | Required | The two-letter country code in [ISO_3166-1_alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) format. |
| `line_1` | `String` | Optional | The street address. |
| `line_2` | `String` | Optional | Second address line. |
| `line_3` | `String` | Optional | Third address line. |
| `postal_code` | `String` | Optional | The postal code. |
| `state_or_province` | `String` | Optional | The state or province code as defined in [ISO 3166-2](https://www.iso.org/standard/72483.html). For example, **ON** for Ontario, Canada.<br><br>Required for the following countries:<br><br>- Australia<br>- Brazil<br>- Canada<br>- India<br>- Mexico<br>- New Zealand<br>- United States |

## Example (as JSON)

```json
{
  "city": "city0",
  "country": "country4",
  "line1": "line12",
  "line2": "line24",
  "line3": "line32",
  "postalCode": "postalCode8"
}
```

