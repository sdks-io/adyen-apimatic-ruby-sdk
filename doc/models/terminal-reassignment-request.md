
# Terminal Reassignment Request

## Structure

`TerminalReassignmentRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `company_id` | `String` | Optional | The unique identifier of the company account to which the terminal is reassigned. |
| `inventory` | `TrueClass \| FalseClass` | Optional | Must be specified when reassigning terminals to a merchant account:<br><br>- If set to **true**, reassigns terminals to the inventory of the merchant account and the terminals cannot process transactions.<br><br>- If set to **false**, reassigns terminals directly to the merchant account and the terminals can process transactions. |
| `merchant_id` | `String` | Optional | The unique identifier of the merchant account to which the terminal is reassigned. When reassigning terminals to a merchant account, you must specify the `inventory` field. |
| `store_id` | `String` | Optional | The unique identifier of the store to which the terminal is reassigned. |

## Example (as JSON)

```json
{
  "companyId": "companyId0",
  "inventory": false,
  "merchantId": "merchantId6",
  "storeId": "storeId6"
}
```

