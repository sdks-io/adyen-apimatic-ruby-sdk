
# Vipps Info

## Structure

`VippsInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `logo` | `String` | Required | Vipps logo. Format: Base64-encoded string. |
| `subscription_cancel_url` | `String` | Optional | Vipps subscription cancel url (required in case of [recurring payments](https://docs.adyen.com/online-payments/tokenization)) |

## Example (as JSON)

```json
{
  "logo": "logo8",
  "subscriptionCancelUrl": "subscriptionCancelUrl0"
}
```

