
# Install Android App Details

## Structure

`InstallAndroidAppDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_id` | `String` | Optional | The unique identifier of the app to be installed. |
| `type` | [`Type27`](../../doc/models/type-27.md) | Optional | Type of terminal action: Install an Android app.<br><br>**Default**: `Type27::INSTALLANDROIDAPP` |

## Example (as JSON)

```json
{
  "type": "InstallAndroidApp",
  "appId": "appId6"
}
```

