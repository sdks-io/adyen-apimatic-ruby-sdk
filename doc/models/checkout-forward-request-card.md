
# Checkout Forward Request Card

## Structure

`CheckoutForwardRequestCard`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cvc` | `String` | Optional | The [card verification code](https://docs.adyen.com/payments-fundamentals/payment-glossary#card-security-code-cvc-cvv-cid) (1-20 characters). Depending on the card brand, it is also known as:<br><br>* CVV2/CVC2 – length: 3 digits<br>* CID – length: 4 digits |
| `encrypted_card_number` | `String` | Optional | The encrypted card number. |
| `encrypted_expiry_month` | `String` | Optional | The encrypted expiryMonth |
| `encrypted_expiry_year` | `String` | Optional | The encrypted card expiry year. |
| `encrypted_security_code` | `String` | Optional | The encrypted security code. |
| `expiry_month` | `String` | Optional | The card expiry month.<br>Format: 2 digits, zero-padded for single digits. For example:<br><br>* 03 = March<br>* 11 = November |
| `expiry_year` | `String` | Optional | The card expiry year. |
| `holder_name` | `String` | Optional | The name of the cardholder. |
| `number` | `String` | Optional | The card number. Only collect raw card data if you are fully [PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide).<br>Format: Do not use separators. |
| `type` | [`Type16`](../../doc/models/type-16.md) | Optional | Default payment method details. Common for scheme payment methods, and for simple payment method details.<br><br>**Default**: `Type16::SCHEME` |

## Example (as JSON)

```json
{
  "type": "scheme",
  "cvc": "cvc4",
  "encryptedCardNumber": "encryptedCardNumber8",
  "encryptedExpiryMonth": "encryptedExpiryMonth6",
  "encryptedExpiryYear": "encryptedExpiryYear0",
  "encryptedSecurityCode": "encryptedSecurityCode6"
}
```

