
# Create Merchant Request

## Structure

`CreateMerchantRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `business_line_id` | `String` | Optional | The unique identifier of the [business line](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/businessLines). Required for an Adyen for Platforms Manage integration. |
| `company_id` | `String` | Required | The unique identifier of the company account. |
| `description` | `String` | Optional | Your description for the merchant account, maximum 300 characters.<br><br>**Constraints**: *Maximum Length*: `300` |
| `legal_entity_id` | `String` | Optional | The unique identifier of the [legal entity](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/legalEntities). Required for an Adyen for Platforms Manage integration. |
| `pricing_plan` | `String` | Optional | Sets the pricing plan for the merchant account. Required for an Adyen for Platforms Manage integration. Your Adyen contact will provide the values that you can use. |
| `reference` | `String` | Optional | Your reference for the merchant account. To make this reference the unique identifier of the merchant account, your Adyen contact can set up a template on your company account. The template can have 6 to 255 characters with upper- and lower-case letters, underscores, and numbers. When your company account has a template, then the `reference` is required and must be unique within the company account. |
| `sales_channels` | `Array[String]` | Optional | List of sales channels that the merchant will process payments with |

## Example (as JSON)

```json
{
  "businessLineId": "businessLineId8",
  "companyId": "companyId6",
  "description": "description6",
  "legalEntityId": "legalEntityId2",
  "pricingPlan": "pricingPlan2",
  "reference": "reference2"
}
```

