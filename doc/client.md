
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](../README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| connection | `Faraday::Connection` | The Faraday connection object passed by the SDK user for making requests |
| adapter | `Faraday::Adapter` | The Faraday adapter object passed by the SDK user for performing http requests |
| timeout | `Float` | The value to use for connection timeout. <br> **Default: 30** |
| max_retries | `Integer` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| retry_interval | `Float` | Pause in seconds between retries. <br> **Default: 1** |
| backoff_factor | `Float` | The amount to multiply each successive retry's interval amount by in order to provide backoff. <br> **Default: 2** |
| retry_statuses | `Array` | A list of HTTP statuses to retry. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array` | A list of HTTP methods to retry. <br> **Default: %i[get put]** |
| http_callback | `HttpCallBack` | The Http CallBack allows defining callables for pre and post API calls. |
| proxy_settings | [`ProxySettings`](../doc/proxy-settings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| logging_configuration | [`LoggingConfiguration`](../doc/logging-configuration.md) | The SDK logging configuration for API calls |
| api_key_auth_credentials | [`ApiKeyAuthCredentials`](auth/custom-header-signature.md) | The credential object for Custom Header Signature |
| basic_auth_credentials | [`BasicAuthCredentials`](auth/basic-authentication.md) | The credential object for Basic Authentication |

The API client can be initialized as follows:

## Code-Based Client Initialization

```ruby
require 'adyen_ap_is'
include AdyenApIs

client = Client.new(
  api_key_auth_credentials: ApiKeyAuthCredentials.new(
    x_api_key: 'X-API-Key'
  ),
  basic_auth_credentials: BasicAuthCredentials.new(
    username: 'Username',
    password: 'Password'
  ),
  environment: Environment::PRODUCTION,
  logging_configuration: LoggingConfiguration.new(
    log_level: Logger::INFO,
    request_logging_config: RequestLoggingConfiguration.new(
      log_body: true
    ),
    response_logging_config: ResponseLoggingConfiguration.new(
      log_headers: true
    )
  )
)
```

## Environment-Based Client Initialization

```ruby
require 'adyen_ap_is'
include AdyenApIs

# Create client from environment
client = Client.from_env
```

See the [`Environment-Based Client Initialization`](../doc/environment-based-client-initialization.md) section for details.

## Adyen APIs Client

The gateway for the SDK. This class acts as a factory for the Apis and also holds the configuration of the SDK.

## Apis

| Name | Description |
|  --- | --- |
| payments | Gets PaymentsApi |
| donations | Gets DonationsApi |
| payment_links | Gets PaymentLinksApi |
| modifications | Gets ModificationsApi |
| recurring | Gets RecurringApi |
| orders | Gets OrdersApi |
| utility | Gets UtilityApi |
| account_company_level | Gets AccountCompanyLevelApi |
| account_merchant_level | Gets AccountMerchantLevelApi |
| account_store_level | Gets AccountStoreLevelApi |
| payout_settings_merchant_level | Gets PayoutSettingsMerchantLevelApi |
| users_company_level | Gets UsersCompanyLevelApi |
| users_merchant_level | Gets UsersMerchantLevelApi |
| my_api_credential | Gets MyApiCredentialApi |
| api_credentials_company_level | Gets ApiCredentialsCompanyLevelApi |
| api_credentials_merchant_level | Gets ApiCredentialsMerchantLevelApi |
| api_key_company_level | Gets ApiKeyCompanyLevelApi |
| api_key_merchant_level | Gets ApiKeyMerchantLevelApi |
| client_key_company_level | Gets ClientKeyCompanyLevelApi |
| client_key_merchant_level | Gets ClientKeyMerchantLevelApi |
| allowed_origins_company_level | Gets AllowedOriginsCompanyLevelApi |
| allowed_origins_merchant_level | Gets AllowedOriginsMerchantLevelApi |
| webhooks_company_level | Gets WebhooksCompanyLevelApi |
| webhooks_merchant_level | Gets WebhooksMerchantLevelApi |
| payment_methods_merchant_level | Gets PaymentMethodsMerchantLevelApi |
| terminals_terminal_level | Gets TerminalsTerminalLevelApi |
| terminal_actions_company_level | Gets TerminalActionsCompanyLevelApi |
| terminal_actions_terminal_level | Gets TerminalActionsTerminalLevelApi |
| terminal_orders_company_level | Gets TerminalOrdersCompanyLevelApi |
| terminal_orders_merchant_level | Gets TerminalOrdersMerchantLevelApi |
| terminal_settings_company_level | Gets TerminalSettingsCompanyLevelApi |
| terminal_settings_merchant_level | Gets TerminalSettingsMerchantLevelApi |
| terminal_settings_store_level | Gets TerminalSettingsStoreLevelApi |
| terminal_settings_terminal_level | Gets TerminalSettingsTerminalLevelApi |
| android_files_company_level | Gets AndroidFilesCompanyLevelApi |
| split_configuration_merchant_level | Gets SplitConfigurationMerchantLevelApi |

