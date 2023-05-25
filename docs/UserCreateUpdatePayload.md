# Cfchat::UserCreateUpdatePayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Name of the user | [optional] |
| **email** | **String** | Email of the user | [optional] |
| **password** | **String** | Password must contain uppercase, lowercase letters, number and a special character | [optional] |
| **custom_attributes** | **Object** | Custom attributes you want to associate with the user | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::UserCreateUpdatePayload.new(
  name: null,
  email: null,
  password: null,
  custom_attributes: null
)
```

