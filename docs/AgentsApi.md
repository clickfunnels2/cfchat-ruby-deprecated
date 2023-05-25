# Cfchat::AgentsApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_new_agent_to_account**](AgentsApi.md#add_new_agent_to_account) | **POST** /api/v1/accounts/{account_id}/agents | Add a New Agent |
| [**delete_agent_from_account**](AgentsApi.md#delete_agent_from_account) | **DELETE** /api/v1/accounts/{account_id}/agents/{id} | Remove an Agent from Account |
| [**get_account_agents**](AgentsApi.md#get_account_agents) | **GET** /api/v1/accounts/{account_id}/agents | List Agents in Account |
| [**update_agent_in_account**](AgentsApi.md#update_agent_in_account) | **PATCH** /api/v1/accounts/{account_id}/agents/{id} | Update Agent in Account |


## add_new_agent_to_account

> <Agent> add_new_agent_to_account(account_id, data)

Add a New Agent

Add a new Agent to Account

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

api_instance = Cfchat::AgentsApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::AddNewAgentToAccountRequest.new({name: 'name_example', email: 'email_example', role: 'agent'}) # AddNewAgentToAccountRequest | 

begin
  # Add a New Agent
  result = api_instance.add_new_agent_to_account(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AgentsApi->add_new_agent_to_account: #{e}"
end
```

#### Using the add_new_agent_to_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Agent>, Integer, Hash)> add_new_agent_to_account_with_http_info(account_id, data)

```ruby
begin
  # Add a New Agent
  data, status_code, headers = api_instance.add_new_agent_to_account_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Agent>
rescue Cfchat::ApiError => e
  puts "Error when calling AgentsApi->add_new_agent_to_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**AddNewAgentToAccountRequest**](AddNewAgentToAccountRequest.md) |  |  |

### Return type

[**Agent**](Agent.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_agent_from_account

> delete_agent_from_account(account_id, id)

Remove an Agent from Account

Remove an Agent from Account

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

api_instance = Cfchat::AgentsApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 56 # Integer | The ID of the agent to be deleted

begin
  # Remove an Agent from Account
  api_instance.delete_agent_from_account(account_id, id)
rescue Cfchat::ApiError => e
  puts "Error when calling AgentsApi->delete_agent_from_account: #{e}"
end
```

#### Using the delete_agent_from_account_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_agent_from_account_with_http_info(account_id, id)

```ruby
begin
  # Remove an Agent from Account
  data, status_code, headers = api_instance.delete_agent_from_account_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling AgentsApi->delete_agent_from_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Integer** | The ID of the agent to be deleted |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_account_agents

> <Array<Agent>> get_account_agents(account_id)

List Agents in Account

Get Details of Agents in an Account

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

api_instance = Cfchat::AgentsApi.new
account_id = 56 # Integer | The numeric ID of the account

begin
  # List Agents in Account
  result = api_instance.get_account_agents(account_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AgentsApi->get_account_agents: #{e}"
end
```

#### Using the get_account_agents_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Agent>>, Integer, Hash)> get_account_agents_with_http_info(account_id)

```ruby
begin
  # List Agents in Account
  data, status_code, headers = api_instance.get_account_agents_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Agent>>
rescue Cfchat::ApiError => e
  puts "Error when calling AgentsApi->get_account_agents_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |

### Return type

[**Array&lt;Agent&gt;**](Agent.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_agent_in_account

> <Agent> update_agent_in_account(account_id, id, data)

Update Agent in Account

Update an Agent in Account

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

api_instance = Cfchat::AgentsApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 56 # Integer | The ID of the agent to be updated.
data = Cfchat::UpdateAgentInAccountRequest.new({role: 'agent'}) # UpdateAgentInAccountRequest | 

begin
  # Update Agent in Account
  result = api_instance.update_agent_in_account(account_id, id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AgentsApi->update_agent_in_account: #{e}"
end
```

#### Using the update_agent_in_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Agent>, Integer, Hash)> update_agent_in_account_with_http_info(account_id, id, data)

```ruby
begin
  # Update Agent in Account
  data, status_code, headers = api_instance.update_agent_in_account_with_http_info(account_id, id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Agent>
rescue Cfchat::ApiError => e
  puts "Error when calling AgentsApi->update_agent_in_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Integer** | The ID of the agent to be updated. |  |
| **data** | [**UpdateAgentInAccountRequest**](UpdateAgentInAccountRequest.md) |  |  |

### Return type

[**Agent**](Agent.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

