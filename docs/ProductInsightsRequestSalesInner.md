# ProductInsightsRequestSalesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **str** |  | 
**quantity_sold** | **float** |  | 
**selling_price** | **float** |  | 
**selling_price_converted** | **float** | Price converted to base_currency, when the sale was in another currency | [optional] 
**currency** | **str** |  | [optional] 
**customer_id** | **str** |  | [optional] 
**customer_segment** | **str** |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_request_sales_inner import ProductInsightsRequestSalesInner

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsRequestSalesInner from a JSON string
product_insights_request_sales_inner_instance = ProductInsightsRequestSalesInner.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsRequestSalesInner.to_json())

# convert the object into a dict
product_insights_request_sales_inner_dict = product_insights_request_sales_inner_instance.to_dict()
# create an instance of ProductInsightsRequestSalesInner from a dict
product_insights_request_sales_inner_from_dict = ProductInsightsRequestSalesInner.from_dict(product_insights_request_sales_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


