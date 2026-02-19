
# Payment Method to Store 1

Contains the information required to store a payment method.

## Structure

`PaymentMethodToStore1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `brand` | `String` | Optional | Secondary brand of the card. For example: **plastix**, **hmclub**. |
| `cvc` | `String` | Optional | The card verification code. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). |
| `encrypted_card` | `String` | Optional | The encrypted card.<br><br>**Constraints**: *Maximum Length*: `40000` |
| `encrypted_card_number` | `String` | Optional | The encrypted card number.<br><br>**Constraints**: *Maximum Length*: `15000` |
| `encrypted_expiry_month` | `String` | Optional | The encrypted card expiry month.<br><br>**Constraints**: *Maximum Length*: `15000` |
| `encrypted_expiry_year` | `String` | Optional | The encrypted card expiry year.<br><br>**Constraints**: *Maximum Length*: `15000` |
| `encrypted_security_code` | `String` | Optional | The encrypted card verification code.<br><br>**Constraints**: *Maximum Length*: `15000` |
| `expiry_month` | `String` | Optional | The card expiry month. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). |
| `expiry_year` | `String` | Optional | The card expiry year. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). |
| `holder_name` | `String` | Optional | The name of the card holder. |
| `number` | `String` | Optional | The card number. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). |
| `type` | `String` | Optional | Set to **scheme**. |

## Example (as JSON)

```json
{
  "brand": "brand2",
  "cvc": "cvc2",
  "encryptedCard": "encryptedCard0",
  "encryptedCardNumber": "encryptedCardNumber6",
  "encryptedExpiryMonth": "encryptedExpiryMonth4"
}
```

