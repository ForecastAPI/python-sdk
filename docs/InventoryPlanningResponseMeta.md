# InventoryPlanningResponseMeta


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timing** | [**InventoryPlanningResponseMetaTiming**](InventoryPlanningResponseMetaTiming.md) |  | [optional] 
**auto_selection** | [**AutoSelection**](AutoSelection.md) |  | [optional] 

## Example

```python
from forecastapi.models.inventory_planning_response_meta import InventoryPlanningResponseMeta

# TODO update the JSON string below
json = "{}"
# create an instance of InventoryPlanningResponseMeta from a JSON string
inventory_planning_response_meta_instance = InventoryPlanningResponseMeta.from_json(json)
# print the JSON string representation of the object
print(InventoryPlanningResponseMeta.to_json())

# convert the object into a dict
inventory_planning_response_meta_dict = inventory_planning_response_meta_instance.to_dict()
# create an instance of InventoryPlanningResponseMeta from a dict
inventory_planning_response_meta_from_dict = InventoryPlanningResponseMeta.from_dict(inventory_planning_response_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


