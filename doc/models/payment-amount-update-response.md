
# Payment Amount Update Response

## Structure

`PaymentAmountUpdateResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | [`Amount29`](../../doc/models/amount-29.md) | Required | The updated amount. |
| `industry_usage` | [`IndustryUsage1`](../../doc/models/industry-usage-1.md) | Optional | The reason for the amount update. Possible values:<br><br>* **delayedCharge**<br>* **noShow**<br>* **installment** |
| `line_items` | [`Array[LineItem]`](../../doc/models/line-item.md) | Optional | Price and product information of the refunded items, required for [partial refunds](https://docs.adyen.com/online-payments/refund#refund-a-payment).<br><br>> This field is required for partial refunds with 3x 4x Oney, Affirm, Afterpay, Atome, Clearpay, Klarna, Ratepay, Walley, and Zip. |
| `merchant_account` | `String` | Required | The merchant account that is used to process the payment. |
| `payment_psp_reference` | `String` | Required | The [`pspReference`](https://docs.adyen.com/api-explorer/Checkout/latest/post/payments#responses-200-pspReference) of the payment to update. |
| `psp_reference` | `String` | Required | Adyen's 16-character reference associated with the amount update request. |
| `reference` | `String` | Required | Your reference for the amount update request. Maximum length: 80 characters. |
| `splits` | [`Array[Split]`](../../doc/models/split.md) | Optional | An array of objects specifying how the amount should be split between accounts when using Adyen for Platforms. For more information, see how to process payments for [marketplaces](https://docs.adyen.com/marketplaces/process-payments) or [platforms](https://docs.adyen.com/platforms/process-payments). |
| `status` | `String` | Required, Constant | The status of your request. This will always have the value **received**.<br><br>**Value**: `'received'` |

## Example (as JSON)

```json
{
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "merchantAccount": "merchantAccount8",
  "paymentPspReference": "paymentPspReference4",
  "pspReference": "pspReference8",
  "reference": "reference2",
  "status": "received",
  "industryUsage": "delayedCharge",
  "lineItems": [
    {
      "amountExcludingTax": 38,
      "amountIncludingTax": 148,
      "brand": "brand6",
      "color": "color6",
      "description": "description2"
    }
  ],
  "splits": [
    {
      "account": "account2",
      "amount": {
        "currency": "currency2",
        "value": 110
      },
      "description": "description2",
      "reference": "reference2",
      "type": "Default"
    }
  ]
}
```

