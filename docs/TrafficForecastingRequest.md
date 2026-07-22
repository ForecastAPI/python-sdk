# TrafficForecastingRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** | Metric identifier (e.g., endpoint name, service name) | 
**frequency** | **str** | Data frequency for forecasting: - M: Minute (for real-time traffic) - H: Hourly - D: Daily - W: Weekly - MS: Monthly (start of month) - ME: Monthly (end of month) - Q: Quarterly - Y: Yearly  | 
**start_date** | **datetime** | Optional start date for the forecast period | [optional] 
**periods** | **int** | Number of periods to forecast ahead | 
**enable_intelligent_aggregation** | **bool** | Enable intelligent data aggregation for improved forecasting | [optional] 
**confidence_level** | **float** | Confidence level for forecast intervals (default 0.95) | [optional] 
**data** | [**List[TrafficForecastingRequestDataInner]**](TrafficForecastingRequestDataInner.md) | Historical traffic data for forecasting | 
**traffic_settings** | [**TrafficForecastingRequestTrafficSettings**](TrafficForecastingRequestTrafficSettings.md) |  | 

## Example

```python
from forecastapi.models.traffic_forecasting_request import TrafficForecastingRequest

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingRequest from a JSON string
traffic_forecasting_request_instance = TrafficForecastingRequest.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingRequest.to_json())

# convert the object into a dict
traffic_forecasting_request_dict = traffic_forecasting_request_instance.to_dict()
# create an instance of TrafficForecastingRequest from a dict
traffic_forecasting_request_from_dict = TrafficForecastingRequest.from_dict(traffic_forecasting_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


