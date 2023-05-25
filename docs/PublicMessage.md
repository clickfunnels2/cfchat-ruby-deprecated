# Cfchat::PublicMessage

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Id of the message | [optional] |
| **content** | **String** | Text content of the message | [optional] |
| **message_type** | **String** | Denotes the message type | [optional] |
| **content_type** | **String** | Content type of the message | [optional] |
| **content_attributes** | **String** | Additional content attributes of the message | [optional] |
| **created_at** | **String** | Created at time stamp of the message | [optional] |
| **conversation_id** | **String** | Conversation Id of the message | [optional] |
| **attachments** | **Array&lt;Object&gt;** | Attachments if any | [optional] |
| **sender** | **Object** | Details of the sender | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::PublicMessage.new(
  id: null,
  content: null,
  message_type: null,
  content_type: null,
  content_attributes: null,
  created_at: null,
  conversation_id: null,
  attachments: null,
  sender: null
)
```

