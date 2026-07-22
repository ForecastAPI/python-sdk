# ProductInsightsResponseMetaDataQuality


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_data_points** | **int** |  | [optional] 
**datasets_provided** | **List[str]** |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_response_meta_data_quality import ProductInsightsResponseMetaDataQuality

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsResponseMetaDataQuality from a JSON string
product_insights_response_meta_data_quality_instance = ProductInsightsResponseMetaDataQuality.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsResponseMetaDataQuality.to_json())

# convert the object into a dict
product_insights_response_meta_data_quality_dict = product_insights_response_meta_data_quality_instance.to_dict()
# create an instance of ProductInsightsResponseMetaDataQuality from a dict
product_insights_response_meta_data_quality_from_dict = ProductInsightsResponseMetaDataQuality.from_dict(product_insights_response_meta_data_quality_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


