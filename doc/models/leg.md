
# Leg

## Structure

`Leg`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `carrier_code` | `String` | Optional | The [IATA](https://www.iata.org/services/pages/codes.aspx) 2-letter accounting code (PAX) that identifies the carrier.<br>This field is required if the airline data includes leg details.<br><br>* Example: KLM = KL<br>* minLength: 2 characters<br>* maxLength: 2 characters<br>* Must not start with a space or be all spaces.<br>* Must not be all zeros. |
| `class_of_travel` | `String` | Optional | A one-letter travel class identifier.<br>The following are common:<br><br>* F: first class<br><br>* J: business class<br><br>* Y: economy class<br><br>* W: premium economy<br><br>* Encoding: ASCII<br><br>* minLength: 1 character<br><br>* maxLength: 1 character<br><br>* Must not start with a space or be all spaces.<br><br>* Must not be all zeros. |
| `date_of_travel` | `DateTime` | Optional | Date and time of travel in format `yyyy-MM-ddTHH:mm`.<br><br>* Use local time of departure airport.<br>* minLength: 16 characters<br>* maxLength: 16 characters |
| `departure_airport_code` | `String` | Optional | The [IATA](https://www.iata.org/services/pages/codes.aspx) three-letter airport code of the departure airport.<br>This field is required if the airline data includes leg details.<br><br>* Encoding: ASCII<br>* Example: Amsterdam = AMS<br>* minLength: 3 characters<br>* maxLength: 3 characters<br>* Must not start with a space or be all spaces.<br>* Must not be all zeros. |
| `departure_tax` | `Integer` | Optional | The amount of [departure tax](https://en.wikipedia.org/wiki/Departure_tax) charged, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Encoding: Numeric<br>* minLength: 1<br>* maxLength: 11<br>* Must not be all zeros. |
| `destination_airport_code` | `String` | Optional | The [IATA](https://www.iata.org/services/pages/codes.aspx) 3-letter airport code of the destination airport.<br>This field is required if the airline data includes leg details.<br><br>* Example: Amsterdam = AMS<br>* Encoding: ASCII<br>* minLength: 3 characters<br>* maxLength: 3 characters<br>* Must not start with a space or be all spaces.<br>* Must not be all zeros. |
| `fare_basis_code` | `String` | Optional | The [fare basis code](https://en.wikipedia.org/wiki/Fare_basis_code), alphanumeric.<br><br>* minLength: 1 character<br>* maxLength: 15 characters<br>* Must not start with a space or be all spaces.<br>* Must not be all zeros. |
| `flight_number` | `String` | Optional | The flight identifier.<br><br>* minLength: 1 character<br>* maxLength: 5 characters<br>* Must not start with a space or be all spaces.<br>* Must not be all zeros. |
| `stop_over_code` | `String` | Optional | A one-letter code that indicates whether the passenger is entitled to make a stopover. Can be a space, O if the passenger is entitled to make a stopover, or X if they are not.<br><br>* Encoding: ASCII<br>* minLength: 1 character<br>* maxLength: 1 character |

## Example (as JSON)

```json
{
  "carrierCode": "carrierCode4",
  "classOfTravel": "classOfTravel8",
  "dateOfTravel": "2016-03-13T12:52:32.123Z",
  "departureAirportCode": "departureAirportCode2",
  "departureTax": 64
}
```

