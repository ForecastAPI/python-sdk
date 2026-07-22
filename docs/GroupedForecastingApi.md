# forecastapi.GroupedForecastingApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_grouped_forecast**](GroupedForecastingApi.md#create_grouped_forecast) | **POST** /v2/forecast/grouped | Submit a grouped (hierarchical) forecast with reconciliation
[**get_grouped_forecast**](GroupedForecastingApi.md#get_grouped_forecast) | **GET** /v2/forecast/grouped/{grouped_forecast_id} | Poll a grouped forecast for status and results


# **create_grouped_forecast**
> GroupedForecastAccepted create_grouped_forecast(grouped_forecast_request)

Submit a grouped (hierarchical) forecast with reconciliation

Forecast a set of related series that roll up to a total — MRR by plan and region,
demand by warehouse, revenue by category — and get back one coherent result: every
parent equals the sum of its children, in every period, at every level.

You send only the **leaves** of the hierarchy (every combination of the declared
dimensions, each with its own history). The API derives every aggregate level and the
grand total by summing the leaf histories, forecasts the nodes, reconciles them to
coherence, and stores each node as its own entity with independently tracked accuracy.

Processing is **asynchronous**: submission returns `202` with an id to poll via
`GET /v2/forecast/grouped/{grouped_forecast_id}`. The run executes in the background
as one all-or-nothing job — a hierarchy is one coherent answer, so there is no partial
success. If any node cannot be forecast, the run fails with the reason rather than
returning numbers that don't add up.

If you just want independent forecasts per slice — no coherent roll-up — the batch
endpoint with per-series identifiers or `tenant_context` is simpler and tolerates
per-series failure.


### Example

* Api Key Authentication (apiKey):

```python
import forecastapi
from forecastapi.models.grouped_forecast_accepted import GroupedForecastAccepted
from forecastapi.models.grouped_forecast_request import GroupedForecastRequest
from forecastapi.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://forecastapi.com
# See configuration.py for a list of all supported configuration parameters.
configuration = forecastapi.Configuration(
    host = "https://forecastapi.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKey
configuration.api_key['apiKey'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKey'] = 'Bearer'

# Enter a context with an instance of the API client
with forecastapi.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = forecastapi.GroupedForecastingApi(api_client)
    grouped_forecast_request = {"identifier":"mrr","hierarchy":["region","plan"],"reconciliation":"bottom_up","frequency":"M","periods":6,"data_type":"revenue","series":[{"segment":{"region":"eu","plan":"pro"},"data":[{"date":"2024-01-01","value":42000},{"date":"2024-02-01","value":43800}]},{"segment":{"region":"eu","plan":"free"},"data":[{"date":"2024-01-01","value":3100},{"date":"2024-02-01","value":3300}]},{"segment":{"region":"us","plan":"pro"},"data":[{"date":"2024-01-01","value":61000},{"date":"2024-02-01","value":62500}]}]} # GroupedForecastRequest | 

    try:
        # Submit a grouped (hierarchical) forecast with reconciliation
        api_response = api_instance.create_grouped_forecast(grouped_forecast_request)
        print("The response of GroupedForecastingApi->create_grouped_forecast:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GroupedForecastingApi->create_grouped_forecast: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **grouped_forecast_request** | [**GroupedForecastRequest**](GroupedForecastRequest.md)|  | 

### Return type

[**GroupedForecastAccepted**](GroupedForecastAccepted.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Accepted — the hierarchy is queued for background processing |  -  |
**401** | Unauthorized - Invalid or missing API key |  -  |
**422** | Validation error. Notable rejections beyond field-shape errors: per-series config overrides (&#x60;series.*.periods&#x60;, &#x60;series.*.model&#x60;, …), the planning parameters (&#x60;quantiles&#x60;, &#x60;value_bounds&#x60;, &#x60;adjustments&#x60;, &#x60;accumulate&#x60;) at any level, a &#x60;segment&#x60; not naming exactly the declared hierarchy dimensions, duplicate segments, series not ending on the same date, &#x60;reconciliation: top_down&#x60;, and a hierarchy expanding past 250 nodes.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_grouped_forecast**
> GroupedForecastStatusResponse get_grouped_forecast(grouped_forecast_id)

Poll a grouped forecast for status and results

Returns the run's status. Once `completed`, `results` carries a node map keyed by
segment (`total`, `region=eu`, `plan=pro|region=eu`, …) — every node with its own
forecast rows, its place in the tree, and the reconciliation details. If the run
`failed`, `error` carries the reason and `results` stays null.


### Example

* Api Key Authentication (apiKey):

```python
import forecastapi
from forecastapi.models.grouped_forecast_status_response import GroupedForecastStatusResponse
from forecastapi.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://forecastapi.com
# See configuration.py for a list of all supported configuration parameters.
configuration = forecastapi.Configuration(
    host = "https://forecastapi.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKey
configuration.api_key['apiKey'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKey'] = 'Bearer'

# Enter a context with an instance of the API client
with forecastapi.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = forecastapi.GroupedForecastingApi(api_client)
    grouped_forecast_id = 'k3n9x2m4p8q1w5r7' # str | The id returned by POST /v2/forecast/grouped

    try:
        # Poll a grouped forecast for status and results
        api_response = api_instance.get_grouped_forecast(grouped_forecast_id)
        print("The response of GroupedForecastingApi->get_grouped_forecast:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GroupedForecastingApi->get_grouped_forecast: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **grouped_forecast_id** | **str**| The id returned by POST /v2/forecast/grouped | 

### Return type

[**GroupedForecastStatusResponse**](GroupedForecastStatusResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Current status of the grouped forecast run |  -  |
**401** | Unauthorized - Invalid or missing API key |  -  |
**404** | No grouped forecast with this id exists for your team |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

