# InventoryPlanningRequestInventorySettingsSuppliersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** | Unique supplier identifier | 
**lead_time_days** | **float** | Lead time in days for this supplier | 
**minimum_order_quantity** | **float** | Minimum order quantity required by supplier | 
**cost_per_unit** | **float** | Cost per unit from this supplier | 
**reliability_score** | **float** | Supplier reliability score (0.1-1.0, default 1.0) | [optional] 

## Example

```python
from forecastapi.models.inventory_planning_request_inventory_settings_suppliers_inner import InventoryPlanningRequestInventorySettingsSuppliersInner

# TODO update the JSON string below
json = "{}"
# create an instance of InventoryPlanningRequestInventorySettingsSuppliersInner from a JSON string
inventory_planning_request_inventory_settings_suppliers_inner_instance = InventoryPlanningRequestInventorySettingsSuppliersInner.from_json(json)
# print the JSON string representation of the object
print(InventoryPlanningRequestInventorySettingsSuppliersInner.to_json())

# convert the object into a dict
inventory_planning_request_inventory_settings_suppliers_inner_dict = inventory_planning_request_inventory_settings_suppliers_inner_instance.to_dict()
# create an instance of InventoryPlanningRequestInventorySettingsSuppliersInner from a dict
inventory_planning_request_inventory_settings_suppliers_inner_from_dict = InventoryPlanningRequestInventorySettingsSuppliersInner.from_dict(inventory_planning_request_inventory_settings_suppliers_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


