# InventoryPlanningRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** | SKU, Product ID, or other identifier for the inventory item | 
**frequency** | **str** | Data frequency for forecasting: - D: Daily - W: Weekly - M: Monthly (end of month) - MS: Monthly (start of month) - ME: Monthly (end of month) - Q: Quarterly - Y: Yearly  | 
**start_date** | **date** | Optional start date for the forecast period | [optional] 
**periods** | **int** | Number of periods to forecast ahead | 
**model** | **str** | Forecasting model behind the plan. &#x60;auto&#x60; routes the identifier to whichever model has proven most accurate on it, sharing the scorecard built by /v2/forecast and /v2/batch/forecast; on this endpoint auto&#39;s ensemble default runs as &#x60;standard&#x60; until a winner emerges, and the decision is reported in &#x60;meta.auto_selection&#x60;. Advanced variants, ensemble and auto cost 25% more usage.  | [optional] [default to 'standard']
**enable_intelligent_aggregation** | **bool** | Enable intelligent data aggregation for improved forecasting | [optional] 
**confidence_level** | **float** | Confidence level for forecast intervals (default 0.95) | [optional] 
**data** | [**List[InventoryPlanningRequestDataInner]**](InventoryPlanningRequestDataInner.md) | Historical demand/sales data for forecasting | 
**inventory_settings** | [**InventoryPlanningRequestInventorySettings**](InventoryPlanningRequestInventorySettings.md) |  | 

## Example

```python
from forecastapi.models.inventory_planning_request import InventoryPlanningRequest

# TODO update the JSON string below
json = "{}"
# create an instance of InventoryPlanningRequest from a JSON string
inventory_planning_request_instance = InventoryPlanningRequest.from_json(json)
# print the JSON string representation of the object
print(InventoryPlanningRequest.to_json())

# convert the object into a dict
inventory_planning_request_dict = inventory_planning_request_instance.to_dict()
# create an instance of InventoryPlanningRequest from a dict
inventory_planning_request_from_dict = InventoryPlanningRequest.from_dict(inventory_planning_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


