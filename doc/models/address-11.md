
# Address 11

The address details of the billing entity.

## Structure

`Address11`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `String` | Optional | The name of the city. |
| `company_name` | `String` | Optional | The name of the company. |
| `country` | `String` | Optional | The two-letter country code, in [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) format. |
| `postal_code` | `String` | Optional | The postal code. |
| `state_or_province` | `String` | Optional | The state or province as defined in [ISO 3166-2](https://www.iso.org/standard/72483.html). For example, **ON** for Ontario, Canada.<br><br>Applicable for the following countries:<br><br>- Australia<br>- Brazil<br>- Canada<br>- India<br>- Mexico<br>- New Zealand<br>- United States |
| `street_address` | `String` | Optional | The name of the street, and the house or building number. |
| `street_address_2` | `String` | Optional | Additional address details, if any. |

## Example (as JSON)

```json
{
  "city": "city4",
  "companyName": "companyName8",
  "country": "country0",
  "postalCode": "postalCode2",
  "stateOrProvince": "stateOrProvince6"
}
```

