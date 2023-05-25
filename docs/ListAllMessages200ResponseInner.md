# Cfchat::ListAllMessages200ResponseInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Float** |  | [optional] |
| **content** | **String** | The text content of the message | [optional] |
| **content_type** | **String** | The type of the template message | [optional] |
| **content_attributes** | **Object** | The content attributes for each content_type | [optional] |
| **message_type** | **String** | The type of the message | [optional] |
| **created_at** | **Integer** | The time at which message was created | [optional] |
| **private** | **Boolean** | The flags which shows whether the message is private or not | [optional] |
| **attachment** | **Object** | The file object attached to the image | [optional] |
| **sender** | **Object** | User/Agent/AgentBot object | [optional] |
| **conversation_id** | **Float** | ID of the conversation | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::ListAllMessages200ResponseInner.new(
  id: null,
  content: null,
  content_type: null,
  content_attributes: null,
  message_type: null,
  created_at: null,
  private: null,
  attachment: null,
  sender: null,
  conversation_id: null
)
```

