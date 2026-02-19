
# Shopper Tax Info 2

The tax info of the shopper

## Structure

`ShopperTaxInfo2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tax_id` | `String` | Required | The tax-id of the shopper doing the transaction.<br><br>**Constraints**: *Maximum Length*: `10` |
| `tax_id_country_code` | `String` | Required | The country to which the tax-id belongs to.<br><br>**Constraints**: *Maximum Length*: `2` |

## Example (as JSON)

```json
{
  "taxId": "taxId6",
  "taxIdCountryCode": "taxIdCountryCode2"
}
```

