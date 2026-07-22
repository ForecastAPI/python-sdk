# InventoryPlanningRequestDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** | Date of the data point (YYYY-MM-DD format) | 
**value** | **float** | Demand/sales quantity for the date | 

## Example

```python
from forecastapi.models.inventory_planning_request_data_inner import InventoryPlanningRequestDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of InventoryPlanningRequestDataInner from a JSON string
inventory_planning_request_data_inner_instance = InventoryPlanningRequestDataInner.from_json(json)
# print the JSON string representation of the object
print(InventoryPlanningRequestDataInner.to_json())

# convert the object into a dict
inventory_planning_request_data_inner_dict = inventory_planning_request_data_inner_instance.to_dict()
# create an instance of InventoryPlanningRequestDataInner from a dict
inventory_planning_request_data_inner_from_dict = InventoryPlanningRequestDataInner.from_dict(inventory_planning_request_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


