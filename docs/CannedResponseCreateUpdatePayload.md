# Cfchat::CannedResponseCreateUpdatePayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content** | **String** | Message content for canned response | [optional] |
| **short_code** | **String** | Short Code for quick access of the canned response | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::CannedResponseCreateUpdatePayload.new(
  content: null,
  short_code: null
)
```

