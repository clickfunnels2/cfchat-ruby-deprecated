# Cfchat::CustomFilter

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Float** | The ID of the custom filter | [optional] |
| **name** | **String** | The name of the custom filter | [optional] |
| **type** | **String** | The description about the custom filter | [optional] |
| **query** | **Object** | A query that needs to be saved as a custom filter | [optional] |
| **created_at** | **Time** | The time at which the custom filter was created | [optional] |
| **updated_at** | **Time** | The time at which the custom filter was updated | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::CustomFilter.new(
  id: null,
  name: null,
  type: null,
  query: null,
  created_at: null,
  updated_at: null
)
```

