# forecastapi.ProductInsightsApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_batch_product_insights**](ProductInsightsApi.md#create_batch_product_insights) | **POST** /v2/batch/product-insights | Submit a batch of products for insights analysis
[**create_product_insights**](ProductInsightsApi.md#create_product_insights) | **POST** /v2/product-insights | Analyze product performance for anomalies, trends and business insights
[**get_product_insights_batch**](ProductInsightsApi.md#get_product_insights_batch) | **GET** /v2/batch/product-insights/{batch_id} | Poll a product insights batch for status and results


# **create_batch_product_insights**
> ProductInsightsBatchStatusResponse create_batch_product_insights(product_insights_batch_request)

Submit a batch of products for insights analysis

Analyze up to 1,000 products in one asynchronous batch; each entry is the same
shape as a single `/v2/product-insights` request. Returns `202` with the batch
resource to poll via `GET /v2/batch/product-insights/{batch_id}`. The optional
`batch` and `parts` fields let a large batch be submitted in chunks that share one
batch id. Validation is per series: if any entry fails, the whole submission is
rejected with the failing entries listed by index.


### Example

* Api Key Authentication (apiKey):

```python
import forecastapi
from forecastapi.models.product_insights_batch_request import ProductInsightsBatchRequest
from forecastapi.models.product_insights_batch_status_response import ProductInsightsBatchStatusResponse
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
    api_instance = forecastapi.ProductInsightsApi(api_client)
    product_insights_batch_request = forecastapi.ProductInsightsBatchRequest() # ProductInsightsBatchRequest | 

    try:
        # Submit a batch of products for insights analysis
        api_response = api_instance.create_batch_product_insights(product_insights_batch_request)
        print("The response of ProductInsightsApi->create_batch_product_insights:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProductInsightsApi->create_batch_product_insights: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_insights_batch_request** | [**ProductInsightsBatchRequest**](ProductInsightsBatchRequest.md)|  | 

### Return type

[**ProductInsightsBatchStatusResponse**](ProductInsightsBatchStatusResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Accepted — the batch is queued for analysis |  -  |
**401** | Unauthorized - Invalid or missing API key |  -  |
**422** | One or more series failed validation |  -  |
**500** | Internal error during batch creation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_product_insights**
> ProductInsightsResponse create_product_insights(product_insights_request)

Analyze product performance for anomalies, trends and business insights

Analyzes a product's sales, purchase and cost-history data and returns classified
insights — margin compression, sales anomalies, cost changes, lead-time
reliability and more — each with severity, the metrics behind it and a
recommendation. At least one of `sales`, `purchases` or `cost_history` must be
provided. Analyses are stored per product, so repeat calls also return a
`comparison` against the previous analysis with a new/changed/resolved breakdown.


### Example

* Api Key Authentication (apiKey):

```python
import forecastapi
from forecastapi.models.product_insights_request import ProductInsightsRequest
from forecastapi.models.product_insights_response import ProductInsightsResponse
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
    api_instance = forecastapi.ProductInsightsApi(api_client)
    product_insights_request = forecastapi.ProductInsightsRequest() # ProductInsightsRequest | 

    try:
        # Analyze product performance for anomalies, trends and business insights
        api_response = api_instance.create_product_insights(product_insights_request)
        print("The response of ProductInsightsApi->create_product_insights:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProductInsightsApi->create_product_insights: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_insights_request** | [**ProductInsightsRequest**](ProductInsightsRequest.md)|  | 

### Return type

[**ProductInsightsResponse**](ProductInsightsResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Analysis results |  -  |
**400** | The analysis could not run on the provided data |  -  |
**401** | Unauthorized - Invalid or missing API key |  -  |
**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_product_insights_batch**
> ProductInsightsBatchStatusResponse get_product_insights_batch(batch_id)

Poll a product insights batch for status and results

### Example

* Api Key Authentication (apiKey):

```python
import forecastapi
from forecastapi.models.product_insights_batch_status_response import ProductInsightsBatchStatusResponse
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
    api_instance = forecastapi.ProductInsightsApi(api_client)
    batch_id = 'batch_id_example' # str | The batch identifier returned on submission

    try:
        # Poll a product insights batch for status and results
        api_response = api_instance.get_product_insights_batch(batch_id)
        print("The response of ProductInsightsApi->get_product_insights_batch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProductInsightsApi->get_product_insights_batch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **batch_id** | **str**| The batch identifier returned on submission | 

### Return type

[**ProductInsightsBatchStatusResponse**](ProductInsightsBatchStatusResponse.md)

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

