# Cfchat::CustomAttributesApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_new_custom_attribute_to_account**](CustomAttributesApi.md#add_new_custom_attribute_to_account) | **POST** /api/v1/accounts/{account_id}/custom_attribute_definitions | Add a new custom attribute |
| [**delete_custom_attribute_from_account**](CustomAttributesApi.md#delete_custom_attribute_from_account) | **DELETE** /api/v1/accounts/{account_id}/custom_attribute_definitions/{id} | Remove a custom attribute from account |
| [**get_account_custom_attribute**](CustomAttributesApi.md#get_account_custom_attribute) | **GET** /api/v1/accounts/{account_id}/custom_attribute_definitions | List all custom attributes in an account |
| [**get_details_of_a_single_custom_attribute**](CustomAttributesApi.md#get_details_of_a_single_custom_attribute) | **GET** /api/v1/accounts/{account_id}/custom_attribute_definitions/{id} | Get a custom attribute details |
| [**update_custom_attribute_in_account**](CustomAttributesApi.md#update_custom_attribute_in_account) | **PATCH** /api/v1/accounts/{account_id}/custom_attribute_definitions/{id} | Update custom attribute in Account |


## add_new_custom_attribute_to_account

> <CustomAttribute> add_new_custom_attribute_to_account(account_id, data)

Add a new custom attribute

Add a new custom attribute to account

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

api_instance = Cfchat::CustomAttributesApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::CustomAttributeCreateUpdatePayload.new # CustomAttributeCreateUpdatePayload | 

begin
  # Add a new custom attribute
  result = api_instance.add_new_custom_attribute_to_account(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling CustomAttributesApi->add_new_custom_attribute_to_account: #{e}"
end
```

#### Using the add_new_custom_attribute_to_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomAttribute>, Integer, Hash)> add_new_custom_attribute_to_account_with_http_info(account_id, data)

```ruby
begin
  # Add a new custom attribute
  data, status_code, headers = api_instance.add_new_custom_attribute_to_account_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomAttribute>
rescue Cfchat::ApiError => e
  puts "Error when calling CustomAttributesApi->add_new_custom_attribute_to_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**CustomAttributeCreateUpdatePayload**](CustomAttributeCreateUpdatePayload.md) |  |  |

### Return type

[**CustomAttribute**](CustomAttribute.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_custom_attribute_from_account

> delete_custom_attribute_from_account(account_id, id)

Remove a custom attribute from account

Remove a custom attribute from account

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

api_instance = Cfchat::CustomAttributesApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 56 # Integer | The ID of the custom attribute to be deleted

begin
  # Remove a custom attribute from account
  api_instance.delete_custom_attribute_from_account(account_id, id)
rescue Cfchat::ApiError => e
  puts "Error when calling CustomAttributesApi->delete_custom_attribute_from_account: #{e}"
end
```

#### Using the delete_custom_attribute_from_account_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_custom_attribute_from_account_with_http_info(account_id, id)

```ruby
begin
  # Remove a custom attribute from account
  data, status_code, headers = api_instance.delete_custom_attribute_from_account_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling CustomAttributesApi->delete_custom_attribute_from_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Integer** | The ID of the custom attribute to be deleted |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_account_custom_attribute

> <Array<CustomAttribute>> get_account_custom_attribute(account_id, attribute_model)

List all custom attributes in an account

Get details of custom attributes in an Account

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

api_instance = Cfchat::CustomAttributesApi.new
account_id = 56 # Integer | The numeric ID of the account
attribute_model = '0' # String | conversation_attribute(0)/contact_attribute(1)

begin
  # List all custom attributes in an account
  result = api_instance.get_account_custom_attribute(account_id, attribute_model)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling CustomAttributesApi->get_account_custom_attribute: #{e}"
end
```

#### Using the get_account_custom_attribute_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<CustomAttribute>>, Integer, Hash)> get_account_custom_attribute_with_http_info(account_id, attribute_model)

```ruby
begin
  # List all custom attributes in an account
  data, status_code, headers = api_instance.get_account_custom_attribute_with_http_info(account_id, attribute_model)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<CustomAttribute>>
rescue Cfchat::ApiError => e
  puts "Error when calling CustomAttributesApi->get_account_custom_attribute_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **attribute_model** | **String** | conversation_attribute(0)/contact_attribute(1) |  |

### Return type

[**Array&lt;CustomAttribute&gt;**](CustomAttribute.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## get_details_of_a_single_custom_attribute

> <CustomAttribute> get_details_of_a_single_custom_attribute(account_id, id)

Get a custom attribute details

Get the details of a custom attribute in the account

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

api_instance = Cfchat::CustomAttributesApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 56 # Integer | The ID of the custom attribute to be updated.

begin
  # Get a custom attribute details
  result = api_instance.get_details_of_a_single_custom_attribute(account_id, id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling CustomAttributesApi->get_details_of_a_single_custom_attribute: #{e}"
end
```

#### Using the get_details_of_a_single_custom_attribute_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomAttribute>, Integer, Hash)> get_details_of_a_single_custom_attribute_with_http_info(account_id, id)

```ruby
begin
  # Get a custom attribute details
  data, status_code, headers = api_instance.get_details_of_a_single_custom_attribute_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomAttribute>
rescue Cfchat::ApiError => e
  puts "Error when calling CustomAttributesApi->get_details_of_a_single_custom_attribute_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Integer** | The ID of the custom attribute to be updated. |  |

### Return type

[**CustomAttribute**](CustomAttribute.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_custom_attribute_in_account

> <CustomAttribute> update_custom_attribute_in_account(account_id, id, data)

Update custom attribute in Account

Update a custom attribute in account

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

api_instance = Cfchat::CustomAttributesApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 56 # Integer | The ID of the custom attribute to be updated.
data = Cfchat::CustomAttributeCreateUpdatePayload.new # CustomAttributeCreateUpdatePayload | 

begin
  # Update custom attribute in Account
  result = api_instance.update_custom_attribute_in_account(account_id, id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling CustomAttributesApi->update_custom_attribute_in_account: #{e}"
end
```

#### Using the update_custom_attribute_in_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomAttribute>, Integer, Hash)> update_custom_attribute_in_account_with_http_info(account_id, id, data)

```ruby
begin
  # Update custom attribute in Account
  data, status_code, headers = api_instance.update_custom_attribute_in_account_with_http_info(account_id, id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomAttribute>
rescue Cfchat::ApiError => e
  puts "Error when calling CustomAttributesApi->update_custom_attribute_in_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Integer** | The ID of the custom attribute to be updated. |  |
| **data** | [**CustomAttributeCreateUpdatePayload**](CustomAttributeCreateUpdatePayload.md) |  |  |

### Return type

[**CustomAttribute**](CustomAttribute.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

