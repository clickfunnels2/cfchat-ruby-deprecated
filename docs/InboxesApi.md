# Cfchat::InboxesApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_new_agent_to_inbox**](InboxesApi.md#add_new_agent_to_inbox) | **POST** /api/v1/accounts/{account_id}/inbox_members | Add a New Agent |
| [**delete_agent_in_inbox**](InboxesApi.md#delete_agent_in_inbox) | **DELETE** /api/v1/accounts/{account_id}/inbox_members | Remove an Agent from Inbox |
| [**get_inbox**](InboxesApi.md#get_inbox) | **GET** /api/v1/accounts/{account_id}/inboxes/{id}/ | Get an inbox |
| [**get_inbox_agent_bot**](InboxesApi.md#get_inbox_agent_bot) | **GET** /api/v1/accounts/{account_id}/inboxes/{id}/agent_bot | Show Inbox Agent Bot |
| [**get_inbox_members**](InboxesApi.md#get_inbox_members) | **GET** /api/v1/accounts/{account_id}/inbox_members/{inbox_id} | List Agents in Inbox |
| [**inbox_creation**](InboxesApi.md#inbox_creation) | **POST** /api/v1/accounts/{account_id}/inboxes/ | Create an inbox |
| [**list_all_inboxes**](InboxesApi.md#list_all_inboxes) | **GET** /api/v1/accounts/{account_id}/inboxes | List all inboxes |
| [**update_agent_bot**](InboxesApi.md#update_agent_bot) | **POST** /api/v1/accounts/{account_id}/inboxes/{id}/set_agent_bot | Add or remove agent bot |
| [**update_agents_in_inbox**](InboxesApi.md#update_agents_in_inbox) | **PATCH** /api/v1/accounts/{account_id}/inbox_members | Update Agents in Inbox |
| [**update_inbox**](InboxesApi.md#update_inbox) | **PATCH** /api/v1/accounts/{account_id}/inboxes/{id} | Update Inbox |


## add_new_agent_to_inbox

> <Array<Agent>> add_new_agent_to_inbox(account_id, data)

Add a New Agent

Add a new Agent to Inbox

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

api_instance = Cfchat::InboxesApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::AddNewAgentToInboxRequest.new({inbox_id: 'inbox_id_example', user_ids: [37]}) # AddNewAgentToInboxRequest | 

begin
  # Add a New Agent
  result = api_instance.add_new_agent_to_inbox(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->add_new_agent_to_inbox: #{e}"
end
```

#### Using the add_new_agent_to_inbox_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Agent>>, Integer, Hash)> add_new_agent_to_inbox_with_http_info(account_id, data)

```ruby
begin
  # Add a New Agent
  data, status_code, headers = api_instance.add_new_agent_to_inbox_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Agent>>
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->add_new_agent_to_inbox_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**AddNewAgentToInboxRequest**](AddNewAgentToInboxRequest.md) |  |  |

### Return type

[**Array&lt;Agent&gt;**](Agent.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_agent_in_inbox

> delete_agent_in_inbox(account_id, data)

Remove an Agent from Inbox

Remove an Agent from Inbox

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

api_instance = Cfchat::InboxesApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::DeleteAgentInInboxRequest.new({inbox_id: 'inbox_id_example', user_ids: [37]}) # DeleteAgentInInboxRequest | 

begin
  # Remove an Agent from Inbox
  api_instance.delete_agent_in_inbox(account_id, data)
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->delete_agent_in_inbox: #{e}"
end
```

#### Using the delete_agent_in_inbox_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_agent_in_inbox_with_http_info(account_id, data)

```ruby
begin
  # Remove an Agent from Inbox
  data, status_code, headers = api_instance.delete_agent_in_inbox_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->delete_agent_in_inbox_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**DeleteAgentInInboxRequest**](DeleteAgentInInboxRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: Not defined


## get_inbox

> <Inbox> get_inbox(account_id, id)

Get an inbox

Get an inbox available in the current account

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

api_instance = Cfchat::InboxesApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 8.14 # Float | ID of the inbox

begin
  # Get an inbox
  result = api_instance.get_inbox(account_id, id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->get_inbox: #{e}"
end
```

#### Using the get_inbox_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Inbox>, Integer, Hash)> get_inbox_with_http_info(account_id, id)

```ruby
begin
  # Get an inbox
  data, status_code, headers = api_instance.get_inbox_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Inbox>
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->get_inbox_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Float** | ID of the inbox |  |

### Return type

[**Inbox**](Inbox.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## get_inbox_agent_bot

> <AgentBot> get_inbox_agent_bot(account_id, id)

Show Inbox Agent Bot

See if an agent bot is associated to the Inbox

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

api_instance = Cfchat::InboxesApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 8.14 # Float | ID of the inbox

begin
  # Show Inbox Agent Bot
  result = api_instance.get_inbox_agent_bot(account_id, id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->get_inbox_agent_bot: #{e}"
end
```

#### Using the get_inbox_agent_bot_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AgentBot>, Integer, Hash)> get_inbox_agent_bot_with_http_info(account_id, id)

```ruby
begin
  # Show Inbox Agent Bot
  data, status_code, headers = api_instance.get_inbox_agent_bot_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AgentBot>
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->get_inbox_agent_bot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Float** | ID of the inbox |  |

### Return type

[**AgentBot**](AgentBot.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## get_inbox_members

> <Array<Agent>> get_inbox_members(account_id, inbox_id)

List Agents in Inbox

Get Details of Agents in an Inbox

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

api_instance = Cfchat::InboxesApi.new
account_id = 56 # Integer | The numeric ID of the account
inbox_id = 56 # Integer | The ID of the Inbox

begin
  # List Agents in Inbox
  result = api_instance.get_inbox_members(account_id, inbox_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->get_inbox_members: #{e}"
end
```

#### Using the get_inbox_members_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Agent>>, Integer, Hash)> get_inbox_members_with_http_info(account_id, inbox_id)

```ruby
begin
  # List Agents in Inbox
  data, status_code, headers = api_instance.get_inbox_members_with_http_info(account_id, inbox_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Agent>>
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->get_inbox_members_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **inbox_id** | **Integer** | The ID of the Inbox |  |

### Return type

[**Array&lt;Agent&gt;**](Agent.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## inbox_creation

> <Inbox> inbox_creation(account_id, data)

Create an inbox

You can create more than one website inbox in each account

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

api_instance = Cfchat::InboxesApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::InboxCreationRequest.new # InboxCreationRequest | 

begin
  # Create an inbox
  result = api_instance.inbox_creation(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->inbox_creation: #{e}"
end
```

#### Using the inbox_creation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Inbox>, Integer, Hash)> inbox_creation_with_http_info(account_id, data)

```ruby
begin
  # Create an inbox
  data, status_code, headers = api_instance.inbox_creation_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Inbox>
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->inbox_creation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**InboxCreationRequest**](InboxCreationRequest.md) |  |  |

### Return type

[**Inbox**](Inbox.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## list_all_inboxes

> <Array<Inbox>> list_all_inboxes(account_id)

List all inboxes

List all inboxes available in the current account

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

api_instance = Cfchat::InboxesApi.new
account_id = 56 # Integer | The numeric ID of the account

begin
  # List all inboxes
  result = api_instance.list_all_inboxes(account_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->list_all_inboxes: #{e}"
end
```

#### Using the list_all_inboxes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Inbox>>, Integer, Hash)> list_all_inboxes_with_http_info(account_id)

```ruby
begin
  # List all inboxes
  data, status_code, headers = api_instance.list_all_inboxes_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Inbox>>
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->list_all_inboxes_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |

### Return type

[**Array&lt;Inbox&gt;**](Inbox.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_agent_bot

> update_agent_bot(account_id, id, data)

Add or remove agent bot

To add an agent bot pass agent_bot id, to remove agent bot from an inbox pass null

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

api_instance = Cfchat::InboxesApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 8.14 # Float | ID of the inbox
data = Cfchat::UpdateAgentBotRequest.new({agent_bot: 3.56}) # UpdateAgentBotRequest | 

begin
  # Add or remove agent bot
  api_instance.update_agent_bot(account_id, id, data)
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->update_agent_bot: #{e}"
end
```

#### Using the update_agent_bot_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> update_agent_bot_with_http_info(account_id, id, data)

```ruby
begin
  # Add or remove agent bot
  data, status_code, headers = api_instance.update_agent_bot_with_http_info(account_id, id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->update_agent_bot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Float** | ID of the inbox |  |
| **data** | [**UpdateAgentBotRequest**](UpdateAgentBotRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: Not defined


## update_agents_in_inbox

> <Array<Agent>> update_agents_in_inbox(account_id, data)

Update Agents in Inbox

All agents except the one passed in params will be removed

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

api_instance = Cfchat::InboxesApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::AddNewAgentToInboxRequest.new({inbox_id: 'inbox_id_example', user_ids: [37]}) # AddNewAgentToInboxRequest | 

begin
  # Update Agents in Inbox
  result = api_instance.update_agents_in_inbox(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->update_agents_in_inbox: #{e}"
end
```

#### Using the update_agents_in_inbox_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Agent>>, Integer, Hash)> update_agents_in_inbox_with_http_info(account_id, data)

```ruby
begin
  # Update Agents in Inbox
  data, status_code, headers = api_instance.update_agents_in_inbox_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Agent>>
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->update_agents_in_inbox_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**AddNewAgentToInboxRequest**](AddNewAgentToInboxRequest.md) |  |  |

### Return type

[**Array&lt;Agent&gt;**](Agent.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## update_inbox

> <Inbox> update_inbox(account_id, id, data)

Update Inbox

Add avatar and disable auto assignment for an inbox

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

api_instance = Cfchat::InboxesApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 8.14 # Float | ID of the inbox
data = Cfchat::UpdateInboxRequest.new({enable_auto_assignment: false}) # UpdateInboxRequest | 

begin
  # Update Inbox
  result = api_instance.update_inbox(account_id, id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->update_inbox: #{e}"
end
```

#### Using the update_inbox_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Inbox>, Integer, Hash)> update_inbox_with_http_info(account_id, id, data)

```ruby
begin
  # Update Inbox
  data, status_code, headers = api_instance.update_inbox_with_http_info(account_id, id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Inbox>
rescue Cfchat::ApiError => e
  puts "Error when calling InboxesApi->update_inbox_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Float** | ID of the inbox |  |
| **data** | [**UpdateInboxRequest**](UpdateInboxRequest.md) |  |  |

### Return type

[**Inbox**](Inbox.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

