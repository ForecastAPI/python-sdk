# forecastapi.BatchForecastingApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_batch_forecast**](BatchForecastingApi.md#create_batch_forecast) | **POST** /v2/batch/forecast | Submit a batch of series for forecasting
[**get_batch_forecast**](BatchForecastingApi.md#get_batch_forecast) | **GET** /v2/batch/forecast/{batch_id} | Poll a batch forecast for status and results
[**presign_batch_forecast**](BatchForecastingApi.md#presign_batch_forecast) | **POST** /v2/batch/forecast/presign | Get a presigned URL for a file-based batch upload


# **create_batch_forecast**
> BatchForecastAccepted create_batch_forecast(batch_forecast_request)

Submit a batch of series for forecasting

Forecast up to 100,000 independent series in one call (10 on the free tier), at a
discount per forecast. Each series is processed independently — one failing series
does not fail the others. Submission returns `202` with a `batch_id` to poll via
`GET /v2/batch/forecast/{batch_id}`.

Request-level `periods`, `frequency`, `data_type`, `confidence` and the four
planning parameters (`quantiles`, `value_bounds`, `adjustments`, `accumulate`) act
as defaults every series inherits; any series may override any of them. `model` is
request-level only.

For payloads too large to send inline, get a presigned upload URL from
`POST /v2/batch/forecast/presign` and submit `file_key` instead of `series`.


### Example

* Api Key Authentication (apiKey):

```python
import forecastapi
from forecastapi.models.batch_forecast_accepted import BatchForecastAccepted
from forecastapi.models.batch_forecast_request import BatchForecastRequest
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
    api_instance = forecastapi.BatchForecastingApi(api_client)
    batch_forecast_request = {"series":[{"identifier":"SKU-001","data":[{"date":"2024-01-01","value":100},{"date":"2024-02-01","value":150}],"data_type":"sales","periods":3},{"identifier":"CHURN-RATE","data":[{"date":"2024-01-01","value":0.041},{"date":"2024-02-01","value":0.038}],"periods":3,"value_bounds":{"min":0,"max":1}}],"frequency":"M","confidence":0.8,"quantiles":[0.1,0.5,0.9]} # BatchForecastRequest | 

    try:
        # Submit a batch of series for forecasting
        api_response = api_instance.create_batch_forecast(batch_forecast_request)
        print("The response of BatchForecastingApi->create_batch_forecast:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BatchForecastingApi->create_batch_forecast: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **batch_forecast_request** | [**BatchForecastRequest**](BatchForecastRequest.md)|  | 

### Return type

[**BatchForecastAccepted**](BatchForecastAccepted.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Accepted — the batch is queued for processing |  -  |
**401** | Unauthorized - Invalid or missing API key |  -  |
**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_batch_forecast**
> BatchForecastStatusResponse get_batch_forecast(batch_id)

Poll a batch forecast for status and results

Returns the batch's status, a summary once it finalises, and each series' results
under `results.data` — keyed by **entity id** rather than by your identifier,
because one batch may contain the same identifier under several `tenant_context`
values. Match series via the `identifier` and `tenant_context` echoed inside each
result object.


### Example

* Api Key Authentication (apiKey):

```python
import forecastapi
from forecastapi.models.batch_forecast_status_response import BatchForecastStatusResponse
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
    api_instance = forecastapi.BatchForecastingApi(api_client)
    batch_id = 'batch_id_example' # str | The id returned by POST /v2/batch/forecast

    try:
        # Poll a batch forecast for status and results
        api_response = api_instance.get_batch_forecast(batch_id)
        print("The response of BatchForecastingApi->get_batch_forecast:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BatchForecastingApi->get_batch_forecast: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **batch_id** | **str**| The id returned by POST /v2/batch/forecast | 

### Return type

[**BatchForecastStatusResponse**](BatchForecastStatusResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Current status and results of the batch |  -  |
**401** | Unauthorized - Invalid or missing API key |  -  |
**404** | No batch with this id exists for your team |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **presign_batch_forecast**
> BatchPresignResponse presign_batch_forecast()

Get a presigned URL for a file-based batch upload

Returns a presigned URL for uploading a JSON file containing the batch request
body — an object with a `series` array, the same shape as the inline
`/v2/batch/forecast` request. HTTP PUT the file to `upload_url` (including any
returned `headers`), then submit the batch by POSTing the returned `file_key` to
`/v2/batch/forecast`. The URL is valid for 30 minutes.


### Example

* Api Key Authentication (apiKey):

```python
import forecastapi
from forecastapi.models.batch_presign_response import BatchPresignResponse
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
    api_instance = forecastapi.BatchForecastingApi(api_client)

    try:
        # Get a presigned URL for a file-based batch upload
        api_response = api_instance.presign_batch_forecast()
        print("The response of BatchForecastingApi->presign_batch_forecast:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BatchForecastingApi->presign_batch_forecast: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**BatchPresignResponse**](BatchPresignResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Presigned upload details |  -  |
**401** | Unauthorized - Invalid or missing API key |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

