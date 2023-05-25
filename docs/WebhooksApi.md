# Cfchat::WebhooksApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_a_webhook**](WebhooksApi.md#create_a_webhook) | **POST** /api/v1/accounts/{account_id}/webhooks | Add a webhook |
| [**delete_a_webhook**](WebhooksApi.md#delete_a_webhook) | **DELETE** /api/v1/accounts/{account_id}/webhooks/{webhook_id} | Delete a webhook |
| [**list_all_webhooks**](WebhooksApi.md#list_all_webhooks) | **GET** /api/v1/accounts/{account_id}/webhooks | List all webhooks |
| [**update_a_webhook**](WebhooksApi.md#update_a_webhook) | **PATCH** /api/v1/accounts/{account_id}/webhooks/{webhook_id} | Update a webhook object |


## create_a_webhook

> <Webhook> create_a_webhook(account_id, data)

Add a webhook

Add a webhook subscription to the account

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

api_instance = Cfchat::WebhooksApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::WebhookCreateUpdatePayload.new # WebhookCreateUpdatePayload | 

begin
  # Add a webhook
  result = api_instance.create_a_webhook(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling WebhooksApi->create_a_webhook: #{e}"
end
```

#### Using the create_a_webhook_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Webhook>, Integer, Hash)> create_a_webhook_with_http_info(account_id, data)

```ruby
begin
  # Add a webhook
  data, status_code, headers = api_instance.create_a_webhook_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Webhook>
rescue Cfchat::ApiError => e
  puts "Error when calling WebhooksApi->create_a_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**WebhookCreateUpdatePayload**](WebhookCreateUpdatePayload.md) |  |  |

### Return type

[**Webhook**](Webhook.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_a_webhook

> delete_a_webhook(account_id, webhook_id)

Delete a webhook

Delete a webhook from the account

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

api_instance = Cfchat::WebhooksApi.new
account_id = 56 # Integer | The numeric ID of the account
webhook_id = 56 # Integer | The numeric ID of the webhook

begin
  # Delete a webhook
  api_instance.delete_a_webhook(account_id, webhook_id)
rescue Cfchat::ApiError => e
  puts "Error when calling WebhooksApi->delete_a_webhook: #{e}"
end
```

#### Using the delete_a_webhook_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_a_webhook_with_http_info(account_id, webhook_id)

```ruby
begin
  # Delete a webhook
  data, status_code, headers = api_instance.delete_a_webhook_with_http_info(account_id, webhook_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling WebhooksApi->delete_a_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **webhook_id** | **Integer** | The numeric ID of the webhook |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## list_all_webhooks

> <Array<Webhook>> list_all_webhooks(account_id)

List all webhooks

List all webhooks in the account

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

api_instance = Cfchat::WebhooksApi.new
account_id = 56 # Integer | The numeric ID of the account

begin
  # List all webhooks
  result = api_instance.list_all_webhooks(account_id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling WebhooksApi->list_all_webhooks: #{e}"
end
```

#### Using the list_all_webhooks_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Webhook>>, Integer, Hash)> list_all_webhooks_with_http_info(account_id)

```ruby
begin
  # List all webhooks
  data, status_code, headers = api_instance.list_all_webhooks_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Webhook>>
rescue Cfchat::ApiError => e
  puts "Error when calling WebhooksApi->list_all_webhooks_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |

### Return type

[**Array&lt;Webhook&gt;**](Webhook.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_a_webhook

> <Webhook> update_a_webhook(account_id, webhook_id, data)

Update a webhook object

Update a webhook object in the account

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

api_instance = Cfchat::WebhooksApi.new
account_id = 56 # Integer | The numeric ID of the account
webhook_id = 56 # Integer | The numeric ID of the webhook
data = Cfchat::WebhookCreateUpdatePayload.new # WebhookCreateUpdatePayload | 

begin
  # Update a webhook object
  result = api_instance.update_a_webhook(account_id, webhook_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling WebhooksApi->update_a_webhook: #{e}"
end
```

#### Using the update_a_webhook_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Webhook>, Integer, Hash)> update_a_webhook_with_http_info(account_id, webhook_id, data)

```ruby
begin
  # Update a webhook object
  data, status_code, headers = api_instance.update_a_webhook_with_http_info(account_id, webhook_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Webhook>
rescue Cfchat::ApiError => e
  puts "Error when calling WebhooksApi->update_a_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **webhook_id** | **Integer** | The numeric ID of the webhook |  |
| **data** | [**WebhookCreateUpdatePayload**](WebhookCreateUpdatePayload.md) |  |  |

### Return type

[**Webhook**](Webhook.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

