
# Payment Method Setup Info

## Structure

`PaymentMethodSetupInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accel` | [`AccelInfo1`](../../doc/models/accel-info-1.md) | Optional | Details to provide if `type` is **accel**. |
| `affirm` | [`AffirmInfo1`](../../doc/models/affirm-info-1.md) | Optional | Details to provide if `type` is **affirm**. |
| `afterpay_touch` | [`AfterpayTouchInfo1`](../../doc/models/afterpay-touch-info-1.md) | Optional | Details to provide if `type` is **afterpaytouch**. |
| `alipay_plus` | [`AlipayPlusInfo1`](../../doc/models/alipay-plus-info-1.md) | Optional | Details to provide if `type` is **alipay_plus**. |
| `amex` | [`AmexInfo1`](../../doc/models/amex-info-1.md) | Optional | Details to provide if `type` is **amex**. |
| `apple_pay` | [`ApplePayInfo1`](../../doc/models/apple-pay-info-1.md) | Optional | Details to provide if `type` is **applepay**. |
| `bcmc` | [`BcmcInfo1`](../../doc/models/bcmc-info-1.md) | Optional | Details to provide if `type` is **bcmc** (Bancontact). |
| `business_line_id` | `String` | Optional | The unique identifier of the business line. Required if you are a [platform model](https://docs.adyen.com/platforms). |
| `cartes_bancaires` | [`CartesBancairesInfo1`](../../doc/models/cartes-bancaires-info-1.md) | Optional | Details to provide if `type` is **cartebancaire**. |
| `clearpay` | [`ClearpayInfo1`](../../doc/models/clearpay-info-1.md) | Optional | Details to provide if `type` is **clearpay**. |
| `countries` | `Array[String]` | Optional | The list of countries where a payment method is available. By default, all countries supported by the payment method. |
| `cup` | [`GenericPmWithTdiInfo1`](../../doc/models/generic-pm-with-tdi-info-1.md) | Optional | Details to provide if `type` is **cup** (China Union Pay). |
| `currencies` | `Array[String]` | Optional | The list of currencies that a payment method supports. By default, all currencies supported by the payment method. |
| `custom_routing_flags` | `Array[String]` | Optional | The list of custom routing flags to route payment to the intended acquirer. |
| `diners` | [`DinersInfo1`](../../doc/models/diners-info-1.md) | Optional | Details to provide if `type` is **diners**.<br>For merchants operating in Japan, Diners payments are processed through the JCB network. This means that you must include [JCB-specific fields](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/paymentMethodSettings/(paymentMethodId)#request-jcb) in this object. |
| `discover` | [`GenericPmWithTdiInfo2`](../../doc/models/generic-pm-with-tdi-info-2.md) | Optional | Details to provide if `type` is **discover**.<br>For merchants operating in Japan, request [Diners](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/paymentMethodSettings/(paymentMethodId)#request-diners) payment method instead. Discover is automatically requested, together with Diners. |
| `eft_directdebit_ca` | [`GenericPmWithTdiInfo3`](../../doc/models/generic-pm-with-tdi-info-3.md) | Optional | Details to provide if `type` is **eft_directdebit_CA** (EFT PAD). |
| `eftpos_australia` | [`GenericPmWithTdiInfo4`](../../doc/models/generic-pm-with-tdi-info-4.md) | Optional | Details to provide if `type` is **eftpos_australia**. |
| `girocard` | [`GenericPmWithTdiInfo5`](../../doc/models/generic-pm-with-tdi-info-5.md) | Optional | Details to provide if `type` is **girocard**. |
| `givex` | [`GivexInfo1`](../../doc/models/givex-info-1.md) | Optional | Details to provide if `type` is **givex**. |
| `google_pay` | [`GooglePayInfo1`](../../doc/models/google-pay-info-1.md) | Optional | Details to provide if `type` is **googlepay**. |
| `ideal` | [`GenericPmWithTdiInfo6`](../../doc/models/generic-pm-with-tdi-info-6.md) | Optional | Details to provide if `type` is **ideal**. |
| `interac_card` | [`GenericPmWithTdiInfo7`](../../doc/models/generic-pm-with-tdi-info-7.md) | Optional | Details to provide if `type` is **interac_card**. |
| `jcb` | [`JcbInfo1`](../../doc/models/jcb-info-1.md) | Optional | Details to provide if `type` is **jcb**.<br>For merchants operating in Japan, `midNumber`, `reuseMidNumber`, and `serviceLevel` fields are required.<br>For merchants operating outside of Japan, these fields are not required. |
| `klarna` | [`KlarnaInfo1`](../../doc/models/klarna-info-1.md) | Optional | Details to provide if `type` is **klarna** or its variant.<br><br>You can use the following payment method `type` values for Klarna:<br><br>* **klarna**: Klarna Pay Later<br>* **klarna_account**: Klarna Pay over time<br>* **klarna_paynow**: Klarna Pay now<br>* **klarna_b2b**: [Billie via Klarna](https://docs.adyen.com/payment-methods/klarna/billie) |
| `maestro` | [`GenericPmWithTdiInfo8`](../../doc/models/generic-pm-with-tdi-info-8.md) | Optional | Details to provide if `type` is **maestro**.<br>In the US, `maestro` is not supported; use `maestro_usa` instead. |
| `maestro_usa` | [`GenericPmWithTdiInfo9`](../../doc/models/generic-pm-with-tdi-info-9.md) | Optional | Details to provide if `type` is **maestro_usa**.<br>Only for Maestro USA, otherwise use `maestro`. |
| `mc` | [`GenericPmWithTdiInfo10`](../../doc/models/generic-pm-with-tdi-info-10.md) | Optional | Details to provide if `type` is **mc**. |
| `meal_voucher_fr` | [`MealVoucherFrInfo1`](../../doc/models/meal-voucher-fr-info-1.md) | Optional | Details to provide if `type` is **mealVoucher_FR**. |
| `nyce` | [`NyceInfo1`](../../doc/models/nyce-info-1.md) | Optional | Details to provide if `type` is **nyce**. |
| `paybybank_plaid` | [`PayByBankPlaidInfo1`](../../doc/models/pay-by-bank-plaid-info-1.md) | Optional | Details to provide if `type` is **paybybank_plaid**. |
| `payme` | [`PayMeInfo1`](../../doc/models/pay-me-info-1.md) | Optional | Details to provide if `type` is **payme**. |
| `paypal` | [`PayPalInfo1`](../../doc/models/pay-pal-info-1.md) | Optional | Details to provide if `type` is **paypal**. |
| `payto` | [`PayToInfo1`](../../doc/models/pay-to-info-1.md) | Optional | Details to provide if `type` is **payto**. |
| `pulse` | [`PulseInfo1`](../../doc/models/pulse-info-1.md) | Optional | Details to provide if `type` is **pulse**. |
| `reference` | `String` | Optional | Your reference for the payment method. Supported characters a-z, A-Z, 0-9.<br><br>**Constraints**: *Maximum Length*: `150` |
| `sepadirectdebit` | [`SepaDirectDebitInfo1`](../../doc/models/sepa-direct-debit-info-1.md) | Optional | Details to provide if `type` is **sepadirectdebit**. |
| `shopper_interaction` | [`ShopperInteraction1`](../../doc/models/shopper-interaction-1.md) | Optional | The sales channel. Required if the merchant account does not have a sales channel. When you provide this field, it overrides the default sales channel set on the merchant account.<br><br>Possible values: **eCommerce**, **pos**, **contAuth**, and **moto**. |
| `sodexo` | [`SodexoInfo1`](../../doc/models/sodexo-info-1.md) | Optional | Details to provide if `type` is **sodexo**. |
| `sofort` | [`SofortInfo1`](../../doc/models/sofort-info-1.md) | Optional | Sofort details. |
| `star` | [`StarInfo1`](../../doc/models/star-info-1.md) | Optional | Details to provide if `type` is **star**. |
| `store_ids` | `Array[String]` | Optional | The unique identifier of the store for which to configure the payment method, if any. |
| `svs` | [`SvsInfo1`](../../doc/models/svs-info-1.md) | Optional | Details to provide if `type` is **svs**. |
| `swish` | [`SwishInfo1`](../../doc/models/swish-info-1.md) | Optional | Details to provide if `type` is **swish**.<br><br>- This field is required only if you have a contract with Swish. Swish handles settlement directly with you (not through Adyen).<br>- If not specified then it's assumed that you are using Adyen's contract with Swish.You don't have a direct relationship with Swish. |
| `ticket` | [`TicketInfo1`](../../doc/models/ticket-info-1.md) | Optional | Details to provide if `type` is **ticket** (Edenred Brazil). |
| `twint` | [`TwintInfo1`](../../doc/models/twint-info-1.md) | Optional | Details to provide if `type` is **twint**. |
| `type` | [`Type410`](../../doc/models/type-410.md) | Required | Payment method [variant](https://docs.adyen.com/development-resources/paymentmethodvariant#management-api). |
| `valuelink` | [`ValuelinkInfo1`](../../doc/models/valuelink-info-1.md) | Optional | Details to provide if `type` is **valuelink**. |
| `vipps` | [`VippsInfo1`](../../doc/models/vipps-info-1.md) | Optional | Details to provide if `type` is **vipps**. |
| `visa` | [`GenericPmWithTdiInfo11`](../../doc/models/generic-pm-with-tdi-info-11.md) | Optional | Details to provide if `type` is **visa**. |
| `wechatpay` | [`WeChatPayInfo1`](../../doc/models/we-chat-pay-info-1.md) | Optional | Details to provide if `type` is **wechatpay**. |
| `wechatpay_pos` | [`WeChatPayPosInfo1`](../../doc/models/we-chat-pay-pos-info-1.md) | Optional | Details to provide if `type` is **wechatpay_pos**. |

## Example (as JSON)

```json
{
  "accel": {
    "processingType": "billpay",
    "transactionDescription": {
      "doingBusinessAsName": "doingBusinessAsName0",
      "type": "fixed"
    }
  },
  "affirm": {
    "pricePlan": "BRONZE",
    "supportEmail": "supportEmail2"
  },
  "afterpayTouch": {
    "supportEmail": "supportEmail8",
    "supportUrl": "supportUrl4"
  },
  "alipayPlus": {
    "settlementCurrencyCode": "settlementCurrencyCode0"
  },
  "amex": {
    "midNumber": "midNumber4",
    "reuseMidNumber": false,
    "serviceLevel": "gatewayContract"
  },
  "type": "nutricash_prepaid"
}
```

