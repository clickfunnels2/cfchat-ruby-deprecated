# Cfchat::MessagesAPIApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_a_message**](MessagesAPIApi.md#create_a_message) | **POST** /public/api/v1/inboxes/{inbox_identifier}/contacts/{contact_identifier}/conversations/{conversation_id}/messages | Create a message |
| [**list_all_converation_messages**](MessagesAPIApi.md#list_all_converation_messages) | **GET** /public/api/v1/inboxes/{inbox_identifier}/contacts/{contact_identifier}/conversations/{conversation_id}/messages | List all messages |
| [**update_a_message**](MessagesAPIApi.md#update_a_message) | **PATCH** /public/api/v1/inboxes/{inbox_identifier}/contacts/{contact_identifier}/conversations/{conversation_id}/messages/{message_id} | Update a message |


## create_a_message

> <PublicMessage> create_a_message(inbox_identifier, contact_identifier, conversation_id, data)

Create a message

Create a message

### Examples

```ruby
require 'time'
require 'cfchat'

api_instance = Cfchat::MessagesAPIApi.new
inbox_identifier = 'inbox_identifier_example' # String | The identifier obtained from API inbox channel
contact_identifier = 'contact_identifier_example' # String | The source id of contact obtained on contact create
conversation_id = 56 # Integer | The numeric ID of the conversation
data = Cfchat::PublicMessageCreatePayload.new # PublicMessageCreatePayload | 

begin
  # Create a message
  result = api_instance.create_a_message(inbox_identifier, contact_identifier, conversation_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling MessagesAPIApi->create_a_message: #{e}"
end
```

#### Using the create_a_message_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PublicMessage>, Integer, Hash)> create_a_message_with_http_info(inbox_identifier, contact_identifier, conversation_id, data)

```ruby
begin
  # Create a message
  data, status_code, headers = api_instance.create_a_message_with_http_info(inbox_identifier, contact_identifier, conversation_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PublicMessage>
rescue Cfchat::ApiError => e
  puts "Error when calling MessagesAPIApi->create_a_message_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inbox_identifier** | **String** | The identifier obtained from API inbox channel |  |
| **contact_identifier** | **String** | The source id of contact obtained on contact create |  |
| **conversation_id** | **Integer** | The numeric ID of the conversation |  |
| **data** | [**PublicMessageCreatePayload**](PublicMessageCreatePayload.md) |  |  |

### Return type

[**PublicMessage**](PublicMessage.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## list_all_converation_messages

> <Array<PublicMessage>> list_all_converation_messages(inbox_identifier, contact_identifier, conversation_id)

List all messages

List all messages in the conversation

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

api_instance = Cfchat::MessagesAPIApi.new
inbox_identifier = 'inbox_identifier_example' # String | The identifier obtained from API inbox channel
contact_identifier = 'contact_identifier_example' # String | The source id of contact obtained on contact create
conversation_id = 56 # Integer | The numeric ID of the conversation

begin
  # List all messages
  result = api_instance.list_all_converation_messages(inbox_identifier, contact_identifier, conversation_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling MessagesAPIApi->list_all_converation_messages: #{e}"
end
```

#### Using the list_all_converation_messages_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<PublicMessage>>, Integer, Hash)> list_all_converation_messages_with_http_info(inbox_identifier, contact_identifier, conversation_id)

```ruby
begin
  # List all messages
  data, status_code, headers = api_instance.list_all_converation_messages_with_http_info(inbox_identifier, contact_identifier, conversation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<PublicMessage>>
rescue Cfchat::ApiError => e
  puts "Error when calling MessagesAPIApi->list_all_converation_messages_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inbox_identifier** | **String** | The identifier obtained from API inbox channel |  |
| **contact_identifier** | **String** | The source id of contact obtained on contact create |  |
| **conversation_id** | **Integer** | The numeric ID of the conversation |  |

### Return type

[**Array&lt;PublicMessage&gt;**](PublicMessage.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_a_message

> <PublicMessage> update_a_message(inbox_identifier, contact_identifier, conversation_id, message_id, data)

Update a message

Update a message

### Examples

```ruby
require 'time'
require 'cfchat'

api_instance = Cfchat::MessagesAPIApi.new
inbox_identifier = 'inbox_identifier_example' # String | The identifier obtained from API inbox channel
contact_identifier = 'contact_identifier_example' # String | The source id of contact obtained on contact create
conversation_id = 56 # Integer | The numeric ID of the conversation
message_id = 56 # Integer | The numeric ID of the message
data = Cfchat::PublicMessageUpdatePayload.new # PublicMessageUpdatePayload | 

begin
  # Update a message
  result = api_instance.update_a_message(inbox_identifier, contact_identifier, conversation_id, message_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling MessagesAPIApi->update_a_message: #{e}"
end
```

#### Using the update_a_message_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PublicMessage>, Integer, Hash)> update_a_message_with_http_info(inbox_identifier, contact_identifier, conversation_id, message_id, data)

```ruby
begin
  # Update a message
  data, status_code, headers = api_instance.update_a_message_with_http_info(inbox_identifier, contact_identifier, conversation_id, message_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PublicMessage>
rescue Cfchat::ApiError => e
  puts "Error when calling MessagesAPIApi->update_a_message_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inbox_identifier** | **String** | The identifier obtained from API inbox channel |  |
| **contact_identifier** | **String** | The source id of contact obtained on contact create |  |
| **conversation_id** | **Integer** | The numeric ID of the conversation |  |
| **message_id** | **Integer** | The numeric ID of the message |  |
| **data** | [**PublicMessageUpdatePayload**](PublicMessageUpdatePayload.md) |  |  |

### Return type

[**PublicMessage**](PublicMessage.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

