# Users-Companylevel

```ruby
users_companylevel_api = client.users_companylevel
```

## Class Name

`UsersCompanylevelApi`

## Methods

* [List Company Users](../../doc/controllers/users-companylevel.md#list-company-users)
* [Create Company User](../../doc/controllers/users-companylevel.md#create-company-user)
* [Get Company User](../../doc/controllers/users-companylevel.md#get-company-user)
* [Update Company User](../../doc/controllers/users-companylevel.md#update-company-user)


# List Company Users

Returns the list of users for the `companyId` identified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Users read and write

```ruby
def list_company_users(company_id,
                       page_number: nil,
                       page_size: nil,
                       username: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `company_id` | `String` | Template, Required | The unique identifier of the company account. |
| `page_number` | `Integer` | Query, Optional | The number of the page to return. |
| `page_size` | `Integer` | Query, Optional | The number of items to have on a page. Maximum value is **100**. The default is **10** items on a page. |
| `username` | `String` | Query, Optional | The partial or complete username to select all users that match. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ListCompanyUsersResponse`](../../doc/models/list-company-users-response.md).

## Example Usage

```ruby
company_id = 'companyId0'

result = users_company_level_api.list_company_users(company_id)

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


# Create Company User

Creates the user for the `companyId` identified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Users read and write

```ruby
def create_company_user(company_id,
                        body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `company_id` | `String` | Template, Required | The unique identifier of the company account. |
| `body` | [`CreateCompanyUserRequest`](../../doc/models/create-company-user-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`CreateCompanyUserResponse`](../../doc/models/create-company-user-response.md).

## Example Usage

```ruby
company_id = 'companyId0'

body = CreateCompanyUserRequest.new(
  email: 'john.smith@example.com',
  name: Name.new(
    first_name: 'John',
    last_name: 'Smith'
  ),
  username: 'johnsmith',
  associated_merchant_accounts: [
    'YOUR_MERCHANT_ACCOUNT'
  ],
  login_method: 'Email',
  roles: [
    'Merchant standard role',
    'Merchant admin'
  ],
  time_zone_code: 'Europe/Amsterdam'
)

result = users_company_level_api.create_company_user(
  company_id,
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
  "id": "S2-5C334C6770",
  "name": {
    "firstName": "John",
    "lastName": "Smith"
  },
  "email": "john.smith@example.com",
  "timeZoneCode": "Europe/Amsterdam",
  "username": "johnsmith",
  "roles": [
    "Merchant standard role",
    "Merchant admin"
  ],
  "active": true,
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/users/S2-5C334C6770"
    }
  },
  "associatedMerchantAccounts": [
    "YOUR_MERCHANT_ACCOUNT"
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


# Get Company User

Returns user details for the `userId` and the `companyId` identified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Users read and write

```ruby
def get_company_user(company_id,
                     user_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `company_id` | `String` | Template, Required | The unique identifier of the company account. |
| `user_id` | `String` | Template, Required | The unique identifier of the user. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`CompanyUser`](../../doc/models/company-user.md).

## Example Usage

```ruby
company_id = 'companyId0'

user_id = 'userId0'

result = users_company_level_api.get_company_user(
  company_id,
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


# Update Company User

Updates user details for the `userId` and the `companyId` identified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Users read and write

```ruby
def update_company_user(company_id,
                        user_id,
                        body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `company_id` | `String` | Template, Required | The unique identifier of the company account. |
| `user_id` | `String` | Template, Required | The unique identifier of the user. |
| `body` | [`UpdateCompanyUserRequest`](../../doc/models/update-company-user-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`CompanyUser`](../../doc/models/company-user.md).

## Example Usage

```ruby
company_id = 'companyId0'

user_id = 'userId0'

result = users_company_level_api.update_company_user(
  company_id,
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

