# Cfchat::Team

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Float** | The ID of the team | [optional] |
| **name** | **String** | The name of the team | [optional] |
| **description** | **String** | The description about the team | [optional] |
| **allow_auto_assign** | **Boolean** | If this setting is turned on, the system would automatically assign the conversation to an agent in the team while assigning the conversation to a team | [optional] |
| **account_id** | **Float** | The ID of the account with the team is a part of | [optional] |
| **is_member** | **Boolean** | This field shows whether the current user is a part of the team | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::Team.new(
  id: null,
  name: null,
  description: null,
  allow_auto_assign: null,
  account_id: null,
  is_member: null
)
```

