# Cfchat::AgentBotsApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_an_agent_bot**](AgentBotsApi.md#create_an_agent_bot) | **POST** /platform/api/v1/agent_bots | Create an Agent Bot |
| [**delete_an_agent_bot**](AgentBotsApi.md#delete_an_agent_bot) | **DELETE** /platform/api/v1/agent_bots/{id} | Delete an AgentBot |
| [**get_details_of_a_single_agent_bot**](AgentBotsApi.md#get_details_of_a_single_agent_bot) | **GET** /platform/api/v1/agent_bots/{id} | Get an agent bot details |
| [**list_all_agent_bots**](AgentBotsApi.md#list_all_agent_bots) | **GET** /platform/api/v1/agent_bots | List all AgentBots |
| [**update_an_agent_bot**](AgentBotsApi.md#update_an_agent_bot) | **PATCH** /platform/api/v1/agent_bots/{id} | Update an agent bot |


## create_an_agent_bot

> <AgentBot> create_an_agent_bot(data)

Create an Agent Bot

Create an agent bot

### Examples

```ruby
require 'time'
require 'cfchat'
# setup authorization
Cfchat.configure do |config|
  # Configure API key authorization: platformAppApiKey
  config.api_key['platformAppApiKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['platformAppApiKey'] = 'Bearer'
end

api_instance = Cfchat::AgentBotsApi.new
data = Cfchat::AgentBotCreateUpdatePayload.new # AgentBotCreateUpdatePayload | 

begin
  # Create an Agent Bot
  result = api_instance.create_an_agent_bot(data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AgentBotsApi->create_an_agent_bot: #{e}"
end
```

#### Using the create_an_agent_bot_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AgentBot>, Integer, Hash)> create_an_agent_bot_with_http_info(data)

```ruby
begin
  # Create an Agent Bot
  data, status_code, headers = api_instance.create_an_agent_bot_with_http_info(data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AgentBot>
rescue Cfchat::ApiError => e
  puts "Error when calling AgentBotsApi->create_an_agent_bot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**AgentBotCreateUpdatePayload**](AgentBotCreateUpdatePayload.md) |  |  |

### Return type

[**AgentBot**](AgentBot.md)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_an_agent_bot

> delete_an_agent_bot(id)

Delete an AgentBot

Delete an AgentBot

### Examples

```ruby
require 'time'
require 'cfchat'
# setup authorization
Cfchat.configure do |config|
  # Configure API key authorization: platformAppApiKey
  config.api_key['platformAppApiKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['platformAppApiKey'] = 'Bearer'
end

api_instance = Cfchat::AgentBotsApi.new
id = 56 # Integer | The ID of the agentbot to be updated

begin
  # Delete an AgentBot
  api_instance.delete_an_agent_bot(id)
rescue Cfchat::ApiError => e
  puts "Error when calling AgentBotsApi->delete_an_agent_bot: #{e}"
end
```

#### Using the delete_an_agent_bot_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_an_agent_bot_with_http_info(id)

```ruby
begin
  # Delete an AgentBot
  data, status_code, headers = api_instance.delete_an_agent_bot_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling AgentBotsApi->delete_an_agent_bot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The ID of the agentbot to be updated |  |

### Return type

nil (empty response body)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_details_of_a_single_agent_bot

> <AgentBot> get_details_of_a_single_agent_bot(id)

Get an agent bot details

Get the details of an agent bot

### Examples

```ruby
require 'time'
require 'cfchat'
# setup authorization
Cfchat.configure do |config|
  # Configure API key authorization: platformAppApiKey
  config.api_key['platformAppApiKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['platformAppApiKey'] = 'Bearer'
end

api_instance = Cfchat::AgentBotsApi.new
id = 56 # Integer | The ID of the agentbot to be updated

begin
  # Get an agent bot details
  result = api_instance.get_details_of_a_single_agent_bot(id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AgentBotsApi->get_details_of_a_single_agent_bot: #{e}"
end
```

#### Using the get_details_of_a_single_agent_bot_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AgentBot>, Integer, Hash)> get_details_of_a_single_agent_bot_with_http_info(id)

```ruby
begin
  # Get an agent bot details
  data, status_code, headers = api_instance.get_details_of_a_single_agent_bot_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AgentBot>
rescue Cfchat::ApiError => e
  puts "Error when calling AgentBotsApi->get_details_of_a_single_agent_bot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The ID of the agentbot to be updated |  |

### Return type

[**AgentBot**](AgentBot.md)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## list_all_agent_bots

> <Array<AgentBot>> list_all_agent_bots

List all AgentBots

List all agent bots available

### Examples

```ruby
require 'time'
require 'cfchat'
# setup authorization
Cfchat.configure do |config|
  # Configure API key authorization: platformAppApiKey
  config.api_key['platformAppApiKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['platformAppApiKey'] = 'Bearer'
end

api_instance = Cfchat::AgentBotsApi.new

begin
  # List all AgentBots
  result = api_instance.list_all_agent_bots
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AgentBotsApi->list_all_agent_bots: #{e}"
end
```

#### Using the list_all_agent_bots_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<AgentBot>>, Integer, Hash)> list_all_agent_bots_with_http_info

```ruby
begin
  # List all AgentBots
  data, status_code, headers = api_instance.list_all_agent_bots_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<AgentBot>>
rescue Cfchat::ApiError => e
  puts "Error when calling AgentBotsApi->list_all_agent_bots_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;AgentBot&gt;**](AgentBot.md)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_an_agent_bot

> <AgentBot> update_an_agent_bot(id, data)

Update an agent bot

Update an agent bot's attributes

### Examples

```ruby
require 'time'
require 'cfchat'
# setup authorization
Cfchat.configure do |config|
  # Configure API key authorization: platformAppApiKey
  config.api_key['platformAppApiKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['platformAppApiKey'] = 'Bearer'
end

api_instance = Cfchat::AgentBotsApi.new
id = 56 # Integer | The ID of the agentbot to be updated
data = Cfchat::AgentBotCreateUpdatePayload.new # AgentBotCreateUpdatePayload | 

begin
  # Update an agent bot
  result = api_instance.update_an_agent_bot(id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AgentBotsApi->update_an_agent_bot: #{e}"
end
```

#### Using the update_an_agent_bot_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AgentBot>, Integer, Hash)> update_an_agent_bot_with_http_info(id, data)

```ruby
begin
  # Update an agent bot
  data, status_code, headers = api_instance.update_an_agent_bot_with_http_info(id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AgentBot>
rescue Cfchat::ApiError => e
  puts "Error when calling AgentBotsApi->update_an_agent_bot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The ID of the agentbot to be updated |  |
| **data** | [**AgentBotCreateUpdatePayload**](AgentBotCreateUpdatePayload.md) |  |  |

### Return type

[**AgentBot**](AgentBot.md)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

