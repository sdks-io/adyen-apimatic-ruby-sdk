
# Response Additional Data Card

## Structure

`ResponseAdditionalDataCard`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `card_bin` | `String` | Optional | The first six digits of the card number.<br><br>This is the [Bank Identification Number (BIN)](https://docs.adyen.com/get-started-with-adyen/payment-glossary#bank-identification-number-bin) for card numbers with a six-digit BIN.<br><br>Example: 521234 |
| `card_holder_name` | `String` | Optional | The cardholder name passed in the payment request. |
| `card_issuing_bank` | `String` | Optional | The bank or the financial institution granting lines of credit through card association branded payment cards. This information can be included when available. |
| `card_issuing_country` | `String` | Optional | The country where the card was issued.<br><br>Example: US |
| `card_issuing_currency` | `String` | Optional | The currency in which the card is issued, if this information is available. Provided as the currency code or currency number from the ISO-4217 standard.<br><br>Example: USD |
| `card_payment_method` | `String` | Optional | The card payment method used for the transaction.<br><br>Example: amex |
| `card_product_id` | [`CardProductId`](../../doc/models/card-product-id.md) | Optional | The Card Product ID represents the type of card following card scheme product definitions and can be returned for Adyen Acquiring service level payments.<br><br>Possible values Visa:<br><br>* **A** - Visa Traditional<br>* **B** - Visa Traditional Rewards<br>* **C** - Visa Signature<br>* **D** - Visa Signature Preferred<br>* **F** - Visa Classic<br><br>Possible values Mastercard:<br><br>* **MCC** - Mastercard Card<br>* **MCE** - Mastercard Electronic Card<br>* **MCF** - Mastercard Corporate Fleet Card<br>* **MCG** - Gold Mastercard Card<br>* **MCH** - Mastercard Premium Charge<br>* **MCI** - Mastercard Select Debit |
| `card_summary` | `String` | Optional | The last four digits of a card number.<br><br>> Returned only in case of a card payment. |
| `issuer_bin` | `String` | Optional | The first eight digits of the card number. Only returned if the card number is 16 digits or more.<br><br>This is the [Bank Identification Number (BIN)](https://docs.adyen.com/get-started-with-adyen/payment-glossary#bank-identification-number-bin) for card numbers with an eight-digit BIN.<br><br>Example: 52123423 |

## Example (as JSON)

```json
{
  "cardBin": "cardBin4",
  "cardHolderName": "cardHolderName2",
  "cardIssuingBank": "cardIssuingBank4",
  "cardIssuingCountry": "cardIssuingCountry4",
  "cardIssuingCurrency": "cardIssuingCurrency2"
}
```

