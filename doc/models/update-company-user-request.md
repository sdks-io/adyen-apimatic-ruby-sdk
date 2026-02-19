
# Update Company User Request

## Structure

`UpdateCompanyUserRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_groups` | `Array[String]` | Optional | The list of [account groups](https://docs.adyen.com/account/account-structure#account-groups) associated with this user. |
| `active` | `TrueClass \| FalseClass` | Optional | Indicates whether this user is active. |
| `associated_merchant_accounts` | `Array[String]` | Optional | The list of [merchant accounts](https://docs.adyen.com/account/account-structure#merchant-accounts) to associate the user with. |
| `email` | `String` | Optional | The email address of the user. |
| `login_method` | `String` | Optional | The requested login method for the user. To use SSO, you must already have SSO configured with Adyen before creating the user.<br><br>Possible values: **Username & account**, **Email**, or **SSO** |
| `name` | [`Name22`](../../doc/models/name-22.md) | Optional | The user's full name. |
| `roles` | `Array[String]` | Optional | The list of [roles](https://docs.adyen.com/account/user-roles) for this user. |
| `time_zone_code` | `String` | Optional | The [tz database name](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) of the time zone of the user. For example, **Europe/Amsterdam**. |

## Example (as JSON)

```json
{
  "accountGroups": [
    "accountGroups3",
    "accountGroups4",
    "accountGroups5"
  ],
  "active": false,
  "associatedMerchantAccounts": [
    "associatedMerchantAccounts6"
  ],
  "email": "email0",
  "loginMethod": "loginMethod8"
}
```

