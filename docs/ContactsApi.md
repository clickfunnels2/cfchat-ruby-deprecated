# Cfchat::ContactsApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_conversations**](ContactsApi.md#contact_conversations) | **GET** /api/v1/accounts/{account_id}/contacts/{id}/conversations | Contact Conversations |
| [**contact_create**](ContactsApi.md#contact_create) | **POST** /api/v1/accounts/{account_id}/contacts | Create Contact |
| [**contact_delete**](ContactsApi.md#contact_delete) | **DELETE** /api/v1/accounts/{account_id}/contacts/{id} | Delete Contact |
| [**contact_details**](ContactsApi.md#contact_details) | **GET** /api/v1/accounts/{account_id}/contacts/{id} | Show Contact |
| [**contact_filter**](ContactsApi.md#contact_filter) | **POST** /api/v1/accounts/{account_id}/contacts/filter | Contact Filter |
| [**contact_list**](ContactsApi.md#contact_list) | **GET** /api/v1/accounts/{account_id}/contacts | List Contacts |
| [**contact_search**](ContactsApi.md#contact_search) | **GET** /api/v1/accounts/{account_id}/contacts/search | Search Contacts |
| [**contact_update**](ContactsApi.md#contact_update) | **PUT** /api/v1/accounts/{account_id}/contacts/{id} | Update Contact |


## contact_conversations

> <Array<ContactConversationsInner>> contact_conversations(account_id, id)

Contact Conversations

Get conversations associated to that contact

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

api_instance = Cfchat::ContactsApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 8.14 # Float | ID of the contact

begin
  # Contact Conversations
  result = api_instance.contact_conversations(account_id, id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_conversations: #{e}"
end
```

#### Using the contact_conversations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ContactConversationsInner>>, Integer, Hash)> contact_conversations_with_http_info(account_id, id)

```ruby
begin
  # Contact Conversations
  data, status_code, headers = api_instance.contact_conversations_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ContactConversationsInner>>
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_conversations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Float** | ID of the contact |  |

### Return type

[**Array&lt;ContactConversationsInner&gt;**](ContactConversationsInner.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## contact_create

> <ExtendedContact> contact_create(account_id, data)

Create Contact

Create a new Contact

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

api_instance = Cfchat::ContactsApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::ContactCreate.new({inbox_id: 3.56}) # ContactCreate | 

begin
  # Create Contact
  result = api_instance.contact_create(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_create: #{e}"
end
```

#### Using the contact_create_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ExtendedContact>, Integer, Hash)> contact_create_with_http_info(account_id, data)

```ruby
begin
  # Create Contact
  data, status_code, headers = api_instance.contact_create_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ExtendedContact>
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**ContactCreate**](ContactCreate.md) |  |  |

### Return type

[**ExtendedContact**](ExtendedContact.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## contact_delete

> contact_delete(account_id, id)

Delete Contact

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

api_instance = Cfchat::ContactsApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 8.14 # Float | ID of the contact

begin
  # Delete Contact
  api_instance.contact_delete(account_id, id)
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_delete: #{e}"
end
```

#### Using the contact_delete_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> contact_delete_with_http_info(account_id, id)

```ruby
begin
  # Delete Contact
  data, status_code, headers = api_instance.contact_delete_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Float** | ID of the contact |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## contact_details

> <ExtendedContact> contact_details(account_id, id)

Show Contact

Get a contact belonging to the account using ID

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

api_instance = Cfchat::ContactsApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 8.14 # Float | ID of the contact

begin
  # Show Contact
  result = api_instance.contact_details(account_id, id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_details: #{e}"
end
```

#### Using the contact_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ExtendedContact>, Integer, Hash)> contact_details_with_http_info(account_id, id)

```ruby
begin
  # Show Contact
  data, status_code, headers = api_instance.contact_details_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ExtendedContact>
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Float** | ID of the contact |  |

### Return type

[**ExtendedContact**](ExtendedContact.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## contact_filter

> <Array<ContactListInner>> contact_filter(account_id, payload, opts)

Contact Filter

Filter contacts with custom filter options and pagination

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

  # Configure API key authorization: agentBotApiKey
  config.api_key['agentBotApiKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['agentBotApiKey'] = 'Bearer'
end

api_instance = Cfchat::ContactsApi.new
account_id = 56 # Integer | The numeric ID of the account
payload = [Cfchat::ContactFilterRequestInner.new] # Array<ContactFilterRequestInner> | 
opts = {
  page: 56 # Integer | 
}

begin
  # Contact Filter
  result = api_instance.contact_filter(account_id, payload, opts)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_filter: #{e}"
end
```

#### Using the contact_filter_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ContactListInner>>, Integer, Hash)> contact_filter_with_http_info(account_id, payload, opts)

```ruby
begin
  # Contact Filter
  data, status_code, headers = api_instance.contact_filter_with_http_info(account_id, payload, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ContactListInner>>
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_filter_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **payload** | [**Array&lt;ContactFilterRequestInner&gt;**](ContactFilterRequestInner.md) |  |  |
| **page** | **Integer** |  | [optional] |

### Return type

[**Array&lt;ContactListInner&gt;**](ContactListInner.md)

### Authorization

[userApiKey](../README.md#userApiKey), [agentBotApiKey](../README.md#agentBotApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## contact_list

> <Array<ContactListInner>> contact_list(account_id, opts)

List Contacts

Listing all the resolved contacts with pagination (Page size = 15) . Resolved contacts are the ones with a value for identifier, email or phone number

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

api_instance = Cfchat::ContactsApi.new
account_id = 56 # Integer | The numeric ID of the account
opts = {
  sort: 'name', # String | The attribute by which list should be sorted
  page: 56 # Integer | The page parameter
}

begin
  # List Contacts
  result = api_instance.contact_list(account_id, opts)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_list: #{e}"
end
```

#### Using the contact_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ContactListInner>>, Integer, Hash)> contact_list_with_http_info(account_id, opts)

```ruby
begin
  # List Contacts
  data, status_code, headers = api_instance.contact_list_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ContactListInner>>
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_list_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **sort** | **String** | The attribute by which list should be sorted | [optional] |
| **page** | **Integer** | The page parameter | [optional][default to 1] |

### Return type

[**Array&lt;ContactListInner&gt;**](ContactListInner.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## contact_search

> <ContactSearch200Response> contact_search(account_id, opts)

Search Contacts

Search the resolved contacts using a search key, currently supports email search (Page size = 15). Resolved contacts are the ones with a value for identifier, email or phone number

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

api_instance = Cfchat::ContactsApi.new
account_id = 56 # Integer | The numeric ID of the account
opts = {
  q: 'q_example', # String | Search using contact `name`, `identifier`, `email` or `phone number`
  sort: 'name', # String | The attribute by which list should be sorted
  page: 56 # Integer | The page parameter
}

begin
  # Search Contacts
  result = api_instance.contact_search(account_id, opts)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_search: #{e}"
end
```

#### Using the contact_search_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ContactSearch200Response>, Integer, Hash)> contact_search_with_http_info(account_id, opts)

```ruby
begin
  # Search Contacts
  data, status_code, headers = api_instance.contact_search_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ContactSearch200Response>
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_search_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **q** | **String** | Search using contact &#x60;name&#x60;, &#x60;identifier&#x60;, &#x60;email&#x60; or &#x60;phone number&#x60; | [optional] |
| **sort** | **String** | The attribute by which list should be sorted | [optional] |
| **page** | **Integer** | The page parameter | [optional][default to 1] |

### Return type

[**ContactSearch200Response**](ContactSearch200Response.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## contact_update

> <ContactBase> contact_update(account_id, id, data)

Update Contact

Update a contact belonging to the account using ID

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

api_instance = Cfchat::ContactsApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 8.14 # Float | ID of the contact
data = Cfchat::ContactUpdate.new # ContactUpdate | 

begin
  # Update Contact
  result = api_instance.contact_update(account_id, id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_update: #{e}"
end
```

#### Using the contact_update_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ContactBase>, Integer, Hash)> contact_update_with_http_info(account_id, id, data)

```ruby
begin
  # Update Contact
  data, status_code, headers = api_instance.contact_update_with_http_info(account_id, id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ContactBase>
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsApi->contact_update_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Float** | ID of the contact |  |
| **data** | [**ContactUpdate**](ContactUpdate.md) |  |  |

### Return type

[**ContactBase**](ContactBase.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

