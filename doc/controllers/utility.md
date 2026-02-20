# Utility

```ruby
utility_api = client.utility
```

## Class Name

`UtilityApi`

## Methods

* [Get Apple Pay Session](../../doc/controllers/utility.md#get-apple-pay-session)
* [Generate Origin Keys](../../doc/controllers/utility.md#generate-origin-keys)
* [Update Pay Pal Order](../../doc/controllers/utility.md#update-pay-pal-order)
* [Validate Shopper Id](../../doc/controllers/utility.md#validate-shopper-id)


# Get Apple Pay Session

You need to use this endpoint if you have an API-only integration with Apple Pay which uses Adyen's Apple Pay certificate.

The endpoint returns the Apple Pay session data which you need to complete the [Apple Pay session validation](https://docs.adyen.com/payment-methods/apple-pay/api-only?tab=adyen-certificate-validation_1#complete-apple-pay-session-validation).

```ruby
def get_apple_pay_session(idempotency_key: nil,
                          body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `idempotency_key` | `String` | Header, Optional | A unique identifier for the message with a maximum of 64 characters (we recommend a UUID). |
| `body` | [`ApplePaySessionRequest`](../../doc/models/apple-pay-session-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ApplePaySessionResponse`](../../doc/models/apple-pay-session-response.md).

## Example Usage

```ruby
body = ApplePaySessionRequest.new(
  display_name: 'YOUR_MERCHANT_NAME',
  domain_name: 'YOUR_DOMAIN_NAME',
  merchant_identifier: 'YOUR_MERCHANT_ID'
)

result = utility_api.get_apple_pay_session(body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "data": "eyJ2Z..."
}
```


# Generate Origin Keys

**This endpoint is deprecated.**

This operation takes the origin domains and returns a JSON object containing the corresponding origin keys for the domains.

> If you're still using origin key for your Web Drop-in or Components integration, we recommend [switching to client key](https://docs.adyen.com/development-resources/client-side-authentication/migrate-from-origin-key-to-client-key). This allows you to use a single key for all origins, add or remove origins without generating a new key, and detect the card type from the number entered in your payment form.

```ruby
def generate_origin_keys(idempotency_key: nil,
                         body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `idempotency_key` | `String` | Header, Optional | A unique identifier for the message with a maximum of 64 characters (we recommend a UUID). |
| `body` | [`UtilityRequest`](../../doc/models/utility-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UtilityResponse`](../../doc/models/utility-response.md).

## Example Usage

```ruby
body = UtilityRequest.new(
  origin_domains: [
    'https://www.your-domain1.com',
    'https://www.your-domain2.com',
    'https://www.your-domain3.com'
  ]
)

result = utility_api.generate_origin_keys(body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "originKeys": {
    "https://www.your-domain1.com": "pub.v2.8116178901076090.aHR0cHM6Ly93d3cueW91ci1kb21haW4xLmNvbQ.pvbYlrXz0ICP4kwMJXDGDLVMqALhwXr1MSRjT-fkhvw",
    "https://www.your-domain3.com": "pub.v2.8116178901076090.aHR0cHM6Ly93d3cueW91ci1kb21haW4zLmNvbQ.FrTpVz7_RzAywKasM0kXCRoMfoMkKIKaxjFymRGORIc",
    "https://www.your-domain2.com": "pub.v2.8116178901076090.aHR0cHM6Ly93d3cueW91ci1kb21haW4yLmNvbQ.LdN9kvJ35fYFFiBSJA4idMnwwxJ5_yXpeNS__Ap5wkg"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 401 | Unauthorized - authentication required. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |


# Update Pay Pal Order

Updates the order for PayPal Express Checkout. This can be used to update the PayPal lightbox with an updated amount and delivery methods based on the delivery address.

```ruby
def update_pay_pal_order(idempotency_key: nil,
                         body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `idempotency_key` | `String` | Header, Optional | A unique identifier for the message with a maximum of 64 characters (we recommend a UUID). |
| `body` | [`PaypalUpdateOrderRequest`](../../doc/models/paypal-update-order-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`PaypalUpdateOrderResponse`](../../doc/models/paypal-update-order-response.md).

## Example Usage

```ruby
body = PaypalUpdateOrderRequest.new(
  amount: Amount43.new(
    currency: 'EUR',
    value: 12000
  ),
  delivery_methods: [
    DeliveryMethod.new(
      amount: Amount23.new(
        currency: 'EUR',
        value: 1000
      ),
      description: 'Express Shipping',
      reference: '1',
      selected: true,
      type: Type18::SHIPPING
    ),
    DeliveryMethod.new(
      amount: Amount23.new(
        currency: 'EUR',
        value: 500
      ),
      description: 'Standard Ground',
      reference: '2',
      selected: false,
      type: Type18::SHIPPING
    )
  ],
  payment_data: 'po7XZ...',
  psp_reference: 'DZ4DPSHB4WD2WN82'
)

result = utility_api.update_pay_pal_order(body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "paymentData": "po7XZ...",
  "status": "success"
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 401 | Unauthorized - authentication required. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |


# Validate Shopper Id

Validates the shopperId.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def validate_shopper_id(body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`ValidateShopperIdRequest`](../../doc/models/validate-shopper-id-request.md) | Body, Required | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ValidateShopperIdResponse`](../../doc/models/validate-shopper-id-response.md).

## Example Usage

```ruby
body = ValidateShopperIdRequest.new(
  merchant_account: 'merchantAccount2',
  payment_method: ShopperIdPaymentMethod1.new(
    type: 'ShopperIdPaymentMethod1'
  )
)

result = utility_api.validate_shopper_id(body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`DefaultErrorResponseEntityException`](../../doc/models/default-error-response-entity-exception.md) |
| 401 | Unauthorized - authentication required. | [`DefaultErrorResponseEntityException`](../../doc/models/default-error-response-entity-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`DefaultErrorResponseEntityException`](../../doc/models/default-error-response-entity-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`DefaultErrorResponseEntityException`](../../doc/models/default-error-response-entity-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`DefaultErrorResponseEntityException`](../../doc/models/default-error-response-entity-exception.md) |

