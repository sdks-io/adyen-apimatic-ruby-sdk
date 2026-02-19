# Paymentmethods-Merchantlevel

```ruby
paymentmethods_merchantlevel_api = client.paymentmethods_merchantlevel
```

## Class Name

`PaymentmethodsMerchantlevelApi`

## Methods

* [Get-Merchants-Merchant Id-Payment Method Settings](../../doc/controllers/paymentmethods-merchantlevel.md#get-merchants-merchant-id-payment-method-settings)
* [Post-Merchants-Merchant Id-Payment Method Settings](../../doc/controllers/paymentmethods-merchantlevel.md#post-merchants-merchant-id-payment-method-settings)
* [Get-Merchants-Merchant Id-Payment Method Settings-Payment Method Id](../../doc/controllers/paymentmethods-merchantlevel.md#get-merchants-merchant-id-payment-method-settings-payment-method-id)
* [Patch-Merchants-Merchant Id-Payment Method Settings-Payment Method Id](../../doc/controllers/paymentmethods-merchantlevel.md#patch-merchants-merchant-id-payment-method-settings-payment-method-id)
* [Post-Merchants-Merchant Id-Payment Method Settings-Payment Method Id-Add Apple Pay Domains](../../doc/controllers/paymentmethods-merchantlevel.md#post-merchants-merchant-id-payment-method-settings-payment-method-id-add-apple-pay-domains)
* [Get-Merchants-Merchant Id-Payment Method Settings-Payment Method Id-Get Apple Pay Domains](../../doc/controllers/paymentmethods-merchantlevel.md#get-merchants-merchant-id-payment-method-settings-payment-method-id-get-apple-pay-domains)


# Get-Merchants-Merchant Id-Payment Method Settings

Returns details for all payment methods of the merchant account identified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payment methods read

```ruby
def get_merchants_merchant_id_payment_method_settings(merchant_id,
                                                      store_id: nil,
                                                      business_line_id: nil,
                                                      page_size: nil,
                                                      page_number: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `store_id` | `String` | Query, Optional | The unique identifier of the store for which to return the payment methods. |
| `business_line_id` | `String` | Query, Optional | The unique identifier of the Business Line for which to return the payment methods. |
| `page_size` | `Integer` | Query, Optional | The number of items to have on a page, maximum 100. The default is 10 items on a page. |
| `page_number` | `Integer` | Query, Optional | The number of the page to fetch. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`PaymentMethodResponse`](../../doc/models/payment-method-response.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

result = payment_methods_merchant_level_api.get_merchants_merchant_id_payment_method_settings(merchant_id)

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
| 429 | - | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Post-Merchants-Merchant Id-Payment Method Settings

Sends a request to add a new payment method to the merchant account identified in the path.
Depending the payment method [`type`](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/_merchantId_/paymentMethodSettings#request-type), you may need to send an additional object required for the payment method.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payment methods read and write

```ruby
def post_merchants_merchant_id_payment_method_settings(merchant_id,
                                                       body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `body` | [`PaymentMethodSetupInfo`](../../doc/models/payment-method-setup-info.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`PaymentMethod1`](../../doc/models/payment-method-1.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

body = PaymentMethodSetupInfo.new(
  type: Type410::VISA,
  countries: [
    'US'
  ],
  currencies: [
    'USD'
  ]
)

result = payment_methods_merchant_level_api.post_merchants_merchant_id_payment_method_settings(
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
  "id": "PM3227C223224K5FH84M8CBNH",
  "type": "visa",
  "countries": [
    "US"
  ],
  "currencies": [
    "USD"
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
| 429 | - | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Get-Merchants-Merchant Id-Payment Method Settings-Payment Method Id

Returns details for the merchant account and the payment method identified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payment methods read

```ruby
def get_merchants_merchant_id_payment_method_settings_payment_method_id(merchant_id,
                                                                        payment_method_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `payment_method_id` | `String` | Template, Required | The unique identifier of the payment method. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`PaymentMethod1`](../../doc/models/payment-method-1.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

payment_method_id = 'paymentMethodId2'

result = payment_methods_merchant_level_api.get_merchants_merchant_id_payment_method_settings_payment_method_id(
  merchant_id,
  payment_method_id
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
| 429 | - | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Patch-Merchants-Merchant Id-Payment Method Settings-Payment Method Id

Updates payment method details for the merchant account and the payment method identified in the path.
Depending the payment method [`type`](https://docs.adyen.com/api-explorer/Management/latest/patch/merchants/_merchantId_/paymentMethodSettings#request-type), you may need to send an additional object required for the payment method.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payment methods read and write

```ruby
def patch_merchants_merchant_id_payment_method_settings_payment_method_id(merchant_id,
                                                                          payment_method_id,
                                                                          body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `payment_method_id` | `String` | Template, Required | The unique identifier of the payment method. |
| `body` | [`UpdatePaymentMethodInfo`](../../doc/models/update-payment-method-info.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`PaymentMethod1`](../../doc/models/payment-method-1.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

payment_method_id = 'paymentMethodId2'

body = UpdatePaymentMethodInfo.new(
  countries: [
    'NL'
  ],
  currencies: [
    'EUR'
  ]
)

result = payment_methods_merchant_level_api.patch_merchants_merchant_id_payment_method_settings_payment_method_id(
  merchant_id,
  payment_method_id,
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
  "mc": {
    "transactionDescription": {
      "doingBusinessAsName": "YOUR_BUSINESS_NAME",
      "type": "fixed"
    }
  },
  "id": "PM322DZ243226G5LKBTGM7FBQ",
  "type": "mc",
  "enabled": true,
  "countries": [
    "NL"
  ],
  "currencies": [
    "EUR"
  ],
  "customRoutingFlags": []
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 401 | Unauthorized - authentication required. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 429 | - | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Post-Merchants-Merchant Id-Payment Method Settings-Payment Method Id-Add Apple Pay Domains

Adds the new domain to the list of Apple Pay domains that are registered with the merchant account and the payment method identified in the path. For more information, see [Apple Pay documentation](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in/?tab=adyen-certificate-live_1#going-live).

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payment methods read and write

```ruby
def post_merchants_merchant_id_payment_method_settings_payment_method_id_add_apple_pay_domains(merchant_id,
                                                                                               payment_method_id,
                                                                                               body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `payment_method_id` | `String` | Template, Required | The unique identifier of the payment method. |
| `body` | [`ApplePayInfo`](../../doc/models/apple-pay-info.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```ruby
merchant_id = 'merchantId6'

payment_method_id = 'paymentMethodId2'

body = ApplePayInfo.new(
  domains: [
    'https://example.com'
  ]
)

result = payment_methods_merchant_level_api.post_merchants_merchant_id_payment_method_settings_payment_method_id_add_apple_pay_domains(
  merchant_id,
  payment_method_id,
  body: body
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
| 429 | - | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Get-Merchants-Merchant Id-Payment Method Settings-Payment Method Id-Get Apple Pay Domains

Returns all Apple Pay domains that are registered with the merchant account and the payment method identified in the path. For more information, see [Apple Pay documentation](https://docs.adyen.com/payment-methods/apple-pay/enable-apple-pay#register-merchant-domain).

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payment methods read

```ruby
def get_merchants_merchant_id_payment_method_settings_payment_method_id_get_apple_pay_domains(merchant_id,
                                                                                              payment_method_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `payment_method_id` | `String` | Template, Required | The unique identifier of the payment method. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ApplePayInfo`](../../doc/models/apple-pay-info.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

payment_method_id = 'paymentMethodId2'

result = payment_methods_merchant_level_api.get_merchants_merchant_id_payment_method_settings_payment_method_id_get_apple_pay_domains(
  merchant_id,
  payment_method_id
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

