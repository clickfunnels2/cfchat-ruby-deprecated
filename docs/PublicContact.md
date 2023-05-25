# Cfchat::PublicContact

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | Id of the contact | [optional] |
| **source_id** | **String** | The session identifier of the contact | [optional] |
| **name** | **String** | Name of the contact | [optional] |
| **email** | **String** | Email of the contact | [optional] |
| **pubsub_token** | **String** | The token to be used to connect to chatwoot websocket | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::PublicContact.new(
  id: null,
  source_id: null,
  name: null,
  email: null,
  pubsub_token: null
)
```

