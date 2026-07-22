# BatchSeriesResult

One series' results — the same object a single forecast returns under `result` (identifier, tenant_context, forecasts, model_info). Unlike single forecasts, `adjusted` and `accumulated` live INSIDE this object, next to `forecasts` — a batch flattens each series into `results.data[entity_id]`, so there is no sibling level. For a failed series the object is `{\"error\": \"...\", \"reason\": \"...\"}` instead; null while the series is still pending. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** |  | [optional] 
**tenant_context** | **str** |  | [optional] 
**forecasts** | [**List[ForecastPeriod]**](ForecastPeriod.md) |  | [optional] 
**model_info** | **Dict[str, object]** |  | [optional] 
**adjusted** | [**AdjustedForecast**](AdjustedForecast.md) |  | [optional] 
**accumulated** | [**AccumulatedForecast**](AccumulatedForecast.md) |  | [optional] 
**error** | **str** | Present instead of forecasts when this series failed | [optional] 

## Example

```python
from forecastapi.models.batch_series_result import BatchSeriesResult

# TODO update the JSON string below
json = "{}"
# create an instance of BatchSeriesResult from a JSON string
batch_series_result_instance = BatchSeriesResult.from_json(json)
# print the JSON string representation of the object
print(BatchSeriesResult.to_json())

# convert the object into a dict
batch_series_result_dict = batch_series_result_instance.to_dict()
# create an instance of BatchSeriesResult from a dict
batch_series_result_from_dict = BatchSeriesResult.from_dict(batch_series_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


