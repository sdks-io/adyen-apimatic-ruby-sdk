
# Create Merchant Api Credential Request

## Structure

`CreateMerchantApiCredentialRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allowed_origins` | `Array[String]` | Optional | The list of [allowed origins](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) for the new API credential. |
| `description` | `String` | Optional | Description of the API credential. |
| `roles` | `Array[String]` | Optional | List of [roles](https://docs.adyen.com/development-resources/api-credentials#roles-1) for the API credential. Only roles assigned to 'ws@Company.<CompanyName>' can be assigned to other API credentials. |

## Example (as JSON)

```json
{
  "allowedOrigins": [
    "allowedOrigins4",
    "allowedOrigins3"
  ],
  "description": "description4",
  "roles": [
    "roles0",
    "roles1"
  ]
}
```

