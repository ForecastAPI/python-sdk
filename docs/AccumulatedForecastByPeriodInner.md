# AccumulatedForecastByPeriodInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** |  | [optional] 
**weight** | **float** | survival × discount weight applied to this period (period 1 is 1.0) | [optional] 
**cumulative** | **float** | Running weighted total through this period | [optional] 
**cumulative_lower** | **float** | Running lower bound; present only when every period so far has a usable band | [optional] 
**cumulative_upper** | **float** |  | [optional] 

## Example

```python
from forecastapi.models.accumulated_forecast_by_period_inner import AccumulatedForecastByPeriodInner

# TODO update the JSON string below
json = "{}"
# create an instance of AccumulatedForecastByPeriodInner from a JSON string
accumulated_forecast_by_period_inner_instance = AccumulatedForecastByPeriodInner.from_json(json)
# print the JSON string representation of the object
print(AccumulatedForecastByPeriodInner.to_json())

# convert the object into a dict
accumulated_forecast_by_period_inner_dict = accumulated_forecast_by_period_inner_instance.to_dict()
# create an instance of AccumulatedForecastByPeriodInner from a dict
accumulated_forecast_by_period_inner_from_dict = AccumulatedForecastByPeriodInner.from_dict(accumulated_forecast_by_period_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


