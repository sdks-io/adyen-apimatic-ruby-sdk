
# Response Additional Data Sepa

## Structure

`ResponseAdditionalDataSepa`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sepadirectdebit_date_of_signature` | `String` | Optional | The transaction signature date.<br><br>Format: yyyy-MM-dd |
| `sepadirectdebit_mandate_id` | `String` | Optional | Its value corresponds to the pspReference value of the transaction. |
| `sepadirectdebit_sepadirectdebit_due_date` | `String` | Optional | The date that the the shopper's bank account is charged. |
| `sepadirectdebit_sequence_type` | `String` | Optional | This field can take one of the following values:<br><br>* OneOff: (OOFF) Direct debit instruction to initiate exactly one direct debit transaction.<br><br>* First: (FRST) Initial/first collection in a series of direct debit instructions.<br><br>* Recurring: (RCUR) Direct debit instruction to carry out regular direct debit transactions initiated by the creditor.<br><br>* Final: (FNAL) Last/final collection in a series of direct debit instructions.<br><br>Example: OOFF |

## Example (as JSON)

```json
{
  "sepadirectdebit.dateOfSignature": "sepadirectdebit.dateOfSignature2",
  "sepadirectdebit.mandateId": "sepadirectdebit.mandateId4",
  "sepadirectdebit.sepadirectdebit.dueDate": "sepadirectdebit.sepadirectdebit.dueDate0",
  "sepadirectdebit.sequenceType": "sepadirectdebit.sequenceType6"
}
```

