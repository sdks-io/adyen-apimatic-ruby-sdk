# Account-Storelevel

```ruby
account_storelevel_api = client.account_storelevel
```

## Class Name

`AccountStorelevelApi`

## Methods

* [List Merchant Stores](../../doc/controllers/account-storelevel.md#list-merchant-stores)
* [Create Merchant Store](../../doc/controllers/account-storelevel.md#create-merchant-store)
* [Get Merchant Store](../../doc/controllers/account-storelevel.md#get-merchant-store)
* [Update Merchant Store](../../doc/controllers/account-storelevel.md#update-merchant-store)
* [List Stores](../../doc/controllers/account-storelevel.md#list-stores)
* [Create Store](../../doc/controllers/account-storelevel.md#create-store)
* [Get Store](../../doc/controllers/account-storelevel.md#get-store)
* [Update Store](../../doc/controllers/account-storelevel.md#update-store)


# List Merchant Stores

Returns a list of stores for the merchant account identified in the path. The list is grouped into pages as defined by the query parameters.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read
* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```ruby
def list_merchant_stores(merchant_id,
                         page_number: nil,
                         page_size: nil,
                         reference: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `page_number` | `Integer` | Query, Optional | The number of the page to fetch. |
| `page_size` | `Integer` | Query, Optional | The number of items to have on a page, maximum 100. The default is 10 items on a page. |
| `reference` | `String` | Query, Optional | The reference of the store. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ListStoresResponse`](../../doc/models/list-stores-response.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

result = account_store_level_api.list_merchant_stores(merchant_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "_links": {
    "first": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=1&pageSize=1"
    },
    "last": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=2&pageSize=1"
    },
    "next": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=2&pageSize=1"
    },
    "self": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=1&pageSize=1"
    }
  },
  "itemsTotal": 2,
  "pagesTotal": 1,
  "data": [
    {
      "id": "ST322LJ223223K5F4SQNR9XL5",
      "address": {
        "city": "Springfield",
        "country": "US",
        "line1": "200 Main Street",
        "line2": "Building 5A",
        "line3": "Suite 3",
        "postalCode": "20250",
        "stateOrProvince": "NY"
      },
      "description": "City centre store",
      "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
      "phoneNumber": "+13123456789",
      "reference": "Springfield Shop",
      "status": "active",
      "_links": {
        "self": {
          "href": "https://management-test.adyen.com/v1/stores/ST322LJ223223K5F4SQNR9XL5"
        }
      }
    },
    {
      "id": "ST322LJ223223K5F4SQNR9XL6",
      "address": {
        "city": "North Madison",
        "country": "US",
        "line1": "1492 Townline Road",
        "line2": "Rowland Business Park",
        "postalCode": "20577",
        "stateOrProvince": "NY"
      },
      "description": "West location",
      "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
      "phoneNumber": "+1211992213193020",
      "reference": "Second Madison store",
      "status": "active",
      "_links": {
        "self": {
          "href": "https://management-test.adyen.com/v1/stores/ST322LJ223223K5F4SQNR9XL6"
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


# Create Merchant Store

Creates a store for the merchant account identified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```ruby
def create_merchant_store(merchant_id,
                          body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `body` | [`StoreCreationRequest`](../../doc/models/store-creation-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`Store`](../../doc/models/store.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

body = StoreCreationRequest.new(
  address: StoreLocation1.new(
    country: 'US',
    city: 'Springfield',
    line1: '200 Main Street',
    line2: 'Building 5A',
    line3: 'Suite 3',
    postal_code: '20250',
    state_or_province: 'NY'
  ),
  description: 'City centre store',
  phone_number: '13123456789',
  shopper_statement: 'Springfield Shop',
  reference: 'Spring_store_2'
)

result = account_store_level_api.create_merchant_store(
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
  "id": "YOUR_STORE_ID",
  "address": {
    "country": "US",
    "line1": "200 Main Street",
    "line2": "Building 5A",
    "line3": "Suite 3",
    "city": "Springfield",
    "stateOrProvince": "NY",
    "postalCode": "20250"
  },
  "description": "City centre store",
  "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
  "shopperStatement": "Springfield Shop",
  "phoneNumber": "13123456789",
  "reference": "Spring_store_2",
  "status": "active",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/stores/YOUR_STORE_ID"
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


# Get Merchant Store

Returns the details of the store identified in the path.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read
* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```ruby
def get_merchant_store(merchant_id,
                       store_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `store_id` | `String` | Template, Required | The unique identifier of the store. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`Store`](../../doc/models/store.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

store_id = 'storeId6'

result = account_store_level_api.get_merchant_store(
  merchant_id,
  store_id
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
  "address": {
    "city": "Springfield",
    "country": "US",
    "line1": "200 Main Street",
    "line2": "Building 5A",
    "line3": "Suite 3",
    "postalCode": "20250",
    "stateOrProvince": "NY"
  },
  "description": "City centre store",
  "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
  "phoneNumber": "+13123456789",
  "reference": "Springfield Shop",
  "status": "active",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/stores/ST322LJ223223K5F4SQNR9XL5"
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


# Update Merchant Store

Updates the store identified in the path. You can only update some store parameters.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```ruby
def update_merchant_store(merchant_id,
                          store_id,
                          body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `store_id` | `String` | Template, Required | The unique identifier of the store. |
| `body` | [`UpdateStoreRequest`](../../doc/models/update-store-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`Store`](../../doc/models/store.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

store_id = 'storeId6'

body = UpdateStoreRequest.new(
  address: UpdatableAddress1.new(
    line1: '1776 West Pinewood Avenue',
    line2: 'Heartland Building',
    line3: '',
    postal_code: '20251'
  )
)

result = account_store_level_api.update_merchant_store(
  merchant_id,
  store_id,
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
  "id": "YOUR_STORE_ID",
  "address": {
    "country": "US",
    "line1": "1776 West Pinewood Avenue",
    "line2": "Heartland Building",
    "line3": "",
    "city": "Springfield",
    "stateOrProvince": "NY",
    "postalCode": "20251"
  },
  "description": "City centre store",
  "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
  "shopperStatement": "Springfield Shop",
  "phoneNumber": "+13123456789",
  "reference": "Spring_store_2",
  "status": "active",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/stores/YOUR_STORE_ID"
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


# List Stores

Returns a list of stores. The list is grouped into pages as defined by the query parameters.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read
* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```ruby
def list_stores(page_number: nil,
                page_size: nil,
                reference: nil,
                merchant_id: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page_number` | `Integer` | Query, Optional | The number of the page to fetch. |
| `page_size` | `Integer` | Query, Optional | The number of items to have on a page, maximum 100. The default is 10 items on a page. |
| `reference` | `String` | Query, Optional | The reference of the store. |
| `merchant_id` | `String` | Query, Optional | The unique identifier of the merchant account. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ListStoresResponse`](../../doc/models/list-stores-response.md).

## Example Usage

```ruby
result = account_store_level_api.list_stores

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "_links": {
    "first": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=1&pageSize=1"
    },
    "last": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=2&pageSize=1"
    },
    "next": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=2&pageSize=1"
    },
    "self": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=1&pageSize=1"
    }
  },
  "itemsTotal": 2,
  "pagesTotal": 1,
  "data": [
    {
      "id": "ST322LJ223223K5F4SQNR9XL5",
      "address": {
        "city": "Springfield",
        "country": "US",
        "line1": "200 Main Street",
        "line2": "Building 5A",
        "line3": "Suite 3",
        "postalCode": "20250",
        "stateOrProvince": "NY"
      },
      "description": "City centre store",
      "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
      "phoneNumber": "+1312345678",
      "reference": "Springfield Shop",
      "status": "active",
      "_links": {
        "self": {
          "href": "https://management-test.adyen.com/v1/stores/ST322LJ223223K5F4SQNR9XL5"
        }
      }
    },
    {
      "id": "ST322LJ223223K5F4SQNR9XL6",
      "address": {
        "city": "North Madison",
        "country": "US",
        "line1": "1492 Townline Road",
        "line2": "Rowland Business Park",
        "postalCode": "20577",
        "stateOrProvince": "NY"
      },
      "description": "West location",
      "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
      "phoneNumber": "+1211992213193020",
      "reference": "Second Madison store",
      "status": "active",
      "_links": {
        "self": {
          "href": "https://management-test.adyen.com/v1/stores/ST322LJ223223K5F4SQNR9XL6"
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


# Create Store

Creates a store for the merchant account specified in the request.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```ruby
def create_store(body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`StoreCreationWithMerchantCodeRequest`](../../doc/models/store-creation-with-merchant-code-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`Store`](../../doc/models/store.md).

## Example Usage

```ruby
body = StoreCreationWithMerchantCodeRequest.new(
  address: StoreLocation1.new(
    country: 'US',
    city: 'Springfield',
    line1: '200 Main Street',
    line2: 'Building 5A',
    line3: 'Suite 3',
    postal_code: '20250',
    state_or_province: 'NY'
  ),
  description: 'City centre store',
  merchant_id: 'YOUR_MERCHANT_ACCOUNT_ID',
  phone_number: '+13123456789',
  shopper_statement: 'Springfield Shop',
  reference: 'Spring_store_2'
)

result = account_store_level_api.create_store(body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "id": "YOUR_STORE_ID",
  "address": {
    "country": "US",
    "line1": "200 Main Street",
    "line2": "Building 5A",
    "line3": "Suite 3",
    "city": "Springfield",
    "stateOrProvince": "NY",
    "postalCode": "20250"
  },
  "description": "City centre store",
  "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
  "shopperStatement": "Springfield Shop",
  "phoneNumber": "+13123456789",
  "reference": "Spring_store_2",
  "status": "active",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/stores/YOUR_STORE_ID"
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


# Get Store

Returns the details of the store identified in the path.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read
* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```ruby
def get_store(store_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `store_id` | `String` | Template, Required | The unique identifier of the store. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`Store`](../../doc/models/store.md).

## Example Usage

```ruby
store_id = 'storeId6'

result = account_store_level_api.get_store(store_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "id": "ST322LJ223223K5F4SQNR9XL5",
  "address": {
    "city": "Springfield",
    "country": "US",
    "line1": "200 Main Street",
    "line2": "Building 5A",
    "line3": "Suite 3",
    "postalCode": "20250",
    "stateOrProvince": "NY"
  },
  "description": "City centre store",
  "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
  "phoneNumber": "+13123456789",
  "reference": "Springfield Shop",
  "status": "active",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/stores/ST322LJ223223K5F4SQNR9XL5"
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


# Update Store

Updates the store identified in the path.
You can only update some store parameters.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```ruby
def update_store(store_id,
                 body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `store_id` | `String` | Template, Required | The unique identifier of the store. |
| `body` | [`UpdateStoreRequest`](../../doc/models/update-store-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`Store`](../../doc/models/store.md).

## Example Usage

```ruby
store_id = 'storeId6'

body = UpdateStoreRequest.new(
  address: UpdatableAddress1.new(
    line1: '1776 West Pinewood Avenue',
    line2: 'Heartland Building',
    line3: '',
    postal_code: '20251'
  )
)

result = account_store_level_api.update_store(
  store_id,
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
  "id": "YOUR_STORE_ID",
  "address": {
    "country": "US",
    "line1": "1776 West Pinewood Avenue",
    "line2": "Heartland Building",
    "line3": "",
    "city": "Springfield",
    "stateOrProvince": "NY",
    "postalCode": "20251"
  },
  "description": "City centre store",
  "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
  "shopperStatement": "Springfield Shop",
  "phoneNumber": "+13123456789",
  "reference": "Spring_store_2",
  "status": "active",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/stores/YOUR_STORE_ID"
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

