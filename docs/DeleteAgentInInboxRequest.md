# Cfchat::DeleteAgentInInboxRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inbox_id** | **String** | The ID of the inbox |  |
| **user_ids** | **Array&lt;Integer&gt;** | IDs of users to be deleted from the inbox |  |

## Example

```ruby
require 'cfchat'

instance = Cfchat::DeleteAgentInInboxRequest.new(
  inbox_id: null,
  user_ids: null
)
```

