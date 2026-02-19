
# Valuelink Info 1

Details to provide if `type` is **valuelink**.

## Structure

`ValuelinkInfo1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorisation_mid` | `String` | Required | Authorisation Mid |
| `pin_support` | [`PinSupport`](../../doc/models/pin-support.md) | Required | PIN Support. For ecommerce, PIN is required. |
| `submitter_id` | `String` | Optional | Submitter ID |
| `terminal_id` | `String` | Optional | Terminal ID |

## Example (as JSON)

```json
{
  "authorisationMid": "authorisationMid8",
  "pinSupport": "PIN",
  "submitterId": "submitterId4",
  "terminalId": "terminalId0"
}
```

