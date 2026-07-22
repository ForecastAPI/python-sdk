# ProductInsightsResponseResultComparisonDevelopments

New / changed / resolved breakdown so repeat calls make genuine developments easy to pick out

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**new** | **List[Dict[str, object]]** |  | [optional] 
**changed** | **List[Dict[str, object]]** |  | [optional] 
**resolved** | **List[Dict[str, object]]** |  | [optional] 
**unchanged_count** | **int** |  | [optional] 
**summary** | **str** |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_response_result_comparison_developments import ProductInsightsResponseResultComparisonDevelopments

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsResponseResultComparisonDevelopments from a JSON string
product_insights_response_result_comparison_developments_instance = ProductInsightsResponseResultComparisonDevelopments.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsResponseResultComparisonDevelopments.to_json())

# convert the object into a dict
product_insights_response_result_comparison_developments_dict = product_insights_response_result_comparison_developments_instance.to_dict()
# create an instance of ProductInsightsResponseResultComparisonDevelopments from a dict
product_insights_response_result_comparison_developments_from_dict = ProductInsightsResponseResultComparisonDevelopments.from_dict(product_insights_response_result_comparison_developments_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


