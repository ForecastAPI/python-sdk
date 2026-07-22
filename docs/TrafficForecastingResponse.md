# TrafficForecastingResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result** | [**TrafficForecastingResponseResult**](TrafficForecastingResponseResult.md) |  | [optional] 
**meta** | [**TrafficForecastingResponseMeta**](TrafficForecastingResponseMeta.md) |  | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_response import TrafficForecastingResponse

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingResponse from a JSON string
traffic_forecasting_response_instance = TrafficForecastingResponse.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingResponse.to_json())

# convert the object into a dict
traffic_forecasting_response_dict = traffic_forecasting_response_instance.to_dict()
# create an instance of TrafficForecastingResponse from a dict
traffic_forecasting_response_from_dict = TrafficForecastingResponse.from_dict(traffic_forecasting_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


