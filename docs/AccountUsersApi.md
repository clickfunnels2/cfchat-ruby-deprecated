# Cfchat::AccountUsersApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_an_account_user**](AccountUsersApi.md#create_an_account_user) | **POST** /platform/api/v1/accounts/{account_id}/account_users | Create an Account User |
| [**delete_an_account_user**](AccountUsersApi.md#delete_an_account_user) | **DELETE** /platform/api/v1/accounts/{account_id}/account_users | Delete an Account User |
| [**list_all_account_users**](AccountUsersApi.md#list_all_account_users) | **GET** /platform/api/v1/accounts/{account_id}/account_users | List all Account Users |


## create_an_account_user

> Object create_an_account_user(account_id, data)

Create an Account User

Create an Account User

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

api_instance = Cfchat::AccountUsersApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::CreateAnAccountUserRequest.new({user_id: 37, role: 'role_example'}) # CreateAnAccountUserRequest | 

begin
  # Create an Account User
  result = api_instance.create_an_account_user(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AccountUsersApi->create_an_account_user: #{e}"
end
```

#### Using the create_an_account_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> create_an_account_user_with_http_info(account_id, data)

```ruby
begin
  # Create an Account User
  data, status_code, headers = api_instance.create_an_account_user_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue Cfchat::ApiError => e
  puts "Error when calling AccountUsersApi->create_an_account_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**CreateAnAccountUserRequest**](CreateAnAccountUserRequest.md) |  |  |

### Return type

**Object**

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_an_account_user

> delete_an_account_user(account_id, data)

Delete an Account User

Delete an Account User

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

api_instance = Cfchat::AccountUsersApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::DeleteAnAccountUserRequest.new({user_id: 37}) # DeleteAnAccountUserRequest | 

begin
  # Delete an Account User
  api_instance.delete_an_account_user(account_id, data)
rescue Cfchat::ApiError => e
  puts "Error when calling AccountUsersApi->delete_an_account_user: #{e}"
end
```

#### Using the delete_an_account_user_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_an_account_user_with_http_info(account_id, data)

```ruby
begin
  # Delete an Account User
  data, status_code, headers = api_instance.delete_an_account_user_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling AccountUsersApi->delete_an_account_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**DeleteAnAccountUserRequest**](DeleteAnAccountUserRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: Not defined


## list_all_account_users

> <Array<ListAllAccountUsers200ResponseInner>> list_all_account_users(account_id)

List all Account Users

List all account users

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

api_instance = Cfchat::AccountUsersApi.new
account_id = 56 # Integer | The numeric ID of the account

begin
  # List all Account Users
  result = api_instance.list_all_account_users(account_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AccountUsersApi->list_all_account_users: #{e}"
end
```

#### Using the list_all_account_users_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ListAllAccountUsers200ResponseInner>>, Integer, Hash)> list_all_account_users_with_http_info(account_id)

```ruby
begin
  # List all Account Users
  data, status_code, headers = api_instance.list_all_account_users_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ListAllAccountUsers200ResponseInner>>
rescue Cfchat::ApiError => e
  puts "Error when calling AccountUsersApi->list_all_account_users_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |

### Return type

[**Array&lt;ListAllAccountUsers200ResponseInner&gt;**](ListAllAccountUsers200ResponseInner.md)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8

