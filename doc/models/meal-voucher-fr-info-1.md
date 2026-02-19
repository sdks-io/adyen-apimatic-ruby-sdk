
# Meal Voucher Fr Info 1

Details to provide if `type` is **mealVoucher_FR**.

## Structure

`MealVoucherFrInfo1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `conecs_id` | `String` | Required | Meal Voucher conecsId. Format: digits only |
| `siret` | `String` | Required | Meal Voucher siret. Format: 14 digits.<br><br>**Constraints**: *Minimum Length*: `14`, *Maximum Length*: `14` |
| `sub_types` | `Array[String]` | Required | The list of additional payment methods. Allowed values: **mealVoucher_FR_edenred**, **mealVoucher_FR_groupeup**, **mealVoucher_FR_natixis**, **mealVoucher_FR_sodexo**. |

## Example (as JSON)

```json
{
  "conecsId": "conecsId4",
  "siret": "siret8",
  "subTypes": [
    "subTypes1",
    "subTypes2"
  ]
}
```

