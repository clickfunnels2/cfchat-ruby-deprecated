# Cfchat::ContactsAPIApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_a_contact**](ContactsAPIApi.md#create_a_contact) | **POST** /public/api/v1/inboxes/{inbox_identifier}/contacts | Create a contact |
| [**get_details_of_a_contact**](ContactsAPIApi.md#get_details_of_a_contact) | **GET** /public/api/v1/inboxes/{inbox_identifier}/contacts/{contact_identifier} | Get a contact |
| [**update_a_contact**](ContactsAPIApi.md#update_a_contact) | **PATCH** /public/api/v1/inboxes/{inbox_identifier}/contacts/{contact_identifier} | Update a contact |


## create_a_contact

> <PublicContact> create_a_contact(inbox_identifier, data)

Create a contact

Create a contact

### Examples

```ruby
require 'time'
require 'cfchat'

api_instance = Cfchat::ContactsAPIApi.new
inbox_identifier = 'inbox_identifier_example' # String | The identifier obtained from API inbox channel
data = Cfchat::PublicContactCreateUpdatePayload.new # PublicContactCreateUpdatePayload | 

begin
  # Create a contact
  result = api_instance.create_a_contact(inbox_identifier, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsAPIApi->create_a_contact: #{e}"
end
```

#### Using the create_a_contact_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PublicContact>, Integer, Hash)> create_a_contact_with_http_info(inbox_identifier, data)

```ruby
begin
  # Create a contact
  data, status_code, headers = api_instance.create_a_contact_with_http_info(inbox_identifier, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PublicContact>
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsAPIApi->create_a_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inbox_identifier** | **String** | The identifier obtained from API inbox channel |  |
| **data** | [**PublicContactCreateUpdatePayload**](PublicContactCreateUpdatePayload.md) |  |  |

### Return type

[**PublicContact**](PublicContact.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## get_details_of_a_contact

> <PublicContact> get_details_of_a_contact(inbox_identifier, contact_identifier)

Get a contact

Get the details of a contact

### Examples

```ruby
require 'time'
require 'cfchat'

api_instance = Cfchat::ContactsAPIApi.new
inbox_identifier = 'inbox_identifier_example' # String | The identifier obtained from API inbox channel
contact_identifier = 'contact_identifier_example' # String | The source id of contact obtained on contact create

begin
  # Get a contact
  result = api_instance.get_details_of_a_contact(inbox_identifier, contact_identifier)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsAPIApi->get_details_of_a_contact: #{e}"
end
```

#### Using the get_details_of_a_contact_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PublicContact>, Integer, Hash)> get_details_of_a_contact_with_http_info(inbox_identifier, contact_identifier)

```ruby
begin
  # Get a contact
  data, status_code, headers = api_instance.get_details_of_a_contact_with_http_info(inbox_identifier, contact_identifier)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PublicContact>
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsAPIApi->get_details_of_a_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inbox_identifier** | **String** | The identifier obtained from API inbox channel |  |
| **contact_identifier** | **String** | The source id of contact obtained on contact create |  |

### Return type

[**PublicContact**](PublicContact.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_a_contact

> <PublicContact> update_a_contact(inbox_identifier, contact_identifier, data)

Update a contact

Update a contact's attributes

### Examples

```ruby
require 'time'
require 'cfchat'

api_instance = Cfchat::ContactsAPIApi.new
inbox_identifier = 'inbox_identifier_example' # String | The identifier obtained from API inbox channel
contact_identifier = 'contact_identifier_example' # String | The source id of contact obtained on contact create
data = Cfchat::PublicContactCreateUpdatePayload.new # PublicContactCreateUpdatePayload | 

begin
  # Update a contact
  result = api_instance.update_a_contact(inbox_identifier, contact_identifier, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsAPIApi->update_a_contact: #{e}"
end
```

#### Using the update_a_contact_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PublicContact>, Integer, Hash)> update_a_contact_with_http_info(inbox_identifier, contact_identifier, data)

```ruby
begin
  # Update a contact
  data, status_code, headers = api_instance.update_a_contact_with_http_info(inbox_identifier, contact_identifier, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PublicContact>
rescue Cfchat::ApiError => e
  puts "Error when calling ContactsAPIApi->update_a_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **inbox_identifier** | **String** | The identifier obtained from API inbox channel |  |
| **contact_identifier** | **String** | The source id of contact obtained on contact create |  |
| **data** | [**PublicContactCreateUpdatePayload**](PublicContactCreateUpdatePayload.md) |  |  |

### Return type

[**PublicContact**](PublicContact.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

