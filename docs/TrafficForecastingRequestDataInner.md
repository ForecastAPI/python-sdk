# TrafficForecastingRequestDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **str** | Date/time of the data point (supports both date and datetime formats) | 
**value** | **float** | Traffic volume for the period | 

## Example

```python
from forecastapi.models.traffic_forecasting_request_data_inner import TrafficForecastingRequestDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingRequestDataInner from a JSON string
traffic_forecasting_request_data_inner_instance = TrafficForecastingRequestDataInner.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingRequestDataInner.to_json())

# convert the object into a dict
traffic_forecasting_request_data_inner_dict = traffic_forecasting_request_data_inner_instance.to_dict()
# create an instance of TrafficForecastingRequestDataInner from a dict
traffic_forecasting_request_data_inner_from_dict = TrafficForecastingRequestDataInner.from_dict(traffic_forecasting_request_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


