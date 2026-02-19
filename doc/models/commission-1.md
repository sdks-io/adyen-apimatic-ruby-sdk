
# Commission 1

Defines your platform's commission for the processed payments as a fixed amount (specified in minor units), a percentage (specified in basis points), or both. The commission is booked to your platform's liable balance account.

## Structure

`Commission1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `fixed_amount` | `Integer` | Optional | A fixed commission fee, in minor units. |
| `variable_percentage` | `Integer` | Optional | A variable commission fee, in basis points. |

## Example (as JSON)

```json
{
  "fixedAmount": 100,
  "variablePercentage": 64
}
```

