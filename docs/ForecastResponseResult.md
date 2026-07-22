# ForecastResponseResult

The baseline forecast — the only path that is stored and accuracy-tracked

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** | Echoes the series identifier from the request | [optional] 
**tenant_context** | **str** |  | [optional] 
**forecasts** | [**List[ForecastPeriod]**](ForecastPeriod.md) | One row per forecast period. Each period carries its own bounds, and they widen with horizon. | [optional] 
**model_info** | **Dict[str, object]** | The selected model (&#x60;best_model&#x60;), the models evaluated, the interval source, and per-model back-testing scores (smape/mape/mase) when validation runs. Also carries &#x60;bounds_transform&#x60; when &#x60;value_bounds&#x60; was sent, and &#x60;quantile_levels&#x60; when a fan was requested.  | [optional] 

## Example

```python
from forecastapi.models.forecast_response_result import ForecastResponseResult

# TODO update the JSON string below
json = "{}"
# create an instance of ForecastResponseResult from a JSON string
forecast_response_result_instance = ForecastResponseResult.from_json(json)
# print the JSON string representation of the object
print(ForecastResponseResult.to_json())

# convert the object into a dict
forecast_response_result_dict = forecast_response_result_instance.to_dict()
# create an instance of ForecastResponseResult from a dict
forecast_response_result_from_dict = ForecastResponseResult.from_dict(forecast_response_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


