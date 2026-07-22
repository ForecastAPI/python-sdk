# GroupedForecastNode


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** | The measure — the same for every node | [optional] 
**segment** | **Dict[str, object]** | The dimension values this node covers — empty for the total, all declared dimensions for a leaf | [optional] 
**level** | **int** | Depth in the tree; 0 is the total | [optional] 
**is_leaf** | **bool** |  | [optional] 
**parent** | **str** | Segment key of the parent node; null for the total | [optional] 
**children** | **List[str]** | Segment keys of the children; empty for leaves | [optional] 
**forecasts** | [**List[ForecastPeriod]**](ForecastPeriod.md) | The reconciled path — this is what is stored and accuracy-tracked per node | [optional] 
**model_info** | **Dict[str, object]** | Method and reconciliation details for this node. With min_trace, the node&#39;s unreconciled path is reported under &#x60;reconciliation.base_forecast&#x60;. When an aggregate band cannot be built honestly (a child&#39;s band coverage is unknown), the band is omitted and &#x60;reconciliation.interval_reason&#x60; states why.  | [optional] 

## Example

```python
from forecastapi.models.grouped_forecast_node import GroupedForecastNode

# TODO update the JSON string below
json = "{}"
# create an instance of GroupedForecastNode from a JSON string
grouped_forecast_node_instance = GroupedForecastNode.from_json(json)
# print the JSON string representation of the object
print(GroupedForecastNode.to_json())

# convert the object into a dict
grouped_forecast_node_dict = grouped_forecast_node_instance.to_dict()
# create an instance of GroupedForecastNode from a dict
grouped_forecast_node_from_dict = GroupedForecastNode.from_dict(grouped_forecast_node_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


