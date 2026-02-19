
# Payment Method Issuer

## Structure

`PaymentMethodIssuer`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `disabled` | `TrueClass \| FalseClass` | Optional | A boolean value indicating whether this issuer is unavailable. Can be `true` whenever the issuer is offline.<br><br>**Default**: `false` |
| `id` | `String` | Required | The unique identifier of this issuer, to submit in requests to /payments. |
| `name` | `String` | Required | A localized name of the issuer. |

## Example (as JSON)

```json
{
  "disabled": false,
  "id": "id2",
  "name": "name2"
}
```

