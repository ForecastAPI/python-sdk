# TrafficForecastingResponseMetaTiming


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**validation** | **float** | Time taken for request validation in milliseconds | [optional] 
**forecasting** | **float** | Time taken for traffic forecasting in milliseconds | [optional] 
**total** | **float** | Total processing time in milliseconds | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_response_meta_timing import TrafficForecastingResponseMetaTiming

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingResponseMetaTiming from a JSON string
traffic_forecasting_response_meta_timing_instance = TrafficForecastingResponseMetaTiming.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingResponseMetaTiming.to_json())

# convert the object into a dict
traffic_forecasting_response_meta_timing_dict = traffic_forecasting_response_meta_timing_instance.to_dict()
# create an instance of TrafficForecastingResponseMetaTiming from a dict
traffic_forecasting_response_meta_timing_from_dict = TrafficForecastingResponseMetaTiming.from_dict(traffic_forecasting_response_meta_timing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


