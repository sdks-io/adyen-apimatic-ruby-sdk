
# Receipt Printing 1

Transaction outcomes that you want the terminal to print a merchant receipt or a shopper receipt for.

## Structure

`ReceiptPrinting1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_approved` | `TrueClass \| FalseClass` | Optional | Print a merchant receipt when the payment is approved. |
| `merchant_cancelled` | `TrueClass \| FalseClass` | Optional | Print a merchant receipt when the transaction is cancelled. |
| `merchant_capture_approved` | `TrueClass \| FalseClass` | Optional | Print a merchant receipt when capturing the payment is approved. |
| `merchant_capture_refused` | `TrueClass \| FalseClass` | Optional | Print a merchant receipt when capturing the payment is refused. |
| `merchant_refund_approved` | `TrueClass \| FalseClass` | Optional | Print a merchant receipt when the refund is approved. |
| `merchant_refund_refused` | `TrueClass \| FalseClass` | Optional | Print a merchant receipt when the refund is refused. |
| `merchant_refused` | `TrueClass \| FalseClass` | Optional | Print a merchant receipt when the payment is refused. |
| `merchant_void` | `TrueClass \| FalseClass` | Optional | Print a merchant receipt when a previous transaction is voided. |
| `shopper_approved` | `TrueClass \| FalseClass` | Optional | Print a shopper receipt when the payment is approved. |
| `shopper_cancelled` | `TrueClass \| FalseClass` | Optional | Print a shopper receipt when the transaction is cancelled. |
| `shopper_capture_approved` | `TrueClass \| FalseClass` | Optional | Print a shopper receipt when capturing the payment is approved. |
| `shopper_capture_refused` | `TrueClass \| FalseClass` | Optional | Print a shopper receipt when capturing the payment is refused. |
| `shopper_refund_approved` | `TrueClass \| FalseClass` | Optional | Print a shopper receipt when the refund is approved. |
| `shopper_refund_refused` | `TrueClass \| FalseClass` | Optional | Print a shopper receipt when the refund is refused. |
| `shopper_refused` | `TrueClass \| FalseClass` | Optional | Print a shopper receipt when the payment is refused. |
| `shopper_void` | `TrueClass \| FalseClass` | Optional | Print a shopper receipt when a previous transaction is voided. |

## Example (as JSON)

```json
{
  "merchantApproved": false,
  "merchantCancelled": false,
  "merchantCaptureApproved": false,
  "merchantCaptureRefused": false,
  "merchantRefundApproved": false
}
```

