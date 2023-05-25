# Cfchat::ContactPayloadContact

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email** | **String** | Email address of the contact | [optional] |
| **name** | **String** | The name of the contact | [optional] |
| **phone_number** | **String** | Phone number of the contact | [optional] |
| **thumbnail** | **String** | Avatar URL of the contact | [optional] |
| **additional_attributes** | **Object** | The object containing additional attributes related to the contact | [optional] |
| **custom_attributes** | **Object** | The object to save custom attributes for contact, accepts custom attributes key and value | [optional] |
| **contact_inboxes** | [**Array&lt;ContactInboxes&gt;**](ContactInboxes.md) |  | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::ContactPayloadContact.new(
  email: null,
  name: null,
  phone_number: null,
  thumbnail: null,
  additional_attributes: null,
  custom_attributes: {&quot;attribute_key&quot;:&quot;attribute_value&quot;,&quot;signed_up_at&quot;:&quot;dd/mm/yyyy&quot;},
  contact_inboxes: null
)
```

