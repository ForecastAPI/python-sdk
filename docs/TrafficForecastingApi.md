# forecastapi.TrafficForecastingApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_traffic_forecast**](TrafficForecastingApi.md#create_traffic_forecast) | **POST** /v2/traffic-forecasting | Generate traffic forecasting with infrastructure scaling recommendations


# **create_traffic_forecast**
> TrafficForecastingResponse create_traffic_forecast(traffic_forecasting_request)

Generate traffic forecasting with infrastructure scaling recommendations

Generate comprehensive traffic forecasts with infrastructure scaling recommendations, capacity analysis,
cost optimization, and traffic anomaly alerts. This endpoint is designed for web applications, APIs,
and infrastructure teams to predict traffic patterns and optimize resource allocation.

**Key Features:**
- Intelligent traffic pattern forecasting with multiple algorithms
- Infrastructure scaling recommendations (scale up/down/maintain)
- Real-time capacity utilization analysis
- Traffic spike and anomaly detection alerts
- Cost optimization recommendations with potential savings
- Auto-scaling benefit analysis
- Support for various time frequencies (minute, hourly, daily, etc.)


### Example

* Api Key Authentication (apiKey):

```python
import forecastapi
from forecastapi.models.traffic_forecasting_request import TrafficForecastingRequest
from forecastapi.models.traffic_forecasting_response import TrafficForecastingResponse
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
    api_instance = forecastapi.TrafficForecastingApi(api_client)
    traffic_forecasting_request = {"identifier":"api-endpoint-users","frequency":"H","start_date":"2024-01-01","periods":24,"enable_intelligent_aggregation":true,"data":[{"date":"2023-12-01 00:00:00","value":1200},{"date":"2023-12-01 01:00:00","value":800},{"date":"2023-12-01 02:00:00","value":600},{"date":"2023-12-01 03:00:00","value":500},{"date":"2023-12-01 04:00:00","value":450}],"traffic_settings":{"current_capacity":2000,"baseline_traffic":1000,"scaling_buffer":0.2,"scale_up_threshold":0.8,"scale_down_threshold":0.3,"alert_threshold":1.5,"anomaly_threshold":3.0,"cost_per_unit":0.01,"fixed_cost_per_capacity":0.1,"base_scaling_time":5,"enable_auto_scaling":false}} # TrafficForecastingRequest | 

    try:
        # Generate traffic forecasting with infrastructure scaling recommendations
        api_response = api_instance.create_traffic_forecast(traffic_forecasting_request)
        print("The response of TrafficForecastingApi->create_traffic_forecast:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TrafficForecastingApi->create_traffic_forecast: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **traffic_forecasting_request** | [**TrafficForecastingRequest**](TrafficForecastingRequest.md)|  | 

### Return type

[**TrafficForecastingResponse**](TrafficForecastingResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful traffic forecasting generation |  -  |
**400** | Forecasting failed due to insufficient data or invalid parameters |  -  |
**401** | Unauthorized - Invalid or missing API key |  -  |
**422** | Validation error |  -  |
**500** | Internal server error during traffic forecasting |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

