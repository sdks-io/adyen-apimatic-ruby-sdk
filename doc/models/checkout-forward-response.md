
# Checkout Forward Response

## Structure

`CheckoutForwardResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_reference` | `String` | Optional | Merchant defined payment reference. |
| `psp_reference` | `String` | Optional | Adyen's 16-character reference associated with the transaction/request. This value is globally unique. Use this reference when you communicate with us about this request. |
| `response` | [`CheckoutForwardResponseFromUrl2`](../../doc/models/checkout-forward-response-from-url-2.md) | Required | The details of the response Adyen received from the third party. |
| `stored_payment_method_id` | `String` | Optional | The unique identifier of the token. |

## Example (as JSON)

```json
{
  "merchantReference": "merchantReference4",
  "pspReference": "pspReference6",
  "response": {
    "body": "body6",
    "headers": {
      "key0": "headers3",
      "key1": "headers4",
      "key2": "headers5"
    },
    "status": 110
  },
  "storedPaymentMethodId": "storedPaymentMethodId6"
}
```

