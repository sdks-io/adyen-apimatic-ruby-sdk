
# User

## Structure

`User`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `links` | [`Links1`](../../doc/models/links-1.md) | Optional | References to resources connected with this user. |
| `account_groups` | `Array[String]` | Optional | The list of [account groups](https://docs.adyen.com/account/account-structure#account-groups) associated with this user. |
| `active` | `TrueClass \| FalseClass` | Optional | Indicates whether this user is active. |
| `apps` | `Array[String]` | Optional | Set of apps available to this user |
| `email` | `String` | Required | The email address of the user. |
| `id` | `String` | Required | The unique identifier of the user. |
| `name` | [`Name`](../../doc/models/name.md) | Optional | The user's full name. |
| `roles` | `Array[String]` | Required | The list of [roles](https://docs.adyen.com/account/user-roles) for this user. |
| `time_zone_code` | `String` | Required | The [tz database name](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) of the time zone of the user. For example, **Europe/Amsterdam**. |
| `username` | `String` | Required | The username for this user.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |

## Example (as JSON)

```json
{
  "_links": {
    "self": {
      "href": "href0"
    }
  },
  "accountGroups": [
    "accountGroups1",
    "accountGroups0",
    "accountGroups9"
  ],
  "active": false,
  "apps": [
    "apps0",
    "apps1"
  ],
  "email": "email0",
  "id": "id6",
  "name": {
    "firstName": "firstName4",
    "lastName": "lastName4"
  },
  "roles": [
    "roles0",
    "roles9"
  ],
  "timeZoneCode": "timeZoneCode8",
  "username": "username6"
}
```

