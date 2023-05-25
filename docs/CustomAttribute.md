# Cfchat::CustomAttribute

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | Identifier | [optional] |
| **attribute_display_name** | **String** | Attribute display name | [optional] |
| **attribute_display_type** | **String** | Attribute display type (text, number, currency, percent, link, date, list, checkbox) | [optional] |
| **attribute_description** | **String** | Attribute description | [optional] |
| **attribute_key** | **String** | Attribute unique key value | [optional] |
| **attribute_values** | **String** | Attribute values | [optional] |
| **default_value** | **String** | Attribute default value | [optional] |
| **attribute_model** | **String** | Attribute type(conversation_attribute/contact_attribute) | [optional] |
| **account_id** | **Integer** | Account Id | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::CustomAttribute.new(
  id: null,
  attribute_display_name: null,
  attribute_display_type: null,
  attribute_description: null,
  attribute_key: null,
  attribute_values: null,
  default_value: null,
  attribute_model: null,
  account_id: null
)
```

