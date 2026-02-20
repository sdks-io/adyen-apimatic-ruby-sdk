# Recurring

```ruby
recurring_api = client.recurring
```

## Class Name

`RecurringApi`

## Methods

* [Forward Request](../../doc/controllers/recurring.md#forward-request)
* [List Stored Payment Methods](../../doc/controllers/recurring.md#list-stored-payment-methods)
* [Create Stored Payment Method](../../doc/controllers/recurring.md#create-stored-payment-method)
* [Delete Stored Payment Method](../../doc/controllers/recurring.md#delete-stored-payment-method)


# Forward Request

Forwards the payment details you stored with Adyen to a third-party that you specify and returns the response from the third-party. Supports forwarding stored card details or [network tokens](https://docs.adyen.com/online-payments/network-tokenization). For more information, see [Forward stored payment details](https://docs.adyen.com/online-payments/tokenization/forward-payment-details).

```ruby
def forward_request(idempotency_key: nil,
                    body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `idempotency_key` | `String` | Header, Optional | A unique identifier for the message with a maximum of 64 characters (we recommend a UUID). |
| `body` | [`CheckoutForwardRequest`](../../doc/models/checkout-forward-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`CheckoutForwardResponse`](../../doc/models/checkout-forward-response.md).

## Example Usage

```ruby
body = CheckoutForwardRequest.new(
  base_url: 'http://thirdparty.example.com',
  merchant_account: 'YOUR_MERCHANT_ACCOUNT',
  request: CheckoutOutgoingForwardRequest2.new(
    body: '{"amount":{"value":100,"currency":"USD"},"paymentMethod":{"creditCard":{"holderName":"{{holderName}}","number":"{{number}}","expiryMonth":"{{expiryMonth}}","expiryYear":"{{expiryYear}}"}}}',
    http_method: HttpMethod::POST,
    credentials: 'YOUR_CREDENTIALS_FOR_THE_THIRD_PARTY',
    headers: {
      'Authorization' => 'Basic {{credentials}}'
    },
    url_suffix: '/payments'
  ),
  shopper_reference: 'YOUR_SHOPPER_REFERENCE',
  stored_payment_method_id: 'M5N7TQ4TG5PFWR50'
)

result = recurring_api.forward_request(body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "storedPaymentMethodId": "M5N7TQ4TG5PFWR50",
  "pspReference": "XB7XNCQ8HXSKGK82",
  "response": {
    "status": 200,
    "headers": {
      "thirdparty-version": "2023-10-16"
    },
    "body": "{\"success\": \"ok\",\"data\": {\"tokenizeCreditCard\": {\"paymentMethod\": {\"id\": \"PAYMENT_METHOD_ID\"}}}}"
  }
}
```


# List Stored Payment Methods

Lists the tokens for stored payment details for the shopper identified in the path, if there are any available. The token ID can be used with payment requests for the shopper's payment. A summary of the stored details is included.

```ruby
def list_stored_payment_methods(shopper_reference: nil,
                                merchant_account: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `shopper_reference` | `String` | Query, Optional | Your reference to uniquely identify this shopper, for example user ID or account ID. Minimum length: 3 characters.<br><br>> Your reference must not include personally identifiable information (PII), for example name or email address. |
| `merchant_account` | `String` | Query, Optional | Your merchant account. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ListStoredPaymentMethodsResponse`](../../doc/models/list-stored-payment-methods-response.md).

## Example Usage

```ruby
result = recurring_api.list_stored_payment_methods

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "merchantAccount": "YOUR_MERCHANT_ACCOUNT",
  "shopperReference": "YOUR_SHOPPER_REFERENCE",
  "storedPaymentMethods": [
    {
      "brand": "visa",
      "expiryMonth": "10",
      "expiryYear": "30",
      "holderName": "John Smith",
      "id": "7219687191761347",
      "issuerName": "ISSUER_NAME",
      "lastFour": "1111",
      "name": "VISA",
      "shopperEmail": "john.smith@example.com",
      "shopperReference": "YOUR_SHOPPER_REFERENCE",
      "supportedRecurringProcessingModels": [
        "CardOnFile",
        "Subscription",
        "UnscheduledCardOnFile"
      ],
      "type": "scheme"
    }
  ]
}
```


# Create Stored Payment Method

Creates a token to store the shopper's payment details. This token can be used for the shopper's future payments.

```ruby
def create_stored_payment_method(idempotency_key: nil,
                                 body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `idempotency_key` | `String` | Header, Optional | A unique identifier for the message with a maximum of 64 characters (we recommend a UUID). |
| `body` | [`StoredPaymentMethodRequest`](../../doc/models/stored-payment-method-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`StoredPaymentMethodResource`](../../doc/models/stored-payment-method-resource.md).

## Example Usage

```ruby
body = StoredPaymentMethodRequest.new(
  merchant_account: 'YOUR_MERCHANT_ACCOUNT',
  payment_method: PaymentMethodToStore1.new(
    encrypted_card_number: 'test_4111111111111111',
    encrypted_expiry_month: 'test_03',
    encrypted_expiry_year: 'test_2030',
    encrypted_security_code: 'test_737',
    holder_name: 'John Smith',
    type: 'scheme'
  ),
  recurring_processing_model: RecurringProcessingModel1::SUBSCRIPTION,
  shopper_reference: 'YOUR_SHOPPER_REFERENCE',
  shopper_email: 's.hopper@test.com',
  shopper_ip: '192.0.2.1'
)

result = recurring_api.create_stored_payment_method(body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "expiryMonth": "03",
  "expiryYear": "2030",
  "holderName": "John Smith",
  "id": "KHQC5N7G84BLNK43",
  "lastFour": "1111",
  "shopperReference": "YOUR_SHOPPER_REFERENCE",
  "type": "scheme"
}
```


# Delete Stored Payment Method

Deletes the token identified in the path. The token can no longer be used with payment requests.

```ruby
def delete_stored_payment_method(stored_payment_method_id,
                                 shopper_reference,
                                 merchant_account)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `stored_payment_method_id` | `String` | Template, Required | The unique identifier of the token. |
| `shopper_reference` | `String` | Query, Required | Your reference to uniquely identify this shopper, for example user ID or account ID. Minimum length: 3 characters.<br><br>> Your reference must not include personally identifiable information (PII), for example name or email address. |
| `merchant_account` | `String` | Query, Required | Your merchant account. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```ruby
stored_payment_method_id = 'storedPaymentMethodId4'

shopper_reference = 'shopperReference8'

merchant_account = 'merchantAccount8'

result = recurring_api.delete_stored_payment_method(
  stored_payment_method_id,
  shopper_reference,
  merchant_account
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

