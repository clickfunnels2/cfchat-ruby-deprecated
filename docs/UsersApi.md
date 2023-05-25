# Cfchat::UsersApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_a_user**](UsersApi.md#create_a_user) | **POST** /platform/api/v1/users | Create a User |
| [**delete_a_user**](UsersApi.md#delete_a_user) | **DELETE** /platform/api/v1/users/{id} | Delete a User |
| [**get_details_of_a_user**](UsersApi.md#get_details_of_a_user) | **GET** /platform/api/v1/users/{id} | Get an user details |
| [**get_sso_url_of_a_user**](UsersApi.md#get_sso_url_of_a_user) | **GET** /platform/api/v1/users/{id}/login | Get User SSO Link |
| [**update_a_user**](UsersApi.md#update_a_user) | **PATCH** /platform/api/v1/users/{id} | Update a user |


## create_a_user

> <User> create_a_user(data)

Create a User

Create a User

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

api_instance = Cfchat::UsersApi.new
data = Cfchat::UserCreateUpdatePayload.new # UserCreateUpdatePayload | 

begin
  # Create a User
  result = api_instance.create_a_user(data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling UsersApi->create_a_user: #{e}"
end
```

#### Using the create_a_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<User>, Integer, Hash)> create_a_user_with_http_info(data)

```ruby
begin
  # Create a User
  data, status_code, headers = api_instance.create_a_user_with_http_info(data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <User>
rescue Cfchat::ApiError => e
  puts "Error when calling UsersApi->create_a_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**UserCreateUpdatePayload**](UserCreateUpdatePayload.md) |  |  |

### Return type

[**User**](User.md)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_a_user

> delete_a_user(id)

Delete a User

Delete a User

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

api_instance = Cfchat::UsersApi.new
id = 56 # Integer | The numeric ID of the user on the platform

begin
  # Delete a User
  api_instance.delete_a_user(id)
rescue Cfchat::ApiError => e
  puts "Error when calling UsersApi->delete_a_user: #{e}"
end
```

#### Using the delete_a_user_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_a_user_with_http_info(id)

```ruby
begin
  # Delete a User
  data, status_code, headers = api_instance.delete_a_user_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling UsersApi->delete_a_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The numeric ID of the user on the platform |  |

### Return type

nil (empty response body)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_details_of_a_user

> <User> get_details_of_a_user(id)

Get an user details

Get the details of an user

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

api_instance = Cfchat::UsersApi.new
id = 56 # Integer | The numeric ID of the user on the platform

begin
  # Get an user details
  result = api_instance.get_details_of_a_user(id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling UsersApi->get_details_of_a_user: #{e}"
end
```

#### Using the get_details_of_a_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<User>, Integer, Hash)> get_details_of_a_user_with_http_info(id)

```ruby
begin
  # Get an user details
  data, status_code, headers = api_instance.get_details_of_a_user_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <User>
rescue Cfchat::ApiError => e
  puts "Error when calling UsersApi->get_details_of_a_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The numeric ID of the user on the platform |  |

### Return type

[**User**](User.md)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## get_sso_url_of_a_user

> <GetSsoUrlOfAUser200Response> get_sso_url_of_a_user(id)

Get User SSO Link

Get the sso link of a user

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

api_instance = Cfchat::UsersApi.new
id = 56 # Integer | The numeric ID of the user on the platform

begin
  # Get User SSO Link
  result = api_instance.get_sso_url_of_a_user(id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling UsersApi->get_sso_url_of_a_user: #{e}"
end
```

#### Using the get_sso_url_of_a_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetSsoUrlOfAUser200Response>, Integer, Hash)> get_sso_url_of_a_user_with_http_info(id)

```ruby
begin
  # Get User SSO Link
  data, status_code, headers = api_instance.get_sso_url_of_a_user_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetSsoUrlOfAUser200Response>
rescue Cfchat::ApiError => e
  puts "Error when calling UsersApi->get_sso_url_of_a_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The numeric ID of the user on the platform |  |

### Return type

[**GetSsoUrlOfAUser200Response**](GetSsoUrlOfAUser200Response.md)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_a_user

> <User> update_a_user(id, data)

Update a user

Update a user's attributes

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

api_instance = Cfchat::UsersApi.new
id = 56 # Integer | The numeric ID of the user on the platform
data = Cfchat::UserCreateUpdatePayload.new # UserCreateUpdatePayload | 

begin
  # Update a user
  result = api_instance.update_a_user(id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling UsersApi->update_a_user: #{e}"
end
```

#### Using the update_a_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<User>, Integer, Hash)> update_a_user_with_http_info(id, data)

```ruby
begin
  # Update a user
  data, status_code, headers = api_instance.update_a_user_with_http_info(id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <User>
rescue Cfchat::ApiError => e
  puts "Error when calling UsersApi->update_a_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The numeric ID of the user on the platform |  |
| **data** | [**UserCreateUpdatePayload**](UserCreateUpdatePayload.md) |  |  |

### Return type

[**User**](User.md)

### Authorization

[platformAppApiKey](../README.md#platformAppApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

