# Paymentlinks

```ruby
paymentlinks_api = client.paymentlinks
```

## Class Name

`PaymentlinksApi`

## Methods

* [Create Payment Link](../../doc/controllers/paymentlinks.md#create-payment-link)
* [Get Payment Link](../../doc/controllers/paymentlinks.md#get-payment-link)
* [Update Payment Link](../../doc/controllers/paymentlinks.md#update-payment-link)


# Create Payment Link

Creates a payment link to a [Pay by Link](https://docs.adyen.com/unified-commerce/pay-by-link/) page where the shopper can pay. The list of payment methods presented to the shopper depends on the `currency` and `country` parameters sent in the request.

For more information, refer to [Pay by Link documentation](https://docs.adyen.com/online-payments/pay-by-link#create-payment-links-through-api).

```ruby
def create_payment_link(idempotency_key: nil,
                        body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `idempotency_key` | `String` | Header, Optional | A unique identifier for the message with a maximum of 64 characters (we recommend a UUID). |
| `body` | [`PaymentLinkRequest`](../../doc/models/payment-link-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`PaymentLinkResponse`](../../doc/models/payment-link-response.md).

## Example Usage

```ruby
body = PaymentLinkRequest.new(
  amount: Amount34.new(
    currency: 'BRL',
    value: 1250
  ),
  merchant_account: 'YOUR_MERCHANT_ACCOUNT',
  reference: 'YOUR_ORDER_NUMBER',
  billing_address: Address3.new(
    city: 'São Paulo',
    country: 'BR',
    house_number_or_name: '999',
    postal_code: '59000060',
    street: 'Roque Petroni Jr',
    state_or_province: 'SP'
  ),
  country_code: 'BR',
  delivery_address: Address2.new(
    city: 'São Paulo',
    country: 'BR',
    house_number_or_name: '999',
    postal_code: '59000060',
    street: 'Roque Petroni Jr',
    state_or_province: 'SP'
  ),
  shopper_email: 'test@email.com',
  shopper_locale: 'pt-BR',
  shopper_reference: 'YOUR_SHOPPER_REFERENCE'
)

result = payment_links_api.create_payment_link(body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "amount": {
    "currency": "BRL",
    "value": 1250
  },
  "billingAddress": {
    "city": "São Paulo",
    "country": "BR",
    "houseNumberOrName": "999",
    "postalCode": "59000060",
    "stateOrProvince": "SP",
    "street": "Roque Petroni Jr"
  },
  "countryCode": "BR",
  "deliveryAddress": {
    "city": "São Paulo",
    "country": "BR",
    "houseNumberOrName": "999",
    "postalCode": "59000060",
    "stateOrProvince": "SP",
    "street": "Roque Petroni Jr"
  },
  "expiresAt": "2022-10-28T09:16:22Z",
  "merchantAccount": "YOUR_MERCHANT_ACCOUNT",
  "reference": "YOUR_ORDER_NUMBER",
  "reusable": false,
  "shopperEmail": "test@email.com",
  "shopperLocale": "pt-BR",
  "shopperReference": "YOUR_SHOPPER_REFERENCE",
  "id": "PLE83C39B0A0DE0C1E",
  "status": "active",
  "url": "https://test.adyen.link/PLE83C39B0A0DE0C1E"
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


# Get Payment Link

Retrieves the payment link details using the payment link `id`.

```ruby
def get_payment_link(link_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `link_id` | `String` | Template, Required | Unique identifier of the payment link. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`PaymentLinkResponse`](../../doc/models/payment-link-response.md).

## Example Usage

```ruby
link_id = 'linkId6'

result = payment_links_api.get_payment_link(link_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "amount": {
    "currency": "EUR",
    "value": 8700
  },
  "countryCode": "NL",
  "expiresAt": "2021-04-08T14:06:39Z",
  "merchantAccount": "YOUR_MERCHANT_ACCOUNT",
  "reference": "shopper-reference-ekvL83",
  "shopperLocale": "hu-HU",
  "shopperReference": "shopper-reference-LZfdWZ",
  "status": "active",
  "url": "https://test.adyen.link/PL61C53A8B97E6915A",
  "id": "PL61C53A8B97E6915A"
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


# Update Payment Link

Updates the status of a payment link. Use this endpoint to [force the expiry of a payment link](https://docs.adyen.com/online-payments/pay-by-link#update-payment-link-status).

```ruby
def update_payment_link(link_id,
                        body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `link_id` | `String` | Template, Required | Unique identifier of the payment link. |
| `body` | [`UpdatePaymentLinkRequest`](../../doc/models/update-payment-link-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`PaymentLinkResponse`](../../doc/models/payment-link-response.md).

## Example Usage

```ruby
link_id = 'linkId6'

body = UpdatePaymentLinkRequest.new(
  status: 'expired'
)

result = payment_links_api.update_payment_link(
  link_id,
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
  "amount": {
    "currency": "EUR",
    "value": 8700
  },
  "countryCode": "NL",
  "expiresAt": "2021-04-08T14:06:39Z",
  "merchantAccount": "YOUR_MERCHANT_ACCOUNT",
  "reference": "shopper-reference-ekvL83",
  "shopperLocale": "hu-HU",
  "shopperReference": "shopper-reference-LZfdWZ",
  "status": "expired",
  "url": "https://test.adyen.link/PL61C53A8B97E6915A",
  "id": "PL61C53A8B97E6915A"
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

