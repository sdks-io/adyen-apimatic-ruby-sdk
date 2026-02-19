
# Delivery Address 1

The address where the purchased goods should be delivered.

## Structure

`DeliveryAddress1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `String` | Required | The name of the city. Maximum length: 3000 characters.<br><br>**Constraints**: *Maximum Length*: `3000` |
| `country` | `String` | Required | The two-character ISO-3166-1 alpha-2 country code. For example, **US**.<br><br>> If you don't know the country or are not collecting the country from the shopper, provide `country` as `ZZ`. |
| `first_name` | `String` | Optional | - |
| `house_number_or_name` | `String` | Required | The number or name of the house. Maximum length: 3000 characters.<br><br>**Constraints**: *Maximum Length*: `3000` |
| `last_name` | `String` | Optional | - |
| `postal_code` | `String` | Required | A maximum of five digits for an address in the US, or a maximum of ten characters for an address in all other countries. |
| `state_or_province` | `String` | Optional | The two-character ISO 3166-2 state or province code. For example, **CA** in the US or **ON** in Canada.<br><br>> Required for the US and Canada.<br><br>**Constraints**: *Maximum Length*: `1000` |
| `street` | `String` | Required | The name of the street. Maximum length: 3000 characters.<br><br>> The house number should not be included in this field; it should be separately provided via `houseNumberOrName`.<br><br>**Constraints**: *Maximum Length*: `3000` |

## Example (as JSON)

```json
{
  "city": "city0",
  "country": "country4",
  "firstName": "firstName4",
  "houseNumberOrName": "houseNumberOrName8",
  "lastName": "lastName4",
  "postalCode": "postalCode8",
  "stateOrProvince": "stateOrProvince8",
  "street": "street0"
}
```

