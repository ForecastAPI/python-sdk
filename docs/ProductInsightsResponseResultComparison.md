# ProductInsightsResponseResultComparison

Present from the second analysis of a product onward; null on the first

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_from** | **datetime** | Timestamp of the previous analysis | [optional] 
**to** | **datetime** |  | [optional] 
**result** | **Dict[str, object]** |  | [optional] 
**developments** | [**ProductInsightsResponseResultComparisonDevelopments**](ProductInsightsResponseResultComparisonDevelopments.md) |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_response_result_comparison import ProductInsightsResponseResultComparison

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsResponseResultComparison from a JSON string
product_insights_response_result_comparison_instance = ProductInsightsResponseResultComparison.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsResponseResultComparison.to_json())

# convert the object into a dict
product_insights_response_result_comparison_dict = product_insights_response_result_comparison_instance.to_dict()
# create an instance of ProductInsightsResponseResultComparison from a dict
product_insights_response_result_comparison_from_dict = ProductInsightsResponseResultComparison.from_dict(product_insights_response_result_comparison_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


