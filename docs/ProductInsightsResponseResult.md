# ProductInsightsResponseResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** |  | [optional] 
**tenant_context** | **str** |  | [optional] 
**product_info** | [**ProductInsightsResponseResultProductInfo**](ProductInsightsResponseResultProductInfo.md) |  | [optional] 
**base_currency** | **str** |  | [optional] 
**insights** | [**List[ProductInsight]**](ProductInsight.md) |  | [optional] 
**summary** | [**ProductInsightsResponseResultSummary**](ProductInsightsResponseResultSummary.md) |  | [optional] 
**comparison** | [**ProductInsightsResponseResultComparison**](ProductInsightsResponseResultComparison.md) |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_response_result import ProductInsightsResponseResult

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsResponseResult from a JSON string
product_insights_response_result_instance = ProductInsightsResponseResult.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsResponseResult.to_json())

# convert the object into a dict
product_insights_response_result_dict = product_insights_response_result_instance.to_dict()
# create an instance of ProductInsightsResponseResult from a dict
product_insights_response_result_from_dict = ProductInsightsResponseResult.from_dict(product_insights_response_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


