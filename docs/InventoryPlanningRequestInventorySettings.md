# InventoryPlanningRequestInventorySettings

Current inventory status and supplier information

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**current_stock** | **float** | Current quantity in stock | 
**minimum_stock** | **float** | Minimum stock level to maintain | 
**service_level** | **float** | Target service level (probability of not stocking out) | 
**suppliers** | [**List[InventoryPlanningRequestInventorySettingsSuppliersInner]**](InventoryPlanningRequestInventorySettingsSuppliersInner.md) | Available suppliers with their characteristics | 

## Example

```python
from forecastapi.models.inventory_planning_request_inventory_settings import InventoryPlanningRequestInventorySettings

# TODO update the JSON string below
json = "{}"
# create an instance of InventoryPlanningRequestInventorySettings from a JSON string
inventory_planning_request_inventory_settings_instance = InventoryPlanningRequestInventorySettings.from_json(json)
# print the JSON string representation of the object
print(InventoryPlanningRequestInventorySettings.to_json())

# convert the object into a dict
inventory_planning_request_inventory_settings_dict = inventory_planning_request_inventory_settings_instance.to_dict()
# create an instance of InventoryPlanningRequestInventorySettings from a dict
inventory_planning_request_inventory_settings_from_dict = InventoryPlanningRequestInventorySettings.from_dict(inventory_planning_request_inventory_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


