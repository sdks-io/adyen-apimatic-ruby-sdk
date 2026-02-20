# Payoutsettings-Merchantlevel

```ruby
payoutsettings_merchantlevel_api = client.payoutsettings_merchantlevel
```

## Class Name

`PayoutsettingsMerchantlevelApi`

## Methods

* [List Payout Settings](../../doc/controllers/payoutsettings-merchantlevel.md#list-payout-settings)
* [Create Payout Setting](../../doc/controllers/payoutsettings-merchantlevel.md#create-payout-setting)
* [Delete Payout Setting](../../doc/controllers/payoutsettings-merchantlevel.md#delete-payout-setting)
* [Get Payout Setting](../../doc/controllers/payoutsettings-merchantlevel.md#get-payout-setting)
* [Update Payout Setting](../../doc/controllers/payoutsettings-merchantlevel.md#update-payout-setting)


# List Payout Settings

Returns the list of payout settings for the merchant account identified in the path.

Use this endpoint if your integration requires it, such as Adyen for Platforms Manage. Your Adyen contact will set up your access.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payout account settings read

```ruby
def list_payout_settings(merchant_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`PayoutSettingsResponse`](../../doc/models/payout-settings-response.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

result = payout_settings_merchant_level_api.list_payout_settings(merchant_id)

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


# Create Payout Setting

Sends a request to add a payout setting for the merchant account specified in the path. A payout setting links the merchant account to the [transfer instrument](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/transferInstruments) that contains the details of the payout bank account. Adyen verifies the bank account before allowing and enabling the payout setting.

If you're accepting payments in multiple currencies, you may add multiple payout settings for the merchant account.

Use this endpoint if your integration requires it, such as Adyen for Platforms Manage. Your Adyen contact will set up your access.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payout account settings read and write

```ruby
def create_payout_setting(merchant_id,
                          body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `body` | [`PayoutSettingsRequest`](../../doc/models/payout-settings-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`PayoutSettings`](../../doc/models/payout-settings.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

result = payout_settings_merchant_level_api.create_payout_setting(merchant_id)

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


# Delete Payout Setting

Deletes the payout setting identified in the path.

Use this endpoint if your integration requires it, such as Adyen for Platforms Manage. Your Adyen contact will set up your access.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payout account settings read and write

```ruby
def delete_payout_setting(merchant_id,
                          payout_settings_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `payout_settings_id` | `String` | Template, Required | The unique identifier of the payout setting. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```ruby
merchant_id = 'merchantId6'

payout_settings_id = 'payoutSettingsId6'

result = payout_settings_merchant_level_api.delete_payout_setting(
  merchant_id,
  payout_settings_id
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


# Get Payout Setting

Returns the payout setting identified in the path.

Use this endpoint if your integration requires it, such as Adyen for Platforms Manage. Your Adyen contact will set up your access.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payout account settings read

```ruby
def get_payout_setting(merchant_id,
                       payout_settings_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `payout_settings_id` | `String` | Template, Required | The unique identifier of the payout setting. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`PayoutSettings`](../../doc/models/payout-settings.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

payout_settings_id = 'payoutSettingsId6'

result = payout_settings_merchant_level_api.get_payout_setting(
  merchant_id,
  payout_settings_id
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


# Update Payout Setting

Updates the payout setting identified in the path. You can enable or disable the payout setting.

Use this endpoint if your integration requires it, such as Adyen for Platforms Manage. Your Adyen contact will set up your access.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payout account settings read and write

```ruby
def update_payout_setting(merchant_id,
                          payout_settings_id,
                          body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `payout_settings_id` | `String` | Template, Required | The unique identifier of the payout setting. |
| `body` | [`UpdatePayoutSettingsRequest`](../../doc/models/update-payout-settings-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`PayoutSettings`](../../doc/models/payout-settings.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

payout_settings_id = 'payoutSettingsId6'

result = payout_settings_merchant_level_api.update_payout_setting(
  merchant_id,
  payout_settings_id
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

