
# Additional Data Temporary Services

## Structure

`AdditionalDataTemporaryServices`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enhanced_scheme_data_customer_reference` | `String` | Optional | The customer code, if supplied by a customer.<br><br>* Encoding: ASCII<br>* maxLength: 25 |
| `enhanced_scheme_data_employee_name` | `String` | Optional | The name or ID of the person working in a temporary capacity.<br><br>* maxLength: 40.<br>* Must not be all spaces.<br>  *Must not be all zeros. |
| `enhanced_scheme_data_job_description` | `String` | Optional | The job description of the person working in a temporary capacity.<br><br>* maxLength: 40<br>* Must not be all spaces.<br>  *Must not be all zeros. |
| `enhanced_scheme_data_regular_hours_rate` | `String` | Optional | The amount paid for regular hours worked, [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* maxLength: 7<br>* Must not be empty<br>* Can be all zeros |
| `enhanced_scheme_data_regular_hours_worked` | `String` | Optional | The hours worked.<br><br>* maxLength: 7<br>* Must not be empty<br>* Can be all zeros |
| `enhanced_scheme_data_request_name` | `String` | Optional | The name of the person requesting temporary services.<br><br>* maxLength: 40<br>* Must not be all zeros<br>* Must not be all spaces |
| `enhanced_scheme_data_temp_start_date` | `String` | Optional | The billing period start date.<br><br>* Format: ddMMyy<br>* maxLength: 6 |
| `enhanced_scheme_data_temp_week_ending` | `String` | Optional | The billing period end date.<br><br>* Format: ddMMyy<br>* maxLength: 6 |
| `enhanced_scheme_data_total_tax_amount` | `String` | Optional | The total tax amount, in [minor units](https://docs.adyen.com/development-resources/currency-codes). For example, 2000 means USD 20.00<br><br>* maxLength: 12 |

## Example (as JSON)

```json
{
  "enhancedSchemeData.customerReference": "enhancedSchemeData.customerReference4",
  "enhancedSchemeData.employeeName": "enhancedSchemeData.employeeName4",
  "enhancedSchemeData.jobDescription": "enhancedSchemeData.jobDescription4",
  "enhancedSchemeData.regularHoursRate": "enhancedSchemeData.regularHoursRate8",
  "enhancedSchemeData.regularHoursWorked": "enhancedSchemeData.regularHoursWorked8"
}
```

