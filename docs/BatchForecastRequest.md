# BatchForecastRequest

Either `series` (inline) or `file_key` (file-based, from /v2/batch/forecast/presign) is required. Every other field is a request-level default that each series inherits unless it declares its own override — `model` included. `confidence_level` is accepted as an alias for `confidence`; if both are sent, `confidence` wins. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**series** | [**List[BatchForecastSeries]**](BatchForecastSeries.md) | The series to forecast — up to 100,000 per call on a paid plan, 10 on the free tier | [optional] 
**file_key** | **str** | Instead of inline &#x60;series&#x60; — the key returned by /v2/batch/forecast/presign, after uploading a JSON file of the same shape as this request body (an object with a &#x60;series&#x60; array). Series from a file are validated as they are streamed: an invalid series fails that series, not the whole batch.  | [optional] 
**periods** | **int** | Default forecast horizon for series that don&#39;t set their own | [optional] [default to 6]
**frequency** | **str** | Default data frequency | [optional] 
**data_type** | **str** | Default data type | [optional] 
**model** | **str** | Default forecasting engine for series that don&#39;t set their own. &#x60;auto&#x60; routes each series independently on its own realized-accuracy scorecard. Usage is billed per series at its effective model&#39;s rate.  | [optional] [default to 'standard']
**confidence** | **float** | Default confidence level for prediction intervals | [optional] [default to 0.8]
**confidence_level** | **float** | Alias for &#x60;confidence&#x60; | [optional] 
**quantiles** | **List[float]** | Decile levels to return per period — only deciles between 0.1 and 0.9 are accepted, because those are the levels every backend produces natively; anything finer would be interpolation served under a label the model never predicted. Adds a &#x60;quantiles&#x60; object to each forecast row alongside the usual bounds. Honoured by /v2/forecast and /v2/batch/forecast (request-level default or per-series override); rejected on grouped forecasts; ignored by other endpoints sharing this request shape.  | [optional] 
**value_bounds** | [**ValueBounds**](ValueBounds.md) |  | [optional] 
**adjustments** | [**List[AdjustmentsInner]**](AdjustmentsInner.md) | What-if scenario applied on top of the forecast (\&quot;assume we lose the enterprise deal\&quot;). Adjustments compose in array order — ×2 then +50 is not +50 then ×2. Each one moves the point, both bounds and any quantile fan together. Returns an &#x60;adjusted&#x60; block; the adjusted path is never stored or accuracy-tracked. Honoured by /v2/forecast and /v2/batch/forecast (request-level default or per-series override — period windows are checked against each series&#39; own horizon); rejected on grouped forecasts; ignored by other endpoints sharing this request shape.  | [optional] 
**accumulate** | [**AccumulateOptions**](AccumulateOptions.md) |  | [optional] 

## Example

```python
from forecastapi.models.batch_forecast_request import BatchForecastRequest

# TODO update the JSON string below
json = "{}"
# create an instance of BatchForecastRequest from a JSON string
batch_forecast_request_instance = BatchForecastRequest.from_json(json)
# print the JSON string representation of the object
print(BatchForecastRequest.to_json())

# convert the object into a dict
batch_forecast_request_dict = batch_forecast_request_instance.to_dict()
# create an instance of BatchForecastRequest from a dict
batch_forecast_request_from_dict = BatchForecastRequest.from_dict(batch_forecast_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


