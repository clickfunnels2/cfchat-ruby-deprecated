# Cfchat::CreateAnAccountUserRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **user_id** | **Integer** | The ID of the user |  |
| **role** | **String** | whether user is an administrator or agent |  |

## Example

```ruby
require 'cfchat'

instance = Cfchat::CreateAnAccountUserRequest.new(
  user_id: null,
  role: null
)
```

