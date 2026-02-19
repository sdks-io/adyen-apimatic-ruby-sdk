
# Passenger

## Structure

`Passenger`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `date_of_birth` | `Date` | Optional | The passenger's date of birth.<br><br>* Format `yyyy-MM-dd`<br>* minLength: 10<br>* maxLength: 10 |
| `first_name` | `String` | Optional | The passenger's first name.<br><br>> This field is required if the airline data includes passenger details or leg details.<br><br>* Encoding: ASCII |
| `last_name` | `String` | Optional | The passenger's last name.<br><br>> This field is required if the airline data includes passenger details or leg details.<br><br>* Encoding: ASCII |
| `phone_number` | `String` | Optional | The passenger's phone number, including country code. This is an alphanumeric field that can include the '+' and '-' signs.<br><br>* Encoding: ASCII<br>* minLength: 3 characters<br>* maxLength: 30 characters |
| `traveller_type` | `String` | Optional | The IATA passenger type code (PTC).<br><br>* Encoding: ASCII<br>* minLength: 3 characters<br>* maxLength: 6 characters |

## Example (as JSON)

```json
{
  "dateOfBirth": "2016-03-13",
  "firstName": "firstName8",
  "lastName": "lastName0",
  "phoneNumber": "phoneNumber4",
  "travellerType": "travellerType4"
}
```

