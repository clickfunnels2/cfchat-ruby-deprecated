# Cfchat::IntegrationsApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_an_integration_hook**](IntegrationsApi.md#create_an_integration_hook) | **POST** /api/v1/accounts/{account_id}/integrations/hooks | Create an integration hook |
| [**delete_an_integration_hook**](IntegrationsApi.md#delete_an_integration_hook) | **DELETE** /api/v1/accounts/{account_id}/integrations/hooks/{hook_id} | Delete an Integration Hook |
| [**get_details_of_all_integrations**](IntegrationsApi.md#get_details_of_all_integrations) | **GET** /api/v1/accounts/{account_id}/integrations/apps | List all the Integrations |
| [**update_an_integrations_hook**](IntegrationsApi.md#update_an_integrations_hook) | **PATCH** /api/v1/accounts/{account_id}/integrations/hooks/{hook_id} | Update an Integration Hook |


## create_an_integration_hook

> <IntegrationsHook> create_an_integration_hook(account_id, data)

Create an integration hook

Create an integration hook

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

api_instance = Cfchat::IntegrationsApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::IntegrationsHookCreatePayload.new # IntegrationsHookCreatePayload | 

begin
  # Create an integration hook
  result = api_instance.create_an_integration_hook(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling IntegrationsApi->create_an_integration_hook: #{e}"
end
```

#### Using the create_an_integration_hook_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<IntegrationsHook>, Integer, Hash)> create_an_integration_hook_with_http_info(account_id, data)

```ruby
begin
  # Create an integration hook
  data, status_code, headers = api_instance.create_an_integration_hook_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <IntegrationsHook>
rescue Cfchat::ApiError => e
  puts "Error when calling IntegrationsApi->create_an_integration_hook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**IntegrationsHookCreatePayload**](IntegrationsHookCreatePayload.md) |  |  |

### Return type

[**IntegrationsHook**](IntegrationsHook.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_an_integration_hook

> delete_an_integration_hook(account_id, hook_id)

Delete an Integration Hook

Delete an Integration Hook

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

api_instance = Cfchat::IntegrationsApi.new
account_id = 56 # Integer | The numeric ID of the account
hook_id = 56 # Integer | The numeric ID of the integration hook

begin
  # Delete an Integration Hook
  api_instance.delete_an_integration_hook(account_id, hook_id)
rescue Cfchat::ApiError => e
  puts "Error when calling IntegrationsApi->delete_an_integration_hook: #{e}"
end
```

#### Using the delete_an_integration_hook_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_an_integration_hook_with_http_info(account_id, hook_id)

```ruby
begin
  # Delete an Integration Hook
  data, status_code, headers = api_instance.delete_an_integration_hook_with_http_info(account_id, hook_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling IntegrationsApi->delete_an_integration_hook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **hook_id** | **Integer** | The numeric ID of the integration hook |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_details_of_all_integrations

> <Array<IntegrationsApp>> get_details_of_all_integrations(account_id)

List all the Integrations

Get the details of all Integrations available for the account

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

api_instance = Cfchat::IntegrationsApi.new
account_id = 56 # Integer | The numeric ID of the account

begin
  # List all the Integrations
  result = api_instance.get_details_of_all_integrations(account_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling IntegrationsApi->get_details_of_all_integrations: #{e}"
end
```

#### Using the get_details_of_all_integrations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<IntegrationsApp>>, Integer, Hash)> get_details_of_all_integrations_with_http_info(account_id)

```ruby
begin
  # List all the Integrations
  data, status_code, headers = api_instance.get_details_of_all_integrations_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<IntegrationsApp>>
rescue Cfchat::ApiError => e
  puts "Error when calling IntegrationsApi->get_details_of_all_integrations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |

### Return type

[**Array&lt;IntegrationsApp&gt;**](IntegrationsApp.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_an_integrations_hook

> <IntegrationsHook> update_an_integrations_hook(account_id, hook_id, data)

Update an Integration Hook

Update an Integration Hook

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

api_instance = Cfchat::IntegrationsApi.new
account_id = 56 # Integer | The numeric ID of the account
hook_id = 56 # Integer | The numeric ID of the integration hook
data = Cfchat::IntegrationsHookUpdatePayload.new # IntegrationsHookUpdatePayload | 

begin
  # Update an Integration Hook
  result = api_instance.update_an_integrations_hook(account_id, hook_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling IntegrationsApi->update_an_integrations_hook: #{e}"
end
```

#### Using the update_an_integrations_hook_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<IntegrationsHook>, Integer, Hash)> update_an_integrations_hook_with_http_info(account_id, hook_id, data)

```ruby
begin
  # Update an Integration Hook
  data, status_code, headers = api_instance.update_an_integrations_hook_with_http_info(account_id, hook_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <IntegrationsHook>
rescue Cfchat::ApiError => e
  puts "Error when calling IntegrationsApi->update_an_integrations_hook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **hook_id** | **Integer** | The numeric ID of the integration hook |  |
| **data** | [**IntegrationsHookUpdatePayload**](IntegrationsHookUpdatePayload.md) |  |  |

### Return type

[**IntegrationsHook**](IntegrationsHook.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

