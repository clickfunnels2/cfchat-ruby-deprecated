# Cfchat::MessagesApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_a_new_message_in_a_conversation**](MessagesApi.md#create_a_new_message_in_a_conversation) | **POST** /api/v1/accounts/{account_id}/conversations/{conversation_id}/messages | Create New Message |
| [**delete_a_message**](MessagesApi.md#delete_a_message) | **DELETE** /api/v1/accounts/{account_id}/conversations/{conversation_id}/messages/{message_id} | Delete a message |
| [**list_all_messages**](MessagesApi.md#list_all_messages) | **GET** /api/v1/accounts/{account_id}/conversations/{conversation_id}/messages | Get messages |


## create_a_new_message_in_a_conversation

> <CreateANewMessageInAConversation200Response> create_a_new_message_in_a_conversation(account_id, conversation_id, data)

Create New Message

Create a new message in the conversation

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

  # Configure API key authorization: agentBotApiKey
  config.api_key['agentBotApiKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['agentBotApiKey'] = 'Bearer'
end

api_instance = Cfchat::MessagesApi.new
account_id = 56 # Integer | The numeric ID of the account
conversation_id = 56 # Integer | The numeric ID of the conversation
data = Cfchat::ConversationMessageCreate.new({content: 'content_example'}) # ConversationMessageCreate | 

begin
  # Create New Message
  result = api_instance.create_a_new_message_in_a_conversation(account_id, conversation_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling MessagesApi->create_a_new_message_in_a_conversation: #{e}"
end
```

#### Using the create_a_new_message_in_a_conversation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateANewMessageInAConversation200Response>, Integer, Hash)> create_a_new_message_in_a_conversation_with_http_info(account_id, conversation_id, data)

```ruby
begin
  # Create New Message
  data, status_code, headers = api_instance.create_a_new_message_in_a_conversation_with_http_info(account_id, conversation_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateANewMessageInAConversation200Response>
rescue Cfchat::ApiError => e
  puts "Error when calling MessagesApi->create_a_new_message_in_a_conversation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **conversation_id** | **Integer** | The numeric ID of the conversation |  |
| **data** | [**ConversationMessageCreate**](ConversationMessageCreate.md) |  |  |

### Return type

[**CreateANewMessageInAConversation200Response**](CreateANewMessageInAConversation200Response.md)

### Authorization

[userApiKey](../README.md#userApiKey), [agentBotApiKey](../README.md#agentBotApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_a_message

> delete_a_message(account_id, conversation_id, message_id)

Delete a message

Delete a message and it's attachments from the conversation.

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

api_instance = Cfchat::MessagesApi.new
account_id = 56 # Integer | The numeric ID of the account
conversation_id = 56 # Integer | The numeric ID of the conversation
message_id = 56 # Integer | The numeric ID of the message

begin
  # Delete a message
  api_instance.delete_a_message(account_id, conversation_id, message_id)
rescue Cfchat::ApiError => e
  puts "Error when calling MessagesApi->delete_a_message: #{e}"
end
```

#### Using the delete_a_message_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_a_message_with_http_info(account_id, conversation_id, message_id)

```ruby
begin
  # Delete a message
  data, status_code, headers = api_instance.delete_a_message_with_http_info(account_id, conversation_id, message_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling MessagesApi->delete_a_message_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **conversation_id** | **Integer** | The numeric ID of the conversation |  |
| **message_id** | **Integer** | The numeric ID of the message |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## list_all_messages

> <Array<ListAllMessages200ResponseInner>> list_all_messages(account_id, conversation_id)

Get messages

List all messages of a conversation

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

api_instance = Cfchat::MessagesApi.new
account_id = 56 # Integer | The numeric ID of the account
conversation_id = 56 # Integer | The numeric ID of the conversation

begin
  # Get messages
  result = api_instance.list_all_messages(account_id, conversation_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling MessagesApi->list_all_messages: #{e}"
end
```

#### Using the list_all_messages_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ListAllMessages200ResponseInner>>, Integer, Hash)> list_all_messages_with_http_info(account_id, conversation_id)

```ruby
begin
  # Get messages
  data, status_code, headers = api_instance.list_all_messages_with_http_info(account_id, conversation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ListAllMessages200ResponseInner>>
rescue Cfchat::ApiError => e
  puts "Error when calling MessagesApi->list_all_messages_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **conversation_id** | **Integer** | The numeric ID of the conversation |  |

### Return type

[**Array&lt;ListAllMessages200ResponseInner&gt;**](ListAllMessages200ResponseInner.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8

