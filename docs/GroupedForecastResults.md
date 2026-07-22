# GroupedForecastResults


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** |  | [optional] 
**tenant_context** | **str** |  | [optional] 
**hierarchy** | **List[str]** |  | [optional] 
**reconciliation** | [**GroupedForecastResultsReconciliation**](GroupedForecastResultsReconciliation.md) |  | [optional] 
**confidence_level** | **float** |  | [optional] 
**node_count** | **int** |  | [optional] 
**nodes** | [**Dict[str, GroupedForecastNode]**](GroupedForecastNode.md) | Every node of the hierarchy, keyed by segment key: &#x60;total&#x60; for the root, then e.g. &#x60;region&#x3D;eu&#x60; for aggregates and &#x60;plan&#x3D;pro|region&#x3D;eu&#x60; for leaves. Every parent equals the sum of its children in every period.  | [optional] 

## Example

```python
from forecastapi.models.grouped_forecast_results import GroupedForecastResults

# TODO update the JSON string below
json = "{}"
# create an instance of GroupedForecastResults from a JSON string
grouped_forecast_results_instance = GroupedForecastResults.from_json(json)
# print the JSON string representation of the object
print(GroupedForecastResults.to_json())

# convert the object into a dict
grouped_forecast_results_dict = grouped_forecast_results_instance.to_dict()
# create an instance of GroupedForecastResults from a dict
grouped_forecast_results_from_dict = GroupedForecastResults.from_dict(grouped_forecast_results_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


