
# Pay Pal Info

## Structure

`PayPalInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `direct_capture` | `TrueClass \| FalseClass` | Optional | Indicates if direct (immediate) capture for PayPal is enabled. If set to **true**, this setting overrides the [capture](https://docs.adyen.com/online-payments/capture) settings of your merchant account. Default value: **true**. |
| `payer_id` | `String` | Required | PayPal Merchant ID. Character length and limitations: 13 single-byte alphanumeric characters.<br><br>**Constraints**: *Minimum Length*: `13`, *Maximum Length*: `13` |
| `subject` | `String` | Required | Your business email address. |

## Example (as JSON)

```json
{
  "directCapture": false,
  "payerId": "payerId2",
  "subject": "subject0"
}
```

