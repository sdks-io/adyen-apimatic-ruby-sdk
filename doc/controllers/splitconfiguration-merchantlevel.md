# Splitconfiguration-Merchantlevel

```ruby
splitconfiguration_merchantlevel_api = client.splitconfiguration_merchantlevel
```

## Class Name

`SplitconfigurationMerchantlevelApi`

## Methods

* [List Split Configurations](../../doc/controllers/splitconfiguration-merchantlevel.md#list-split-configurations)
* [Create Split Configuration](../../doc/controllers/splitconfiguration-merchantlevel.md#create-split-configuration)
* [Delete Split Configuration](../../doc/controllers/splitconfiguration-merchantlevel.md#delete-split-configuration)
* [Get Split Configuration](../../doc/controllers/splitconfiguration-merchantlevel.md#get-split-configuration)
* [Update Split Configuration](../../doc/controllers/splitconfiguration-merchantlevel.md#update-split-configuration)
* [Create Split Configuration Rule](../../doc/controllers/splitconfiguration-merchantlevel.md#create-split-configuration-rule)
* [Delete Split Configuration Rule](../../doc/controllers/splitconfiguration-merchantlevel.md#delete-split-configuration-rule)
* [Update Split Configuration Rule](../../doc/controllers/splitconfiguration-merchantlevel.md#update-split-configuration-rule)
* [Update Split Logic](../../doc/controllers/splitconfiguration-merchantlevel.md#update-split-logic)


# List Split Configurations

Returns the list of split configuration profiles for the merchant account.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API - SplitConfiguration read and write

```ruby
def list_split_configurations(merchant_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`SplitConfigurationList`](../../doc/models/split-configuration-list.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

result = split_configuration_merchant_level_api.list_split_configurations(merchant_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "description": "Your description for the split configuration",
      "rules": [
        {
          "currency": "GBP",
          "fundingSource": "ANY",
          "paymentMethod": "ANY",
          "ruleId": "SCRL4224P22322585HP89PPCST6BCZ",
          "shopperInteraction": "ANY",
          "splitLogic": {
            "additionalCommission": {
              "fixedAmount": 100,
              "variablePercentage": 100,
              "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
            },
            "chargeback": "deductFromLiableAccount",
            "commission": {
              "fixedAmount": 200,
              "variablePercentage": 100
            },
            "splitLogicId": "SCLG4224P22322585HP89PPCSV27VP",
            "paymentFee": "deductFromLiableAccount",
            "remainder": "addToOneBalanceAccount",
            "tip": "addToOneBalanceAccount"
          }
        }
      ],
      "splitConfigurationId": "SCNF4224P22322585HP89PPCSS24MF"
    },
    {
      "description": "Your description for the second split configuration",
      "rules": [
        {
          "currency": "ANY",
          "fundingSource": "ANY",
          "paymentMethod": "ANY",
          "ruleId": "SCRL4224P22322585HPCX384JW65VW",
          "shopperInteraction": "ANY",
          "splitLogic": {
            "additionalCommission": {
              "fixedAmount": 10,
              "variablePercentage": 50,
              "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
            },
            "chargeback": "deductFromLiableAccount",
            "commission": {
              "fixedAmount": 10,
              "variablePercentage": 100
            },
            "splitLogicId": "SCLG4224P22322585HPCX384JX52M2",
            "paymentFee": "deductFromLiableAccount",
            "remainder": "addToOneBalanceAccount",
            "tip": "addToOneBalanceAccount"
          }
        },
        {
          "currency": "EUR",
          "fundingSource": "ANY",
          "paymentMethod": "visa",
          "ruleId": "SCRL4224P22322585HPCX5V4KV6L2R",
          "shopperInteraction": "ANY",
          "splitLogic": {
            "additionalCommission": {
              "fixedAmount": 100,
              "variablePercentage": 0,
              "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
            },
            "chargeback": "deductFromLiableAccount",
            "commission": {
              "fixedAmount": 100,
              "variablePercentage": 100
            },
            "splitLogicId": "SCLG4224P22322585HPCX5V4KW26C9",
            "paymentFee": "deductFromLiableAccount",
            "remainder": "addToLiableAccount",
            "tip": "addToLiableAccount"
          }
        }
      ],
      "splitConfigurationId": "SCNF4224P22322585HPCX384JV6JGX"
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


# Create Split Configuration

Creates a split configuration profile to [split payments automatically](https://docs.adyen.com/platforms/automatic-split-configuration/). After you [associate it with a store](https://docs.adyen.com/api-explorer/Management/latest/patch/merchants/(merchantId)/stores/(storeId)#request-splitConfiguration) in your merchant account, it splits the funds of all transactions processed through that store between your liable balance account and [your user's balance account](https://docs.adyen.com/api-explorer/Management/latest/patch/merchants/(merchantId)/stores/(storeId)#request-splitConfiguration-balanceAccountId).

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API - SplitConfiguration read and write

```ruby
def create_split_configuration(merchant_id,
                               body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `body` | [`SplitConfiguration`](../../doc/models/split-configuration.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`SplitConfiguration`](../../doc/models/split-configuration.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

body = SplitConfiguration.new(
  description: 'Your description for the split configuration',
  rules: [
    SplitConfigurationRule.new(
      currency: 'ANY',
      funding_source: FundingSource1::ANY,
      payment_method: 'ANY',
      shopper_interaction: ShopperInteraction11::ANY,
      split_logic: SplitConfigurationLogic2.new(
        commission: Commission1.new(
          fixed_amount: 10,
          variable_percentage: 100
        ),
        additional_commission: AdditionalCommission1.new(
          balance_account_id: 'BA3227C223222H5HQ2XX77VVH',
          fixed_amount: 10,
          variable_percentage: 50
        ),
        chargeback: Behavior::DEDUCTFROMLIABLEACCOUNT,
        payment_fee: PaymentFee::DEDUCTFROMLIABLEACCOUNT,
        remainder: Remainder::ADDTOONEBALANCEACCOUNT,
        tip: Tip::ADDTOONEBALANCEACCOUNT
      )
    )
  ]
)

result = split_configuration_merchant_level_api.create_split_configuration(
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
  "description": "Your description for the split configuration",
  "rules": [
    {
      "currency": "ANY",
      "fundingSource": "ANY",
      "paymentMethod": "ANY",
      "ruleId": "SCRL4224P22322585HPCX384JW65VW",
      "shopperInteraction": "ANY",
      "splitLogic": {
        "additionalCommission": {
          "fixedAmount": 10,
          "variablePercentage": 50,
          "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
        },
        "chargeback": "deductFromLiableAccount",
        "commission": {
          "fixedAmount": 10,
          "variablePercentage": 100
        },
        "splitLogicId": "SCLG4224P22322585HPCX384JX52M2",
        "paymentFee": "deductFromLiableAccount",
        "remainder": "addToOneBalanceAccount",
        "tip": "addToOneBalanceAccount"
      }
    }
  ],
  "splitConfigurationId": "SCNF4224P22322585HPCX384JV6JGX"
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


# Delete Split Configuration

Deletes the split configuration profile specified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API - SplitConfiguration read and write

```ruby
def delete_split_configuration(merchant_id,
                               split_configuration_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `split_configuration_id` | `String` | Template, Required | The unique identifier of the split configuration. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`SplitConfiguration`](../../doc/models/split-configuration.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

split_configuration_id = 'splitConfigurationId4'

result = split_configuration_merchant_level_api.delete_split_configuration(
  merchant_id,
  split_configuration_id
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


# Get Split Configuration

Returns the details of the split configuration profile specified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API - SplitConfiguration read and write

```ruby
def get_split_configuration(merchant_id,
                            split_configuration_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `split_configuration_id` | `String` | Template, Required | The unique identifier of the split configuration. |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`SplitConfiguration`](../../doc/models/split-configuration.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

split_configuration_id = 'splitConfigurationId4'

result = split_configuration_merchant_level_api.get_split_configuration(
  merchant_id,
  split_configuration_id
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
  "description": "Your description for the split configuration",
  "rules": [
    {
      "currency": "ANY",
      "fundingSource": "ANY",
      "paymentMethod": "ANY",
      "ruleId": "SCRL4224P22322585HPCX384JW65VW",
      "shopperInteraction": "ANY",
      "splitLogic": {
        "additionalCommission": {
          "fixedAmount": 10,
          "variablePercentage": 50,
          "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
        },
        "chargeback": "deductFromLiableAccount",
        "commission": {
          "fixedAmount": 10,
          "variablePercentage": 100
        },
        "splitLogicId": "SCLG4224P22322585HPCX384JX52M2",
        "paymentFee": "deductFromLiableAccount",
        "remainder": "addToOneBalanceAccount",
        "tip": "addToOneBalanceAccount"
      }
    },
    {
      "currency": "EUR",
      "fundingSource": "ANY",
      "paymentMethod": "visa",
      "ruleId": "SCRL4224P22322585HPCX5V4KV6L2R",
      "shopperInteraction": "ANY",
      "splitLogic": {
        "additionalCommission": {
          "fixedAmount": 100,
          "variablePercentage": 0,
          "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
        },
        "chargeback": "deductFromLiableAccount",
        "commission": {
          "fixedAmount": 100,
          "variablePercentage": 100
        },
        "splitLogicId": "SCLG4224P22322585HPCX5V4KW26C9",
        "paymentFee": "deductFromLiableAccount",
        "remainder": "addToLiableAccount",
        "tip": "addToLiableAccount"
      }
    }
  ],
  "splitConfigurationId": "SCNF4224P22322585HPCX384JV6JGX"
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


# Update Split Configuration

Changes the description of the split configuration profile specified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API - SplitConfiguration read and write

```ruby
def update_split_configuration(merchant_id,
                               split_configuration_id,
                               body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `split_configuration_id` | `String` | Template, Required | The unique identifier of the split configuration. |
| `body` | [`UpdateSplitConfigurationRequest`](../../doc/models/update-split-configuration-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`SplitConfiguration`](../../doc/models/split-configuration.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

split_configuration_id = 'splitConfigurationId4'

body = UpdateSplitConfigurationRequest.new(
  description: 'Updated description for the split configuration'
)

result = split_configuration_merchant_level_api.update_split_configuration(
  merchant_id,
  split_configuration_id,
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
  "description": "Updated description for the split configuration",
  "rules": [
    {
      "currency": "ANY",
      "fundingSource": "ANY",
      "paymentMethod": "ANY",
      "ruleId": "SCRL4224P22322585HPCX384JW65VW",
      "shopperInteraction": "ANY",
      "splitLogic": {
        "additionalCommission": {
          "fixedAmount": 10,
          "variablePercentage": 50,
          "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
        },
        "chargeback": "deductFromLiableAccount",
        "commission": {
          "fixedAmount": 10,
          "variablePercentage": 100
        },
        "splitLogicId": "SCLG4224P22322585HPCX384JX52M2",
        "paymentFee": "deductFromLiableAccount",
        "remainder": "addToOneBalanceAccount",
        "tip": "addToOneBalanceAccount"
      }
    },
    {
      "currency": "EUR",
      "fundingSource": "ANY",
      "paymentMethod": "visa",
      "ruleId": "SCRL4224P22322585HPCX5V4KV6L2R",
      "shopperInteraction": "ANY",
      "splitLogic": {
        "additionalCommission": {
          "fixedAmount": 100,
          "variablePercentage": 0,
          "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
        },
        "chargeback": "deductFromLiableAccount",
        "commission": {
          "fixedAmount": 100,
          "variablePercentage": 100
        },
        "splitLogicId": "SCLG4224P22322585HPCX5V4KW26C9",
        "paymentFee": "deductFromLiableAccount",
        "remainder": "addToLiableAccount",
        "tip": "addToLiableAccount"
      }
    }
  ],
  "splitConfigurationId": "SCNF4224P22322585HPCX384JV6JGX"
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


# Create Split Configuration Rule

[Creates a rule](https://docs.adyen.com/platforms/automatic-split-configuration/manage-split-configurations/api/#create-rule) in the split configuration profile specified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API - SplitConfiguration read and write

```ruby
def create_split_configuration_rule(merchant_id,
                                    split_configuration_id,
                                    body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `split_configuration_id` | `String` | Template, Required | The unique identifier of the split configuration. |
| `body` | [`SplitConfigurationRule`](../../doc/models/split-configuration-rule.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`SplitConfiguration`](../../doc/models/split-configuration.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

split_configuration_id = 'splitConfigurationId4'

body = SplitConfigurationRule.new(
  currency: 'USD',
  funding_source: FundingSource1::ANY,
  payment_method: 'visa',
  shopper_interaction: ShopperInteraction11::POS,
  split_logic: SplitConfigurationLogic2.new(
    commission: Commission1.new(
      fixed_amount: 10,
      variable_percentage: 100
    ),
    additional_commission: AdditionalCommission1.new(
      balance_account_id: 'BA3227C223222H5HQ2XX77VVH',
      fixed_amount: 10,
      variable_percentage: 50
    ),
    chargeback: Behavior::DEDUCTFROMLIABLEACCOUNT,
    payment_fee: PaymentFee::DEDUCTFROMLIABLEACCOUNT,
    remainder: Remainder::ADDTOLIABLEACCOUNT,
    tip: Tip::ADDTOONEBALANCEACCOUNT
  )
)

result = split_configuration_merchant_level_api.create_split_configuration_rule(
  merchant_id,
  split_configuration_id,
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
  "description": "My first split configuration",
  "rules": [
    {
      "currency": "ANY",
      "fundingSource": "ANY",
      "paymentMethod": "ANY",
      "ruleId": "SCRL4224P22322585HPCX384JW65VW",
      "shopperInteraction": "ANY",
      "splitLogic": {
        "additionalCommission": {
          "fixedAmount": 10,
          "variablePercentage": 50,
          "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
        },
        "chargeback": "deductFromLiableAccount",
        "commission": {
          "fixedAmount": 10,
          "variablePercentage": 100
        },
        "splitLogicId": "SCLG4224P22322585HPCX384JX52M2",
        "paymentFee": "deductFromLiableAccount",
        "remainder": "addToOneBalanceAccount",
        "tip": "addToOneBalanceAccount"
      }
    },
    {
      "currency": "USD",
      "fundingSource": "ANY",
      "paymentMethod": "visa",
      "ruleId": "SCRL4224P22322585HPCX5V4KV6L2R",
      "shopperInteraction": "POS",
      "splitLogic": {
        "additionalCommission": {
          "fixedAmount": 10,
          "variablePercentage": 50,
          "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
        },
        "chargeback": "deductFromLiableAccount",
        "commission": {
          "fixedAmount": 10,
          "variablePercentage": 100
        },
        "splitLogicId": "SCLG4224P22322585HPCX5V4KW26C9",
        "paymentFee": "deductFromLiableAccount",
        "remainder": "addToLiableAccount",
        "tip": "addToOneBalanceAccount"
      }
    }
  ],
  "splitConfigurationId": "SCNF4224P22322585HPCX384JV6JGX"
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


# Delete Split Configuration Rule

Deletes the rule specified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API - SplitConfiguration read and write

```ruby
def delete_split_configuration_rule(merchant_id,
                                    split_configuration_id,
                                    rule_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `split_configuration_id` | `String` | Template, Required | The unique identifier of the split configuration. |
| `rule_id` | `String` | Template, Required | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`SplitConfiguration`](../../doc/models/split-configuration.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

split_configuration_id = 'splitConfigurationId4'

rule_id = 'ruleId4'

result = split_configuration_merchant_level_api.delete_split_configuration_rule(
  merchant_id,
  split_configuration_id,
  rule_id
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


# Update Split Configuration Rule

Changes the [split conditions of the rule](https://docs.adyen.com/platforms/automatic-split-configuration/manage-split-configurations/api/#update-condition) specified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API - SplitConfiguration read and write

```ruby
def update_split_configuration_rule(merchant_id,
                                    split_configuration_id,
                                    rule_id,
                                    body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `split_configuration_id` | `String` | Template, Required | The identifier of the split configuration. |
| `rule_id` | `String` | Template, Required | The unique identifier of the split configuration rule. |
| `body` | [`UpdateSplitConfigurationRuleRequest`](../../doc/models/update-split-configuration-rule-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`SplitConfiguration`](../../doc/models/split-configuration.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

split_configuration_id = 'splitConfigurationId4'

rule_id = 'ruleId4'

body = UpdateSplitConfigurationRuleRequest.new(
  currency: 'EUR',
  funding_source: 'ANY',
  payment_method: 'visa',
  shopper_interaction: 'ANY'
)

result = split_configuration_merchant_level_api.update_split_configuration_rule(
  merchant_id,
  split_configuration_id,
  rule_id,
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
  "description": "Your description for the split configuration",
  "rules": [
    {
      "currency": "ANY",
      "fundingSource": "ANY",
      "paymentMethod": "ANY",
      "ruleId": "SCRL4224P22322585HPCX384JW65VW",
      "shopperInteraction": "ANY",
      "splitLogic": {
        "additionalCommission": {
          "fixedAmount": 10,
          "variablePercentage": 50,
          "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
        },
        "chargeback": "deductFromLiableAccount",
        "commission": {
          "fixedAmount": 10,
          "variablePercentage": 100
        },
        "splitLogicId": "SCLG4224P22322585HPCX384JX52M2",
        "paymentFee": "deductFromLiableAccount",
        "remainder": "addToOneBalanceAccount",
        "tip": "addToOneBalanceAccount"
      }
    },
    {
      "currency": "EUR",
      "fundingSource": "ANY",
      "paymentMethod": "visa",
      "ruleId": "SCRL4224P22322585HPCX5V4KV6L2R",
      "shopperInteraction": "ANY",
      "splitLogic": {
        "additionalCommission": {
          "fixedAmount": 10,
          "variablePercentage": 50,
          "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
        },
        "chargeback": "deductFromLiableAccount",
        "commission": {
          "fixedAmount": 10,
          "variablePercentage": 100
        },
        "splitLogicId": "SCLG4224P22322585HPCX5V4KW26C9",
        "paymentFee": "deductFromLiableAccount",
        "remainder": "addToLiableAccount",
        "tip": "addToOneBalanceAccount"
      }
    }
  ],
  "splitConfigurationId": "SCNF4224P22322585HPCX384JV6JGX"
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


# Update Split Logic

Changes the [split logic](https://docs.adyen.com/platforms/automatic-split-configuration/manage-split-configurations/api/#update-split-logic) specified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API - SplitConfiguration read and write

```ruby
def update_split_logic(merchant_id,
                       split_configuration_id,
                       rule_id,
                       split_logic_id,
                       body: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `String` | Template, Required | The unique identifier of the merchant account. |
| `split_configuration_id` | `String` | Template, Required | The unique identifier of the split configuration. |
| `rule_id` | `String` | Template, Required | The unique identifier of the split configuration rule. |
| `split_logic_id` | `String` | Template, Required | The unique identifier of the split configuration split. |
| `body` | [`UpdateSplitConfigurationLogicRequest`](../../doc/models/update-split-configuration-logic-request.md) | Body, Optional | - |

## Server

`Server::DEFAULT1`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`SplitConfiguration`](../../doc/models/split-configuration.md).

## Example Usage

```ruby
merchant_id = 'merchantId6'

split_configuration_id = 'splitConfigurationId4'

rule_id = 'ruleId4'

split_logic_id = 'splitLogicId4'

body = UpdateSplitConfigurationLogicRequest.new(
  commission: Commission1.new(
    fixed_amount: 100,
    variable_percentage: 100
  ),
  additional_commission: AdditionalCommission1.new(
    balance_account_id: 'BA3227C223222H5HQ2XX77VVH',
    fixed_amount: 100,
    variable_percentage: 0
  ),
  chargeback: Behavior::DEDUCTFROMLIABLEACCOUNT,
  payment_fee: PaymentFee::DEDUCTFROMLIABLEACCOUNT,
  remainder: Remainder::ADDTOLIABLEACCOUNT,
  tip: Tip::ADDTOLIABLEACCOUNT
)

result = split_configuration_merchant_level_api.update_split_logic(
  merchant_id,
  split_configuration_id,
  rule_id,
  split_logic_id,
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
  "description": "Your description for the split configuration",
  "rules": [
    {
      "currency": "ANY",
      "fundingSource": "ANY",
      "paymentMethod": "ANY",
      "ruleId": "SCRL4224P22322585HPCX384JW65VW",
      "shopperInteraction": "ANY",
      "splitLogic": {
        "additionalCommission": {
          "fixedAmount": 10,
          "variablePercentage": 50,
          "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
        },
        "chargeback": "deductFromLiableAccount",
        "commission": {
          "fixedAmount": 10,
          "variablePercentage": 100
        },
        "splitLogicId": "SCLG4224P22322585HPCX384JX52M2",
        "paymentFee": "deductFromLiableAccount",
        "remainder": "addToOneBalanceAccount",
        "tip": "addToOneBalanceAccount"
      }
    },
    {
      "currency": "EUR",
      "fundingSource": "ANY",
      "paymentMethod": "visa",
      "ruleId": "SCRL4224P22322585HPCX5V4KV6L2R",
      "shopperInteraction": "ANY",
      "splitLogic": {
        "additionalCommission": {
          "fixedAmount": 100,
          "variablePercentage": 0,
          "balanceAccountId": "BA3227C223222H5HQ2XX77VVH"
        },
        "chargeback": "deductFromLiableAccount",
        "commission": {
          "fixedAmount": 100,
          "variablePercentage": 100
        },
        "splitLogicId": "SCLG4224P22322585HPCX5V4KW26C9",
        "paymentFee": "deductFromLiableAccount",
        "remainder": "addToLiableAccount",
        "tip": "addToLiableAccount"
      }
    }
  ],
  "splitConfigurationId": "SCNF4224P22322585HPCX384JV6JGX"
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

