
# Donation Campaign

## Structure

`DonationCampaign`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amounts` | [`Amounts1`](../../doc/models/amounts-1.md) | Optional | The object that contains the fixed donation amounts that the shopper can select from. |
| `banner_url` | `String` | Optional | The URL for the banner of the nonprofit or campaign. |
| `campaign_name` | `String` | Optional | The name of the donation campaign.. |
| `cause_name` | `String` | Optional | The cause of the nonprofit. |
| `donation` | [`Donation1`](../../doc/models/donation-1.md) | Optional | The object that contains the details of the donation. |
| `id` | `String` | Optional | The unique campaign ID of the donation campaign. |
| `logo_url` | `String` | Optional | The URL for the logo of the nonprofit. |
| `nonprofit_description` | `String` | Optional | The description of the nonprofit. |
| `nonprofit_name` | `String` | Optional | The name of the nonprofit organization that receives the donation. |
| `nonprofit_url` | `String` | Optional | The website URL of the nonprofit. |
| `terms_and_conditions_url` | `String` | Optional | The URL of the terms and conditions page of the nonprofit and the campaign. |

## Example (as JSON)

```json
{
  "amounts": {
    "currency": "currency6",
    "values": [
      48,
      49
    ]
  },
  "bannerUrl": "bannerUrl0",
  "campaignName": "campaignName2",
  "causeName": "causeName6",
  "donation": {
    "currency": "currency0",
    "donationType": "donationType2",
    "maxRoundupAmount": 114,
    "type": "type0",
    "values": [
      106,
      105,
      104
    ]
  }
}
```

