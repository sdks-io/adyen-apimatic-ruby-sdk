# Users-Merchantlevel

```ruby
users_merchantlevel_api = client.users_merchantlevel
```

## Class Name

`UsersMerchantlevelApi`

## Methods

* [List Merchant Users](../../doc/controllers/users-merchantlevel.md#list-merchant-users)
* [Create Merchant User](../../doc/controllers/users-merchantlevel.md#create-merchant-user)
* [Get Merchant User](../../doc/controllers/users-merchantlevel.md#get-merchant-user)
* [Update Merchant User](../../doc/controllers/users-merchantlevel.md#update-merchant-user)


# List Merchant Users

Returns a list of users associated with the `merchantId` specified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Users read and write

```ruby
def list_merchant_users(merchant_id,
                        page_number: nil,
                        page_size: nil,
                        username: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | Unique identifier of the merchant. |
| `page_number` | `Integer` | Query, Optional | The number of the page to fetch. |
| `page_size` | `Integer` | Query, Optional | The number of items to have on a page. Maximum value is **100**. The default is **10** items on a page. |
| `username` | `String` | Query, Optional | The partial or complete username to select all users that match. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ListMerchantUsersResponse`](../../doc/models/list-merchant-users-response.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

result = users_merchant_level_api.list_merchant_users(merchant_id)

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


# Create Merchant User

Creates a user for the `merchantId` specified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Users read and write

```ruby
def create_merchant_user(merchant_id,
                         body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | Unique identifier of the merchant. |
| `body` | [`CreateMerchantUserRequest`](../../doc/models/create-merchant-user-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`CreateUserResponse`](../../doc/models/create-user-response.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

body = CreateMerchantUserRequest.new(
  email: 'john.smith@example.com',
  name: Name.new(
    first_name: 'John',
    last_name: 'Smith'
  ),
  username: 'johnsmith',
  login_method: 'Email',
  roles: [
    'Merchant standard role'
  ],
  time_zone_code: 'Europe/Amsterdam'
)

result = users_merchant_level_api.create_merchant_user(
  merchant_id,
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
  "id": "S2-3B3C3C3B22",
  "name": {
    "firstName": "John",
    "lastName": "Smith"
  },
  "email": "john.smith@example.com",
  "timeZoneCode": "Europe/Amsterdam",
  "username": "johnsmith",
  "roles": [
    "Merchant standard role"
  ],
  "active": true,
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT/users/S2-3B3C3C3B22"
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


# Get Merchant User

Returns user details for the `userId` and the `merchantId` specified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Users read and write

```ruby
def get_merchant_user(merchant_id,
                      user_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | Unique identifier of the merchant. |
| `user_id` | `String` | Template, Required | Unique identifier of the user. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`User`](../../doc/models/user.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

user_id = 'userId0'

result = users_merchant_level_api.get_merchant_user(
  merchant_id,
  user_id
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


# Update Merchant User

Updates user details for the `userId` and the `merchantId` specified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Users read and write

```ruby
def update_merchant_user(merchant_id,
                         user_id,
                         body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | Unique identifier of the merchant. |
| `user_id` | `String` | Template, Required | Unique identifier of the user. |
| `body` | [`UpdateMerchantUserRequest`](../../doc/models/update-merchant-user-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`User`](../../doc/models/user.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

user_id = 'userId0'

result = users_merchant_level_api.update_merchant_user(
  merchant_id,
  user_id
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

