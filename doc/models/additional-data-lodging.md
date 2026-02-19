
# Additional Data Lodging

## Structure

`AdditionalDataLodging`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lodging_special_program_code` | `String` | Optional | A code that corresponds to the category of lodging charges for the payment. Possible values:<br><br>* 1: Lodging<br>* 2: No show reservation<br>* 3: Advanced deposit |
| `lodging_check_in_date` | `String` | Optional | The arrival date.<br><br>* Date format: **yyyyMmDd**. For example, for 2023 April 22, **20230422**. |
| `lodging_check_out_date` | `String` | Optional | The departure date.<br><br>* Date format: **yyyyMmDd**. For example, for 2023 April 22, **20230422**. |
| `lodging_customer_service_toll_free_number` | `String` | Optional | The toll-free phone number for the lodging.<br><br>* Format: numeric<br>* Max length: 17 characters.<br>* For US and CA numbers must be 10 characters in length<br>* Must not start with a space<br>* Must not contain any special characters such as + or -<br>* Must not be all zeros. |
| `lodging_fire_safety_act_indicator` | `String` | Optional | Identifies that the facility complies with the Hotel and Motel Fire Safety Act of 1990. Must be 'Y' or 'N'.<br><br>* Format: alphabetic<br>* Max length: 1 character |
| `lodging_folio_cash_advances` | `String` | Optional | The folio cash advances, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Format: numeric<br>* Max length: 12 characters |
| `lodging_folio_number` | `String` | Optional | The card acceptor’s internal invoice or billing ID reference number.<br><br>* Max length: 25 characters<br>* Must not start with a space<br>* Must not contain any special characters<br>* Must not be all zeros. |
| `lodging_food_beverage_charges` | `String` | Optional | Any charges for food and beverages associated with the booking, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Format: numeric<br>* Max length: 12 characters |
| `lodging_no_show_indicator` | `String` | Optional | Indicates if the customer didn't check in for their booking.<br>Possible values:<br><br>* **Y**: the customer didn't check in<br>* **N**: the customer checked in |
| `lodging_prepaid_expenses` | `String` | Optional | The prepaid expenses for the booking.<br><br>* Format: numeric<br>* Max length: 12 characters |
| `lodging_property_phone_number` | `String` | Optional | The lodging property location's phone number.<br><br>* Format: numeric<br>* Min length: 10 characters<br>* Max length: 17 characters<br>* For US and CA numbers must be 10 characters in length<br>* Must not start with a space<br>* Must not contain any special characters such as + or -<br>* Must not be all zeros. |
| `lodging_room_1_number_of_nights` | `String` | Optional | The total number of nights the room is booked for.<br><br>* Format: numeric<br>* Must be a number between 0 and 99<br>* Max length: 4 characters |
| `lodging_room_1_rate` | `String` | Optional | The rate for the room, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Format: numeric<br>* Max length: 12 characters<br>* Must not be a negative number |
| `lodging_total_room_tax` | `String` | Optional | The total room tax amount, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Format: numeric<br>* Max length: 12 characters<br>* Must not be a negative number |
| `lodging_total_tax` | `String` | Optional | The total tax amount, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Format: numeric<br>* Max length: 12 characters<br>* Must not be a negative number |
| `travel_entertainment_auth_data_duration` | `String` | Optional | The number of nights. This should be included in the auth message.<br><br>* Format: numeric<br>* Max length: 4 characters |
| `travel_entertainment_auth_data_market` | `String` | Optional | Indicates what market-specific dataset will be submitted. Must be 'H' for Hotel. This should be included in the auth message.<br><br>* Format: alphanumeric<br>* Max length: 1 character |

## Example (as JSON)

```json
{
  "lodging.SpecialProgramCode": "lodging.SpecialProgramCode8",
  "lodging.checkInDate": "lodging.checkInDate2",
  "lodging.checkOutDate": "lodging.checkOutDate6",
  "lodging.customerServiceTollFreeNumber": "lodging.customerServiceTollFreeNumber4",
  "lodging.fireSafetyActIndicator": "lodging.fireSafetyActIndicator4"
}
```

