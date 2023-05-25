# Cfchat::ContactUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | name of the contact | [optional] |
| **email** | **String** | email of the contact | [optional] |
| **phone_number** | **String** | phone number of the contact | [optional] |
| **avatar** | **File** | Send the form data with the avatar image binary or use the avatar_url | [optional] |
| **avatar_url** | **String** | The url to a jpeg, png file for the contact avatar | [optional] |
| **identifier** | **String** | A unique identifier for the contact in external system | [optional] |
| **custom_attributes** | **Object** | An object where you can store custom attributes for contact. example {\&quot;type\&quot;:\&quot;customer\&quot;, \&quot;age\&quot;:30} | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::ContactUpdate.new(
  name: null,
  email: null,
  phone_number: null,
  avatar: null,
  avatar_url: null,
  identifier: null,
  custom_attributes: null
)
```

