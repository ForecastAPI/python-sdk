# AdjustedForecast

The what-if scenario path. Present only when `adjustments` was sent, as a sibling of `result` — never a field inside it. The adjusted path is never stored, so scenarios cannot pollute accuracy tracking. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**forecasts** | [**List[ForecastPeriod]**](ForecastPeriod.md) | The baseline path with every adjustment applied, in array order | [optional] 
**adjustments_applied** | [**List[AdjustedForecastAdjustmentsAppliedInner]**](AdjustedForecastAdjustmentsAppliedInner.md) | Echo of each adjustment as applied, in order | [optional] 
**stored** | **bool** | Always false — only the baseline in &#x60;result&#x60; is persisted and scored for accuracy | [optional] 

## Example

```python
from forecastapi.models.adjusted_forecast import AdjustedForecast

# TODO update the JSON string below
json = "{}"
# create an instance of AdjustedForecast from a JSON string
adjusted_forecast_instance = AdjustedForecast.from_json(json)
# print the JSON string representation of the object
print(AdjustedForecast.to_json())

# convert the object into a dict
adjusted_forecast_dict = adjusted_forecast_instance.to_dict()
# create an instance of AdjustedForecast from a dict
adjusted_forecast_from_dict = AdjustedForecast.from_dict(adjusted_forecast_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


