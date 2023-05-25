# Cfchat::UpdateInboxRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The name of the inbox | [optional] |
| **enable_auto_assignment** | **Boolean** | Enable Auto Assignment |  |
| **avatar** | **File** | Image file for avatar | [optional] |
| **channel** | [**UpdateInboxRequestChannel**](UpdateInboxRequestChannel.md) |  | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::UpdateInboxRequest.new(
  name: null,
  enable_auto_assignment: null,
  avatar: null,
  channel: null
)
```

