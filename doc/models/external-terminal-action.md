
# External Terminal Action

## Structure

`ExternalTerminalAction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action_type` | `String` | Optional | The type of terminal action: **InstallAndroidApp**, **UninstallAndroidApp**, **InstallAndroidCertificate**, or **UninstallAndroidCertificate**. |
| `config` | `String` | Optional | Technical information about the terminal action. |
| `confirmed_at` | `DateTime` | Optional | The date and time when the action was carried out. |
| `id` | `String` | Optional | The unique ID of the terminal action. |
| `result` | `String` | Optional | The result message for the action. |
| `scheduled_at` | `DateTime` | Optional | The date and time when the action was scheduled to happen. |
| `status` | `String` | Optional | The status of the terminal action: **pending**, **successful**, **failed**, **cancelled**, or **tryLater**. |
| `terminal_id` | `String` | Optional | The unique ID of the terminal that the action applies to. |

## Example (as JSON)

```json
{
  "actionType": "actionType6",
  "config": "config2",
  "confirmedAt": "2016-03-13T12:52:32.123Z",
  "id": "id6",
  "result": "result0"
}
```

