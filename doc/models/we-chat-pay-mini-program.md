
# We Chat Pay Mini Program

*This model accepts additional fields of type Object.*

## Structure

`WeChatPayMiniProgram`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_id` | `String` | Optional | - |
| `checkout_attempt_id` | `String` | Optional | The checkout attempt identifier. |
| `openid` | `String` | Optional | - |
| `recurring_detail_reference` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. |
| `sdk_data` | `String` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` |
| `stored_payment_method_id` | `String` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` |
| `type` | [`Type51`](../../doc/models/type-51.md) | Optional | **wechatpayMiniProgram**<br><br>**Default**: `Type51::WECHATPAYMINIPROGRAM` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "wechatpayMiniProgram",
  "appId": "appId2",
  "checkoutAttemptId": "checkoutAttemptId2",
  "openid": "openid6",
  "recurringDetailReference": "recurringDetailReference6",
  "sdkData": "sdkData6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

