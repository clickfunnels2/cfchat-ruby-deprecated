# Cfchat::PublicContactCreateUpdatePayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **identifier** | **String** | External identifier of the contact | [optional] |
| **identifier_hash** | **String** | Identifier hash prepared for HMAC authentication | [optional] |
| **email** | **String** | Email of the contact | [optional] |
| **name** | **String** | Name of the contact | [optional] |
| **phone_number** | **String** | Phone number of the contact | [optional] |
| **avatar_url** | **String** | The url to a jpeg, png file for the user avatar | [optional] |
| **custom_attributes** | **Object** | Custom attributes of the customer | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::PublicContactCreateUpdatePayload.new(
  identifier: null,
  identifier_hash: null,
  email: null,
  name: null,
  phone_number: null,
  avatar_url: null,
  custom_attributes: null
)
```

