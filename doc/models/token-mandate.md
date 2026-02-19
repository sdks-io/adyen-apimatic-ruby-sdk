
# Token Mandate

## Structure

`TokenMandate`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_id_type` | `String` | Optional | The type of account identifier for the masked account number. |
| `amount` | `String` | Required | The billing amount (in minor units) of the recurring transactions. |
| `amount_rule` | [`AmountRule`](../../doc/models/amount-rule.md) | Optional | The limitation rule of the billing amount.<br><br>Possible values:<br><br>* **max**: The transaction amount can not exceed the `amount`.<br><br>* **exact**: The transaction amount should be the same as the `amount`. |
| `billing_attempts_rule` | [`BillingAttemptsRule`](../../doc/models/billing-attempts-rule.md) | Optional | The rule to specify the period, within which the recurring debit can happen, relative to the mandate recurring date.<br><br>Possible values:<br><br>* **on**: On a specific date.<br><br>* **before**:  Before and on a specific date.<br><br>* **after**: On and after a specific date. |
| `billing_day` | `String` | Optional | The number of the day, on which the recurring debit can happen. Should be within the same calendar month as the mandate recurring date.<br><br>Possible values: 1-31 based on the `frequency`. |
| `count` | `String` | Optional | The number of transactions that can be performed within the given frequency. |
| `currency` | `String` | Required | The three-character [ISO currency code](https://docs.adyen.com/development-resources/currency-codes). |
| `ends_at` | `String` | Required | End date of the billing plan, in YYYY-MM-DD format. |
| `frequency` | [`Frequency`](../../doc/models/frequency.md) | Required | The frequency with which a shopper should be charged.<br><br>Possible values: **adhoc**, **daily**, **weekly**, **biWeekly**, **monthly**, **quarterly**, **halfYearly**, **yearly**. |
| `mandate_id` | `String` | Required | The unique identifier of the mandate. |
| `masked_account_id` | `String` | Optional | The masked account number associated with the mandate. |
| `provider_id` | `String` | Required | The provider-specific identifier for this mandate. |
| `remarks` | `String` | Optional | Additional remarks or notes about the mandate. |
| `starts_at` | `String` | Optional | Start date of the billing plan, in YYYY-MM-DD format. By default, the transaction date. |
| `status` | `String` | Required | The status of the mandate. Examples : active, revoked, completed, expired |
| `tx_variant` | `String` | Required | The transaction variant used for this mandate. |

## Example (as JSON)

```json
{
  "accountIdType": "accountIdType8",
  "amount": "amount0",
  "amountRule": "max",
  "billingAttemptsRule": "on",
  "billingDay": "billingDay0",
  "count": "count6",
  "currency": "currency8",
  "endsAt": "endsAt8",
  "frequency": "adhoc",
  "mandateId": "mandateId0",
  "providerId": "providerId2",
  "status": "status0",
  "txVariant": "txVariant6"
}
```

