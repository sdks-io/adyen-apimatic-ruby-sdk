
# Additional Data Ratepay

## Structure

`AdditionalDataRatepay`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ratepay_installment_amount` | `String` | Optional | Amount the customer has to pay each month. |
| `ratepay_interest_rate` | `String` | Optional | Interest rate of this installment. |
| `ratepay_last_installment_amount` | `String` | Optional | Amount of the last installment. |
| `ratepay_payment_firstday` | `String` | Optional | Calendar day of the first payment. |
| `ratepaydata_delivery_date` | `String` | Optional | Date the merchant delivered the goods to the customer. |
| `ratepaydata_due_date` | `String` | Optional | Date by which the customer must settle the payment. |
| `ratepaydata_invoice_date` | `String` | Optional | Invoice date, defined by the merchant. If not included, the invoice date is set to the delivery date. |
| `ratepaydata_invoice_id` | `String` | Optional | Identification name or number for the invoice, defined by the merchant. |

## Example (as JSON)

```json
{
  "ratepay.installmentAmount": "ratepay.installmentAmount4",
  "ratepay.interestRate": "ratepay.interestRate8",
  "ratepay.lastInstallmentAmount": "ratepay.lastInstallmentAmount0",
  "ratepay.paymentFirstday": "ratepay.paymentFirstday2",
  "ratepaydata.deliveryDate": "ratepaydata.deliveryDate2"
}
```

