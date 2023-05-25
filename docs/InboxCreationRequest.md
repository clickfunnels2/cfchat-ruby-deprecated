# Cfchat::InboxCreationRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The name of the inbox | [optional] |
| **avatar** | **File** | File for avatar image | [optional] |
| **channel** | [**InboxCreationRequestChannel**](InboxCreationRequestChannel.md) |  | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::InboxCreationRequest.new(
  name: null,
  avatar: null,
  channel: null
)
```

