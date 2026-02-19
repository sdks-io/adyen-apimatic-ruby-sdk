
# Additional Commission 1

Defines whether to book an additional commission for payments to your user's balance account. The commission amount can be defined as a fixed amount (specified in minor units), a percentage (specified in basis points), or both.

## Structure

`AdditionalCommission1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `balance_account_id` | `String` | Optional | Unique identifier of the balance account to which the additional commission is booked. |
| `fixed_amount` | `Integer` | Optional | A fixed commission fee, in minor units. |
| `variable_percentage` | `Integer` | Optional | A variable commission fee, in basis points. |

## Example (as JSON)

```json
{
  "balanceAccountId": "balanceAccountId0",
  "fixedAmount": 246,
  "variablePercentage": 154
}
```

