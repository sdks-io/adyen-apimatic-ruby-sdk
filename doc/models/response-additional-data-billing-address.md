
# Response Additional Data Billing Address

## Structure

`ResponseAdditionalDataBillingAddress`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `billing_address_city` | `String` | Optional | The billing address city passed in the payment request. |
| `billing_address_country` | `String` | Optional | The billing address country passed in the payment request.<br><br>Example: NL |
| `billing_address_house_number_or_name` | `String` | Optional | The billing address house number or name passed in the payment request. |
| `billing_address_postal_code` | `String` | Optional | The billing address postal code passed in the payment request.<br><br>Example: 1011 DJ |
| `billing_address_state_or_province` | `String` | Optional | The billing address state or province passed in the payment request.<br><br>Example: NH |
| `billing_address_street` | `String` | Optional | The billing address street passed in the payment request. |

## Example (as JSON)

```json
{
  "billingAddress.city": "billingAddress.city8",
  "billingAddress.country": "billingAddress.country2",
  "billingAddress.houseNumberOrName": "billingAddress.houseNumberOrName6",
  "billingAddress.postalCode": "billingAddress.postalCode4",
  "billingAddress.stateOrProvince": "billingAddress.stateOrProvince4"
}
```

