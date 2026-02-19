
# Kiosk Mode Settings 1

Settings for kiosk mode.

## Structure

`KioskModeSettings1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allowed_apps_in_kiosk_mode` | `Array[String]` | Optional | List of package names for apps allowed to run in kiosk mode. |
| `kiosk_app_on_startup` | `String` | Optional | The package name of the app to launch on startup. This must be one of the apps included in `allowedAppsInKioskMode`. |

## Example (as JSON)

```json
{
  "allowedAppsInKioskMode": [
    "allowedAppsInKioskMode2",
    "allowedAppsInKioskMode1",
    "allowedAppsInKioskMode0"
  ],
  "kioskAppOnStartup": "kioskAppOnStartup2"
}
```

