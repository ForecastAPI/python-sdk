# forecastapi.AnomalyDetectionApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**detect_anomalies**](AnomalyDetectionApi.md#detect_anomalies) | **POST** /v2/detect-anomalies | Detect anomalies in time series data


# **detect_anomalies**
> AnomalyDetectionResponse detect_anomalies(anomaly_detection_request)

Detect anomalies in time series data

Detects anomalies using statistical methods — z-score, IQR or seasonal — and
automatically selects the best method for the data's characteristics unless one is
named in `anomaly_settings.method`. Returns each anomalous point with its expected
range, severity and type, plus an analysis of how the method was chosen.


### Example

* Api Key Authentication (apiKey):

```python
import forecastapi
from forecastapi.models.anomaly_detection_request import AnomalyDetectionRequest
from forecastapi.models.anomaly_detection_response import AnomalyDetectionResponse
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
    api_instance = forecastapi.AnomalyDetectionApi(api_client)
    anomaly_detection_request = forecastapi.AnomalyDetectionRequest() # AnomalyDetectionRequest | 

    try:
        # Detect anomalies in time series data
        api_response = api_instance.detect_anomalies(anomaly_detection_request)
        print("The response of AnomalyDetectionApi->detect_anomalies:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnomalyDetectionApi->detect_anomalies: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **anomaly_detection_request** | [**AnomalyDetectionRequest**](AnomalyDetectionRequest.md)|  | 

### Return type

[**AnomalyDetectionResponse**](AnomalyDetectionResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Detection results |  -  |
**401** | Unauthorized - Invalid or missing API key |  -  |
**422** | Validation error, or the data is not suitable for the requested detection method (the latter returns &#x60;{error, time_taken_ms}&#x60;)  |  -  |
**500** | Internal error during detection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

