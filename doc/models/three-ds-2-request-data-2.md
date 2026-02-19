
# Three Ds 2 Request Data 2

Request fields for 3D Secure 2. To check if any of the following fields are required for your integration, refer to [Online payments](https://docs.adyen.com/online-payments) or [Classic integration](https://docs.adyen.com/classic-integration) documentation.

## Structure

`ThreeDs2RequestData2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `acct_info` | [`AcctInfo1`](../../doc/models/acct-info-1.md) | Optional | Additional information about the cardholder’s account provided by the 3DS Requestor. |
| `acct_type` | [`AcctType`](../../doc/models/acct-type.md) | Optional | Indicates the type of account. For example, for a multi-account card product. Length: 2 characters. Allowed values:<br><br>* **01** — Not applicable<br>* **02** — Credit<br>* **03** — Debit<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `2` |
| `acquirer_bin` | `String` | Optional | Required for [authentication-only integration](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only). The acquiring BIN enrolled for 3D Secure 2. This string should match the value that you will use in the authorisation. Use 123456 on the Test platform. |
| `acquirer_merchant_id` | `String` | Optional | Required for [authentication-only integration](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only). The merchantId that is enrolled for 3D Secure 2 by the merchant's acquirer. This string should match the value that you will use in the authorisation. Use 123456 on the Test platform. |
| `addr_match` | [`AddrMatch`](../../doc/models/addr-match.md) | Optional | Indicates whether the cardholder shipping address and cardholder billing address are the same. Allowed values:<br><br>* **Y** — Shipping address matches billing address.<br>* **N** — Shipping address does not match billing address.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1` |
| `authentication_only` | `TrueClass \| FalseClass` | Optional | If set to true, you will only perform the [3D Secure 2 authentication](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only), and not the payment authorisation.<br><br>**Default**: `false` |
| `challenge_indicator` | [`ChallengeIndicator`](../../doc/models/challenge-indicator.md) | Optional | Possibility to specify a preference for receiving a challenge from the issuer.<br>Allowed values:<br><br>* `noPreference`<br>* `requestNoChallenge`<br>* `requestChallenge`<br>* `requestChallengeAsMandate` |
| `device_channel` | `String` | Required | The environment of the shopper.<br>Allowed values:<br><br>* `app`<br>* `browser` |
| `device_render_options` | [`DeviceRenderOptions2`](../../doc/models/device-render-options-2.md) | Optional | Display options for the 3D Secure 2 SDK.<br>Optional and only for `deviceChannel` **app**. |
| `home_phone` | [`Phone3`](../../doc/models/phone-3.md) | Optional | The home phone number provided by the cardholder. The phone number must consist of a country code, followed by the number. If the value you provide does not follow the guidelines, we do not submit it for authentication.<br><br>> Required for Visa and JCB transactions that require 3D Secure 2 authentication, if you did not include the `shopperEmail`, and did not send the shopper's phone number in `telephoneNumber`. |
| `mcc` | `String` | Optional | Required for merchants that have been enrolled for 3D Secure 2 by another party than Adyen, mostly [authentication-only integrations](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only). The `mcc` is a four-digit code with which the previously given `acquirerMerchantID` is registered at the scheme. |
| `merchant_name` | `String` | Optional | Required for [authentication-only integration](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only). The merchant name that the issuer presents to the shopper if they get a challenge. We recommend to use the same value that you will use in the authorization. Maximum length is 40 characters.<br><br>> Optional for a [full 3D Secure 2 integration](https://docs.adyen.com/online-payments/3d-secure/native-3ds2/api-integration). Use this field if you are enrolled for 3D Secure 2 with us and want to override the merchant name already configured on your account. |
| `message_version` | `String` | Optional | The `messageVersion` value indicating the 3D Secure 2 protocol version. |
| `mobile_phone` | [`Phone1`](../../doc/models/phone-1.md) | Optional | The mobile phone number provided by the cardholder. The phone number must consist of a country code, followed by the number. If the value you provide does not follow the guidelines, we do not submit it for authentication.<br><br>> Required for Visa and JCB transactions that require 3D Secure 2 authentication, if you did not include the `shopperEmail`, and did not send the shopper's phone number in `telephoneNumber`. |
| `notification_url` | `String` | Optional | URL to where the issuer should send the `CRes`. Required if you are not using components for `channel` **Web** or if you are using classic integration `deviceChannel` **browser**. |
| `pay_token_ind` | `TrueClass \| FalseClass` | Optional | Value **true** indicates that the transaction was de-tokenised prior to being received by the ACS. |
| `payment_authentication_use_case` | `String` | Optional | Indicates the type of payment for which an authentication is requested (message extension) |
| `purchase_instal_data` | `String` | Optional | Indicates the maximum number of authorisations permitted for instalment payments. Length: 1–3 characters.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `3` |
| `recurring_expiry` | `String` | Optional | Date after which no further authorisations shall be performed. Format: YYYYMMDD |
| `recurring_frequency` | `String` | Optional | Indicates the minimum number of days between authorisations. Maximum length: 4 characters.<br><br>**Constraints**: *Maximum Length*: `4` |
| `sdk_app_id` | `String` | Optional | The `sdkAppID` value as received from the 3D Secure 2 SDK.<br>Required for `deviceChannel` set to **app**. |
| `sdk_enc_data` | `String` | Optional | The `sdkEncData` value as received from the 3D Secure 2 SDK.<br>Required for `deviceChannel` set to **app**. |
| `sdk_ephem_pub_key` | [`SdkEphemPubKey3`](../../doc/models/sdk-ephem-pub-key-3.md) | Optional | The `sdkEphemPubKey` value as received from the 3D Secure 2 SDK.<br>Required for `deviceChannel` set to **app**. |
| `sdk_max_timeout` | `Integer` | Optional | The maximum amount of time in minutes for the 3D Secure 2 authentication process.<br>Optional and only for `deviceChannel` set to **app**. Defaults to **60** minutes.<br><br>**Default**: `60` |
| `sdk_reference_number` | `String` | Optional | The `sdkReferenceNumber` value as received from the 3D Secure 2 SDK.<br>Only for `deviceChannel` set to **app**. |
| `sdk_trans_id` | `String` | Optional | The `sdkTransID` value as received from the 3D Secure 2 SDK.<br>Only for `deviceChannel` set to **app**. |
| `sdk_version` | `String` | Optional | Version of the 3D Secure 2 mobile SDK.<br>Only for `deviceChannel` set to **app**. |
| `three_ds_comp_ind` | `String` | Optional | Completion indicator for the device fingerprinting. |
| `three_ds_requestor_authentication_ind` | `String` | Optional | Indicates the type of Authentication request. |
| `three_ds_requestor_authentication_info` | [`ThreeDsRequestorAuthenticationInfo1`](../../doc/models/three-ds-requestor-authentication-info-1.md) | Optional | Information about how the 3DS Requestor authenticated the cardholder before or during the transaction |
| `three_ds_requestor_challenge_ind` | [`ThreeDsRequestorChallengeInd`](../../doc/models/three-ds-requestor-challenge-ind.md) | Optional | Indicates whether a challenge is requested for this transaction. Possible values:<br><br>* **01** — No preference<br>* **02** — No challenge requested<br>* **03** — Challenge requested (3DS Requestor preference)<br>* **04** — Challenge requested (Mandate)<br>* **05** — No challenge (transactional risk analysis is already performed)<br>* **06** — Data Only |
| `three_ds_requestor_id` | `String` | Optional | Required for [authentication-only integration](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only) for Visa. Unique 3D Secure requestor identifier assigned by the Directory Server when you enrol for 3D Secure 2. |
| `three_ds_requestor_name` | `String` | Optional | Required for [authentication-only integration](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only) for Visa. Unique 3D Secure requestor name assigned by the Directory Server when you enrol for 3D Secure 2. |
| `three_ds_requestor_prior_authentication_info` | [`ThreeDsRequestorPriorAuthenticationInfo1`](../../doc/models/three-ds-requestor-prior-authentication-info-1.md) | Optional | Information about how the 3DS Requestor authenticated the cardholder as part of a previous 3DS transaction. |
| `three_ds_requestor_url` | `String` | Optional | URL of the (customer service) website that will be shown to the shopper in case of technical errors during the 3D Secure 2 process. |
| `trans_type` | [`TransType`](../../doc/models/trans-type.md) | Optional | Identifies the type of transaction being authenticated. Length: 2 characters. Allowed values:<br><br>* **01** — Goods/Service Purchase<br>* **03** — Check Acceptance<br>* **10** — Account Funding<br>* **11** — Quasi-Cash Transaction<br>* **28** — Prepaid Activation and Load<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `2` |
| `transaction_type` | [`TransactionType`](../../doc/models/transaction-type.md) | Optional | Identify the type of the transaction being authenticated. |
| `white_list_status` | `String` | Optional | The `whiteListStatus` value returned from a previous 3D Secure 2 transaction, only applicable for 3D Secure 2 protocol version 2.2.0. |
| `work_phone` | [`Phone2`](../../doc/models/phone-2.md) | Optional | The work phone number provided by the cardholder. The phone number must consist of a country code, followed by the number. If the value you provide does not follow the guidelines, we do not submit it for authentication.<br><br>> Required for Visa and JCB transactions that require 3D Secure 2 authentication, if you did not include the `shopperEmail`, and did not send the shopper's phone number in `telephoneNumber`. |

## Example (as JSON)

```json
{
  "authenticationOnly": false,
  "deviceChannel": "deviceChannel8",
  "sdkMaxTimeout": 60,
  "acctInfo": {
    "chAccAgeInd": "05",
    "chAccChange": "chAccChange8",
    "chAccChangeInd": "01",
    "chAccPwChange": "chAccPwChange8",
    "chAccPwChangeInd": "03"
  },
  "acctType": "03",
  "acquirerBIN": "acquirerBIN6",
  "acquirerMerchantID": "acquirerMerchantID4",
  "addrMatch": "Y"
}
```

