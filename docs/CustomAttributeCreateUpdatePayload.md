# Cfchat::CustomAttributeCreateUpdatePayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attribute_display_name** | **String** | Attribute display name | [optional] |
| **attribute_display_type** | **Integer** | Attribute display type (text- 0, number- 1, currency- 2, percent- 3, link- 4, date- 5, list- 6, checkbox- 7) | [optional] |
| **attribute_description** | **String** | Attribute description | [optional] |
| **attribute_key** | **String** | Attribute unique key value | [optional] |
| **attribute_values** | **Array&lt;String&gt;** | Attribute values | [optional] |
| **attribute_model** | **Integer** | Attribute type(conversation_attribute- 0, contact_attribute- 1) | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::CustomAttributeCreateUpdatePayload.new(
  attribute_display_name: null,
  attribute_display_type: null,
  attribute_description: null,
  attribute_key: null,
  attribute_values: null,
  attribute_model: null
)
```

