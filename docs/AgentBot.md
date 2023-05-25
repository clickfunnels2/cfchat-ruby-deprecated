# Cfchat::AgentBot

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Float** | ID of the agent bot | [optional] |
| **name** | **String** | The name of the agent bot | [optional] |
| **description** | **String** | The description about the agent bot | [optional] |
| **account_id** | **Float** | Account ID if it&#39;s an account specific bot | [optional] |
| **outgoing_url** | **String** | The webhook URL for the bot | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::AgentBot.new(
  id: null,
  name: null,
  description: null,
  account_id: null,
  outgoing_url: null
)
```

