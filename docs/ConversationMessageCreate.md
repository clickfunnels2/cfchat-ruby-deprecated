# Cfchat::ConversationMessageCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content** | **String** | The content of the message |  |
| **message_type** | **String** |  | [optional] |
| **private** | **Boolean** | Flag to identify if it is a private note | [optional] |
| **content_type** | **String** | if you want to create custom message types | [optional] |
| **content_attributes** | **Object** | attributes based on your content type | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::ConversationMessageCreate.new(
  content: null,
  message_type: null,
  private: null,
  content_type: cards,
  content_attributes: null
)
```

