
# Custom Header Signature



Documentation for accessing and setting credentials for ApiKeyAuth.

## Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| X-API-Key | `String` | - | `x_api_key` |



**Note:** Auth credentials can be set using `ApiKeyAuthCredentials` object, passed in as named parameter `api_key_auth_credentials` in the client initialization.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```ruby
require 'adyen_ap_is'
include AdyenApIs

client = Client.new(
  api_key_auth_credentials: ApiKeyAuthCredentials.new(
    x_api_key: 'X-API-Key'
  )
)
```


