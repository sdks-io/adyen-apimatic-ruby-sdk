
# Create Order Request

## Structure

`CreateOrderRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | [`Amount20`](../../doc/models/amount-20.md) | Required | The total amount of the order. |
| `expires_at` | `String` | Optional | The date when the order should expire. If not provided, the default expiry duration is 1 day.<br><br>[ISO 8601](https://www.w3.org/TR/NOTE-datetime) format: YYYY-MM-DDThh:mm:ss+TZD, for example, **2020-12-18T10:15:30+01:00**. |
| `merchant_account` | `String` | Required | The merchant account identifier, with which you want to process the order. |
| `reference` | `String` | Required | A custom reference identifying the order. |

## Example (as JSON)

```json
{
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "expiresAt": "expiresAt4",
  "merchantAccount": "merchantAccount0",
  "reference": "reference4"
}
```

