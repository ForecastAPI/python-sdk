# InventoryPlanningResponseResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** | Product identifier from the request | [optional] 
**current_stock** | **float** | Current stock level | [optional] 
**minimum_stock** | **float** | Minimum stock level to maintain | [optional] 
**reorder_point** | **float** | Recommended reorder point for optimal supplier | [optional] 
**safety_stock** | **float** | Calculated safety stock for optimal supplier | [optional] 
**suppliers** | [**List[InventoryPlanningResponseResultSuppliersInner]**](InventoryPlanningResponseResultSuppliersInner.md) | Analysis and recommendations for each supplier | [optional] 
**stock_analysis** | [**InventoryPlanningResponseResultStockAnalysis**](InventoryPlanningResponseResultStockAnalysis.md) |  | [optional] 
**forecast_data** | [**List[InventoryPlanningResponseResultForecastDataInner]**](InventoryPlanningResponseResultForecastDataInner.md) | Underlying forecast data used for planning | [optional] 

## Example

```python
from forecastapi.models.inventory_planning_response_result import InventoryPlanningResponseResult

# TODO update the JSON string below
json = "{}"
# create an instance of InventoryPlanningResponseResult from a JSON string
inventory_planning_response_result_instance = InventoryPlanningResponseResult.from_json(json)
# print the JSON string representation of the object
print(InventoryPlanningResponseResult.to_json())

# convert the object into a dict
inventory_planning_response_result_dict = inventory_planning_response_result_instance.to_dict()
# create an instance of InventoryPlanningResponseResult from a dict
inventory_planning_response_result_from_dict = InventoryPlanningResponseResult.from_dict(inventory_planning_response_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


