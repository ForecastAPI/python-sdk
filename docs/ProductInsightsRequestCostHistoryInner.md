# ProductInsightsRequestCostHistoryInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **str** |  | 
**cost_price** | **float** |  | 
**currency** | **str** |  | [optional] 
**change_reason** | **str** |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_request_cost_history_inner import ProductInsightsRequestCostHistoryInner

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsRequestCostHistoryInner from a JSON string
product_insights_request_cost_history_inner_instance = ProductInsightsRequestCostHistoryInner.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsRequestCostHistoryInner.to_json())

# convert the object into a dict
product_insights_request_cost_history_inner_dict = product_insights_request_cost_history_inner_instance.to_dict()
# create an instance of ProductInsightsRequestCostHistoryInner from a dict
product_insights_request_cost_history_inner_from_dict = ProductInsightsRequestCostHistoryInner.from_dict(product_insights_request_cost_history_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


