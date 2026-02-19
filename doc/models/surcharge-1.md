
# Surcharge 1

## Structure

`Surcharge1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ask_confirmation` | `TrueClass \| FalseClass` | Optional | Show the surcharge details on the terminal, so the shopper can confirm. |
| `configurations` | [`Array[Configuration]`](../../doc/models/configuration.md) | Optional | Surcharge fees or percentages for specific cards, funding sources (credit or debit), and currencies. |
| `exclude_gratuity_from_surcharge` | `TrueClass \| FalseClass` | Optional | Exclude the tip amount from the surcharge calculation. |

## Example (as JSON)

```json
{
  "askConfirmation": false,
  "configurations": [
    {
      "brand": "brand4",
      "commercial": false,
      "country": [
        "country1",
        "country2"
      ],
      "currencies": [
        {
          "amount": 208,
          "currencyCode": "currencyCode6",
          "maxAmount": 98,
          "percentage": 191.04
        },
        {
          "amount": 208,
          "currencyCode": "currencyCode6",
          "maxAmount": 98,
          "percentage": 191.04
        },
        {
          "amount": 208,
          "currencyCode": "currencyCode6",
          "maxAmount": 98,
          "percentage": 191.04
        }
      ],
      "sources": [
        "sources8",
        "sources9"
      ]
    },
    {
      "brand": "brand4",
      "commercial": false,
      "country": [
        "country1",
        "country2"
      ],
      "currencies": [
        {
          "amount": 208,
          "currencyCode": "currencyCode6",
          "maxAmount": 98,
          "percentage": 191.04
        },
        {
          "amount": 208,
          "currencyCode": "currencyCode6",
          "maxAmount": 98,
          "percentage": 191.04
        },
        {
          "amount": 208,
          "currencyCode": "currencyCode6",
          "maxAmount": 98,
          "percentage": 191.04
        }
      ],
      "sources": [
        "sources8",
        "sources9"
      ]
    },
    {
      "brand": "brand4",
      "commercial": false,
      "country": [
        "country1",
        "country2"
      ],
      "currencies": [
        {
          "amount": 208,
          "currencyCode": "currencyCode6",
          "maxAmount": 98,
          "percentage": 191.04
        },
        {
          "amount": 208,
          "currencyCode": "currencyCode6",
          "maxAmount": 98,
          "percentage": 191.04
        },
        {
          "amount": 208,
          "currencyCode": "currencyCode6",
          "maxAmount": 98,
          "percentage": 191.04
        }
      ],
      "sources": [
        "sources8",
        "sources9"
      ]
    }
  ],
  "excludeGratuityFromSurcharge": false
}
```

