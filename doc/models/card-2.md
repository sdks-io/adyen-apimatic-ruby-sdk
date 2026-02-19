
# Card 2

The payment method used by the shopper.

## Structure

`Card2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `billing_sequence_number` | `String` | Optional | The sequence number for the debit. For example, send **2** if this is the second debit for the subscription. The sequence number is included in the notification sent to the shopper. |
| `brand` | `String` | Optional | Secondary brand of the card. For example: **plastix**, **hmclub**. |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `cupsecureplus_smscode` | `String` | Optional | - |
| `cvc` | `String` | Optional | The card verification code. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). |
| `encrypted_card` | `String` | Optional | Only include this for JSON Web Encryption (JWE) implementations. The JWE-encrypted card details.<br><br>**Constraints**: *Maximum Length*: `40000` |
| `encrypted_card_number` | `String` | Optional | The encrypted card number.<br><br>**Constraints**: *Maximum Length*: `15000` |
| `encrypted_expiry_month` | `String` | Optional | The encrypted card expiry month.<br><br>**Constraints**: *Maximum Length*: `15000` |
| `encrypted_expiry_year` | `String` | Optional | The encrypted card expiry year.<br><br>**Constraints**: *Maximum Length*: `15000` |
| `encrypted_password` | `String` | Optional | This field contains an encrypted, one-time password or an authentication code provided by the cardholder.<br><br>**Constraints**: *Maximum Length*: `15000` |
| `encrypted_security_code` | `String` | Optional | The encrypted card verification code.<br><br>**Constraints**: *Maximum Length*: `15000` |
| `expiry_month` | `String` | Optional | The card expiry month. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). |
| `expiry_year` | `String` | Optional | The card expiry year. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). |
| `fastlane_data` | `String` | Optional | The encoded fastlane data blob |
| `funding_source` | [`FundingSource`](../../doc/models/funding-source.md) | Optional | The funding source that should be used when multiple sources are available. For Brazilian combo cards, by default the funding source is credit. To use debit, set this value to **debit**. |
| `holder_name` | `String` | Optional | The name of the card holder.<br><br>**Constraints**: *Maximum Length*: `15000` |
| `network_payment_reference` | `String` | Optional | The transaction identifier from card schemes. This is the [`networkTxReference`](https://docs.adyen.com/api-explorer/Checkout/latest/post/payments#responses-200-additionalData-ResponseAdditionalDataCommon-networkTxReference) from the response to the first payment. |
| `number` | `String` | Optional | The card number. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). |
| `recurring_detail_reference` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `shopper_notification_reference` | `String` | Optional | The `shopperNotificationReference` returned in the response when you requested to notify the shopper. Used only for recurring payments in India. |
| `src_correlation_id` | `String` | Optional | An identifier used for the Click to Pay transaction. |
| `src_digital_card_id` | `String` | Optional | The SRC reference for the Click to Pay token. |
| `src_scheme` | `String` | Optional | The scheme that is being used for Click to Pay. |
| `src_token_reference` | `String` | Optional | The reference for the Click to Pay token. |
| `stored_payment_method_id` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` |
| `three_ds_2_sdk_version` | `String` | Optional | Required for mobile integrations. Version of the 3D Secure 2 mobile SDK.<br><br>**Constraints**: *Maximum Length*: `12` |
| `type` | [`Type12`](../../doc/models/type-12.md) | Optional | Default payment method details. Common for scheme payment methods, and for simple payment method details.<br><br>**Default**: `Type12::SCHEME` |

## Example (as JSON)

```json
{
  "type": "scheme",
  "billingSequenceNumber": "billingSequenceNumber8",
  "brand": "brand2",
  "checkoutAttemptId": "checkoutAttemptId4",
  "cupsecureplus.smscode": "cupsecureplus.smscode6",
  "cvc": "cvc2"
}
```

