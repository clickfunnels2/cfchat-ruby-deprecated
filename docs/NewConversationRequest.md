# Cfchat::NewConversationRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **source_id** | **String** | Conversation source id | [optional] |
| **inbox_id** | **String** | Id of inbox in which the conversation is created &lt;br/&gt; Allowed Inbox Types: Website, Phone, Api, Email  | [optional] |
| **contact_id** | **String** | Contact Id for which conversation is created | [optional] |
| **additional_attributes** | **Object** | Lets you specify attributes like browser information | [optional] |
| **custom_attributes** | **Object** | The object to save custom attributes for conversation, accepts custom attributes key and value | [optional] |
| **status** | **String** | Specify the conversation whether it&#39;s pending, open, closed | [optional] |
| **assignee_id** | **String** | Agent Id for assigning a conversation to an agent | [optional] |
| **team_id** | **String** | Team Id for assigning a conversation to a team | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::NewConversationRequest.new(
  source_id: null,
  inbox_id: null,
  contact_id: null,
  additional_attributes: null,
  custom_attributes: {&quot;attribute_key&quot;:&quot;attribute_value&quot;,&quot;priority_conversation_number&quot;:3},
  status: null,
  assignee_id: null,
  team_id: null
)
```

