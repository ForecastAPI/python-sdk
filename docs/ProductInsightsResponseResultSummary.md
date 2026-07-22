# ProductInsightsResponseResultSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_insights** | **int** |  | [optional] 
**severity_distribution** | **Dict[str, int]** |  | [optional] 
**categories** | **List[str]** |  | [optional] 
**analysis_period** | [**ProductInsightsResponseResultSummaryAnalysisPeriod**](ProductInsightsResponseResultSummaryAnalysisPeriod.md) |  | [optional] 
**data_sources_analyzed** | **List[str]** |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_response_result_summary import ProductInsightsResponseResultSummary

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsResponseResultSummary from a JSON string
product_insights_response_result_summary_instance = ProductInsightsResponseResultSummary.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsResponseResultSummary.to_json())

# convert the object into a dict
product_insights_response_result_summary_dict = product_insights_response_result_summary_instance.to_dict()
# create an instance of ProductInsightsResponseResultSummary from a dict
product_insights_response_result_summary_from_dict = ProductInsightsResponseResultSummary.from_dict(product_insights_response_result_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


