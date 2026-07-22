# ProductInsightsRequestInsightSettings

Sensitivity tuning for the individual insight detectors

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sales_threshold** | **float** |  | [optional] 
**margin_threshold** | **float** |  | [optional] 
**cost_threshold** | **float** |  | [optional] 
**purchase_threshold** | **float** |  | [optional] 
**enable_seasonality_detection** | **bool** |  | [optional] 
**severity_levels** | **List[str]** | Only emit insights at these severities | [optional] 

## Example

```python
from forecastapi.models.product_insights_request_insight_settings import ProductInsightsRequestInsightSettings

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsRequestInsightSettings from a JSON string
product_insights_request_insight_settings_instance = ProductInsightsRequestInsightSettings.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsRequestInsightSettings.to_json())

# convert the object into a dict
product_insights_request_insight_settings_dict = product_insights_request_insight_settings_instance.to_dict()
# create an instance of ProductInsightsRequestInsightSettings from a dict
product_insights_request_insight_settings_from_dict = ProductInsightsRequestInsightSettings.from_dict(product_insights_request_insight_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


