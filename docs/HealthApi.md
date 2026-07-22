# forecastapi.HealthApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_api_root**](HealthApi.md#get_api_root) | **GET** /v2 | API root endpoint
[**health_check**](HealthApi.md#health_check) | **GET** /v2/health | Health check endpoint


# **get_api_root**
> GetApiRoot200Response get_api_root()

API root endpoint

### Example


```python
import forecastapi
from forecastapi.models.get_api_root200_response import GetApiRoot200Response
from forecastapi.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://forecastapi.com
# See configuration.py for a list of all supported configuration parameters.
configuration = forecastapi.Configuration(
    host = "https://forecastapi.com"
)


# Enter a context with an instance of the API client
with forecastapi.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = forecastapi.HealthApi(api_client)

    try:
        # API root endpoint
        api_response = api_instance.get_api_root()
        print("The response of HealthApi->get_api_root:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HealthApi->get_api_root: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetApiRoot200Response**](GetApiRoot200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | API v2 Home |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **health_check**
> HealthCheck200Response health_check()

Health check endpoint

### Example


```python
import forecastapi
from forecastapi.models.health_check200_response import HealthCheck200Response
from forecastapi.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://forecastapi.com
# See configuration.py for a list of all supported configuration parameters.
configuration = forecastapi.Configuration(
    host = "https://forecastapi.com"
)


# Enter a context with an instance of the API client
with forecastapi.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = forecastapi.HealthApi(api_client)

    try:
        # Health check endpoint
        api_response = api_instance.health_check()
        print("The response of HealthApi->health_check:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HealthApi->health_check: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**HealthCheck200Response**](HealthCheck200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Health status of the API |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

