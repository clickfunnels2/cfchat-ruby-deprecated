# Cfchat::ContactApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_inbox_creation**](ContactApi.md#contact_inbox_creation) | **POST** /api/v1/accounts/{account_id}/contacts/{id}/contact_inboxes | Create contact inbox |
| [**contactable_inboxes_get**](ContactApi.md#contactable_inboxes_get) | **GET** /api/v1/accounts/{account_id}/contacts/{id}/contactable_inboxes | Get Contactable Inboxes |


## contact_inbox_creation

> <ContactInboxes> contact_inbox_creation(account_id, id, data)

Create contact inbox

Create a contact inbox record for an inbox

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

api_instance = Cfchat::ContactApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 8.14 # Float | ID of the contact
data = Cfchat::ContactInboxCreationRequest.new({inbox_id: 3.56}) # ContactInboxCreationRequest | 

begin
  # Create contact inbox
  result = api_instance.contact_inbox_creation(account_id, id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ContactApi->contact_inbox_creation: #{e}"
end
```

#### Using the contact_inbox_creation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ContactInboxes>, Integer, Hash)> contact_inbox_creation_with_http_info(account_id, id, data)

```ruby
begin
  # Create contact inbox
  data, status_code, headers = api_instance.contact_inbox_creation_with_http_info(account_id, id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ContactInboxes>
rescue Cfchat::ApiError => e
  puts "Error when calling ContactApi->contact_inbox_creation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Float** | ID of the contact |  |
| **data** | [**ContactInboxCreationRequest**](ContactInboxCreationRequest.md) |  |  |

### Return type

[**ContactInboxes**](ContactInboxes.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## contactable_inboxes_get

> <ContactableInboxes> contactable_inboxes_get(account_id, id)

Get Contactable Inboxes

Get List of contactable Inboxes

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

api_instance = Cfchat::ContactApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 8.14 # Float | ID of the contact

begin
  # Get Contactable Inboxes
  result = api_instance.contactable_inboxes_get(account_id, id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ContactApi->contactable_inboxes_get: #{e}"
end
```

#### Using the contactable_inboxes_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ContactableInboxes>, Integer, Hash)> contactable_inboxes_get_with_http_info(account_id, id)

```ruby
begin
  # Get Contactable Inboxes
  data, status_code, headers = api_instance.contactable_inboxes_get_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ContactableInboxes>
rescue Cfchat::ApiError => e
  puts "Error when calling ContactApi->contactable_inboxes_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Float** | ID of the contact |  |

### Return type

[**ContactableInboxes**](ContactableInboxes.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8

