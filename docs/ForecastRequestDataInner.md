# ForecastRequestDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** | Date of the data point | 
**value** | **float** | Numeric value for the data point | 

## Example

```python
from forecastapi.models.forecast_request_data_inner import ForecastRequestDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of ForecastRequestDataInner from a JSON string
forecast_request_data_inner_instance = ForecastRequestDataInner.from_json(json)
# print the JSON string representation of the object
print(ForecastRequestDataInner.to_json())

# convert the object into a dict
forecast_request_data_inner_dict = forecast_request_data_inner_instance.to_dict()
# create an instance of ForecastRequestDataInner from a dict
forecast_request_data_inner_from_dict = ForecastRequestDataInner.from_dict(forecast_request_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


