# Allowedorigins-Companylevel

```ruby
allowedorigins_companylevel_api = client.allowedorigins_companylevel
```

## Class Name

`AllowedoriginsCompanylevelApi`

## Methods

* [List Company Api Credential Origins](../../doc/controllers/allowedorigins-companylevel.md#list-company-api-credential-origins)
* [Create Company Api Credential Origin](../../doc/controllers/allowedorigins-companylevel.md#create-company-api-credential-origin)
* [Delete Company Api Credential Origin](../../doc/controllers/allowedorigins-companylevel.md#delete-company-api-credential-origin)
* [Get Company Api Credential Origin](../../doc/controllers/allowedorigins-companylevel.md#get-company-api-credential-origin)


# List Company Api Credential Origins

Returns the list of [allowed origins](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) for the API credential identified in the path.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—API credentials read and write

```ruby
def list_company_api_credential_origins(company_id,
                                        api_credential_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `company_id` | `String` | Template, Required | The unique identifier of the company account. |
| `api_credential_id` | `String` | Template, Required | Unique identifier of the API credential. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`AllowedOriginsResponse`](../../doc/models/allowed-origins-response.md).

## Example Usage

```ruby
company_id = 'companyId0'

api_credential_id = 'apiCredentialId8'

result = allowed_origins_company_level_api.list_company_api_credential_origins(
  company_id,
  api_credential_id
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "id": "YOUR_ALLOWED_ORIGIN_1",
      "domain": "https://www.eu.mystore.com",
      "_links": {
        "self": {
          "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/apiCredentials/YOUR_API_CREDENTIAL/allowedOrigins/YOUR_ALLOWED_ORIGIN_1"
        }
      }
    },
    {
      "id": "YOUR_ALLOWED_ORIGIN_2",
      "domain": "https://www.us.mystore.com",
      "_links": {
        "self": {
          "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/apiCredentials/YOUR_API_CREDENTIAL/allowedOrigins/YOUR_ALLOWED_ORIGIN_2"
        }
      }
    }
  ]
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 401 | Unauthorized - authentication required. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Create Company Api Credential Origin

Adds a new [allowed origin](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) to the API credential's list of allowed origins.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—API credentials read and write

```ruby
def create_company_api_credential_origin(company_id,
                                         api_credential_id,
                                         body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `company_id` | `String` | Template, Required | The unique identifier of the company account. |
| `api_credential_id` | `String` | Template, Required | Unique identifier of the API credential. |
| `body` | [`AllowedOrigin`](../../doc/models/allowed-origin.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`AllowedOrigin`](../../doc/models/allowed-origin.md).

## Example Usage

```ruby
company_id = 'companyId0'

api_credential_id = 'apiCredentialId8'

body = AllowedOrigin.new(
  domain: 'https://www.eu.mystore.com'
)

result = allowed_origins_company_level_api.create_company_api_credential_origin(
  company_id,
  api_credential_id,
  body: body
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "id": "YOUR_ALLOWED_ORIGIN",
  "domain": "https://www.eu.mystore.com",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/apiCredentials/YOUR_API_CREDENTIAL/allowedOrigins/YOUR_ALLOWED_ORIGIN"
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 401 | Unauthorized - authentication required. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Delete Company Api Credential Origin

Removes the [allowed origin](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) identified in the path. As soon as an allowed origin is removed, we no longer accept client-side requests from that domain.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—API credentials read and write

```ruby
def delete_company_api_credential_origin(company_id,
                                         api_credential_id,
                                         origin_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `company_id` | `String` | Template, Required | The unique identifier of the company account. |
| `api_credential_id` | `String` | Template, Required | Unique identifier of the API credential. |
| `origin_id` | `String` | Template, Required | Unique identifier of the allowed origin. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```ruby
company_id = 'companyId0'

api_credential_id = 'apiCredentialId8'

origin_id = 'originId6'

result = allowed_origins_company_level_api.delete_company_api_credential_origin(
  company_id,
  api_credential_id,
  origin_id
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 401 | Unauthorized - authentication required. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Get Company Api Credential Origin

Returns the [allowed origin](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) identified in the path.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—API credentials read and write

```ruby
def get_company_api_credential_origin(company_id,
                                      api_credential_id,
                                      origin_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `company_id` | `String` | Template, Required | The unique identifier of the company account. |
| `api_credential_id` | `String` | Template, Required | Unique identifier of the API credential. |
| `origin_id` | `String` | Template, Required | Unique identifier of the allowed origin. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`AllowedOrigin`](../../doc/models/allowed-origin.md).

## Example Usage

```ruby
company_id = 'companyId0'

api_credential_id = 'apiCredentialId8'

origin_id = 'originId6'

result = allowed_origins_company_level_api.get_company_api_credential_origin(
  company_id,
  api_credential_id,
  origin_id
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "id": "YOUR_ALLOWED_ORIGIN",
  "domain": "https://www.us.mystore.com",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/apiCredentials/YOUR_API_CREDENTIAL/allowedOrigins/YOUR_ALLOWED_ORIGIN"
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 401 | Unauthorized - authentication required. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |

