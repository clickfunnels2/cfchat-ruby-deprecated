# Cfchat::ReportsApi

All URIs are relative to *https://chat.myclickfunnels.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_account_conversation_metrics**](ReportsApi.md#get_account_conversation_metrics) | **GET** /api/v2/accounts/{account_id}/reports/conversations | Account Conversation Metrics |
| [**get_agent_conversation_metrics**](ReportsApi.md#get_agent_conversation_metrics) | **GET** /api/v2/accounts/{account_id}/reports/conversations/ | Agent Conversation Metrics |
| [**list_all_conversation_statistics**](ReportsApi.md#list_all_conversation_statistics) | **GET** /api/v2/accounts/{account_id}/reports | Get Account reports |
| [**list_all_conversation_statistics_summary**](ReportsApi.md#list_all_conversation_statistics_summary) | **GET** /api/v2/accounts/{account_id}/reports/summary | Get Account reports summary |


## get_account_conversation_metrics

> <GetAccountConversationMetrics200Response> get_account_conversation_metrics(account_id, type)

Account Conversation Metrics

Get conversation metrics for Account

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

api_instance = Cfchat::ReportsApi.new
account_id = 56 # Integer | The numeric ID of the account
type = 'account' # String | Type of report

begin
  # Account Conversation Metrics
  result = api_instance.get_account_conversation_metrics(account_id, type)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ReportsApi->get_account_conversation_metrics: #{e}"
end
```

#### Using the get_account_conversation_metrics_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetAccountConversationMetrics200Response>, Integer, Hash)> get_account_conversation_metrics_with_http_info(account_id, type)

```ruby
begin
  # Account Conversation Metrics
  data, status_code, headers = api_instance.get_account_conversation_metrics_with_http_info(account_id, type)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetAccountConversationMetrics200Response>
rescue Cfchat::ApiError => e
  puts "Error when calling ReportsApi->get_account_conversation_metrics_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **type** | **String** | Type of report |  |

### Return type

[**GetAccountConversationMetrics200Response**](GetAccountConversationMetrics200Response.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## get_agent_conversation_metrics

> <Array<AgentConversationMetrics>> get_agent_conversation_metrics(account_id, type, opts)

Agent Conversation Metrics

Get conversation metrics for Agent

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

api_instance = Cfchat::ReportsApi.new
account_id = 56 # Integer | The numeric ID of the account
type = 'agent' # String | Type of report
opts = {
  user_id: 'user_id_example' # String | The numeric ID of the user
}

begin
  # Agent Conversation Metrics
  result = api_instance.get_agent_conversation_metrics(account_id, type, opts)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ReportsApi->get_agent_conversation_metrics: #{e}"
end
```

#### Using the get_agent_conversation_metrics_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<AgentConversationMetrics>>, Integer, Hash)> get_agent_conversation_metrics_with_http_info(account_id, type, opts)

```ruby
begin
  # Agent Conversation Metrics
  data, status_code, headers = api_instance.get_agent_conversation_metrics_with_http_info(account_id, type, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<AgentConversationMetrics>>
rescue Cfchat::ApiError => e
  puts "Error when calling ReportsApi->get_agent_conversation_metrics_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **type** | **String** | Type of report |  |
| **user_id** | **String** | The numeric ID of the user | [optional] |

### Return type

[**Array&lt;AgentConversationMetrics&gt;**](AgentConversationMetrics.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## list_all_conversation_statistics

> <Array<ListAllConversationStatistics200ResponseInner>> list_all_conversation_statistics(account_id, metric, type, opts)

Get Account reports

Get Account reports for a specific type, metric and date range

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

api_instance = Cfchat::ReportsApi.new
account_id = 56 # Integer | The numeric ID of the account
metric = 'conversations_count' # String | The type of metric
type = 'account' # String | Type of report
opts = {
  id: 'id_example', # String | The Id of specific object in case of agent/inbox/label
  since: 'since_example', # String | The timestamp from where report should start.
  _until: '_until_example' # String | The timestamp from where report should stop.
}

begin
  # Get Account reports
  result = api_instance.list_all_conversation_statistics(account_id, metric, type, opts)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ReportsApi->list_all_conversation_statistics: #{e}"
end
```

#### Using the list_all_conversation_statistics_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<ListAllConversationStatistics200ResponseInner>>, Integer, Hash)> list_all_conversation_statistics_with_http_info(account_id, metric, type, opts)

```ruby
begin
  # Get Account reports
  data, status_code, headers = api_instance.list_all_conversation_statistics_with_http_info(account_id, metric, type, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<ListAllConversationStatistics200ResponseInner>>
rescue Cfchat::ApiError => e
  puts "Error when calling ReportsApi->list_all_conversation_statistics_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **metric** | **String** | The type of metric |  |
| **type** | **String** | Type of report |  |
| **id** | **String** | The Id of specific object in case of agent/inbox/label | [optional] |
| **since** | **String** | The timestamp from where report should start. | [optional] |
| **_until** | **String** | The timestamp from where report should stop. | [optional] |

### Return type

[**Array&lt;ListAllConversationStatistics200ResponseInner&gt;**](ListAllConversationStatistics200ResponseInner.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8


## list_all_conversation_statistics_summary

> <AccountSummary> list_all_conversation_statistics_summary(account_id, type, opts)

Get Account reports summary

Get Account reports summary for a specific type and date range

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

api_instance = Cfchat::ReportsApi.new
account_id = 56 # Integer | The numeric ID of the account
type = 'account' # String | Type of report
opts = {
  id: 'id_example', # String | The Id of specific object in case of agent/inbox/label
  since: 'since_example', # String | The timestamp from where report should start.
  _until: '_until_example' # String | The timestamp from where report should stop.
}

begin
  # Get Account reports summary
  result = api_instance.list_all_conversation_statistics_summary(account_id, type, opts)
  p result
rescue Cfchat::ApiError => e
  puts "Error when calling ReportsApi->list_all_conversation_statistics_summary: #{e}"
end
```

#### Using the list_all_conversation_statistics_summary_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AccountSummary>, Integer, Hash)> list_all_conversation_statistics_summary_with_http_info(account_id, type, opts)

```ruby
begin
  # Get Account reports summary
  data, status_code, headers = api_instance.list_all_conversation_statistics_summary_with_http_info(account_id, type, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AccountSummary>
rescue Cfchat::ApiError => e
  puts "Error when calling ReportsApi->list_all_conversation_statistics_summary_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | The numeric ID of the account |  |
| **type** | **String** | Type of report |  |
| **id** | **String** | The Id of specific object in case of agent/inbox/label | [optional] |
| **since** | **String** | The timestamp from where report should start. | [optional] |
| **_until** | **String** | The timestamp from where report should stop. | [optional] |

### Return type

[**AccountSummary**](AccountSummary.md)

### Authorization

[userApiKey](../README.md#userApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json; charset=utf-8

