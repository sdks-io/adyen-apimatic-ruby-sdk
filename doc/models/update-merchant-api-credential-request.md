
# Update Merchant Api Credential Request

## Structure

`UpdateMerchantApiCredentialRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `active` | `TrueClass \| FalseClass` | Optional | Indicates if the API credential is enabled. |
| `allowed_origins` | `Array[String]` | Optional | The new list of [allowed origins](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) for the API credential. |
| `description` | `String` | Optional | Description of the API credential. |
| `roles` | `Array[String]` | Optional | List of [roles](https://docs.adyen.com/development-resources/api-credentials#roles-1) for the API credential. Only roles assigned to 'ws@Company.<CompanyName>' can be assigned to other API credentials. |

## Example (as JSON)

```json
{
  "active": false,
  "allowedOrigins": [
    "allowedOrigins0",
    "allowedOrigins1"
  ],
  "description": "description8",
  "roles": [
    "roles4",
    "roles5"
  ]
}
```

