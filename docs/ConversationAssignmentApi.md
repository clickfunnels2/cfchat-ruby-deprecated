# Cfchat::ConversationAssignmentApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**assign_a_conversation**](ConversationAssignmentApi.md#assign_a_conversation) | **POST** /api/v1/accounts/{account_id}/conversations/{conversation_id}/assignments | Assign Conversation |


## assign_a_conversation

> <User> assign_a_conversation(account_id, conversation_id, data)

Assign Conversation

Assign a conversation to an agent or a team

### Examples

```ruby
require 'time'
require 'cfchat'
# setup authorization
Cfchat.configure do |config|
  # Configure API key authorization: userApiKey
  config.api_key['userApiKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['userApiKey'] = 'Bearer'
end

api_instance = Cfchat::ConversationAssignmentApi.new
account_id = 56 # Integer | The numeric ID of the account
conversation_id = 56 # Integer | The numeric ID of the conversation
data = Cfchat::AssignAConversationRequest.new # AssignAConversationRequest | 

begin
  # Assign Conversation
  result = api_instance.assign_a_conversation(account_id, conversation_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationAssignmentApi->assign_a_conversation: #{e}"
end
```

#### Using the assign_a_conversation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<User>, Integer, Hash)> assign_a_conversation_with_http_info(account_id, conversation_id, data)

```ruby
begin
  # Assign Conversation
  data, status_code, headers = api_instance.assign_a_conversation_with_http_info(account_id, conversation_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <User>
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationAssignmentApi->assign_a_conversation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **conversation_id** | **Integer** | The numeric ID of the conversation |  |
| **data** | [**AssignAConversationRequest**](AssignAConversationRequest.md) |  |  |

### Return type

[**User**](User.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

