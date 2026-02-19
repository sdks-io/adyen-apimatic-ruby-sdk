
# Settings 1

General Wi-Fi settings.

## Structure

`Settings1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `band` | `String` | Optional | The preferred Wi-Fi band, for use if the terminals support multiple bands. Possible values: All, 2.4GHz, 5GHz. |
| `roaming` | `TrueClass \| FalseClass` | Optional | Indicates whether roaming is enabled on the terminals. |
| `timeout` | `Integer` | Optional | The connection time-out in seconds. Minimum value: 0. |

## Example (as JSON)

```json
{
  "band": "band6",
  "roaming": false,
  "timeout": 230
}
```

