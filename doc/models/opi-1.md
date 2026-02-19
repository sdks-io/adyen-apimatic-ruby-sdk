
# Opi 1

Settings for an Oracle Payment Interface (OPI) integration.

## Structure

`Opi1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enable_pay_at_table` | `TrueClass \| FalseClass` | Optional | Indicates if Pay at table is enabled. |
| `pay_at_table_store_number` | `String` | Optional | The store number to use for Pay at Table. |
| `pay_at_table_url` | `String` | Optional | The URL and port number used for Pay at Table communication. |

## Example (as JSON)

```json
{
  "enablePayAtTable": false,
  "payAtTableStoreNumber": "payAtTableStoreNumber6",
  "payAtTableURL": "payAtTableURL6"
}
```

