
# Encrypted Order Data 2

The order information required for partial payments.

## Structure

`EncryptedOrderData2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `order_data` | `String` | Required | The encrypted order data.<br><br>**Constraints**: *Maximum Length*: `5000` |
| `psp_reference` | `String` | Required | The `pspReference` that belongs to the order. |

## Example (as JSON)

```json
{
  "orderData": "orderData8",
  "pspReference": "pspReference8"
}
```

