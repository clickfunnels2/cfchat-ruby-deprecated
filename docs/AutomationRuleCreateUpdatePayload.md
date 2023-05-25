# Cfchat::AutomationRuleCreateUpdatePayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Rule name | [optional] |
| **description** | **String** | The description about the automation and actions | [optional] |
| **event_name** | **String** | The event when you want to execute the automation actions | [optional] |
| **active** | **Boolean** | Enable/disable automation rule | [optional] |
| **actions** | **Array&lt;Object&gt;** | Array of actions which you want to perform when condition matches, e.g add label support if message contains content help. | [optional] |
| **conditions** | **Array&lt;Object&gt;** | Array of conditions on which conversation filter would work, e.g message content contains text help. | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::AutomationRuleCreateUpdatePayload.new(
  name: Add label on message create event,
  description: Add label support and sales on message create event if incoming message content contains text help,
  event_name: message_created,
  active: null,
  actions: null,
  conditions: null
)
```

