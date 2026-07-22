# ProductInsightsRequestPurchasesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **str** |  | 
**quantity_purchased** | **float** |  | 
**cost_price** | **float** |  | 
**cost_price_converted** | **float** |  | [optional] 
**currency** | **str** |  | [optional] 
**supplier_id** | **str** |  | [optional] 
**purchase_order_date** | **date** | Used for lead-time reliability analysis | [optional] 
**expected_delivery_date** | **date** |  | [optional] 
**actual_delivery_date** | **date** |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_request_purchases_inner import ProductInsightsRequestPurchasesInner

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsRequestPurchasesInner from a JSON string
product_insights_request_purchases_inner_instance = ProductInsightsRequestPurchasesInner.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsRequestPurchasesInner.to_json())

# convert the object into a dict
product_insights_request_purchases_inner_dict = product_insights_request_purchases_inner_instance.to_dict()
# create an instance of ProductInsightsRequestPurchasesInner from a dict
product_insights_request_purchases_inner_from_dict = ProductInsightsRequestPurchasesInner.from_dict(product_insights_request_purchases_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


