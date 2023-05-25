# Cfchat::CannedResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | ID of the canned response | [optional] |
| **content** | **String** | Message content for canned response | [optional] |
| **short_code** | **String** | Short Code for quick access of the canned response | [optional] |
| **account_id** | **Integer** | Account Id | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::CannedResponse.new(
  id: null,
  content: null,
  short_code: null,
  account_id: null
)
```

