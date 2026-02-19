
# Forex Quote

## Structure

`ForexQuote`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account` | `String` | Optional | The account name. |
| `account_type` | `String` | Optional | The account type. |
| `base_amount` | [`Amount3`](../../doc/models/amount-3.md) | Optional | The base amount. |
| `base_points` | `Integer` | Required | The base points. |
| `buy` | [`Amount4`](../../doc/models/amount-4.md) | Optional | The buy rate. |
| `interbank` | [`Amount5`](../../doc/models/amount-5.md) | Optional | The interbank amount. |
| `reference` | `String` | Optional | The reference assigned to the forex quote request. |
| `sell` | [`Amount6`](../../doc/models/amount-6.md) | Optional | The sell rate. |
| `signature` | `String` | Optional | The signature to validate the integrity. |
| `source` | `String` | Optional | The source of the forex quote. |
| `type` | `String` | Optional | The type of forex. |
| `valid_till` | `DateTime` | Required | The date until which the forex quote is valid. |

## Example (as JSON)

```json
{
  "account": "account6",
  "accountType": "accountType6",
  "baseAmount": {
    "currency": "currency8",
    "value": 202
  },
  "basePoints": 52,
  "buy": {
    "currency": "currency2",
    "value": 72
  },
  "interbank": {
    "currency": "currency4",
    "value": 244
  },
  "validTill": "2016-03-13T12:52:32.123Z"
}
```

