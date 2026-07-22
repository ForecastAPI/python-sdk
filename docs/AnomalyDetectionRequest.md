# AnomalyDetectionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** | SKU, Product ID, or other identifier for the data series | 
**tenant_context** | **str** | Optional segmentation dimension. A series is identified by the pair identifier + tenant_context, so \&quot;mrr\&quot; on \&quot;plan-pro\&quot; and \&quot;mrr\&quot; on \&quot;plan-free\&quot; are two independent series, each with its own history and accuracy tracking. Despite the name it isn&#39;t only for multi-tenancy — use it for any slice: plan, region, store, channel, cohort, device type.  | [optional] 
**frequency** | **str** | Data frequency: - H: Hourly - D: Daily - W: Weekly - M: Monthly (end of month) - MS: Monthly (start of month) - ME: Monthly (end of month) - Q: Quarterly - Y: Yearly  | 
**start_date** | **date** | Optional start date for the forecast | [optional] 
**data_type** | **str** | Type of data (e.g., sales, demand, inventory, web_traffic) | 
**periods** | **int** | Number of periods to forecast | 
**model** | **str** | Which forecasting engine to use. The advanced variants and ensemble provide higher accuracy at a higher usage cost than standard.  | [optional] [default to 'standard']
**confidence_level** | **float** | Confidence level for the prediction interval. Note that 0.80 is the widest band the foundation models (advanced-quantized, advanced-patched, ensemble) produce natively — for genuinely distinct levels beyond that, request a quantile fan via &#x60;quantiles&#x60; instead of repeating the call at several confidence levels.  | [optional] [default to 0.8]
**quantiles** | **List[float]** | Decile levels to return per period — only deciles between 0.1 and 0.9 are accepted, because those are the levels every backend produces natively; anything finer would be interpolation served under a label the model never predicted. Adds a &#x60;quantiles&#x60; object to each forecast row alongside the usual bounds. Honoured by /v2/forecast and /v2/batch/forecast (request-level default or per-series override); rejected on grouped forecasts; ignored by other endpoints sharing this request shape.  | [optional] 
**value_bounds** | [**ValueBounds**](ValueBounds.md) |  | [optional] 
**adjustments** | [**List[AdjustmentsInner]**](AdjustmentsInner.md) | What-if scenario applied on top of the forecast (\&quot;assume we lose the enterprise deal\&quot;). Adjustments compose in array order — ×2 then +50 is not +50 then ×2. Each one moves the point, both bounds and any quantile fan together. Returns an &#x60;adjusted&#x60; block; the adjusted path is never stored or accuracy-tracked. Honoured by /v2/forecast and /v2/batch/forecast (request-level default or per-series override — period windows are checked against each series&#39; own horizon); rejected on grouped forecasts; ignored by other endpoints sharing this request shape.  | [optional] 
**accumulate** | [**AccumulateOptions**](AccumulateOptions.md) |  | [optional] 
**selection_metric** | **str** | Which back-testing error metric decides the winning model when candidates are compared: - auto: combined for demand/sales/inventory, sMAPE otherwise (default) - combined: 0.6·MASE + 0.4·sMAPE — balances accuracy and trend capture - mase: Mean Absolute Scaled Error — accuracy relative to a naive forecast - smape: Symmetric Mean Absolute Percentage Error  | [optional] 
**data** | [**List[ForecastRequestDataInner]**](ForecastRequestDataInner.md) | Historical time series data | 
**anomaly_settings** | [**AnomalyDetectionRequestAllOfAnomalySettings**](AnomalyDetectionRequestAllOfAnomalySettings.md) |  | [optional] 

## Example

```python
from forecastapi.models.anomaly_detection_request import AnomalyDetectionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AnomalyDetectionRequest from a JSON string
anomaly_detection_request_instance = AnomalyDetectionRequest.from_json(json)
# print the JSON string representation of the object
print(AnomalyDetectionRequest.to_json())

# convert the object into a dict
anomaly_detection_request_dict = anomaly_detection_request_instance.to_dict()
# create an instance of AnomalyDetectionRequest from a dict
anomaly_detection_request_from_dict = AnomalyDetectionRequest.from_dict(anomaly_detection_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


