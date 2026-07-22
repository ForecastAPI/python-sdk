# ForecastResponseMeta


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**selection_metric** | **str** | The back-testing metric that actually chose the winning model | [optional] 
**timing** | [**ForecastResponseMetaTiming**](ForecastResponseMetaTiming.md) |  | [optional] 

## Example

```python
from forecastapi.models.forecast_response_meta import ForecastResponseMeta

# TODO update the JSON string below
json = "{}"
# create an instance of ForecastResponseMeta from a JSON string
forecast_response_meta_instance = ForecastResponseMeta.from_json(json)
# print the JSON string representation of the object
print(ForecastResponseMeta.to_json())

# convert the object into a dict
forecast_response_meta_dict = forecast_response_meta_instance.to_dict()
# create an instance of ForecastResponseMeta from a dict
forecast_response_meta_from_dict = ForecastResponseMeta.from_dict(forecast_response_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


