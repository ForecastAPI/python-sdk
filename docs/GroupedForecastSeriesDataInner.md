# GroupedForecastSeriesDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** |  | 
**value** | **float** |  | 

## Example

```python
from forecastapi.models.grouped_forecast_series_data_inner import GroupedForecastSeriesDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of GroupedForecastSeriesDataInner from a JSON string
grouped_forecast_series_data_inner_instance = GroupedForecastSeriesDataInner.from_json(json)
# print the JSON string representation of the object
print(GroupedForecastSeriesDataInner.to_json())

# convert the object into a dict
grouped_forecast_series_data_inner_dict = grouped_forecast_series_data_inner_instance.to_dict()
# create an instance of GroupedForecastSeriesDataInner from a dict
grouped_forecast_series_data_inner_from_dict = GroupedForecastSeriesDataInner.from_dict(grouped_forecast_series_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


