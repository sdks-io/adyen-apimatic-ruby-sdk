
# Standalone

## Structure

`Standalone`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `currency_code` | `String` | Optional | The default currency of the standalone payment terminal as an [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217) currency code.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `3` |
| `enable_gratuities` | `TrueClass \| FalseClass` | Optional | Indicates whether the tipping options specified in `gratuities` are enabled on the standalone terminal. |
| `enable_standalone` | `TrueClass \| FalseClass` | Optional | Enable standalone mode. |

## Example (as JSON)

```json
{
  "currencyCode": "currencyCode2",
  "enableGratuities": false,
  "enableStandalone": false
}
```

