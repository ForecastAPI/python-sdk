# InventoryPlanningResponseResultForecastDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | **int** | Forecast period number | [optional] 
**var_date** | **date** | Date for this forecast period | [optional] 
**forecast** | **float** | Forecasted demand for this period | [optional] 
**lower** | **float** | Lower confidence bound | [optional] 
**upper** | **float** | Upper confidence bound | [optional] 

## Example

```python
from forecastapi.models.inventory_planning_response_result_forecast_data_inner import InventoryPlanningResponseResultForecastDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of InventoryPlanningResponseResultForecastDataInner from a JSON string
inventory_planning_response_result_forecast_data_inner_instance = InventoryPlanningResponseResultForecastDataInner.from_json(json)
# print the JSON string representation of the object
print(InventoryPlanningResponseResultForecastDataInner.to_json())

# convert the object into a dict
inventory_planning_response_result_forecast_data_inner_dict = inventory_planning_response_result_forecast_data_inner_instance.to_dict()
# create an instance of InventoryPlanningResponseResultForecastDataInner from a dict
inventory_planning_response_result_forecast_data_inner_from_dict = InventoryPlanningResponseResultForecastDataInner.from_dict(inventory_planning_response_result_forecast_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


