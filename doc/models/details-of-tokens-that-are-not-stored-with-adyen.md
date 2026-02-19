
# Details of Tokens That Are Not Stored With Adyen

## Structure

`DetailsOfTokensThatAreNotStoredWithAdyen`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `expiry_month` | `String` | Optional | The card expiry month. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). |
| `expiry_year` | `String` | Optional | The card expiry year. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). |
| `holder_name` | `String` | Optional | The name of the card holder.<br><br>**Constraints**: *Maximum Length*: `15000` |
| `number` | `String` | Optional | The card number. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). |
| `stored_payment_method_id` | `String` | Required | Identifier used to fetch the token from the external service<br><br>**Constraints**: *Maximum Length*: `64` |
| `subtype` | `String` | Required, Constant | The external service from which to fetch the token. Supported only for specific companies. Contact Adyen if you want to use this feature.<br><br>**Value**: `'hilton'` |
| `type` | `String` | Required, Constant | The type of token. Allowed value: **externalToken**.<br><br>**Value**: `'externalToken'` |

## Example (as JSON)

```json
{
  "storedPaymentMethodId": "storedPaymentMethodId8",
  "subtype": "hilton",
  "type": "externalToken",
  "checkoutAttemptId": "checkoutAttemptId0",
  "expiryMonth": "expiryMonth8",
  "expiryYear": "expiryYear8",
  "holderName": "holderName0",
  "number": "number2"
}
```

