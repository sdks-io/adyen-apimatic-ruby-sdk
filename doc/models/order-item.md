
# Order Item

## Structure

`OrderItem`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | The unique identifier of the product. |
| `installments` | `Integer` | Optional | The number of installments for the specified product `id`. |
| `name` | `String` | Optional | The name of the product. |
| `quantity` | `Integer` | Optional | The number of items with the specified product `id` included in the order. |

## Example (as JSON)

```json
{
  "id": "id2",
  "installments": 214,
  "name": "name2",
  "quantity": 32
}
```

