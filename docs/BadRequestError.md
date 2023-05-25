# Cfchat::BadRequestError

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **description** | **String** |  | [optional] |
| **errors** | [**Array&lt;RequestError&gt;**](RequestError.md) |  | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::BadRequestError.new(
  description: null,
  errors: null
)
```

