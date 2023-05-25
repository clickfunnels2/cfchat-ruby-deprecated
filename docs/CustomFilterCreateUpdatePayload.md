# Cfchat::CustomFilterCreateUpdatePayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The name of the custom filter | [optional] |
| **type** | **String** | The description about the custom filter | [optional] |
| **query** | **Object** | A query that needs to be saved as a custom filter | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::CustomFilterCreateUpdatePayload.new(
  name: null,
  type: null,
  query: null
)
```

