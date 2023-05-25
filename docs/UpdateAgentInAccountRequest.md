# Cfchat::UpdateAgentInAccountRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **role** | **String** | Whether its administrator or agent |  |
| **availability** | **String** | The availability setting of the agent. | [optional] |
| **auto_offline** | **Boolean** | Whether the availability status of agent is configured to go offline automatically when away. | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::UpdateAgentInAccountRequest.new(
  role: null,
  availability: null,
  auto_offline: null
)
```

