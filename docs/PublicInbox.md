# Cfchat::PublicInbox

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **identifier** | **String** | Inbox identifier | [optional] |
| **name** | **String** | Name of the inbox | [optional] |
| **timezone** | **String** | The timezone defined on the inbox | [optional] |
| **working_hours** | [**Array&lt;PublicInboxWorkingHoursInner&gt;**](PublicInboxWorkingHoursInner.md) | The working hours defined on the inbox | [optional] |
| **working_hours_enabled** | **Boolean** | Whether of not the working hours are enabled on the inbox | [optional] |
| **csat_survey_enabled** | **Boolean** | Whether of not the Customer Satisfaction survey is enabled on the inbox | [optional] |
| **greeting_enabled** | **Boolean** | Whether of not the Greeting Message is enabled on the inbox | [optional] |
| **identity_validation_enabled** | **Boolean** | Whether of not the User Identity Validation is enforced on the inbox | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::PublicInbox.new(
  identifier: null,
  name: null,
  timezone: null,
  working_hours: null,
  working_hours_enabled: null,
  csat_survey_enabled: null,
  greeting_enabled: null,
  identity_validation_enabled: null
)
```

