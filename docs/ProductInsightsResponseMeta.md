# ProductInsightsResponseMeta


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timing** | [**ProductInsightsResponseMetaTiming**](ProductInsightsResponseMetaTiming.md) |  | [optional] 
**data_quality** | [**ProductInsightsResponseMetaDataQuality**](ProductInsightsResponseMetaDataQuality.md) |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_response_meta import ProductInsightsResponseMeta

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsResponseMeta from a JSON string
product_insights_response_meta_instance = ProductInsightsResponseMeta.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsResponseMeta.to_json())

# convert the object into a dict
product_insights_response_meta_dict = product_insights_response_meta_instance.to_dict()
# create an instance of ProductInsightsResponseMeta from a dict
product_insights_response_meta_from_dict = ProductInsightsResponseMeta.from_dict(product_insights_response_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


