
# Create Order Response

## Structure

`CreateOrderResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `additional_data` | `Hash[String, String]` | Optional | Contains additional information about the payment. Some data fields are included only if you select them first: Go to **Customer Area** > **Developers** > **Additional data**. |
| `amount` | [`Amount11`](../../doc/models/amount-11.md) | Required | The initial amount of the order. |
| `expires_at` | `String` | Required | The date that the order will expire. |
| `fraud_result` | [`FraudResult1`](../../doc/models/fraud-result-1.md) | Optional | The fraud result properties of the payment. |
| `order_data` | `String` | Required | The encrypted data that will be used by merchant for adding payments to the order. |
| `psp_reference` | `String` | Optional | Adyen's 16-character reference associated with the transaction/request. This value is globally unique; quote it when communicating with us about this request. |
| `reference` | `String` | Optional | The reference provided by merchant for creating the order. |
| `refusal_reason` | `String` | Optional | If the payment's authorisation is refused or an error occurs during authorisation, this field holds Adyen's mapped reason for the refusal or a description of the error. When a transaction fails, the authorisation response includes `resultCode` and `refusalReason` values.<br><br>For more information, see [Refusal reasons](https://docs.adyen.com/development-resources/refusal-reasons). |
| `remaining_amount` | [`Amount22`](../../doc/models/amount-22.md) | Required | The remaining amount in the order. |
| `result_code` | `String` | Required, Constant | The result of the order creation request.<br>The value is always **Success**.<br><br>**Value**: `'Success'` |

## Example (as JSON)

```json
{
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "expiresAt": "expiresAt4",
  "orderData": "orderData0",
  "remainingAmount": {
    "currency": "currency6",
    "value": 156
  },
  "resultCode": "Success",
  "additionalData": {
    "key0": "additionalData8",
    "key1": "additionalData9"
  },
  "fraudResult": {
    "accountScore": 232,
    "results": [
      {
        "accountScore": 102,
        "checkId": 246,
        "name": "name6"
      },
      {
        "accountScore": 102,
        "checkId": 246,
        "name": "name6"
      }
    ]
  },
  "pspReference": "pspReference0",
  "reference": "reference6",
  "refusalReason": "refusalReason8"
}
```

