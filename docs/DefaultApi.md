# forecastapi.DefaultApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deprecated_v1**](DefaultApi.md#deprecated_v1) | **GET** /v1/{any} | Deprecated v1 endpoints


# **deprecated_v1**
> deprecated_v1(any)

Deprecated v1 endpoints

### Example


```python
import forecastapi
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
    api_instance = forecastapi.DefaultApi(api_client)
    any = 'any_example' # str | 

    try:
        # Deprecated v1 endpoints
        api_instance.deprecated_v1(any)
    except Exception as e:
        print("Exception when calling DefaultApi->deprecated_v1: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **any** | **str**|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**404** | API v1 has been deprecated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

