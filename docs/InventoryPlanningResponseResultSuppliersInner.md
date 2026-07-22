# InventoryPlanningResponseResultSuppliersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**supplier** | **str** | Supplier identifier | [optional] 
**order_quantity** | **float** | Recommended order quantity | [optional] 
**total_cost** | **float** | Total cost for the recommended order | [optional] 
**cost_per_unit** | **float** | Cost per unit from this supplier | [optional] 
**expected_delivery** | **date** | Expected delivery date | [optional] 
**lead_time_days** | **float** | Lead time in days | [optional] 
**minimum_order_quantity** | **float** | Minimum order quantity | [optional] 
**reliability_score** | **float** | Supplier reliability score | [optional] 
**lead_time_demand** | **float** | Expected demand during lead time | [optional] 
**safety_stock** | **float** | Calculated safety stock for this supplier | [optional] 
**reorder_point** | **float** | Calculated reorder point for this supplier | [optional] 
**reason** | **str** | Explanation for the recommendation | [optional] 

## Example

```python
from forecastapi.models.inventory_planning_response_result_suppliers_inner import InventoryPlanningResponseResultSuppliersInner

# TODO update the JSON string below
json = "{}"
# create an instance of InventoryPlanningResponseResultSuppliersInner from a JSON string
inventory_planning_response_result_suppliers_inner_instance = InventoryPlanningResponseResultSuppliersInner.from_json(json)
# print the JSON string representation of the object
print(InventoryPlanningResponseResultSuppliersInner.to_json())

# convert the object into a dict
inventory_planning_response_result_suppliers_inner_dict = inventory_planning_response_result_suppliers_inner_instance.to_dict()
# create an instance of InventoryPlanningResponseResultSuppliersInner from a dict
inventory_planning_response_result_suppliers_inner_from_dict = InventoryPlanningResponseResultSuppliersInner.from_dict(inventory_planning_response_result_suppliers_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


