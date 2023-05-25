# Cfchat::TeamCreateUpdatePayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The name of the team | [optional] |
| **description** | **String** | The description of the team | [optional] |
| **allow_auto_assign** | **Boolean** | If this setting is turned on, the system would automatically assign the conversation to an agent in the team while assigning the conversation to a team | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::TeamCreateUpdatePayload.new(
  name: null,
  description: null,
  allow_auto_assign: null
)
```

