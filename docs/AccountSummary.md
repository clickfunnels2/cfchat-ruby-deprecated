# Cfchat::AccountSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **avg_first_response_time** | **String** |  | [optional] |
| **avg_resolution_time** | **String** |  | [optional] |
| **conversations_count** | **Float** |  | [optional] |
| **incoming_messages_count** | **Float** |  | [optional] |
| **outgoing_messages_count** | **Float** |  | [optional] |
| **resolutions_count** | **Float** |  | [optional] |
| **previous** | [**AccountSummaryPrevious**](AccountSummaryPrevious.md) |  | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::AccountSummary.new(
  avg_first_response_time: null,
  avg_resolution_time: null,
  conversations_count: null,
  incoming_messages_count: null,
  outgoing_messages_count: null,
  resolutions_count: null,
  previous: null
)
```

