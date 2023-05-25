# Cfchat::Agent

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  | [optional] |
| **uid** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **available_name** | **String** |  | [optional] |
| **display_name** | **String** |  | [optional] |
| **email** | **String** |  | [optional] |
| **account_id** | **Integer** |  | [optional] |
| **role** | **String** |  | [optional] |
| **confirmed** | **Boolean** |  | [optional] |
| **availability_status** | **String** | The availability status of the agent computed by Chatwoot. | [optional] |
| **auto_offline** | **Boolean** | Whether the availability status of agent is configured to go offline automatically when away. | [optional] |
| **custom_attributes** | **Object** | Available for users who are created through platform APIs and has custom attributes associated. | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::Agent.new(
  id: null,
  uid: null,
  name: null,
  available_name: null,
  display_name: null,
  email: null,
  account_id: null,
  role: null,
  confirmed: null,
  availability_status: null,
  auto_offline: null,
  custom_attributes: null
)
```

