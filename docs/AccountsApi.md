# Cfchat::AccountsApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_an_account**](AccountsApi.md#create_an_account) | **POST** /platform/api/v1/accounts | Create an Account |
| [**delete_an_account**](AccountsApi.md#delete_an_account) | **DELETE** /platform/api/v1/accounts/{account_id} | Delete an Account |
| [**get_details_of_an_account**](AccountsApi.md#get_details_of_an_account) | **GET** /platform/api/v1/accounts/{account_id} | Get an account details |
| [**update_an_account**](AccountsApi.md#update_an_account) | **PATCH** /platform/api/v1/accounts/{account_id} | Update an account |


## create_an_account

> <PlatformAccount> create_an_account(data)

Create an Account

Create an Account

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

api_instance = Cfchat::AccountsApi.new
data = Cfchat::AccountCreateUpdatePayload.new # AccountCreateUpdatePayload | 

begin
  # Create an Account
  result = api_instance.create_an_account(data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AccountsApi->create_an_account: #{e}"
end
```

#### Using the create_an_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PlatformAccount>, Integer, Hash)> create_an_account_with_http_info(data)

```ruby
begin
  # Create an Account
  data, status_code, headers = api_instance.create_an_account_with_http_info(data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PlatformAccount>
rescue Cfchat::ApiError => e
  puts "Error when calling AccountsApi->create_an_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**AccountCreateUpdatePayload**](AccountCreateUpdatePayload.md) |  |  |

### Return type

[**PlatformAccount**](PlatformAccount.md)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_an_account

> delete_an_account(account_id)

Delete an Account

Delete an Account

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

api_instance = Cfchat::AccountsApi.new
account_id = 56 # Integer | The numeric ID of the account

begin
  # Delete an Account
  api_instance.delete_an_account(account_id)
rescue Cfchat::ApiError => e
  puts "Error when calling AccountsApi->delete_an_account: #{e}"
end
```

#### Using the delete_an_account_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_an_account_with_http_info(account_id)

```ruby
begin
  # Delete an Account
  data, status_code, headers = api_instance.delete_an_account_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling AccountsApi->delete_an_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |

### Return type

nil (empty response body)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_details_of_an_account

> <PlatformAccount> get_details_of_an_account(account_id)

Get an account details

Get the details of an account

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

api_instance = Cfchat::AccountsApi.new
account_id = 56 # Integer | The numeric ID of the account

begin
  # Get an account details
  result = api_instance.get_details_of_an_account(account_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AccountsApi->get_details_of_an_account: #{e}"
end
```

#### Using the get_details_of_an_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PlatformAccount>, Integer, Hash)> get_details_of_an_account_with_http_info(account_id)

```ruby
begin
  # Get an account details
  data, status_code, headers = api_instance.get_details_of_an_account_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PlatformAccount>
rescue Cfchat::ApiError => e
  puts "Error when calling AccountsApi->get_details_of_an_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |

### Return type

[**PlatformAccount**](PlatformAccount.md)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_an_account

> <PlatformAccount> update_an_account(account_id, data)

Update an account

Update an account's attributes

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

api_instance = Cfchat::AccountsApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::AccountCreateUpdatePayload.new # AccountCreateUpdatePayload | 

begin
  # Update an account
  result = api_instance.update_an_account(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AccountsApi->update_an_account: #{e}"
end
```

#### Using the update_an_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PlatformAccount>, Integer, Hash)> update_an_account_with_http_info(account_id, data)

```ruby
begin
  # Update an account
  data, status_code, headers = api_instance.update_an_account_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PlatformAccount>
rescue Cfchat::ApiError => e
  puts "Error when calling AccountsApi->update_an_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**AccountCreateUpdatePayload**](AccountCreateUpdatePayload.md) |  |  |

### Return type

[**PlatformAccount**](PlatformAccount.md)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

