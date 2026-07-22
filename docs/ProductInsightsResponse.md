# ProductInsightsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result** | [**ProductInsightsResponseResult**](ProductInsightsResponseResult.md) |  | [optional] 
**meta** | [**ProductInsightsResponseMeta**](ProductInsightsResponseMeta.md) |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_response import ProductInsightsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsResponse from a JSON string
product_insights_response_instance = ProductInsightsResponse.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsResponse.to_json())

# convert the object into a dict
product_insights_response_dict = product_insights_response_instance.to_dict()
# create an instance of ProductInsightsResponse from a dict
product_insights_response_from_dict = ProductInsightsResponse.from_dict(product_insights_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


