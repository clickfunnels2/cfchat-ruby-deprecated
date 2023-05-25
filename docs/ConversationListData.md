# Cfchat::ConversationListData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **meta** | [**ConversationListMeta200ResponseMeta**](ConversationListMeta200ResponseMeta.md) |  | [optional] |
| **payload** | [**Array&lt;ConversationListDataPayloadInner&gt;**](ConversationListDataPayloadInner.md) | array of conversations | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::ConversationListData.new(
  meta: null,
  payload: null
)
```

