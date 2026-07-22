# AccumulatedForecastAssumptions

The assumptions behind the total and its band, stated explicitly

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**correlation** | **float** |  | [optional] 
**correlation_source** | **str** |  | [optional] 
**measured** | **bool** | True only when the correlation in force is our measured default — a caller-supplied value is never labelled measured | [optional] 
**basis** | **str** | The statistical model behind the total&#39;s band | [optional] 
**decay** | **float** |  | [optional] 
**discount_rate** | **float** |  | [optional] 
**periods_per_year** | **float** | How the annual discount rate was converted to the series frequency | [optional] 
**timing** | **str** |  | [optional] 

## Example

```python
from forecastapi.models.accumulated_forecast_assumptions import AccumulatedForecastAssumptions

# TODO update the JSON string below
json = "{}"
# create an instance of AccumulatedForecastAssumptions from a JSON string
accumulated_forecast_assumptions_instance = AccumulatedForecastAssumptions.from_json(json)
# print the JSON string representation of the object
print(AccumulatedForecastAssumptions.to_json())

# convert the object into a dict
accumulated_forecast_assumptions_dict = accumulated_forecast_assumptions_instance.to_dict()
# create an instance of AccumulatedForecastAssumptions from a dict
accumulated_forecast_assumptions_from_dict = AccumulatedForecastAssumptions.from_dict(accumulated_forecast_assumptions_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


