# Cfchat::PublicMessageCreatePayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content** | **String** | Content for the message | [optional] |
| **echo_id** | **String** | Temporary identifier which will be passed back via websockets | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::PublicMessageCreatePayload.new(
  content: null,
  echo_id: null
)
```

