# Cfchat::IntegrationsApp

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The ID of the integration | [optional] |
| **name** | **String** | The name of the integration | [optional] |
| **description** | **String** | The description about the team | [optional] |
| **hook_type** | **String** | Whether the integration is an account or inbox integration | [optional] |
| **enabled** | **Boolean** | Whether the integration is enabled for the account | [optional] |
| **allow_multiple_hooks** | **Boolean** | Whether multiple hooks can be created for the integration | [optional] |
| **hooks** | **Array&lt;Object&gt;** | If there are any hooks created for this integration | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::IntegrationsApp.new(
  id: null,
  name: null,
  description: null,
  hook_type: null,
  enabled: null,
  allow_multiple_hooks: null,
  hooks: null
)
```

