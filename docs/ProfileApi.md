# Cfchat::ProfileApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**fetch_profile**](ProfileApi.md#fetch_profile) | **GET** /api/v1/profile | Fetch user profile |


## fetch_profile

> <User> fetch_profile

Fetch user profile

Get the user profile details

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

api_instance = Cfchat::ProfileApi.new

begin
  # Fetch user profile
  result = api_instance.fetch_profile
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ProfileApi->fetch_profile: #{e}"
end
```

#### Using the fetch_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<User>, Integer, Hash)> fetch_profile_with_http_info

```ruby
begin
  # Fetch user profile
  data, status_code, headers = api_instance.fetch_profile_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <User>
rescue Cfchat::ApiError => e
  puts "Error when calling ProfileApi->fetch_profile_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**User**](User.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8

