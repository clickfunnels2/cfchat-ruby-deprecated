# Cfchat::CannedResponseApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**update_canned_response_in_account**](CannedResponseApi.md#update_canned_response_in_account) | **PATCH** /api/v1/accounts/{account_id}/canned_responses/{id} | Update Canned Response in Account |


## update_canned_response_in_account

> <CannedResponse> update_canned_response_in_account(account_id, id, data)

Update Canned Response in Account

Update a Canned Response in Account

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

api_instance = Cfchat::CannedResponseApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 56 # Integer | The ID of the canned response to be updated.
data = Cfchat::CannedResponseCreateUpdatePayload.new # CannedResponseCreateUpdatePayload | 

begin
  # Update Canned Response in Account
  result = api_instance.update_canned_response_in_account(account_id, id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling CannedResponseApi->update_canned_response_in_account: #{e}"
end
```

#### Using the update_canned_response_in_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CannedResponse>, Integer, Hash)> update_canned_response_in_account_with_http_info(account_id, id, data)

```ruby
begin
  # Update Canned Response in Account
  data, status_code, headers = api_instance.update_canned_response_in_account_with_http_info(account_id, id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CannedResponse>
rescue Cfchat::ApiError => e
  puts "Error when calling CannedResponseApi->update_canned_response_in_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Integer** | The ID of the canned response to be updated. |  |
| **data** | [**CannedResponseCreateUpdatePayload**](CannedResponseCreateUpdatePayload.md) |  |  |

### Return type

[**CannedResponse**](CannedResponse.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

