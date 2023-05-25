# Cfchat::AgentBotCreateUpdatePayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The name of the agent bot | [optional] |
| **description** | **String** | The description about the agent bot | [optional] |
| **outgoing_url** | **String** | The webhook URL for the bot | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::AgentBotCreateUpdatePayload.new(
  name: null,
  description: null,
  outgoing_url: null
)
```

