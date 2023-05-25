# Cfchat::Webhook

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Float** | The ID of the webhook | [optional] |
| **url** | **String** | The url to which the events will be send | [optional] |
| **subscriptions** | **Array&lt;String&gt;** | The list of subscribed events | [optional] |
| **account_id** | **Float** | The id of the account which the webhook object belongs to | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::Webhook.new(
  id: null,
  url: null,
  subscriptions: null,
  account_id: null
)
```

