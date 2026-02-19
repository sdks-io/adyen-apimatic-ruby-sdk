
# Offline Processing

## Structure

`OfflineProcessing`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `chip_floor_limit` | `Integer` | Optional | The maximum offline transaction amount for chip cards, in the processing currency and specified in [minor units](https://docs.adyen.com/development-resources/currency-codes). |
| `offline_swipe_limits` | [`Array[MinorUnitsMonetaryValue]`](../../doc/models/minor-units-monetary-value.md) | Optional | The maximum offline transaction amount for swiped cards, in the specified currency. |

## Example (as JSON)

```json
{
  "chipFloorLimit": 146,
  "offlineSwipeLimits": [
    {
      "amount": 136,
      "currencyCode": "currencyCode8"
    }
  ]
}
```

