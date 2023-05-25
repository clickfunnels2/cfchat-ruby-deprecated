# Cfchat::UpdateInboxRequestChannel

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **website_url** | **String** | URL at which the widget will be loaded | [optional] |
| **welcome_title** | **String** | Welcome title to be displayed on the widget | [optional] |
| **welcome_tagline** | **String** | Welcome tagline to be displayed on the widget | [optional] |
| **agent_away_message** | **String** | A message which will be sent if there is not agent available. This is not available if agentbot is connected | [optional] |
| **widget_color** | **String** | A Hex-color string used to customize the widget | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::UpdateInboxRequestChannel.new(
  website_url: null,
  welcome_title: null,
  welcome_tagline: null,
  agent_away_message: null,
  widget_color: null
)
```

