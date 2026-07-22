# ProductInsight


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_class** | **str** | Insight family (e.g. margin, sales, cost, lead_time) | [optional] 
**type** | **str** |  | [optional] 
**severity** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**metrics** | **Dict[str, object]** | The numbers behind the insight | [optional] 
**recommendation** | [**ProductInsightRecommendation**](ProductInsightRecommendation.md) |  | [optional] 
**confidence** | **str** |  | [optional] 
**var_date** | **str** |  | [optional] 
**change_status** | **str** | How this insight compares to the previous analysis of the same product — every insight is \&quot;new\&quot; on the first analysis | [optional] 

## Example

```python
from forecastapi.models.product_insight import ProductInsight

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsight from a JSON string
product_insight_instance = ProductInsight.from_json(json)
# print the JSON string representation of the object
print(ProductInsight.to_json())

# convert the object into a dict
product_insight_dict = product_insight_instance.to_dict()
# create an instance of ProductInsight from a dict
product_insight_from_dict = ProductInsight.from_dict(product_insight_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


