
# Additional Commission

## Structure

`AdditionalCommission`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `balance_account_id` | `String` | Optional | Unique identifier of the balance account to which the additional commission is booked. |
| `fixed_amount` | `Integer` | Optional | A fixed commission fee, in minor units. |
| `variable_percentage` | `Integer` | Optional | A variable commission fee, in basis points. |

## Example (as JSON)

```json
{
  "balanceAccountId": "balanceAccountId8",
  "fixedAmount": 254,
  "variablePercentage": 166
}
```

