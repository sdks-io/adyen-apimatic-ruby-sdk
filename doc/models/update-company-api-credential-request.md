
# Update Company Api Credential Request

## Structure

`UpdateCompanyApiCredentialRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `active` | `TrueClass \| FalseClass` | Optional | Indicates if the API credential is enabled. |
| `allowed_origins` | `Array[String]` | Optional | The new list of [allowed origins](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) for the API credential. |
| `associated_merchant_accounts` | `Array[String]` | Optional | List of merchant accounts that the API credential has access to. |
| `description` | `String` | Optional | Description of the API credential. |
| `roles` | `Array[String]` | Optional | List of [roles](https://docs.adyen.com/development-resources/api-credentials#roles-1) for the API credential. Only roles assigned to 'ws@Company.<CompanyName>' can be assigned to other API credentials. |

## Example (as JSON)

```json
{
  "active": false,
  "allowedOrigins": [
    "allowedOrigins0",
    "allowedOrigins9",
    "allowedOrigins8"
  ],
  "associatedMerchantAccounts": [
    "associatedMerchantAccounts6",
    "associatedMerchantAccounts7"
  ],
  "description": "description6",
  "roles": [
    "roles0",
    "roles9"
  ]
}
```

