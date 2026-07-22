# InventoryPlanningResponseMetaTiming


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**validation** | **float** | Time taken for request validation in milliseconds | [optional] 
**planning** | **float** | Time taken for inventory planning in milliseconds | [optional] 
**total** | **float** | Total processing time in milliseconds | [optional] 

## Example

```python
from forecastapi.models.inventory_planning_response_meta_timing import InventoryPlanningResponseMetaTiming

# TODO update the JSON string below
json = "{}"
# create an instance of InventoryPlanningResponseMetaTiming from a JSON string
inventory_planning_response_meta_timing_instance = InventoryPlanningResponseMetaTiming.from_json(json)
# print the JSON string representation of the object
print(InventoryPlanningResponseMetaTiming.to_json())

# convert the object into a dict
inventory_planning_response_meta_timing_dict = inventory_planning_response_meta_timing_instance.to_dict()
# create an instance of InventoryPlanningResponseMetaTiming from a dict
inventory_planning_response_meta_timing_from_dict = InventoryPlanningResponseMetaTiming.from_dict(inventory_planning_response_meta_timing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


