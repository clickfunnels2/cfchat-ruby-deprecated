# Cfchat::AddNewAgentToAccountRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Full Name of the agent |  |
| **email** | **String** | Email of the Agent |  |
| **role** | **String** | Whether its administrator or agent |  |
| **availability_status** | **String** | The availability setting of the agent. | [optional] |
| **auto_offline** | **Boolean** | Whether the availability status of agent is configured to go offline automatically when away. | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::AddNewAgentToAccountRequest.new(
  name: null,
  email: null,
  role: null,
  availability_status: null,
  auto_offline: null
)
```

