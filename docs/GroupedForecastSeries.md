# GroupedForecastSeries


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**segment** | **Dict[str, object]** | Names exactly the declared hierarchy dimensions — no more, no fewer. Values are non-empty scalars of at most 128 characters.  | 
**data** | [**List[GroupedForecastSeriesDataInner]**](GroupedForecastSeriesDataInner.md) | Historical data for this leaf (at most 1,000 points per series on the free tier) | 

## Example

```python
from forecastapi.models.grouped_forecast_series import GroupedForecastSeries

# TODO update the JSON string below
json = "{}"
# create an instance of GroupedForecastSeries from a JSON string
grouped_forecast_series_instance = GroupedForecastSeries.from_json(json)
# print the JSON string representation of the object
print(GroupedForecastSeries.to_json())

# convert the object into a dict
grouped_forecast_series_dict = grouped_forecast_series_instance.to_dict()
# create an instance of GroupedForecastSeries from a dict
grouped_forecast_series_from_dict = GroupedForecastSeries.from_dict(grouped_forecast_series_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


