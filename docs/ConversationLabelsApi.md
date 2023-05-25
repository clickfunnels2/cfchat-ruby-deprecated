# Cfchat::ConversationLabelsApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**conversation_add_labels**](ConversationLabelsApi.md#conversation_add_labels) | **POST** /api/v1/accounts/{account_id}/conversations/{conversation_id}/labels | Add Labels |
| [**list_all_labels_of_a_conversation**](ConversationLabelsApi.md#list_all_labels_of_a_conversation) | **GET** /api/v1/accounts/{account_id}/conversations/{conversation_id}/labels | List Labels |


## conversation_add_labels

> <ConversationLabels> conversation_add_labels(account_id, conversation_id, data)

Add Labels

Add labels to a conversation. Note that this API would overwrite the existing list of labels associated to the conversation.

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

api_instance = Cfchat::ConversationLabelsApi.new
account_id = 56 # Integer | The numeric ID of the account
conversation_id = 56 # Integer | The numeric ID of the conversation
data = Cfchat::ConversationAddLabelsRequest.new # ConversationAddLabelsRequest | 

begin
  # Add Labels
  result = api_instance.conversation_add_labels(account_id, conversation_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationLabelsApi->conversation_add_labels: #{e}"
end
```

#### Using the conversation_add_labels_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConversationLabels>, Integer, Hash)> conversation_add_labels_with_http_info(account_id, conversation_id, data)

```ruby
begin
  # Add Labels
  data, status_code, headers = api_instance.conversation_add_labels_with_http_info(account_id, conversation_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConversationLabels>
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationLabelsApi->conversation_add_labels_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **conversation_id** | **Integer** | The numeric ID of the conversation |  |
| **data** | [**ConversationAddLabelsRequest**](ConversationAddLabelsRequest.md) |  |  |

### Return type

[**ConversationLabels**](ConversationLabels.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## list_all_labels_of_a_conversation

> <ConversationLabels> list_all_labels_of_a_conversation(account_id, conversation_id)

List Labels

Lists all the labels of a conversation

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

api_instance = Cfchat::ConversationLabelsApi.new
account_id = 56 # Integer | The numeric ID of the account
conversation_id = 56 # Integer | The numeric ID of the conversation

begin
  # List Labels
  result = api_instance.list_all_labels_of_a_conversation(account_id, conversation_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationLabelsApi->list_all_labels_of_a_conversation: #{e}"
end
```

#### Using the list_all_labels_of_a_conversation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConversationLabels>, Integer, Hash)> list_all_labels_of_a_conversation_with_http_info(account_id, conversation_id)

```ruby
begin
  # List Labels
  data, status_code, headers = api_instance.list_all_labels_of_a_conversation_with_http_info(account_id, conversation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConversationLabels>
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationLabelsApi->list_all_labels_of_a_conversation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **conversation_id** | **Integer** | The numeric ID of the conversation |  |

### Return type

[**ConversationLabels**](ConversationLabels.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8

