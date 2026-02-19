
# Checkout Forward Request

## Structure

`CheckoutForwardRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `base_url` | `String` | Required | The base URL of the third party API, where Adyen will send the request to forward the payment details. |
| `merchant_account` | `String` | Required | Your merchant account. |
| `merchant_reference` | `String` | Optional | Merchant defined payment reference. |
| `options` | [`CheckoutForwardRequestOptions2`](../../doc/models/checkout-forward-request-options-2.md) | Optional | The customizations that can be applied when making a forward request. |
| `payment_method` | [`CheckoutForwardRequestCard2`](../../doc/models/checkout-forward-request-card-2.md) | Optional | The card details. |
| `request` | [`CheckoutOutgoingForwardRequest2`](../../doc/models/checkout-outgoing-forward-request-2.md) | Required | The [details of the request](https://docs.adyen.com/online-payments/tokenization/forward-payment-details#request-to-adyen-card) that you want to forward to the third-party. |
| `shopper_reference` | `String` | Required | Your reference to uniquely identify this shopper, for example user ID or account ID. The value is case-sensitive and must be at least three characters.<br><br>> Your reference must not include personally identifiable information (PII) such as name or email address. |
| `stored_payment_method_id` | `String` | Optional | The unique identifier of the token that you want to forward to the third party. This is the `storedPaymentMethodId` you received in the webhook after you created the token. |

## Example (as JSON)

```json
{
  "baseUrl": "baseUrl6",
  "merchantAccount": "merchantAccount0",
  "merchantReference": "merchantReference2",
  "options": {
    "accountUpdate": false,
    "dryRun": false,
    "networkToken": {
      "includeCryptogram": false,
      "useNetworkToken": false
    },
    "networkTxReferencePaths": [
      "networkTxReferencePaths7"
    ],
    "tokenize": false
  },
  "paymentMethod": {
    "cvc": "cvc6",
    "encryptedCardNumber": "encryptedCardNumber0",
    "encryptedExpiryMonth": "encryptedExpiryMonth2",
    "encryptedExpiryYear": "encryptedExpiryYear2",
    "encryptedSecurityCode": "encryptedSecurityCode2"
  },
  "request": {
    "body": "body2",
    "credentials": "credentials0",
    "headers": {
      "key0": "headers9"
    },
    "httpMethod": "post",
    "urlSuffix": "urlSuffix2"
  },
  "shopperReference": "shopperReference6",
  "storedPaymentMethodId": "storedPaymentMethodId2"
}
```

