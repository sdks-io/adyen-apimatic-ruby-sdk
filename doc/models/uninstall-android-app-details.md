
# Uninstall Android App Details

*This model accepts additional fields of type Object.*

## Structure

`UninstallAndroidAppDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_id` | `String` | Optional | The unique identifier of the app to be uninstalled. |
| `type` | [`Type61`](../../doc/models/type-61.md) | Optional | Type of terminal action: Uninstall an Android app.<br><br>**Default**: `Type61::UNINSTALLANDROIDAPP` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "UninstallAndroidApp",
  "appId": "appId0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

