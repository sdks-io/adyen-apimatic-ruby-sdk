
# Android App

## Structure

`AndroidApp`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Optional | The description that was provided when uploading the app. The description is not shown on the terminal. |
| `error_code` | `String` | Optional | The error code of the Android app with the `status` of either **error** or **invalid**. |
| `errors` | [`Array[AndroidAppError]`](../../doc/models/android-app-error.md) | Optional | The list of errors of the Android app. |
| `id` | `String` | Required | The unique identifier of the app. |
| `label` | `String` | Optional | The app name that is shown on the terminal. |
| `package_name` | `String` | Optional | The package name that uniquely identifies the Android app. |
| `status` | [`Status5`](../../doc/models/status-5.md) | Required | The status of the app. Possible values:<br><br>* `processing`: the app is being signed and converted to a format that the terminal can handle.<br>* `error`: something went wrong. Check that the app matches the [requirements](https://docs.adyen.com/point-of-sale/android-terminals/app-requirements).<br>* `invalid`: there is something wrong with the APK file of the app.<br>* `ready`: the app has been signed and converted.<br>* `archived`: the app is no longer available. |
| `version_code` | `Integer` | Optional | The version number of the app. |
| `version_name` | `String` | Optional | The app version number that is shown on the terminal. |

## Example (as JSON)

```json
{
  "description": "description0",
  "errorCode": "errorCode6",
  "errors": [
    {
      "errorCode": "errorCode6",
      "terminalModels": [
        "terminalModels3",
        "terminalModels4"
      ]
    },
    {
      "errorCode": "errorCode6",
      "terminalModels": [
        "terminalModels3",
        "terminalModels4"
      ]
    }
  ],
  "id": "id0",
  "label": "label0",
  "packageName": "packageName6",
  "status": "invalid"
}
```

