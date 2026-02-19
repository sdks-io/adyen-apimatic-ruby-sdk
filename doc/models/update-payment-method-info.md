
# Update Payment Method Info

## Structure

`UpdatePaymentMethodInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accel` | [`AccelInfo1`](../../doc/models/accel-info-1.md) | Optional | Details to provide if `type` is **accel**. |
| `bcmc` | [`BcmcInfo1`](../../doc/models/bcmc-info-1.md) | Optional | Details to provide if `type` is **bcmc** (Bancontact). |
| `cartes_bancaires` | [`CartesBancairesInfo1`](../../doc/models/cartes-bancaires-info-1.md) | Optional | Details to provide if `type` is **cartebancaire**. |
| `countries` | `Array[String]` | Optional | The list of countries where a payment method is available. By default, all countries supported by the payment method. |
| `cup` | [`GenericPmWithTdiInfo1`](../../doc/models/generic-pm-with-tdi-info-1.md) | Optional | Details to provide if `type` is **cup** (China Union Pay). |
| `currencies` | `Array[String]` | Optional | The list of currencies that a payment method supports. By default, all currencies supported by the payment method. |
| `custom_routing_flags` | `Array[String]` | Optional | Custom routing flags for acquirer routing. |
| `diners` | [`GenericPmWithTdiInfo24`](../../doc/models/generic-pm-with-tdi-info-24.md) | Optional | Details to provide if `type` is **diners**.<br>For merchants operating in Japan, Diners payments are processed through the JCB network. This means that you must include [JCB-specific fields](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/paymentMethodSettings/(paymentMethodId)#request-jcb) in this object. |
| `discover` | [`GenericPmWithTdiInfo2`](../../doc/models/generic-pm-with-tdi-info-2.md) | Optional | Details to provide if `type` is **discover**.<br>For merchants operating in Japan, request [Diners](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/paymentMethodSettings/(paymentMethodId)#request-diners) payment method instead. Discover is automatically requested, together with Diners. |
| `eft_directdebit_ca` | [`GenericPmWithTdiInfo3`](../../doc/models/generic-pm-with-tdi-info-3.md) | Optional | Details to provide if `type` is **eft_directdebit_CA** (EFT PAD). |
| `eftpos_australia` | [`GenericPmWithTdiInfo4`](../../doc/models/generic-pm-with-tdi-info-4.md) | Optional | Details to provide if `type` is **eftpos_australia**. |
| `enabled` | `TrueClass \| FalseClass` | Optional | Indicates whether the payment method is enabled (**true**) or disabled (**false**). |
| `girocard` | [`GenericPmWithTdiInfo5`](../../doc/models/generic-pm-with-tdi-info-5.md) | Optional | Details to provide if `type` is **girocard**. |
| `ideal` | [`GenericPmWithTdiInfo6`](../../doc/models/generic-pm-with-tdi-info-6.md) | Optional | Details to provide if `type` is **ideal**. |
| `interac_card` | [`GenericPmWithTdiInfo7`](../../doc/models/generic-pm-with-tdi-info-7.md) | Optional | Details to provide if `type` is **interac_card**. |
| `jcb` | [`GenericPmWithTdiInfo31`](../../doc/models/generic-pm-with-tdi-info-31.md) | Optional | Details to provide if `type` is **jcb**.<br>For merchants operating in Japan, `midNumber`, `reuseMidNumber`, and `serviceLevel` fields are required.<br>For merchants operating outside of Japan, these fields are not required. |
| `maestro` | [`GenericPmWithTdiInfo8`](../../doc/models/generic-pm-with-tdi-info-8.md) | Optional | Details to provide if `type` is **maestro**.<br>In the US, `maestro` is not supported; use `maestro_usa` instead. |
| `maestro_usa` | [`GenericPmWithTdiInfo9`](../../doc/models/generic-pm-with-tdi-info-9.md) | Optional | Details to provide if `type` is **maestro_usa**.<br>Only for Maestro USA, otherwise use `maestro`. |
| `mc` | [`GenericPmWithTdiInfo10`](../../doc/models/generic-pm-with-tdi-info-10.md) | Optional | Details to provide if `type` is **mc**. |
| `nyce` | [`NyceInfo1`](../../doc/models/nyce-info-1.md) | Optional | Details to provide if `type` is **nyce**. |
| `paybybank_plaid` | [`PayByBankPlaidInfo1`](../../doc/models/pay-by-bank-plaid-info-1.md) | Optional | Details to provide if `type` is **paybybank_plaid**. |
| `pulse` | [`PulseInfo1`](../../doc/models/pulse-info-1.md) | Optional | Details to provide if `type` is **pulse**. |
| `sepadirectdebit` | [`SepaDirectDebitInfo1`](../../doc/models/sepa-direct-debit-info-1.md) | Optional | Details to provide if `type` is **sepadirectdebit**. |
| `star` | [`StarInfo1`](../../doc/models/star-info-1.md) | Optional | Details to provide if `type` is **star**. |
| `store_id` | `String` | Optional | The store for this payment method |
| `store_ids` | `Array[String]` | Optional | The list of stores for this payment method |
| `visa` | [`GenericPmWithTdiInfo11`](../../doc/models/generic-pm-with-tdi-info-11.md) | Optional | Details to provide if `type` is **visa**. |

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
  "bcmc": {
    "enableBcmcMobile": false
  },
  "cartesBancaires": {
    "siret": "siret8",
    "transactionDescription": {
      "doingBusinessAsName": "doingBusinessAsName0",
      "type": "fixed"
    }
  },
  "countries": [
    "countries3",
    "countries2",
    "countries1"
  ],
  "cup": {
    "transactionDescription": {
      "doingBusinessAsName": "doingBusinessAsName0",
      "type": "fixed"
    }
  }
}
```

