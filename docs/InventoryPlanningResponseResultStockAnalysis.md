# InventoryPlanningResponseResultStockAnalysis

Current stock situation analysis

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**days_of_coverage** | **int** | Number of days current stock will last | [optional] 
**stockout_risk** | **float** | Risk of stockout (0-1, where 1 is certain stockout) | [optional] 
**next_order_date** | **date** | Recommended date for next order | [optional] 
**daily_demand_rate** | **float** | Average daily demand rate | [optional] 
**stock_status** | **str** | Current stock status assessment | [optional] 

## Example

```python
from forecastapi.models.inventory_planning_response_result_stock_analysis import InventoryPlanningResponseResultStockAnalysis

# TODO update the JSON string below
json = "{}"
# create an instance of InventoryPlanningResponseResultStockAnalysis from a JSON string
inventory_planning_response_result_stock_analysis_instance = InventoryPlanningResponseResultStockAnalysis.from_json(json)
# print the JSON string representation of the object
print(InventoryPlanningResponseResultStockAnalysis.to_json())

# convert the object into a dict
inventory_planning_response_result_stock_analysis_dict = inventory_planning_response_result_stock_analysis_instance.to_dict()
# create an instance of InventoryPlanningResponseResultStockAnalysis from a dict
inventory_planning_response_result_stock_analysis_from_dict = InventoryPlanningResponseResultStockAnalysis.from_dict(inventory_planning_response_result_stock_analysis_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


