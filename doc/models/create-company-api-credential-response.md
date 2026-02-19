
# Create Company Api Credential Response

## Structure

`CreateCompanyApiCredentialResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `links` | [`ApiCredentialLinks2`](../../doc/models/api-credential-links-2.md) | Optional | References to resources linked to the API credential. |
| `active` | `TrueClass \| FalseClass` | Required | Indicates if the API credential is enabled. Must be set to **true** to use the credential in your integration. |
| `allowed_ip_addresses` | `Array[String]` | Required | List of IP addresses from which your client can make requests.<br><br>If the list is empty, we allow requests from any IP.<br>If the list is not empty and we get a request from an IP which is not on the list, you get a security error. |
| `allowed_origins` | [`Array[AllowedOrigin]`](../../doc/models/allowed-origin.md) | Optional | List containing the [allowed origins](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) linked to the API credential. |
| `api_key` | `String` | Required | The API key for the API credential that was created. |
| `associated_merchant_accounts` | `Array[String]` | Required | List of merchant accounts that the API credential has access to. |
| `client_key` | `String` | Required | Public key used for [client-side authentication](https://docs.adyen.com/development-resources/client-side-authentication). The client key is required for Drop-in and Components integrations. |
| `description` | `String` | Optional | Description of the API credential.<br><br>**Constraints**: *Maximum Length*: `50` |
| `id` | `String` | Required | Unique identifier of the API credential. |
| `password` | `String` | Required | The password for the API credential that was created. |
| `roles` | `Array[String]` | Required | List of [roles](https://docs.adyen.com/development-resources/api-credentials#roles-1) for the API credential. |
| `username` | `String` | Required | The name of the [API credential](https://docs.adyen.com/development-resources/api-credentials), for example **ws@Company.TestCompany**. |

## Example (as JSON)

```json
{
  "_links": {
    "allowedOrigins": {
      "href": "href6"
    },
    "company": {
      "href": "href2"
    },
    "generateApiKey": {
      "href": "href6"
    },
    "generateClientKey": {
      "href": "href4"
    },
    "merchant": {
      "href": "href6"
    },
    "self": {
      "href": "href0"
    }
  },
  "active": false,
  "allowedIpAddresses": [
    "allowedIpAddresses7"
  ],
  "allowedOrigins": [
    {
      "_links": {
        "self": {
          "href": "href0"
        }
      },
      "domain": "domain0",
      "id": "id4"
    }
  ],
  "apiKey": "apiKey8",
  "associatedMerchantAccounts": [
    "associatedMerchantAccounts8",
    "associatedMerchantAccounts9",
    "associatedMerchantAccounts0"
  ],
  "clientKey": "clientKey8",
  "description": "description2",
  "id": "id8",
  "password": "password2",
  "roles": [
    "roles8"
  ],
  "username": "username2"
}
```

