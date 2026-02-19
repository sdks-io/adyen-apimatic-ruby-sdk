
# Donation Campaigns Request

## Structure

`DonationCampaignsRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `currency` | `String` | Required | The three-character [ISO currency code](https://docs.adyen.com/development-resources/currency-codes/). |
| `locale` | `String` | Optional | Locale on the shopper interaction device. |
| `merchant_account` | `String` | Required | Your merchant account identifier. |

## Example (as JSON)

```json
{
  "currency": "currency0",
  "locale": "locale8",
  "merchantAccount": "merchantAccount8"
}
```

