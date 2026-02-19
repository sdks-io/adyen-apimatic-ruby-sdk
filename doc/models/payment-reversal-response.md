
# Payment Reversal Response

## Structure

`PaymentReversalResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_account` | `String` | Required | The merchant account that is used to process the payment. |
| `payment_psp_reference` | `String` | Required | The [`pspReference`](https://docs.adyen.com/api-explorer/Checkout/latest/post/payments#responses-200-pspReference) of the payment to reverse. |
| `psp_reference` | `String` | Required | Adyen's 16-character reference associated with the reversal request. |
| `reference` | `String` | Optional | Your reference for the reversal request. |
| `status` | `String` | Required, Constant | The status of your request. This will always have the value **received**.<br><br>**Value**: `'received'` |

## Example (as JSON)

```json
{
  "merchantAccount": "merchantAccount4",
  "paymentPspReference": "paymentPspReference0",
  "pspReference": "pspReference6",
  "status": "received",
  "reference": "reference2"
}
```

