# Cfchat::IntegrationsHookCreatePayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **app_id** | **String** | The ID of app for which integration hook is being created | [optional] |
| **inbox_id** | **String** | The inbox ID, if the hook is an inbox hook | [optional] |
| **settings** | **Object** | The settings required by the integration | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::IntegrationsHookCreatePayload.new(
  app_id: null,
  inbox_id: null,
  settings: null
)
```

