
# Notification 2

Configures sending event notifications by pressing a button on a terminal, for example used for pay-at-table.

## Structure

`Notification2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `category` | [`Category`](../../doc/models/category.md) | Optional | The type of event notification sent when you select the notification button. |
| `details` | `String` | Optional | The text shown in the prompt which opens when you select the notification button. For example, the description of the input box for pay-at-table. |
| `enabled` | `TrueClass \| FalseClass` | Optional | Enables sending event notifications either by pressing the Confirm key on terminals with a keypad or by tapping the event notification button on the terminal screen. |
| `show_button` | `TrueClass \| FalseClass` | Optional | Shows or hides the event notification button on the screen of terminal models that have a keypad. |
| `title` | `String` | Optional | The name of the notification button on the terminal screen. |

## Example (as JSON)

```json
{
  "category": "SaleWakeUp",
  "details": "details8",
  "enabled": false,
  "showButton": false,
  "title": "title6"
}
```

