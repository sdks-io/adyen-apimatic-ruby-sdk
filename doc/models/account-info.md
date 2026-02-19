
# Account Info

## Structure

`AccountInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_age_indicator` | [`AccountAgeIndicator`](../../doc/models/account-age-indicator.md) | Optional | Indicator for the length of time since this shopper account was created in the merchant's environment.<br>Allowed values:<br><br>* notApplicable<br>* thisTransaction<br>* lessThan30Days<br>* from30To60Days<br>* moreThan60Days |
| `account_change_date` | `DateTime` | Optional | Date when the shopper's account was last changed. |
| `account_change_indicator` | [`AccountChangeIndicator`](../../doc/models/account-change-indicator.md) | Optional | Indicator for the length of time since the shopper's account was last updated.<br>Allowed values:<br><br>* thisTransaction<br>* lessThan30Days<br>* from30To60Days<br>* moreThan60Days |
| `account_creation_date` | `DateTime` | Optional | Date when the shopper's account was created. |
| `account_type` | [`AccountType`](../../doc/models/account-type.md) | Optional | Indicates the type of account. For example, for a multi-account card product.<br>Allowed values:<br><br>* notApplicable<br>* credit<br>* debit |
| `add_card_attempts_day` | `Integer` | Optional | Number of attempts the shopper tried to add a card to their account in the last day. |
| `delivery_address_usage_date` | `DateTime` | Optional | Date the selected delivery address was first used. |
| `delivery_address_usage_indicator` | [`DeliveryAddressUsageIndicator`](../../doc/models/delivery-address-usage-indicator.md) | Optional | Indicator for the length of time since this delivery address was first used.<br>Allowed values:<br><br>* thisTransaction<br>* lessThan30Days<br>* from30To60Days<br>* moreThan60Days |
| `home_phone` | `String` | Optional | Shopper's home phone number (including the country code). |
| `mobile_phone` | `String` | Optional | Shopper's mobile phone number (including the country code). |
| `password_change_date` | `DateTime` | Optional | Date when the shopper last changed their password. |
| `password_change_indicator` | [`PasswordChangeIndicator`](../../doc/models/password-change-indicator.md) | Optional | Indicator when the shopper has changed their password.<br>Allowed values:<br><br>* notApplicable<br>* thisTransaction<br>* lessThan30Days<br>* from30To60Days<br>* moreThan60Days |
| `past_transactions_day` | `Integer` | Optional | Number of all transactions (successful and abandoned) from this shopper in the past 24 hours. |
| `past_transactions_year` | `Integer` | Optional | Number of all transactions (successful and abandoned) from this shopper in the past year. |
| `payment_account_age` | `DateTime` | Optional | Date this payment method was added to the shopper's account. |
| `payment_account_indicator` | [`PaymentAccountIndicator`](../../doc/models/payment-account-indicator.md) | Optional | Indicator for the length of time since this payment method was added to this shopper's account.<br>Allowed values:<br><br>* notApplicable<br>* thisTransaction<br>* lessThan30Days<br>* from30To60Days<br>* moreThan60Days |
| `purchases_last_6_months` | `Integer` | Optional | Number of successful purchases in the last six months. |
| `suspicious_activity` | `TrueClass \| FalseClass` | Optional | Whether suspicious activity was recorded on this account. |
| `work_phone` | `String` | Optional | Shopper's work phone number (including the country code). |

## Example (as JSON)

```json
{
  "accountAgeIndicator": "lessThan30Days",
  "accountChangeDate": "2016-03-13T12:52:32.123Z",
  "accountChangeIndicator": "thisTransaction",
  "accountCreationDate": "2016-03-13T12:52:32.123Z",
  "accountType": "credit"
}
```

