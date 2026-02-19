
# Stored Payment Method Resource

## Structure

`StoredPaymentMethodResource`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `brand` | `String` | Optional | The brand of the card. |
| `card_bin` | `String` | Optional | The bank identification number (BIN) of the card. |
| `expiry_month` | `String` | Optional | The month the card expires. |
| `expiry_year` | `String` | Optional | The last two digits of the year the card expires. For example, **22** for the year 2022. |
| `external_response_code` | `String` | Optional | The response code returned by an external system (for example after a provisioning operation). |
| `external_token_reference` | `String` | Optional | The token reference of a linked token in an external system (for example a network token reference). |
| `holder_name` | `String` | Optional | The unique payment method code. |
| `iban` | `String` | Optional | The IBAN of the bank account. |
| `id` | `String` | Optional | A unique identifier of this stored payment method. |
| `issuer_name` | `String` | Optional | The name of the issuer of token or card. |
| `last_four` | `String` | Optional | The last four digits of the PAN. |
| `mandate` | [`TokenMandate2`](../../doc/models/token-mandate-2.md) | Optional | Mandate details for the stored payment method. |
| `name` | `String` | Optional | The display name of the stored payment method. |
| `network_tx_reference` | `String` | Optional | Returned in the response if you are not tokenizing with Adyen and are using the Merchant-initiated transactions (MIT) framework from Mastercard or Visa.<br><br>This contains either the Mastercard Trace ID or the Visa Transaction ID. |
| `owner_name` | `String` | Optional | The name of the bank account holder. |
| `shopper_email` | `String` | Optional | The shopper’s email address. |
| `shopper_reference` | `String` | Optional | Your reference to uniquely identify this shopper, for example user ID or account ID. The value is case-sensitive and must be at least three characters.<br><br>> Your reference must not include personally identifiable information (PII) such as name or email address.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `256` |
| `supported_recurring_processing_models` | `Array[String]` | Optional | Defines a recurring payment type.<br>Allowed values:<br><br>* `Subscription` – A transaction for a fixed or variable amount, which follows a fixed schedule.<br>* `CardOnFile` – With a card-on-file (CoF) transaction, card details are stored to enable one-click or omnichannel journeys, or simply to streamline the checkout process. Any subscription not following a fixed schedule is also considered a card-on-file transaction.<br>* `UnscheduledCardOnFile` – An unscheduled card-on-file (UCoF) transaction is a transaction that occurs on a non-fixed schedule and/or have variable amounts. For example, automatic top-ups when a cardholder's balance drops below a certain amount. |
| `type` | `String` | Optional | The type of payment method. |

## Example (as JSON)

```json
{
  "brand": "brand0",
  "cardBin": "cardBin2",
  "expiryMonth": "expiryMonth0",
  "expiryYear": "expiryYear0",
  "externalResponseCode": "externalResponseCode0"
}
```

