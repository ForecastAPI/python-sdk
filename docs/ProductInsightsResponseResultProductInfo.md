# ProductInsightsResponseResultProductInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**group_id** | **str** |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_response_result_product_info import ProductInsightsResponseResultProductInfo

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsResponseResultProductInfo from a JSON string
product_insights_response_result_product_info_instance = ProductInsightsResponseResultProductInfo.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsResponseResultProductInfo.to_json())

# convert the object into a dict
product_insights_response_result_product_info_dict = product_insights_response_result_product_info_instance.to_dict()
# create an instance of ProductInsightsResponseResultProductInfo from a dict
product_insights_response_result_product_info_from_dict = ProductInsightsResponseResultProductInfo.from_dict(product_insights_response_result_product_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


