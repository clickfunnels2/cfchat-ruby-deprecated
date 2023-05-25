# Cfchat::PublicConversation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | Id of the conversation | [optional] |
| **inbox_id** | **String** | The inbox id of the conversation | [optional] |
| **messages** | [**Array&lt;Message&gt;**](Message.md) | Messages in the conversation | [optional] |
| **contact** | **Object** | The contact information associated to the conversation | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::PublicConversation.new(
  id: null,
  inbox_id: null,
  messages: null,
  contact: null
)
```

