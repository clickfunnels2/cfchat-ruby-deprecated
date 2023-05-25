# Cfchat::IntegrationsHook

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The ID of the integration hook | [optional] |
| **app_id** | **String** | The ID of the integration app | [optional] |
| **inbox_id** | **String** | Inbox ID if its an Inbox integration | [optional] |
| **account_id** | **String** | Account ID of the integration | [optional] |
| **status** | **Boolean** | Whether the integration hook is enabled for the account | [optional] |
| **hook_type** | **Boolean** | Whether its an account or inbox integration hook | [optional] |
| **settings** | **Object** | The associated settings for the integration | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::IntegrationsHook.new(
  id: null,
  app_id: null,
  inbox_id: null,
  account_id: null,
  status: null,
  hook_type: null,
  settings: null
)
```

