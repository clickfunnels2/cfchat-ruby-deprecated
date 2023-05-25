# Cfchat::CannedResponsesApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_new_canned_response_to_account**](CannedResponsesApi.md#add_new_canned_response_to_account) | **POST** /api/v1/accounts/{account_id}/canned_responses | Add a New Canned Response |
| [**delete_canned_response_from_account**](CannedResponsesApi.md#delete_canned_response_from_account) | **DELETE** /api/v1/accounts/{account_id}/canned_responses/{id} | Remove a Canned Response from Account |
| [**get_account_canned_response**](CannedResponsesApi.md#get_account_canned_response) | **GET** /api/v1/accounts/{account_id}/canned_responses | List all Canned Responses in an Account |


## add_new_canned_response_to_account

> <CannedResponse> add_new_canned_response_to_account(account_id, data)

Add a New Canned Response

Add a new Canned Response to Account

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

api_instance = Cfchat::CannedResponsesApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::CannedResponseCreateUpdatePayload.new # CannedResponseCreateUpdatePayload | 

begin
  # Add a New Canned Response
  result = api_instance.add_new_canned_response_to_account(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling CannedResponsesApi->add_new_canned_response_to_account: #{e}"
end
```

#### Using the add_new_canned_response_to_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CannedResponse>, Integer, Hash)> add_new_canned_response_to_account_with_http_info(account_id, data)

```ruby
begin
  # Add a New Canned Response
  data, status_code, headers = api_instance.add_new_canned_response_to_account_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CannedResponse>
rescue Cfchat::ApiError => e
  puts "Error when calling CannedResponsesApi->add_new_canned_response_to_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**CannedResponseCreateUpdatePayload**](CannedResponseCreateUpdatePayload.md) |  |  |

### Return type

[**CannedResponse**](CannedResponse.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_canned_response_from_account

> delete_canned_response_from_account(account_id, id)

Remove a Canned Response from Account

Remove a Canned Response from Account

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

api_instance = Cfchat::CannedResponsesApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 56 # Integer | The ID of the canned response to be deleted

begin
  # Remove a Canned Response from Account
  api_instance.delete_canned_response_from_account(account_id, id)
rescue Cfchat::ApiError => e
  puts "Error when calling CannedResponsesApi->delete_canned_response_from_account: #{e}"
end
```

#### Using the delete_canned_response_from_account_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_canned_response_from_account_with_http_info(account_id, id)

```ruby
begin
  # Remove a Canned Response from Account
  data, status_code, headers = api_instance.delete_canned_response_from_account_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling CannedResponsesApi->delete_canned_response_from_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Integer** | The ID of the canned response to be deleted |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_account_canned_response

> <Array<CannedResponse>> get_account_canned_response(account_id)

List all Canned Responses in an Account

Get Details of Canned Responses in an Account

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

api_instance = Cfchat::CannedResponsesApi.new
account_id = 56 # Integer | The numeric ID of the account

begin
  # List all Canned Responses in an Account
  result = api_instance.get_account_canned_response(account_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling CannedResponsesApi->get_account_canned_response: #{e}"
end
```

#### Using the get_account_canned_response_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<CannedResponse>>, Integer, Hash)> get_account_canned_response_with_http_info(account_id)

```ruby
begin
  # List all Canned Responses in an Account
  data, status_code, headers = api_instance.get_account_canned_response_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<CannedResponse>>
rescue Cfchat::ApiError => e
  puts "Error when calling CannedResponsesApi->get_account_canned_response_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |

### Return type

[**Array&lt;CannedResponse&gt;**](CannedResponse.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8

