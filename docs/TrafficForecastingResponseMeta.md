# TrafficForecastingResponseMeta


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timing** | [**TrafficForecastingResponseMetaTiming**](TrafficForecastingResponseMetaTiming.md) |  | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_response_meta import TrafficForecastingResponseMeta

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingResponseMeta from a JSON string
traffic_forecasting_response_meta_instance = TrafficForecastingResponseMeta.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingResponseMeta.to_json())

# convert the object into a dict
traffic_forecasting_response_meta_dict = traffic_forecasting_response_meta_instance.to_dict()
# create an instance of TrafficForecastingResponseMeta from a dict
traffic_forecasting_response_meta_from_dict = TrafficForecastingResponseMeta.from_dict(traffic_forecasting_response_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


