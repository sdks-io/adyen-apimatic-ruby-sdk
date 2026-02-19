
# Offline Processing 1

Settings for [offline payment](https://docs.adyen.com/point-of-sale/offline-payments) features.

## Structure

`OfflineProcessing1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `chip_floor_limit` | `Integer` | Optional | The maximum offline transaction amount for chip cards, in the processing currency and specified in [minor units](https://docs.adyen.com/development-resources/currency-codes). |
| `offline_swipe_limits` | [`Array[MinorUnitsMonetaryValue]`](../../doc/models/minor-units-monetary-value.md) | Optional | The maximum offline transaction amount for swiped cards, in the specified currency. |

## Example (as JSON)

```json
{
  "chipFloorLimit": 218,
  "offlineSwipeLimits": [
    {
      "amount": 136,
      "currencyCode": "currencyCode8"
    },
    {
      "amount": 136,
      "currencyCode": "currencyCode8"
    }
  ]
}
```

