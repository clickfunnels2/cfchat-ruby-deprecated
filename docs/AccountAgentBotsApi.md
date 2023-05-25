# Cfchat::AccountAgentBotsApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_an_account_agent_bot**](AccountAgentBotsApi.md#create_an_account_agent_bot) | **POST** /api/v1/accounts/{account_id}/agent_bots | Create an Agent Bot |
| [**delete_an_account_agent_bot**](AccountAgentBotsApi.md#delete_an_account_agent_bot) | **DELETE** /api/v1/accounts/{account_id}/agent_bots/{id} | Delete an AgentBot |
| [**get_details_of_a_single_account_agent_bot**](AccountAgentBotsApi.md#get_details_of_a_single_account_agent_bot) | **GET** /api/v1/accounts/{account_id}/agent_bots/{id} | Get an agent bot details |
| [**list_all_account_agent_bots**](AccountAgentBotsApi.md#list_all_account_agent_bots) | **GET** /api/v1/accounts/{account_id}/agent_bots | List all AgentBots |
| [**update_an_account_agent_bot**](AccountAgentBotsApi.md#update_an_account_agent_bot) | **PATCH** /api/v1/accounts/{account_id}/agent_bots/{id} | Update an agent bot |


## create_an_account_agent_bot

> <AgentBot> create_an_account_agent_bot(account_id, data)

Create an Agent Bot

Create an agent bot in the account

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

api_instance = Cfchat::AccountAgentBotsApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::AgentBotCreateUpdatePayload.new # AgentBotCreateUpdatePayload | 

begin
  # Create an Agent Bot
  result = api_instance.create_an_account_agent_bot(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AccountAgentBotsApi->create_an_account_agent_bot: #{e}"
end
```

#### Using the create_an_account_agent_bot_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AgentBot>, Integer, Hash)> create_an_account_agent_bot_with_http_info(account_id, data)

```ruby
begin
  # Create an Agent Bot
  data, status_code, headers = api_instance.create_an_account_agent_bot_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AgentBot>
rescue Cfchat::ApiError => e
  puts "Error when calling AccountAgentBotsApi->create_an_account_agent_bot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**AgentBotCreateUpdatePayload**](AgentBotCreateUpdatePayload.md) |  |  |

### Return type

[**AgentBot**](AgentBot.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_an_account_agent_bot

> delete_an_account_agent_bot(account_id, id)

Delete an AgentBot

Delete an AgentBot from the account

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

api_instance = Cfchat::AccountAgentBotsApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 56 # Integer | The ID of the agentbot to be updated

begin
  # Delete an AgentBot
  api_instance.delete_an_account_agent_bot(account_id, id)
rescue Cfchat::ApiError => e
  puts "Error when calling AccountAgentBotsApi->delete_an_account_agent_bot: #{e}"
end
```

#### Using the delete_an_account_agent_bot_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_an_account_agent_bot_with_http_info(account_id, id)

```ruby
begin
  # Delete an AgentBot
  data, status_code, headers = api_instance.delete_an_account_agent_bot_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling AccountAgentBotsApi->delete_an_account_agent_bot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Integer** | The ID of the agentbot to be updated |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_details_of_a_single_account_agent_bot

> <AgentBot> get_details_of_a_single_account_agent_bot(account_id, id)

Get an agent bot details

Get the details of an agent bot in the account

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

api_instance = Cfchat::AccountAgentBotsApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 56 # Integer | The ID of the agentbot to be updated

begin
  # Get an agent bot details
  result = api_instance.get_details_of_a_single_account_agent_bot(account_id, id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AccountAgentBotsApi->get_details_of_a_single_account_agent_bot: #{e}"
end
```

#### Using the get_details_of_a_single_account_agent_bot_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AgentBot>, Integer, Hash)> get_details_of_a_single_account_agent_bot_with_http_info(account_id, id)

```ruby
begin
  # Get an agent bot details
  data, status_code, headers = api_instance.get_details_of_a_single_account_agent_bot_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AgentBot>
rescue Cfchat::ApiError => e
  puts "Error when calling AccountAgentBotsApi->get_details_of_a_single_account_agent_bot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Integer** | The ID of the agentbot to be updated |  |

### Return type

[**AgentBot**](AgentBot.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## list_all_account_agent_bots

> <Array<AgentBot>> list_all_account_agent_bots(account_id)

List all AgentBots

List all agent bots available for the current account

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

api_instance = Cfchat::AccountAgentBotsApi.new
account_id = 56 # Integer | The numeric ID of the account

begin
  # List all AgentBots
  result = api_instance.list_all_account_agent_bots(account_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AccountAgentBotsApi->list_all_account_agent_bots: #{e}"
end
```

#### Using the list_all_account_agent_bots_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<AgentBot>>, Integer, Hash)> list_all_account_agent_bots_with_http_info(account_id)

```ruby
begin
  # List all AgentBots
  data, status_code, headers = api_instance.list_all_account_agent_bots_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<AgentBot>>
rescue Cfchat::ApiError => e
  puts "Error when calling AccountAgentBotsApi->list_all_account_agent_bots_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |

### Return type

[**Array&lt;AgentBot&gt;**](AgentBot.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_an_account_agent_bot

> <AgentBot> update_an_account_agent_bot(account_id, id, data)

Update an agent bot

Update an agent bot's attributes

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

api_instance = Cfchat::AccountAgentBotsApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 56 # Integer | The ID of the agentbot to be updated
data = Cfchat::AgentBotCreateUpdatePayload.new # AgentBotCreateUpdatePayload | 

begin
  # Update an agent bot
  result = api_instance.update_an_account_agent_bot(account_id, id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AccountAgentBotsApi->update_an_account_agent_bot: #{e}"
end
```

#### Using the update_an_account_agent_bot_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AgentBot>, Integer, Hash)> update_an_account_agent_bot_with_http_info(account_id, id, data)

```ruby
begin
  # Update an agent bot
  data, status_code, headers = api_instance.update_an_account_agent_bot_with_http_info(account_id, id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AgentBot>
rescue Cfchat::ApiError => e
  puts "Error when calling AccountAgentBotsApi->update_an_account_agent_bot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Integer** | The ID of the agentbot to be updated |  |
| **data** | [**AgentBotCreateUpdatePayload**](AgentBotCreateUpdatePayload.md) |  |  |

### Return type

[**AgentBot**](AgentBot.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

