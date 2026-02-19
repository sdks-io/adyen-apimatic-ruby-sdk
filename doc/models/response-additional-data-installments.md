
# Response Additional Data Installments

## Structure

`ResponseAdditionalDataInstallments`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `installment_payment_data_installment_type` | `String` | Optional | Type of installment. The value of `installmentType` should be **IssuerFinanced**. |
| `installment_payment_data_option_item_nr_annual_percentage_rate` | `String` | Optional | Annual interest rate. |
| `installment_payment_data_option_item_nr_first_installment_amount` | `String` | Optional | First Installment Amount in minor units. |
| `installment_payment_data_option_item_nr_installment_fee` | `String` | Optional | Installment fee amount in minor units. |
| `installment_payment_data_option_item_nr_interest_rate` | `String` | Optional | Interest rate for the installment period. |
| `installment_payment_data_option_item_nr_maximum_number_of_installments` | `String` | Optional | Maximum number of installments possible for this payment. |
| `installment_payment_data_option_item_nr_minimum_number_of_installments` | `String` | Optional | Minimum number of installments possible for this payment. |
| `installment_payment_data_option_item_nr_number_of_installments` | `String` | Optional | Total number of installments possible for this payment. |
| `installment_payment_data_option_item_nr_subsequent_installment_amount` | `String` | Optional | Subsequent Installment Amount in minor units. |
| `installment_payment_data_option_item_nr_total_amount_due` | `String` | Optional | Total amount in minor units. |
| `installment_payment_data_payment_options` | `String` | Optional | Possible values:<br><br>* PayInInstallmentsOnly<br>* PayInFullOnly<br>* PayInFullOrInstallments |
| `installments_value` | `String` | Optional | The number of installments that the payment amount should be charged with.<br><br>Example: 5<br><br>> Only relevant for card payments in countries that support installments. |

## Example (as JSON)

```json
{
  "installmentPaymentData.installmentType": "installmentPaymentData.installmentType8",
  "installmentPaymentData.option[itemNr].annualPercentageRate": "installmentPaymentData.option[itemNr].annualPercentageRate2",
  "installmentPaymentData.option[itemNr].firstInstallmentAmount": "installmentPaymentData.option[itemNr].firstInstallmentAmount6",
  "installmentPaymentData.option[itemNr].installmentFee": "installmentPaymentData.option[itemNr].installmentFee8",
  "installmentPaymentData.option[itemNr].interestRate": "installmentPaymentData.option[itemNr].interestRate4"
}
```

