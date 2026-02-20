# My AP Icredential

```ruby
my_ap_icredential_api = client.my_ap_icredential
```

## Class Name

`MyApIcredentialApi`

## Methods

* [Get My Api Credential](../../doc/controllers/my-ap-icredential.md#get-my-api-credential)
* [List My Allowed Origins](../../doc/controllers/my-ap-icredential.md#list-my-allowed-origins)
* [Create My Allowed Origin](../../doc/controllers/my-ap-icredential.md#create-my-allowed-origin)
* [Delete My Allowed Origin](../../doc/controllers/my-ap-icredential.md#delete-my-allowed-origin)
* [Get My Allowed Origin](../../doc/controllers/my-ap-icredential.md#get-my-allowed-origin)
* [Generate My Client Key](../../doc/controllers/my-ap-icredential.md#generate-my-client-key)


# Get My Api Credential

Returns your [API credential](https://docs.adyen.com/development-resources/api-credentials) details based on the API Key you used in the request.

You can make this request with any of the Management API roles.

```ruby
def get_my_api_credential
```

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`MeApiCredential`](../../doc/models/me-api-credential.md).

## Example Usage

```ruby
result = my_api_credential_api.get_my_api_credential

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


# List My Allowed Origins

Returns the list of [allowed origins](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) of your [API credential](https://docs.adyen.com/development-resources/api-credentials) based on the API key you used in the request.

You can make this request with any of the Management API roles.

```ruby
def list_my_allowed_origins
```

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`AllowedOriginsResponse`](../../doc/models/allowed-origins-response.md).

## Example Usage

```ruby
result = my_api_credential_api.list_my_allowed_origins

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


# Create My Allowed Origin

Adds an allowed origin to the list of [allowed origins](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) of your API credential.
The API key from the request is used to identify the [API credential](https://docs.adyen.com/development-resources/api-credentials).

You can make this request with any of the Management API roles.

```ruby
def create_my_allowed_origin(body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateAllowedOriginRequest`](../../doc/models/create-allowed-origin-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`AllowedOrigin`](../../doc/models/allowed-origin.md).

## Example Usage

```ruby
body = CreateAllowedOriginRequest.new(
  domain: 'https://adyen.com'
)

result = my_api_credential_api.create_my_allowed_origin(body: body)

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


# Delete My Allowed Origin

Removes the [allowed origin](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) specified in the path.
The API key from the request is used to identify the [API credential](https://docs.adyen.com/development-resources/api-credentials).

You can make this request with any of the Management API roles.

```ruby
def delete_my_allowed_origin(origin_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `origin_id` | `String` | Template, Required | Unique identifier of the allowed origin. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```ruby
origin_id = 'originId6'

result = my_api_credential_api.delete_my_allowed_origin(origin_id)

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


# Get My Allowed Origin

Returns the details of the [allowed origin](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) specified in the path.
The API key from the request is used to identify the [API credential](https://docs.adyen.com/development-resources/api-credentials).

You can make this request with any of the Management API roles.

```ruby
def get_my_allowed_origin(origin_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `origin_id` | `String` | Template, Required | Unique identifier of the allowed origin. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`AllowedOrigin`](../../doc/models/allowed-origin.md).

## Example Usage

```ruby
origin_id = 'originId6'

result = my_api_credential_api.get_my_allowed_origin(origin_id)

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


# Generate My Client Key

Generates a new [client key](https://docs.adyen.com/development-resources/client-side-authentication/) used to authenticate requests from your payment environment.
You can use the new client key a few minutes after generating it.
The old client key stops working 24 hours after generating a new one.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—API credentials read and write

```ruby
def generate_my_client_key
```

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`GenerateClientKeyResponse`](../../doc/models/generate-client-key-response.md).

## Example Usage

```ruby
result = my_api_credential_api.generate_my_client_key

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

