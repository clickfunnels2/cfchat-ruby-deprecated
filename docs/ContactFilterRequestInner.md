# Cfchat::ContactFilterRequestInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attribute_key** | **String** | filter attribute name | [optional] |
| **filter_operator** | **String** | filter operator name | [optional] |
| **values** | **Array&lt;String&gt;** | array of the attribute values to filter | [optional] |
| **query_operator** | **String** | query operator name | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::ContactFilterRequestInner.new(
  attribute_key: null,
  filter_operator: null,
  values: null,
  query_operator: null
)
```

