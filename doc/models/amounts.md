
# Amounts

## Structure

`Amounts`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `currency` | `String` | Required | The three-character [ISO currency code](https://docs.adyen.com/development-resources/currency-codes/). |
| `values` | `Array[Integer]` | Required | The amounts of the donation (in [minor units](https://docs.adyen.com/development-resources/currency-codes/)). |

## Example (as JSON)

```json
{
  "currency": "currency0",
  "values": [
    214,
    213
  ]
}
```

