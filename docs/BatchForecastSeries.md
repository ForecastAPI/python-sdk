# BatchForecastSeries


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** | SKU, Product ID, or other identifier for this series | 
**tenant_context** | **str** | Optional segmentation dimension — the same identifier may appear under several tenant_context values in one batch | [optional] 
**data** | [**List[BatchForecastSeriesDataInner]**](BatchForecastSeriesDataInner.md) | Historical data for this series (at most 1,000 points per series on the free tier) | 
**periods** | **int** | Override of the request-level horizon for this series | [optional] 
**frequency** | **str** | Override of the request-level frequency | [optional] 
**data_type** | **str** | Override of the request-level data type | [optional] 
**confidence** | **float** | Override of the request-level confidence | [optional] 
**confidence_level** | **float** | Alias for &#x60;confidence&#x60; | [optional] 
**quantiles** | **List[float]** | Decile levels to return per period — only deciles between 0.1 and 0.9 are accepted, because those are the levels every backend produces natively; anything finer would be interpolation served under a label the model never predicted. Adds a &#x60;quantiles&#x60; object to each forecast row alongside the usual bounds. Honoured by /v2/forecast and /v2/batch/forecast (request-level default or per-series override); rejected on grouped forecasts; ignored by other endpoints sharing this request shape.  | [optional] 
**value_bounds** | [**ValueBounds**](ValueBounds.md) |  | [optional] 
**adjustments** | [**List[AdjustmentsInner]**](AdjustmentsInner.md) | What-if scenario applied on top of the forecast (\&quot;assume we lose the enterprise deal\&quot;). Adjustments compose in array order — ×2 then +50 is not +50 then ×2. Each one moves the point, both bounds and any quantile fan together. Returns an &#x60;adjusted&#x60; block; the adjusted path is never stored or accuracy-tracked. Honoured by /v2/forecast and /v2/batch/forecast (request-level default or per-series override — period windows are checked against each series&#39; own horizon); rejected on grouped forecasts; ignored by other endpoints sharing this request shape.  | [optional] 
**accumulate** | [**AccumulateOptions**](AccumulateOptions.md) |  | [optional] 

## Example

```python
from forecastapi.models.batch_forecast_series import BatchForecastSeries

# TODO update the JSON string below
json = "{}"
# create an instance of BatchForecastSeries from a JSON string
batch_forecast_series_instance = BatchForecastSeries.from_json(json)
# print the JSON string representation of the object
print(BatchForecastSeries.to_json())

# convert the object into a dict
batch_forecast_series_dict = batch_forecast_series_instance.to_dict()
# create an instance of BatchForecastSeries from a dict
batch_forecast_series_from_dict = BatchForecastSeries.from_dict(batch_forecast_series_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


