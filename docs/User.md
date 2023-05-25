# Cfchat::User

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Float** |  | [optional] |
| **uid** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **available_name** | **String** |  | [optional] |
| **display_name** | **String** |  | [optional] |
| **email** | **String** |  | [optional] |
| **account_id** | **Float** |  | [optional] |
| **role** | **String** |  | [optional] |
| **confirmed** | **Boolean** |  | [optional] |
| **custom_attributes** | **Object** | Available for users who are created through platform APIs and has custom attributes associated. | [optional] |
| **accounts** | [**Array&lt;Account&gt;**](Account.md) |  | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::User.new(
  id: null,
  uid: null,
  name: null,
  available_name: null,
  display_name: null,
  email: null,
  account_id: null,
  role: null,
  confirmed: null,
  custom_attributes: null,
  accounts: null
)
```

