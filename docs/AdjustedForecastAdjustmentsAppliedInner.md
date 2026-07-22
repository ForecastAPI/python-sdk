# AdjustedForecastAdjustmentsAppliedInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | [optional] 
**value** | **float** |  | [optional] 
**from_period** | **int** |  | [optional] 
**to_period** | **int** |  | [optional] 
**periods_affected** | **int** | How many forecast periods this adjustment touched | [optional] 

## Example

```python
from forecastapi.models.adjusted_forecast_adjustments_applied_inner import AdjustedForecastAdjustmentsAppliedInner

# TODO update the JSON string below
json = "{}"
# create an instance of AdjustedForecastAdjustmentsAppliedInner from a JSON string
adjusted_forecast_adjustments_applied_inner_instance = AdjustedForecastAdjustmentsAppliedInner.from_json(json)
# print the JSON string representation of the object
print(AdjustedForecastAdjustmentsAppliedInner.to_json())

# convert the object into a dict
adjusted_forecast_adjustments_applied_inner_dict = adjusted_forecast_adjustments_applied_inner_instance.to_dict()
# create an instance of AdjustedForecastAdjustmentsAppliedInner from a dict
adjusted_forecast_adjustments_applied_inner_from_dict = AdjustedForecastAdjustmentsAppliedInner.from_dict(adjusted_forecast_adjustments_applied_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


