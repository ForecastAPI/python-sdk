# GroupedForecastResultsReconciliation

How coherence was achieved. bottom_up reports the sibling correlation in force, its source, and `measured: false` — the correlation is a stated assumption, not a fitted number. min_trace reports the MinTrace variant and whether the non-negative solve was applied. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**method** | **str** |  | [optional] 
**correlation** | **float** | bottom_up only | [optional] 
**correlation_source** | **str** | bottom_up only | [optional] 
**measured** | **bool** | bottom_up only — always false; the cross-sibling correlation is an assumption | [optional] 
**variant** | **str** | min_trace only — the MinTrace weighting used | [optional] 
**nonnegative** | **bool** | min_trace only — whether the non-negative solve was applied | [optional] 

## Example

```python
from forecastapi.models.grouped_forecast_results_reconciliation import GroupedForecastResultsReconciliation

# TODO update the JSON string below
json = "{}"
# create an instance of GroupedForecastResultsReconciliation from a JSON string
grouped_forecast_results_reconciliation_instance = GroupedForecastResultsReconciliation.from_json(json)
# print the JSON string representation of the object
print(GroupedForecastResultsReconciliation.to_json())

# convert the object into a dict
grouped_forecast_results_reconciliation_dict = grouped_forecast_results_reconciliation_instance.to_dict()
# create an instance of GroupedForecastResultsReconciliation from a dict
grouped_forecast_results_reconciliation_from_dict = GroupedForecastResultsReconciliation.from_dict(grouped_forecast_results_reconciliation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


