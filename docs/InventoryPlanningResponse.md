# InventoryPlanningResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result** | [**InventoryPlanningResponseResult**](InventoryPlanningResponseResult.md) |  | [optional] 
**meta** | [**InventoryPlanningResponseMeta**](InventoryPlanningResponseMeta.md) |  | [optional] 

## Example

```python
from forecastapi.models.inventory_planning_response import InventoryPlanningResponse

# TODO update the JSON string below
json = "{}"
# create an instance of InventoryPlanningResponse from a JSON string
inventory_planning_response_instance = InventoryPlanningResponse.from_json(json)
# print the JSON string representation of the object
print(InventoryPlanningResponse.to_json())

# convert the object into a dict
inventory_planning_response_dict = inventory_planning_response_instance.to_dict()
# create an instance of InventoryPlanningResponse from a dict
inventory_planning_response_from_dict = InventoryPlanningResponse.from_dict(inventory_planning_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


