# Cfchat::AutomationRule

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **event_name** | **String** | Automation Rule event, on which we call the actions(conversation_created, conversation_updated, message_created) | [optional] |
| **name** | **String** | The name of the rule | [optional] |
| **description** | **String** | Description to give more context about the rule | [optional] |
| **active** | **Boolean** | Enable/disable automation rule | [optional] |
| **actions** | **Array&lt;Object&gt;** | Array of actions which we perform when condition matches | [optional] |
| **conditions** | **Array&lt;Object&gt;** | Array of conditions on which conversation/message filter would work | [optional] |
| **account_id** | **Integer** | Account Id | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::AutomationRule.new(
  event_name: message_created,
  name: Add label on message create event,
  description: Add label support and sales on message create event if incoming message content contains text help,
  active: null,
  actions: null,
  conditions: null,
  account_id: null
)
```

