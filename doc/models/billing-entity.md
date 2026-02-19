
# Billing Entity

## Structure

`BillingEntity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `address` | [`Address11`](../../doc/models/address-11.md) | Optional | The address details of the billing entity. |
| `email` | `String` | Optional | The email address of the billing entity. |
| `id` | `String` | Optional | The unique identifier of the billing entity, for use as `billingEntityId` when creating an order. |
| `name` | `String` | Optional | The unique name of the billing entity. |
| `tax_id` | `String` | Optional | The tax number of the billing entity. |

## Example (as JSON)

```json
{
  "address": {
    "city": "city6",
    "companyName": "companyName8",
    "country": "country0",
    "postalCode": "postalCode8",
    "stateOrProvince": "stateOrProvince4"
  },
  "email": "email6",
  "id": "id0",
  "name": "name0",
  "taxId": "taxId6"
}
```

