
# Payment Validations Name Result Raw Response 2

Contains the raw response(s) returned by the scheme for the name validation.

## Structure

`PaymentValidationsNameResultRawResponse2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `first_name` | `String` | Optional | The raw first name validation result that Adyen received from the scheme. First name validation result is only returned for Visa. |
| `full_name` | `String` | Optional | The raw full name validation result that Adyen received from the scheme. Full name is the only field that is validated for Mastercard |
| `last_name` | `String` | Optional | The raw last name validation result that Adyen received from the scheme. Last name validation result is only returned for Visa. |
| `middle_name` | `String` | Optional | The raw middle name validation result that Adyen received from the scheme. Middle name validation result is only returned for Visa. |
| `status` | `String` | Optional | The raw name validation status value that Adyen received from the scheme. Only returned for Visa. |

## Example (as JSON)

```json
{
  "firstName": "firstName8",
  "fullName": "fullName6",
  "lastName": "lastName0",
  "middleName": "middleName4",
  "status": "status2"
}
```

