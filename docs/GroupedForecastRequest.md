# GroupedForecastRequest

Configuration is request-level only: every node of a hierarchy must share `periods`, `frequency`, `model` and `confidence`, so per-series overrides are rejected rather than silently ignored. The planning parameters (`quantiles`, `value_bounds`, `adjustments`, `accumulate`) are not supported on grouped forecasts and are rejected explicitly. All series must end on the same date so forecast periods align; histories may start whenever they like — a segment that launched later simply contributes zero before its first data point. A request may expand to at most 250 nodes (leaves plus every derived aggregate and the total) across at most 4 hierarchy levels. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** | Names the measure being forecast (e.g. \&quot;mrr\&quot;). The hierarchy&#39;s total is stored under this identifier exactly like a plain /v2/forecast for it — the total of the hierarchy IS the measure.  | 
**tenant_context** | **str** | Optional tenant scope, independent of segment — tenancy keeps meaning \&quot;whose data is this\&quot;, segment means \&quot;which slice\&quot;.  | [optional] 
**hierarchy** | **List[str]** | The dimensions of the hierarchy, outermost first. Each series&#39; segment must name exactly these dimensions. | 
**reconciliation** | **str** | - bottom_up (default): only the leaves are forecast; every aggregate is the   exact sum of its children. Fast and cheap; best when leaf histories are   substantial enough to forecast well on their own. - min_trace: every node — aggregates included — is forecast, then MinTrace   optimally redistributes the disagreement between levels into a coherent set.   Costs one forecast per node, but lets the usually-smoother aggregate series   inform the result, which tends to help when leaves are short or noisy.  top_down is not supported and is rejected by name.  | [optional] [default to 'bottom_up']
**correlation** | **float** | bottom_up only — the assumed correlation between sibling errors when building aggregate confidence bands. 0 &#x3D; independent siblings, 1 &#x3D; perfectly correlated (equivalent to summing the bounds). Echoed back in the response and never labelled as measured.  | [optional] [default to 0.5]
**frequency** | **str** | Data frequency, shared by every series in the hierarchy | 
**periods** | **int** | Number of periods to forecast, shared by every node | 
**data_type** | **str** | Type of data (e.g., sales, demand, revenue). Sales-family types get non-negative reconciliation treatment. | [optional] [default to 'sales']
**model** | **str** | Forecasting engine used for every node. &#x60;auto&#x60; is not accepted here: it routes per series, and a hierarchy is reconciled under one model.  | [optional] [default to 'standard']
**confidence** | **float** | Confidence level for prediction intervals, shared by every node | [optional] [default to 0.8]
**confidence_level** | **float** | Alias for &#x60;confidence&#x60;; if both are sent, &#x60;confidence&#x60; wins | [optional] 
**series** | [**List[GroupedForecastSeries]**](GroupedForecastSeries.md) | The leaves of the hierarchy — one entry per combination of dimension values, each combination exactly once. Up to 200 series on a paid plan, 10 on the free tier. Aggregate levels are derived by the API and must not be sent.  | 

## Example

```python
from forecastapi.models.grouped_forecast_request import GroupedForecastRequest

# TODO update the JSON string below
json = "{}"
# create an instance of GroupedForecastRequest from a JSON string
grouped_forecast_request_instance = GroupedForecastRequest.from_json(json)
# print the JSON string representation of the object
print(GroupedForecastRequest.to_json())

# convert the object into a dict
grouped_forecast_request_dict = grouped_forecast_request_instance.to_dict()
# create an instance of GroupedForecastRequest from a dict
grouped_forecast_request_from_dict = GroupedForecastRequest.from_dict(grouped_forecast_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


