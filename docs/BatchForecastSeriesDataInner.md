# BatchForecastSeriesDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** |  | 
**value** | **float** |  | 

## Example

```python
from forecastapi.models.batch_forecast_series_data_inner import BatchForecastSeriesDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of BatchForecastSeriesDataInner from a JSON string
batch_forecast_series_data_inner_instance = BatchForecastSeriesDataInner.from_json(json)
# print the JSON string representation of the object
print(BatchForecastSeriesDataInner.to_json())

# convert the object into a dict
batch_forecast_series_data_inner_dict = batch_forecast_series_data_inner_instance.to_dict()
# create an instance of BatchForecastSeriesDataInner from a dict
batch_forecast_series_data_inner_from_dict = BatchForecastSeriesDataInner.from_dict(batch_forecast_series_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


