# Cfchat::CustomFiltersApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_a_custom_filter**](CustomFiltersApi.md#create_a_custom_filter) | **POST** /api/v1/accounts/{account_id}/custom_filters | Create a custom filter |
| [**delete_a_custom_filter**](CustomFiltersApi.md#delete_a_custom_filter) | **DELETE** /api/v1/accounts/{account_id}/custom_filters/{custom_filter_id} | Delete a custom filter |
| [**get_details_of_a_single_custom_filter**](CustomFiltersApi.md#get_details_of_a_single_custom_filter) | **GET** /api/v1/accounts/{account_id}/custom_filters/{custom_filter_id} | Get a custom filter details |
| [**list_all_filters**](CustomFiltersApi.md#list_all_filters) | **GET** /api/v1/accounts/{account_id}/custom_filters | List all custom filters |
| [**update_a_custom_filter**](CustomFiltersApi.md#update_a_custom_filter) | **PATCH** /api/v1/accounts/{account_id}/custom_filters/{custom_filter_id} | Update a custom filter |


## create_a_custom_filter

> <CustomFilter> create_a_custom_filter(account_id, data, opts)

Create a custom filter

Create a custom filter in the account

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

api_instance = Cfchat::CustomFiltersApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::CustomFilterCreateUpdatePayload.new # CustomFilterCreateUpdatePayload | 
opts = {
  filter_type: 'conversation' # String | The type of custom filter
}

begin
  # Create a custom filter
  result = api_instance.create_a_custom_filter(account_id, data, opts)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling CustomFiltersApi->create_a_custom_filter: #{e}"
end
```

#### Using the create_a_custom_filter_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomFilter>, Integer, Hash)> create_a_custom_filter_with_http_info(account_id, data, opts)

```ruby
begin
  # Create a custom filter
  data, status_code, headers = api_instance.create_a_custom_filter_with_http_info(account_id, data, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomFilter>
rescue Cfchat::ApiError => e
  puts "Error when calling CustomFiltersApi->create_a_custom_filter_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**CustomFilterCreateUpdatePayload**](CustomFilterCreateUpdatePayload.md) |  |  |
| **filter_type** | **String** | The type of custom filter | [optional] |

### Return type

[**CustomFilter**](CustomFilter.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_a_custom_filter

> delete_a_custom_filter(account_id, custom_filter_id)

Delete a custom filter

Delete a custom filter from the account

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

api_instance = Cfchat::CustomFiltersApi.new
account_id = 56 # Integer | The numeric ID of the account
custom_filter_id = 56 # Integer | The numeric ID of the custom filter

begin
  # Delete a custom filter
  api_instance.delete_a_custom_filter(account_id, custom_filter_id)
rescue Cfchat::ApiError => e
  puts "Error when calling CustomFiltersApi->delete_a_custom_filter: #{e}"
end
```

#### Using the delete_a_custom_filter_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_a_custom_filter_with_http_info(account_id, custom_filter_id)

```ruby
begin
  # Delete a custom filter
  data, status_code, headers = api_instance.delete_a_custom_filter_with_http_info(account_id, custom_filter_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling CustomFiltersApi->delete_a_custom_filter_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **custom_filter_id** | **Integer** | The numeric ID of the custom filter |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_details_of_a_single_custom_filter

> <CustomFilter> get_details_of_a_single_custom_filter(account_id, custom_filter_id)

Get a custom filter details

Get the details of a custom filter in the account

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

api_instance = Cfchat::CustomFiltersApi.new
account_id = 56 # Integer | The numeric ID of the account
custom_filter_id = 56 # Integer | The numeric ID of the custom filter

begin
  # Get a custom filter details
  result = api_instance.get_details_of_a_single_custom_filter(account_id, custom_filter_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling CustomFiltersApi->get_details_of_a_single_custom_filter: #{e}"
end
```

#### Using the get_details_of_a_single_custom_filter_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomFilter>, Integer, Hash)> get_details_of_a_single_custom_filter_with_http_info(account_id, custom_filter_id)

```ruby
begin
  # Get a custom filter details
  data, status_code, headers = api_instance.get_details_of_a_single_custom_filter_with_http_info(account_id, custom_filter_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomFilter>
rescue Cfchat::ApiError => e
  puts "Error when calling CustomFiltersApi->get_details_of_a_single_custom_filter_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **custom_filter_id** | **Integer** | The numeric ID of the custom filter |  |

### Return type

[**CustomFilter**](CustomFilter.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## list_all_filters

> <Array<CustomFilter>> list_all_filters(account_id, opts)

List all custom filters

List all custom filters in a category of a user

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

api_instance = Cfchat::CustomFiltersApi.new
account_id = 56 # Integer | The numeric ID of the account
opts = {
  filter_type: 'conversation' # String | The type of custom filter
}

begin
  # List all custom filters
  result = api_instance.list_all_filters(account_id, opts)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling CustomFiltersApi->list_all_filters: #{e}"
end
```

#### Using the list_all_filters_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<CustomFilter>>, Integer, Hash)> list_all_filters_with_http_info(account_id, opts)

```ruby
begin
  # List all custom filters
  data, status_code, headers = api_instance.list_all_filters_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<CustomFilter>>
rescue Cfchat::ApiError => e
  puts "Error when calling CustomFiltersApi->list_all_filters_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **filter_type** | **String** | The type of custom filter | [optional] |

### Return type

[**Array&lt;CustomFilter&gt;**](CustomFilter.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_a_custom_filter

> <CustomFilter> update_a_custom_filter(account_id, custom_filter_id, data)

Update a custom filter

Update a custom filter's attributes

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

api_instance = Cfchat::CustomFiltersApi.new
account_id = 56 # Integer | The numeric ID of the account
custom_filter_id = 56 # Integer | The numeric ID of the custom filter
data = Cfchat::CustomFilterCreateUpdatePayload.new # CustomFilterCreateUpdatePayload | 

begin
  # Update a custom filter
  result = api_instance.update_a_custom_filter(account_id, custom_filter_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling CustomFiltersApi->update_a_custom_filter: #{e}"
end
```

#### Using the update_a_custom_filter_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomFilter>, Integer, Hash)> update_a_custom_filter_with_http_info(account_id, custom_filter_id, data)

```ruby
begin
  # Update a custom filter
  data, status_code, headers = api_instance.update_a_custom_filter_with_http_info(account_id, custom_filter_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomFilter>
rescue Cfchat::ApiError => e
  puts "Error when calling CustomFiltersApi->update_a_custom_filter_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **custom_filter_id** | **Integer** | The numeric ID of the custom filter |  |
| **data** | [**CustomFilterCreateUpdatePayload**](CustomFilterCreateUpdatePayload.md) |  |  |

### Return type

[**CustomFilter**](CustomFilter.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

