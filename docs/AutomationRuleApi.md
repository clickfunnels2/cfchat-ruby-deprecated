# Cfchat::AutomationRuleApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_new_automation_rule_to_account**](AutomationRuleApi.md#add_new_automation_rule_to_account) | **POST** /api/v1/accounts/{account_id}/automation_rules | Add a new automation rule |
| [**delete_automation_rule_from_account**](AutomationRuleApi.md#delete_automation_rule_from_account) | **DELETE** /api/v1/accounts/{account_id}/automation_rules/{id} | Remove a automation rule from account |
| [**get_account_automation_rule**](AutomationRuleApi.md#get_account_automation_rule) | **GET** /api/v1/accounts/{account_id}/automation_rules | List all automation rules in an account |
| [**get_details_of_a_single_automation_rule**](AutomationRuleApi.md#get_details_of_a_single_automation_rule) | **GET** /api/v1/accounts/{account_id}/automation_rules/{id} | Get a automation rule details |
| [**update_automation_rule_in_account**](AutomationRuleApi.md#update_automation_rule_in_account) | **PATCH** /api/v1/accounts/{account_id}/automation_rules/{id} | Update automation rule in Account |


## add_new_automation_rule_to_account

> <AutomationRule> add_new_automation_rule_to_account(account_id, data)

Add a new automation rule

Add a new automation rule to account

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

api_instance = Cfchat::AutomationRuleApi.new
account_id = 56 # Integer | The numeric ID of the account
data = Cfchat::AutomationRuleCreateUpdatePayload.new # AutomationRuleCreateUpdatePayload | 

begin
  # Add a new automation rule
  result = api_instance.add_new_automation_rule_to_account(account_id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AutomationRuleApi->add_new_automation_rule_to_account: #{e}"
end
```

#### Using the add_new_automation_rule_to_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AutomationRule>, Integer, Hash)> add_new_automation_rule_to_account_with_http_info(account_id, data)

```ruby
begin
  # Add a new automation rule
  data, status_code, headers = api_instance.add_new_automation_rule_to_account_with_http_info(account_id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AutomationRule>
rescue Cfchat::ApiError => e
  puts "Error when calling AutomationRuleApi->add_new_automation_rule_to_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **data** | [**AutomationRuleCreateUpdatePayload**](AutomationRuleCreateUpdatePayload.md) |  |  |

### Return type

[**AutomationRule**](AutomationRule.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8


## delete_automation_rule_from_account

> delete_automation_rule_from_account(account_id, id)

Remove a automation rule from account

Remove a automation rule from account

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

api_instance = Cfchat::AutomationRuleApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 56 # Integer | The ID of the automation rule to be deleted

begin
  # Remove a automation rule from account
  api_instance.delete_automation_rule_from_account(account_id, id)
rescue Cfchat::ApiError => e
  puts "Error when calling AutomationRuleApi->delete_automation_rule_from_account: #{e}"
end
```

#### Using the delete_automation_rule_from_account_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_automation_rule_from_account_with_http_info(account_id, id)

```ruby
begin
  # Remove a automation rule from account
  data, status_code, headers = api_instance.delete_automation_rule_from_account_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Cfchat::ApiError => e
  puts "Error when calling AutomationRuleApi->delete_automation_rule_from_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Integer** | The ID of the automation rule to be deleted |  |

### Return type

nil (empty response body)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## get_account_automation_rule

> <Array<AutomationRule>> get_account_automation_rule(account_id, opts)

List all automation rules in an account

Get details of automation rules in an Account

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

api_instance = Cfchat::AutomationRuleApi.new
account_id = 56 # Integer | The numeric ID of the account
opts = {
  page: 56 # Integer | The page parameter
}

begin
  # List all automation rules in an account
  result = api_instance.get_account_automation_rule(account_id, opts)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AutomationRuleApi->get_account_automation_rule: #{e}"
end
```

#### Using the get_account_automation_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<AutomationRule>>, Integer, Hash)> get_account_automation_rule_with_http_info(account_id, opts)

```ruby
begin
  # List all automation rules in an account
  data, status_code, headers = api_instance.get_account_automation_rule_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<AutomationRule>>
rescue Cfchat::ApiError => e
  puts "Error when calling AutomationRuleApi->get_account_automation_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **page** | **Integer** | The page parameter | [optional][default to 1] |

### Return type

[**Array&lt;AutomationRule&gt;**](AutomationRule.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## get_details_of_a_single_automation_rule

> <AutomationRule> get_details_of_a_single_automation_rule(account_id, id)

Get a automation rule details

Get the details of a automation rule in the account

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

api_instance = Cfchat::AutomationRuleApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 56 # Integer | The ID of the automation rule to be updated.

begin
  # Get a automation rule details
  result = api_instance.get_details_of_a_single_automation_rule(account_id, id)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AutomationRuleApi->get_details_of_a_single_automation_rule: #{e}"
end
```

#### Using the get_details_of_a_single_automation_rule_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AutomationRule>, Integer, Hash)> get_details_of_a_single_automation_rule_with_http_info(account_id, id)

```ruby
begin
  # Get a automation rule details
  data, status_code, headers = api_instance.get_details_of_a_single_automation_rule_with_http_info(account_id, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AutomationRule>
rescue Cfchat::ApiError => e
  puts "Error when calling AutomationRuleApi->get_details_of_a_single_automation_rule_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Integer** | The ID of the automation rule to be updated. |  |

### Return type

[**AutomationRule**](AutomationRule.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## update_automation_rule_in_account

> <AutomationRule> update_automation_rule_in_account(account_id, id, data)

Update automation rule in Account

Update a automation rule in account

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

api_instance = Cfchat::AutomationRuleApi.new
account_id = 56 # Integer | The numeric ID of the account
id = 56 # Integer | The ID of the automation rule to be updated.
data = Cfchat::AutomationRuleCreateUpdatePayload.new # AutomationRuleCreateUpdatePayload | 

begin
  # Update automation rule in Account
  result = api_instance.update_automation_rule_in_account(account_id, id, data)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling AutomationRuleApi->update_automation_rule_in_account: #{e}"
end
```

#### Using the update_automation_rule_in_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AutomationRule>, Integer, Hash)> update_automation_rule_in_account_with_http_info(account_id, id, data)

```ruby
begin
  # Update automation rule in Account
  data, status_code, headers = api_instance.update_automation_rule_in_account_with_http_info(account_id, id, data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AutomationRule>
rescue Cfchat::ApiError => e
  puts "Error when calling AutomationRuleApi->update_automation_rule_in_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **id** | **Integer** | The ID of the automation rule to be updated. |  |
| **data** | [**AutomationRuleCreateUpdatePayload**](AutomationRuleCreateUpdatePayload.md) |  |  |

### Return type

[**AutomationRule**](AutomationRule.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: application/json; charset=utf-8
- **Accept**: application/json; charset=utf-8

