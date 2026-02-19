
# Supported Card Types 2

The type of card for which the terminal accepts store-and-forward payments. You can specify multiple card types.

## Structure

`SupportedCardTypes2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `credit` | `TrueClass \| FalseClass` | Optional | Set to **true** to accept credit cards. |
| `debit` | `TrueClass \| FalseClass` | Optional | Set to **true** to accept debit cards. |
| `deferred_debit` | `TrueClass \| FalseClass` | Optional | Set to **true** to accept cards that allow deferred debit. |
| `prepaid` | `TrueClass \| FalseClass` | Optional | Set to **true** to accept prepaid cards. |
| `unknown` | `TrueClass \| FalseClass` | Optional | Set to **true** to accept card types for which the terminal can't determine the funding source while offline. |

## Example (as JSON)

```json
{
  "credit": false,
  "debit": false,
  "deferredDebit": false,
  "prepaid": false,
  "unknown": false
}
```

