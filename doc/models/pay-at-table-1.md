
# Pay at Table 1

Settings for [Pay-at-table](https://docs.adyen.com/point-of-sale/pay-at-x) features.

## Structure

`PayAtTable1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authentication_method` | [`AuthenticationMethod`](../../doc/models/authentication-method.md) | Optional | Allowed authentication methods: Magswipe, Manual Entry. |
| `enable_pay_at_table` | `TrueClass \| FalseClass` | Optional | Enable Pay at table. |
| `payment_instrument` | [`PaymentInstrument`](../../doc/models/payment-instrument.md) | Optional | Sets the allowed payment instrument for Pay at table transactions.  Can be: **cash** or **card**. If not set, the terminal presents both options. |

## Example (as JSON)

```json
{
  "authenticationMethod": "MAGSWIPE",
  "enablePayAtTable": false,
  "paymentInstrument": "Cash"
}
```

