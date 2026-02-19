
# Standalone Payment Cancel Response

## Structure

`StandalonePaymentCancelResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_account` | `String` | Required | The merchant account that is used to process the payment. |
| `payment_reference` | `String` | Required | The [`reference`](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments__reqParam_reference) of the payment to cancel. |
| `psp_reference` | `String` | Required | Adyen's 16-character reference associated with the cancel request. |
| `reference` | `String` | Optional | Your reference for the cancel request. |
| `status` | `String` | Required, Constant | The status of your request. This will always have the value **received**.<br><br>**Value**: `'received'` |

## Example (as JSON)

```json
{
  "merchantAccount": "merchantAccount6",
  "paymentReference": "paymentReference2",
  "pspReference": "pspReference6",
  "status": "received",
  "reference": "reference2"
}
```

