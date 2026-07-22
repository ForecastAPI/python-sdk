# ProductInsightsResponseResultSummaryAnalysisPeriod


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**start_date** | **str** |  | [optional] 
**end_date** | **str** |  | [optional] 
**total_days** | **int** |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_response_result_summary_analysis_period import ProductInsightsResponseResultSummaryAnalysisPeriod

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsResponseResultSummaryAnalysisPeriod from a JSON string
product_insights_response_result_summary_analysis_period_instance = ProductInsightsResponseResultSummaryAnalysisPeriod.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsResponseResultSummaryAnalysisPeriod.to_json())

# convert the object into a dict
product_insights_response_result_summary_analysis_period_dict = product_insights_response_result_summary_analysis_period_instance.to_dict()
# create an instance of ProductInsightsResponseResultSummaryAnalysisPeriod from a dict
product_insights_response_result_summary_analysis_period_from_dict = ProductInsightsResponseResultSummaryAnalysisPeriod.from_dict(product_insights_response_result_summary_analysis_period_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


