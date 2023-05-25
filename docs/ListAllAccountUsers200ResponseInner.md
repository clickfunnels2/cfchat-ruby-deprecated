# Cfchat::ListAllAccountUsers200ResponseInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The ID of the user | [optional] |
| **user_id** | **Integer** | The ID of the user | [optional] |
| **role** | **String** | whether user is an administrator or agent | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::ListAllAccountUsers200ResponseInner.new(
  account_id: null,
  user_id: null,
  role: null
)
```

