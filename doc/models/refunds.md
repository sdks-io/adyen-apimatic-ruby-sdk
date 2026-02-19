
# Refunds

## Structure

`Refunds`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `referenced` | [`Referenced1`](../../doc/models/referenced-1.md) | Optional | Settings for referenced refunds. |
| `unreferenced` | [`Unreferenced2`](../../doc/models/unreferenced-2.md) | Optional | Settings for unreferenced refunds. |

## Example (as JSON)

```json
{
  "referenced": {
    "enableStandaloneRefunds": false
  },
  "unreferenced": {
    "enableUnreferencedRefunds": false
  }
}
```

