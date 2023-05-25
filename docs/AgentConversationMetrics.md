# Cfchat::AgentConversationMetrics

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Float** |  | [optional] |
| **name** | **String** |  | [optional] |
| **email** | **String** |  | [optional] |
| **thumbnail** | **String** |  | [optional] |
| **availability** | **String** |  | [optional] |
| **metric** | [**AgentConversationMetricsMetric**](AgentConversationMetricsMetric.md) |  | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::AgentConversationMetrics.new(
  id: null,
  name: null,
  email: null,
  thumbnail: null,
  availability: null,
  metric: null
)
```

