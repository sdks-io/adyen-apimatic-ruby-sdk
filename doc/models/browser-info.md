
# Browser Info

## Structure

`BrowserInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accept_header` | `String` | Required | The accept header value of the shopper's browser. |
| `color_depth` | `Integer` | Required | The color depth of the shopper's browser in bits per pixel. This should be obtained by using the browser's `screen.colorDepth` property. Accepted values: 1, 4, 8, 15, 16, 24, 30, 32 or 48 bit color depth. |
| `java_enabled` | `TrueClass \| FalseClass` | Required | Boolean value indicating if the shopper's browser is able to execute Java. |
| `java_script_enabled` | `TrueClass \| FalseClass` | Optional | Boolean value indicating if the shopper's browser is able to execute JavaScript. A default 'true' value is assumed if the field is not present.<br><br>**Default**: `true` |
| `language` | `String` | Required | The `navigator.language` value of the shopper's browser (as defined in IETF BCP 47). |
| `screen_height` | `Integer` | Required | The total height of the shopper's device screen in pixels. |
| `screen_width` | `Integer` | Required | The total width of the shopper's device screen in pixels. |
| `time_zone_offset` | `Integer` | Required | Time difference between UTC time and the shopper's browser local time, in minutes. |
| `user_agent` | `String` | Required | The user agent value of the shopper's browser. |

## Example (as JSON)

```json
{
  "acceptHeader": "acceptHeader0",
  "colorDepth": 240,
  "javaEnabled": false,
  "javaScriptEnabled": true,
  "language": "language4",
  "screenHeight": 10,
  "screenWidth": 246,
  "timeZoneOffset": 42,
  "userAgent": "userAgent8"
}
```

