
# Klarna Info

## Structure

`KlarnaInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auto_capture` | `TrueClass \| FalseClass` | Optional | Indicates the status of [Automatic capture](https://docs.adyen.com/online-payments/capture#automatic-capture). Default value: **false**. |
| `dispute_email` | `String` | Required | The email address for disputes. |
| `region` | [`Region`](../../doc/models/region.md) | Required | The region of operation. For example, **NA**, **EU**, **CH**, **AU**.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `2` |
| `support_email` | `String` | Required | The email address of merchant support. |

## Example (as JSON)

```json
{
  "autoCapture": false,
  "disputeEmail": "disputeEmail8",
  "region": "CH",
  "supportEmail": "supportEmail2"
}
```

