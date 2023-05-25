# Cfchat::Conversation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Float** | ID of the conversation | [optional] |
| **messages** | [**Array&lt;Message&gt;**](Message.md) |  | [optional] |
| **account_id** | **Float** | Account Id | [optional] |
| **inbox_id** | **Float** | ID of the inbox | [optional] |
| **status** | **String** | The status of the conversation | [optional] |
| **timestamp** | **String** | The time at which conversation was created | [optional] |
| **contact_last_seen_at** | **String** |  | [optional] |
| **agent_last_seen_at** | **String** |  | [optional] |
| **unread_count** | **Float** | The number of unread messages | [optional] |
| **additional_attributes** | **Object** | The object containing additional attributes related to the conversation | [optional] |
| **custom_attributes** | **Object** | The object to save custom attributes for conversation, accepts custom attributes key and value | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::Conversation.new(
  id: null,
  messages: null,
  account_id: null,
  inbox_id: null,
  status: null,
  timestamp: null,
  contact_last_seen_at: null,
  agent_last_seen_at: null,
  unread_count: null,
  additional_attributes: null,
  custom_attributes: {&quot;attribute_key&quot;:&quot;attribute_value&quot;,&quot;priority_conversation_number&quot;:3}
)
```

