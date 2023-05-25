# Cfchat::ConversationsApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**conversation_filter**](ConversationsApi.md#conversation_filter) | **POST** /api/v1/accounts/{account_id}/conversations/filter | Conversations Filter |
| [**conversation_list**](ConversationsApi.md#conversation_list) | **GET** /api/v1/accounts/{account_id}/conversations | Conversations List |
| [**conversation_list_meta**](ConversationsApi.md#conversation_list_meta) | **GET** /api/v1/accounts/{account_id}/conversations/meta | Get Conversation Counts |
| [**get_details_of_a_conversation**](ConversationsApi.md#get_details_of_a_conversation) | **GET** /api/v1/accounts/{account_id}/conversations/{conversation_id} | Conversation Details |
| [**new_conversation**](ConversationsApi.md#new_conversation) | **POST** /api/v1/accounts/{account_id}/conversations | Create New Conversation |
| [**toggle_status_of_a_conversation**](ConversationsApi.md#toggle_status_of_a_conversation) | **POST** /api/v1/accounts/{account_id}/conversations/{conversation_id}/toggle_status | Toggle Status |


## conversation_filter

> <ConversationList> conversation_filter(account_id, payload, opts)

Conversations Filter

Filter conversations with custom filter options and pagination

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

api_instance = Cfchat::ConversationsApi.new
account_id = 56 # Integer | The numeric ID of the account
payload = [Cfchat::ContactFilterRequestInner.new] # Array<ContactFilterRequestInner> | 
opts = {
  page: 56 # Integer | 
}

begin
  # Conversations Filter
  result = api_instance.conversation_filter(account_id, payload, opts)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationsApi->conversation_filter: #{e}"
end
```

#### Using the conversation_filter_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConversationList>, Integer, Hash)> conversation_filter_with_http_info(account_id, payload, opts)

```ruby
begin
  # Conversations Filter
  data, status_code, headers = api_instance.conversation_filter_with_http_info(account_id, payload, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConversationList>
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationsApi->conversation_filter_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **payload** | [**Array&lt;ContactFilterRequestInner&gt;**](ContactFilterRequestInner.md) |  |  |
| **page** | **Integer** |  | [optional] |

### Return type

[**ConversationList**](ConversationList.md)

### Authorization

[userApiKey](../README.md#userApiKey), [agentBotApiKey](../README.md#agentBotApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## conversation_list

> <ConversationList> conversation_list(account_id, opts)

Conversations List

List all the conversations with pagination

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

api_instance = Cfchat::ConversationsApi.new
account_id = 56 # Integer | The numeric ID of the account
opts = {
  assignee_type: 'me', # String | Filter conversations by assignee type.
  status: 'open', # String | Filter by conversation status.
  q: 'q_example', # String | Filters conversations with messages containing the search term
  inbox_id: 56, # Integer | 
  team_id: 56, # Integer | 
  labels: ['inner_example'], # Array<String> | 
  page: 56 # Integer | paginate through conversations
}

begin
  # Conversations List
  result = api_instance.conversation_list(account_id, opts)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationsApi->conversation_list: #{e}"
end
```

#### Using the conversation_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConversationList>, Integer, Hash)> conversation_list_with_http_info(account_id, opts)

```ruby
begin
  # Conversations List
  data, status_code, headers = api_instance.conversation_list_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConversationList>
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationsApi->conversation_list_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **assignee_type** | **String** | Filter conversations by assignee type. | [optional][default to &#39;all&#39;] |
| **status** | **String** | Filter by conversation status. | [optional][default to &#39;open&#39;] |
| **q** | **String** | Filters conversations with messages containing the search term | [optional] |
| **inbox_id** | **Integer** |  | [optional] |
| **team_id** | **Integer** |  | [optional] |
| **labels** | [**Array&lt;String&gt;**](String.md) |  | [optional] |
| **page** | **Integer** | paginate through conversations | [optional][default to 1] |

### Return type

[**ConversationList**](ConversationList.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## conversation_list_meta

> <ConversationListMeta200Response> conversation_list_meta(account_id, opts)

Get Conversation Counts

Get open, unassigned and all Conversation counts

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

api_instance = Cfchat::ConversationsApi.new
account_id = 56 # Integer | The numeric ID of the account
opts = {
  status: 'open', # String | Filter by conversation status.
  q: 'q_example', # String | Filters conversations with messages containing the search term
  inbox_id: 56, # Integer | 
  team_id: 56, # Integer | 
  labels: ['inner_example'] # Array<String> | 
}

begin
  # Get Conversation Counts
  result = api_instance.conversation_list_meta(account_id, opts)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationsApi->conversation_list_meta: #{e}"
end
```

#### Using the conversation_list_meta_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConversationListMeta200Response>, Integer, Hash)> conversation_list_meta_with_http_info(account_id, opts)

```ruby
begin
  # Get Conversation Counts
  data, status_code, headers = api_instance.conversation_list_meta_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConversationListMeta200Response>
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationsApi->conversation_list_meta_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **status** | **String** | Filter by conversation status. | [optional][default to &#39;open&#39;] |
| **q** | **String** | Filters conversations with messages containing the search term | [optional] |
| **inbox_id** | **Integer** |  | [optional] |
| **team_id** | **Integer** |  | [optional] |
| **labels** | [**Array&lt;String&gt;**](String.md) |  | [optional] |

### Return type

[**ConversationListMeta200Response**](ConversationListMeta200Response.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## get_details_of_a_conversation

> <ConversationShow> get_details_of_a_conversation(account_id, conversation_id)

Conversation Details

Get all details regarding a conversation with all messages in the conversation

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

api_instance = Cfchat::ConversationsApi.new
account_id = 56 # Integer | The numeric ID of the account
conversation_id = 56 # Integer | The numeric ID of the conversation

begin
  # Conversation Details
  result = api_instance.get_details_of_a_conversation(account_id, conversation_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationsApi->get_details_of_a_conversation: #{e}"
end
```

#### Using the get_details_of_a_conversation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConversationShow>, Integer, Hash)> get_details_of_a_conversation_with_http_info(account_id, conversation_id)

```ruby
begin
  # Conversation Details
  data, status_code, headers = api_instance.get_details_of_a_conversation_with_http_info(account_id, conversation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConversationShow>
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationsApi->get_details_of_a_conversation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **conversation_id** | **Integer** | The numeric ID of the conversation |  |

### Return type

[**ConversationShow**](ConversationShow.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## new_conversation

> <NewConversation200Response> new_conversation(account_id, data)

Create New Conversation

Creating a conversation in chatwoot requires a source id.    Learn more about source_id: https://github.com/chatwoot/chatwoot/wiki/Building-on-Top-of-Chatwoot:-Importing-Existing-Contacts-and-Creating-Conversations

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

api_instance = Cfchat::ConversationsApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::NewConversationRequest.new # NewConversationRequest | 

begin
  # Create New Conversation
  result = api_instance.new_conversation(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationsApi->new_conversation: #{e}"
end
```

#### Using the new_conversation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<NewConversation200Response>, Integer, Hash)> new_conversation_with_http_info(account_id, data)

```ruby
begin
  # Create New Conversation
  data, status_code, headers = api_instance.new_conversation_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <NewConversation200Response>
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationsApi->new_conversation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**NewConversationRequest**](NewConversationRequest.md) |  |  |

### Return type

[**NewConversation200Response**](NewConversation200Response.md)

### Authorization

[userApiKey](../README.md#userApiKey), [agentBotApiKey](../README.md#agentBotApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## toggle_status_of_a_conversation

> <ConversationStatusToggle> toggle_status_of_a_conversation(account_id, conversation_id, data)

Toggle Status

Toggles the status of the conversation between open and resolved

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

api_instance = Cfchat::ConversationsApi.new
account_id = 56 # Integer | The numeric ID of the account
conversation_id = 56 # Integer | The numeric ID of the conversation
data = Cfchat::ToggleStatusOfAConversationRequest.new({status: 'open'}) # ToggleStatusOfAConversationRequest | 

begin
  # Toggle Status
  result = api_instance.toggle_status_of_a_conversation(account_id, conversation_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationsApi->toggle_status_of_a_conversation: #{e}"
end
```

#### Using the toggle_status_of_a_conversation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConversationStatusToggle>, Integer, Hash)> toggle_status_of_a_conversation_with_http_info(account_id, conversation_id, data)

```ruby
begin
  # Toggle Status
  data, status_code, headers = api_instance.toggle_status_of_a_conversation_with_http_info(account_id, conversation_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConversationStatusToggle>
rescue Cfchat::ApiError => e
  puts "Error when calling ConversationsApi->toggle_status_of_a_conversation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **conversation_id** | **Integer** | The numeric ID of the conversation |  |
| **data** | [**ToggleStatusOfAConversationRequest**](ToggleStatusOfAConversationRequest.md) |  |  |

### Return type

[**ConversationStatusToggle**](ConversationStatusToggle.md)

### Authorization

[userApiKey](../README.md#userApiKey), [agentBotApiKey](../README.md#agentBotApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

