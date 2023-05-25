# Cfchat::WebhookCreateUpdatePayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | The url where the events should be sent | [optional] |
| **subscriptions** | **Array&lt;String&gt;** | The events you want to subscribe to. | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::WebhookCreateUpdatePayload.new(
  url: null,
  subscriptions: null
)
```

