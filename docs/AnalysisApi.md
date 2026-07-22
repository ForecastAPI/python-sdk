# forecastapi.AnalysisApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**analyze_time_series**](AnalysisApi.md#analyze_time_series) | **POST** /v2/analyze | Analyze time series data without generating forecast


# **analyze_time_series**
> AnalysisResponse analyze_time_series(forecast_request)

Analyze time series data without generating forecast

### Example

* Api Key Authentication (apiKey):

```python
import forecastapi
from forecastapi.models.analysis_response import AnalysisResponse
from forecastapi.models.forecast_request import ForecastRequest
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
    api_instance = forecastapi.AnalysisApi(api_client)
    forecast_request = forecastapi.ForecastRequest() # ForecastRequest | 

    try:
        # Analyze time series data without generating forecast
        api_response = api_instance.analyze_time_series(forecast_request)
        print("The response of AnalysisApi->analyze_time_series:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnalysisApi->analyze_time_series: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **forecast_request** | [**ForecastRequest**](ForecastRequest.md)|  | 

### Return type

[**AnalysisResponse**](AnalysisResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful data analysis |  -  |
**401** | Unauthorized - Invalid or missing API key |  -  |
**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

