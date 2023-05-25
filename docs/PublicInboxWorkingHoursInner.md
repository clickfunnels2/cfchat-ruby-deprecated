# Cfchat::PublicInboxWorkingHoursInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **day_of_week** | **Integer** | Day of the week as a number. Sunday -&gt; 0, Saturday -&gt; 6 | [optional] |
| **open_all_day** | **Boolean** | Whether or not the business is open the whole day | [optional] |
| **closed_all_day** | **Boolean** | Whether or not the business is closed the whole day | [optional] |
| **open_hour** | **Integer** | Opening hour. Can be null if closed all day | [optional] |
| **open_minutes** | **Integer** | Opening minute. Can be null if closed all day | [optional] |
| **close_hour** | **Integer** | Closing hour. Can be null if closed all day | [optional] |
| **close_minutes** | **Integer** | Closing minute. Can be null if closed all day | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::PublicInboxWorkingHoursInner.new(
  day_of_week: null,
  open_all_day: null,
  closed_all_day: null,
  open_hour: null,
  open_minutes: null,
  close_hour: null,
  close_minutes: null
)
```

