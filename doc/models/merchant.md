
# Merchant

## Structure

`Merchant`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `links` | [`MerchantLinks2`](../../doc/models/merchant-links-2.md) | Optional | References to resources connected with this merchant. |
| `capture_delay` | `String` | Optional | The [capture delay](https://docs.adyen.com/online-payments/capture#capture-delay) set for the merchant account.<br><br>Possible values:<br><br>* **Immediate**<br>* **Manual**<br>* Number of days from **1** to **29** |
| `company_id` | `String` | Optional | The unique identifier of the company account this merchant belongs to |
| `data_centers` | [`Array[DataCenter]`](../../doc/models/data-center.md) | Optional | List of available data centers.<br><br>Adyen has several data centers around the world.In the URL that you use for making API requests, we recommend you use the live URL prefix from the data center closest to your shoppers. |
| `default_shopper_interaction` | `String` | Optional | The default [`shopperInteraction`](https://docs.adyen.com/api-explorer/#/CheckoutService/v68/post/payments__reqParam_shopperInteraction) value used when processing payments through this merchant account. |
| `description` | `String` | Optional | Your description for the merchant account, maximum 300 characters |
| `id` | `String` | Optional | The unique identifier of the merchant account. |
| `merchant_city` | `String` | Optional | The city where the legal entity of this merchant account is registered. |
| `name` | `String` | Optional | The name of the legal entity associated with the merchant account. |
| `pricing_plan` | `String` | Optional | Only applies to merchant accounts managed by Adyen's partners. The name of the pricing plan assigned to the merchant account. |
| `primary_settlement_currency` | `String` | Optional | The currency of the country where the legal entity of this merchant account is registered. Format: [ISO currency code](https://docs.adyen.com/development-resources/currency-codes). For example, a legal entity based in the United States has USD as the primary settlement currency. |
| `reference` | `String` | Optional | Reference of the merchant account. |
| `shop_web_address` | `String` | Optional | The URL for the ecommerce website used with this merchant account. |
| `status` | `String` | Optional | The status of the merchant account.<br><br>Possible values:<br><br>* **PreActive**: The merchant account has been created. Users cannot access the merchant account in the Customer Area. The account cannot process payments.<br>* **Active**: Users can access the merchant account in the Customer Area. If the company account is also **Active**, then payment processing and payouts are enabled.<br>* **InactiveWithModifications**: Users can access the merchant account in the Customer Area. You cannot process new payments but you can still modify payments, for example issue refunds. You can still receive payouts.<br>* **Inactive**: Users can access the merchant account in the Customer Area. Payment processing and payouts are disabled.<br>* **Closed**: The account is closed and this cannot be reversed. Users cannot log in. Payment processing and payouts are disabled. |

## Example (as JSON)

```json
{
  "_links": {
    "apiCredentials": {
      "href": "href8"
    },
    "self": {
      "href": "href0"
    },
    "users": {
      "href": "href8"
    },
    "webhooks": {
      "href": "href8"
    }
  },
  "captureDelay": "captureDelay8",
  "companyId": "companyId2",
  "dataCenters": [
    {
      "livePrefix": "livePrefix4",
      "name": "name6"
    }
  ],
  "defaultShopperInteraction": "defaultShopperInteraction0"
}
```

