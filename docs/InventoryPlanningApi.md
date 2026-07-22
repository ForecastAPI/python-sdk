# forecastapi.InventoryPlanningApi

All URIs are relative to *https://forecastapi.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_inventory_plan**](InventoryPlanningApi.md#create_inventory_plan) | **POST** /v2/inventory-planning | Generate comprehensive inventory planning recommendations


# **create_inventory_plan**
> InventoryPlanningResponse create_inventory_plan(inventory_planning_request)

Generate comprehensive inventory planning recommendations

Generate inventory forecasts with supplier recommendations, reorder points, safety stock calculations,
and comprehensive stock analysis. This endpoint combines time series forecasting with inventory
optimization to provide actionable recommendations for stock management and procurement.

**Key Features:**
- Automatic forecasting method selection based on demand patterns
- Multi-supplier cost and lead time optimization
- Safety stock calculation with configurable service levels
- Reorder point recommendations with minimum order quantity considerations
- Stock analysis including stockout risk and days of coverage
- Real-time supplier performance evaluation


### Example

* Api Key Authentication (apiKey):

```python
import forecastapi
from forecastapi.models.inventory_planning_request import InventoryPlanningRequest
from forecastapi.models.inventory_planning_response import InventoryPlanningResponse
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
    api_instance = forecastapi.InventoryPlanningApi(api_client)
    inventory_planning_request = {"identifier":"SKU-12345","frequency":"M","start_date":"2024-01-01","periods":6,"enable_intelligent_aggregation":true,"data":[{"date":"2023-01-01","value":100},{"date":"2023-02-01","value":120},{"date":"2023-03-01","value":95},{"date":"2023-04-01","value":130},{"date":"2023-05-01","value":110}],"inventory_settings":{"current_stock":250,"minimum_stock":50,"service_level":0.95,"suppliers":[{"identifier":"supplier-a","lead_time_days":14,"minimum_order_quantity":100,"cost_per_unit":12.5,"reliability_score":0.98}]}} # InventoryPlanningRequest | 

    try:
        # Generate comprehensive inventory planning recommendations
        api_response = api_instance.create_inventory_plan(inventory_planning_request)
        print("The response of InventoryPlanningApi->create_inventory_plan:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InventoryPlanningApi->create_inventory_plan: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inventory_planning_request** | [**InventoryPlanningRequest**](InventoryPlanningRequest.md)|  | 

### Return type

[**InventoryPlanningResponse**](InventoryPlanningResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful inventory planning generation |  -  |
**400** | Planning failed due to insufficient data or invalid parameters |  -  |
**401** | Unauthorized - Invalid or missing API key |  -  |
**422** | Validation error |  -  |
**500** | Internal server error during inventory planning |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

