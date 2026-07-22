# ForecastResponseMetaTiming


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**validation** | **float** | Time taken for validation in milliseconds | [optional] 
**selection** | **float** | Time taken for method selection in milliseconds | [optional] 
**forecasting** | **float** | Time taken for forecasting in milliseconds | [optional] 
**total** | **float** | Total processing time in milliseconds | [optional] 

## Example

```python
from forecastapi.models.forecast_response_meta_timing import ForecastResponseMetaTiming

# TODO update the JSON string below
json = "{}"
# create an instance of ForecastResponseMetaTiming from a JSON string
forecast_response_meta_timing_instance = ForecastResponseMetaTiming.from_json(json)
# print the JSON string representation of the object
print(ForecastResponseMetaTiming.to_json())

# convert the object into a dict
forecast_response_meta_timing_dict = forecast_response_meta_timing_instance.to_dict()
# create an instance of ForecastResponseMetaTiming from a dict
forecast_response_meta_timing_from_dict = ForecastResponseMetaTiming.from_dict(forecast_response_meta_timing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


