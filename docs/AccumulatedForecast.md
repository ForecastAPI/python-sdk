# AccumulatedForecast

Cumulative projection over the forecast path. Present only when `accumulate` was sent, as a sibling of `result`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **float** | Σ (value × survival × discount) over the horizon. Null when a period lacks a usable point forecast (see &#x60;total_reason&#x60;). | [optional] 
**total_reason** | **str** | Why &#x60;total&#x60; is null; null when the total is usable | [optional] 
**lower** | **float** | Lower bound of the total under the stated correlation assumption. Null with an &#x60;interval_reason&#x60; when any period lacks a band or its coverage is unknown — rather than a band built from a partial set of variances.  | [optional] 
**upper** | **float** |  | [optional] 
**interval_reason** | **str** | Why the total&#39;s band is absent; null when the band is present | [optional] 
**confidence_level** | **float** | Coverage the total&#39;s band targets | [optional] 
**path** | **str** | Which path was accumulated — &#x60;adjusted&#x60; when &#x60;adjustments&#x60; was also sent, otherwise &#x60;baseline&#x60; | [optional] 
**assumptions** | [**AccumulatedForecastAssumptions**](AccumulatedForecastAssumptions.md) |  | [optional] 
**by_period** | [**List[AccumulatedForecastByPeriodInner]**](AccumulatedForecastByPeriodInner.md) | Running accumulation per period — &#x60;cumulative&#x60; through period L is the number a lead-time/safety-stock calculation reads | [optional] 

## Example

```python
from forecastapi.models.accumulated_forecast import AccumulatedForecast

# TODO update the JSON string below
json = "{}"
# create an instance of AccumulatedForecast from a JSON string
accumulated_forecast_instance = AccumulatedForecast.from_json(json)
# print the JSON string representation of the object
print(AccumulatedForecast.to_json())

# convert the object into a dict
accumulated_forecast_dict = accumulated_forecast_instance.to_dict()
# create an instance of AccumulatedForecast from a dict
accumulated_forecast_from_dict = AccumulatedForecast.from_dict(accumulated_forecast_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


