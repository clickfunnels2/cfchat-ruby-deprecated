# Cfchat::InboxAPIApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_details_of_a_inbox**](InboxAPIApi.md#get_details_of_a_inbox) | **GET** /public/api/v1/inboxes/{inbox_identifier} | Inbox details |


## get_details_of_a_inbox

> <PublicInbox> get_details_of_a_inbox(inbox_identifier)

Inbox details

Get the details of an inbox

### Examples

```ruby
require 'time'
require 'cfchat'

api_instance = Cfchat::InboxAPIApi.new
inbox_identifier = 'inbox_identifier_example' # String | The identifier obtained from API inbox channel

begin
  # Inbox details
  result = api_instance.get_details_of_a_inbox(inbox_identifier)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling InboxAPIApi->get_details_of_a_inbox: #{e}"
end
```

#### Using the get_details_of_a_inbox_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PublicInbox>, Integer, Hash)> get_details_of_a_inbox_with_http_info(inbox_identifier)

```ruby
begin
  # Inbox details
  data, status_code, headers = api_instance.get_details_of_a_inbox_with_http_info(inbox_identifier)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PublicInbox>
rescue Cfchat::ApiError => e
  puts "Error when calling InboxAPIApi->get_details_of_a_inbox_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inbox_identifier** | **String** | The identifier obtained from API inbox channel |  |

### Return type

[**PublicInbox**](PublicInbox.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8

