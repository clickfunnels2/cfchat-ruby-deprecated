# Cfchat::TeamsApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_new_agent_to_team**](TeamsApi.md#add_new_agent_to_team) | **POST** /api/v1/accounts/{account_id}/teams/{team_id}/team_members | Add a New Agent |
| [**create_a_team**](TeamsApi.md#create_a_team) | **POST** /api/v1/accounts/{account_id}/teams | Create a team |
| [**delete_a_team**](TeamsApi.md#delete_a_team) | **DELETE** /api/v1/accounts/{account_id}/teams/{team_id} | Delete a team |
| [**delete_agent_in_team**](TeamsApi.md#delete_agent_in_team) | **DELETE** /api/v1/accounts/{account_id}/teams/{team_id}/team_members | Remove an Agent from Team |
| [**get_details_of_a_single_team**](TeamsApi.md#get_details_of_a_single_team) | **GET** /api/v1/accounts/{account_id}/teams/{team_id} | Get a team details |
| [**get_team_members**](TeamsApi.md#get_team_members) | **GET** /api/v1/accounts/{account_id}/teams/{team_id}/team_members | List Agents in Team |
| [**list_all_teams**](TeamsApi.md#list_all_teams) | **GET** /api/v1/accounts/{account_id}/teams | List all teams |
| [**update_a_team**](TeamsApi.md#update_a_team) | **PATCH** /api/v1/accounts/{account_id}/teams/{team_id} | Update a team |
| [**update_agents_in_team**](TeamsApi.md#update_agents_in_team) | **PATCH** /api/v1/accounts/{account_id}/teams/{team_id}/team_members | Update Agents in Team |


## add_new_agent_to_team

> <Array<Agent>> add_new_agent_to_team(account_id, team_id, data)

Add a New Agent

Add a new Agent to Team

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

api_instance = Cfchat::TeamsApi.new
account_id = 56 # Integer | The numeric ID of the account
team_id = 56 # Integer | The ID of the team to be updated
data = Cfchat::AddNewAgentToTeamRequest.new({user_ids: [37]}) # AddNewAgentToTeamRequest | 

begin
  # Add a New Agent
  result = api_instance.add_new_agent_to_team(account_id, team_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->add_new_agent_to_team: #{e}"
end
```

#### Using the add_new_agent_to_team_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Agent>>, Integer, Hash)> add_new_agent_to_team_with_http_info(account_id, team_id, data)

```ruby
begin
  # Add a New Agent
  data, status_code, headers = api_instance.add_new_agent_to_team_with_http_info(account_id, team_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Agent>>
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->add_new_agent_to_team_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **team_id** | **Integer** | The ID of the team to be updated |  |
| **data** | [**AddNewAgentToTeamRequest**](AddNewAgentToTeamRequest.md) |  |  |

### Return type

[**Array&lt;Agent&gt;**](Agent.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## create_a_team

> <Team> create_a_team(account_id, data)

Create a team

Create a team in the account

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

api_instance = Cfchat::TeamsApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::TeamCreateUpdatePayload.new # TeamCreateUpdatePayload | 

begin
  # Create a team
  result = api_instance.create_a_team(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->create_a_team: #{e}"
end
```

#### Using the create_a_team_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Team>, Integer, Hash)> create_a_team_with_http_info(account_id, data)

```ruby
begin
  # Create a team
  data, status_code, headers = api_instance.create_a_team_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Team>
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->create_a_team_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**TeamCreateUpdatePayload**](TeamCreateUpdatePayload.md) |  |  |

### Return type

[**Team**](Team.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_a_team

> delete_a_team(account_id, team_id)

Delete a team

Delete a team from the account

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

api_instance = Cfchat::TeamsApi.new
account_id = 56 # Integer | The numeric ID of the account
team_id = 56 # Integer | The ID of the team to be updated

begin
  # Delete a team
  api_instance.delete_a_team(account_id, team_id)
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->delete_a_team: #{e}"
end
```

#### Using the delete_a_team_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_a_team_with_http_info(account_id, team_id)

```ruby
begin
  # Delete a team
  data, status_code, headers = api_instance.delete_a_team_with_http_info(account_id, team_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->delete_a_team_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **team_id** | **Integer** | The ID of the team to be updated |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## delete_agent_in_team

> delete_agent_in_team(account_id, team_id, data)

Remove an Agent from Team

Remove an Agent from Team

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

api_instance = Cfchat::TeamsApi.new
account_id = 56 # Integer | The numeric ID of the account
team_id = 56 # Integer | The ID of the team to be updated
data = Cfchat::DeleteAgentInTeamRequest.new({user_ids: [37]}) # DeleteAgentInTeamRequest | 

begin
  # Remove an Agent from Team
  api_instance.delete_agent_in_team(account_id, team_id, data)
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->delete_agent_in_team: #{e}"
end
```

#### Using the delete_agent_in_team_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_agent_in_team_with_http_info(account_id, team_id, data)

```ruby
begin
  # Remove an Agent from Team
  data, status_code, headers = api_instance.delete_agent_in_team_with_http_info(account_id, team_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->delete_agent_in_team_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **team_id** | **Integer** | The ID of the team to be updated |  |
| **data** | [**DeleteAgentInTeamRequest**](DeleteAgentInTeamRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: Not defined


## get_details_of_a_single_team

> <Team> get_details_of_a_single_team(account_id, team_id)

Get a team details

Get the details of a team in the account

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

api_instance = Cfchat::TeamsApi.new
account_id = 56 # Integer | The numeric ID of the account
team_id = 56 # Integer | The ID of the team to be updated

begin
  # Get a team details
  result = api_instance.get_details_of_a_single_team(account_id, team_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->get_details_of_a_single_team: #{e}"
end
```

#### Using the get_details_of_a_single_team_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Team>, Integer, Hash)> get_details_of_a_single_team_with_http_info(account_id, team_id)

```ruby
begin
  # Get a team details
  data, status_code, headers = api_instance.get_details_of_a_single_team_with_http_info(account_id, team_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Team>
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->get_details_of_a_single_team_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **team_id** | **Integer** | The ID of the team to be updated |  |

### Return type

[**Team**](Team.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## get_team_members

> <Array<Agent>> get_team_members(account_id, team_id)

List Agents in Team

Get Details of Agents in an Team

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

api_instance = Cfchat::TeamsApi.new
account_id = 56 # Integer | The numeric ID of the account
team_id = 56 # Integer | The ID of the team to be updated

begin
  # List Agents in Team
  result = api_instance.get_team_members(account_id, team_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->get_team_members: #{e}"
end
```

#### Using the get_team_members_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Agent>>, Integer, Hash)> get_team_members_with_http_info(account_id, team_id)

```ruby
begin
  # List Agents in Team
  data, status_code, headers = api_instance.get_team_members_with_http_info(account_id, team_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Agent>>
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->get_team_members_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **team_id** | **Integer** | The ID of the team to be updated |  |

### Return type

[**Array&lt;Agent&gt;**](Agent.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## list_all_teams

> <Array<Team>> list_all_teams(account_id)

List all teams

List all teams available in the current account

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

api_instance = Cfchat::TeamsApi.new
account_id = 56 # Integer | The numeric ID of the account

begin
  # List all teams
  result = api_instance.list_all_teams(account_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->list_all_teams: #{e}"
end
```

#### Using the list_all_teams_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Team>>, Integer, Hash)> list_all_teams_with_http_info(account_id)

```ruby
begin
  # List all teams
  data, status_code, headers = api_instance.list_all_teams_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Team>>
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->list_all_teams_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |

### Return type

[**Array&lt;Team&gt;**](Team.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_a_team

> <Team> update_a_team(account_id, team_id, data)

Update a team

Update a team's attributes

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

api_instance = Cfchat::TeamsApi.new
account_id = 56 # Integer | The numeric ID of the account
team_id = 56 # Integer | The ID of the team to be updated
data = Cfchat::TeamCreateUpdatePayload.new # TeamCreateUpdatePayload | 

begin
  # Update a team
  result = api_instance.update_a_team(account_id, team_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->update_a_team: #{e}"
end
```

#### Using the update_a_team_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Team>, Integer, Hash)> update_a_team_with_http_info(account_id, team_id, data)

```ruby
begin
  # Update a team
  data, status_code, headers = api_instance.update_a_team_with_http_info(account_id, team_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Team>
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->update_a_team_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **team_id** | **Integer** | The ID of the team to be updated |  |
| **data** | [**TeamCreateUpdatePayload**](TeamCreateUpdatePayload.md) |  |  |

### Return type

[**Team**](Team.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## update_agents_in_team

> <Array<Agent>> update_agents_in_team(account_id, team_id, data)

Update Agents in Team

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

api_instance = Cfchat::TeamsApi.new
account_id = 56 # Integer | The numeric ID of the account
team_id = 56 # Integer | The ID of the team to be updated
data = Cfchat::AddNewAgentToTeamRequest.new({user_ids: [37]}) # AddNewAgentToTeamRequest | 

begin
  # Update Agents in Team
  result = api_instance.update_agents_in_team(account_id, team_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->update_agents_in_team: #{e}"
end
```

#### Using the update_agents_in_team_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Agent>>, Integer, Hash)> update_agents_in_team_with_http_info(account_id, team_id, data)

```ruby
begin
  # Update Agents in Team
  data, status_code, headers = api_instance.update_agents_in_team_with_http_info(account_id, team_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Agent>>
rescue Cfchat::ApiError => e
  puts "Error when calling TeamsApi->update_agents_in_team_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **team_id** | **Integer** | The ID of the team to be updated |  |
| **data** | [**AddNewAgentToTeamRequest**](AddNewAgentToTeamRequest.md) |  |  |

### Return type

[**Array&lt;Agent&gt;**](Agent.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

