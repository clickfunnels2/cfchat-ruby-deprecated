# Cfchat::Inbox

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Float** | ID of the inbox | [optional] |
| **name** | **String** | The name of the inbox | [optional] |
| **website_url** | **String** | Website URL | [optional] |
| **channel_type** | **String** | The type of the inbox | [optional] |
| **avatar_url** | **String** | The avatar image of the inbox | [optional] |
| **widget_color** | **String** | Widget Color used for customization of the widget | [optional] |
| **website_token** | **String** | Website Token | [optional] |
| **enable_auto_assignment** | **Boolean** | The flag which shows whether Auto Assignment is enabled or not | [optional] |
| **web_widget_script** | **String** | Script used to load the website widget | [optional] |
| **welcome_title** | **String** | Welcome title to be displayed on the widget | [optional] |
| **welcome_tagline** | **String** | Welcome tagline to be displayed on the widget | [optional] |
| **greeting_enabled** | **Boolean** | The flag which shows whether greeting is enabled | [optional] |
| **greeting_message** | **String** | A greeting message when the user starts the conversation | [optional] |

## Example

```ruby
require 'cfchat'

instance = Cfchat::Inbox.new(
  id: null,
  name: null,
  website_url: null,
  channel_type: null,
  avatar_url: null,
  widget_color: null,
  website_token: null,
  enable_auto_assignment: null,
  web_widget_script: null,
  welcome_title: null,
  welcome_tagline: null,
  greeting_enabled: null,
  greeting_message: null
)
```

