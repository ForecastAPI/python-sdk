# ProductInsightRecommendation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**priority** | **str** |  | [optional] 

## Example

```python
from forecastapi.models.product_insight_recommendation import ProductInsightRecommendation

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightRecommendation from a JSON string
product_insight_recommendation_instance = ProductInsightRecommendation.from_json(json)
# print the JSON string representation of the object
print(ProductInsightRecommendation.to_json())

# convert the object into a dict
product_insight_recommendation_dict = product_insight_recommendation_instance.to_dict()
# create an instance of ProductInsightRecommendation from a dict
product_insight_recommendation_from_dict = ProductInsightRecommendation.from_dict(product_insight_recommendation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


