# BatchForecastStatusResponseResultsSummary

Populated when the batch finalises

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_series** | **int** |  | [optional] 
**completed** | **int** |  | [optional] 
**failed** | **int** |  | [optional] 
**model_distribution** | **Dict[str, int]** |  | [optional] 
**total_processing_time_ms** | **float** |  | [optional] 
**avg_processing_time_ms** | **float** |  | [optional] 
**error** | **str** | Present only when the batch failed | [optional] 

## Example

```python
from forecastapi.models.batch_forecast_status_response_results_summary import BatchForecastStatusResponseResultsSummary

# TODO update the JSON string below
json = "{}"
# create an instance of BatchForecastStatusResponseResultsSummary from a JSON string
batch_forecast_status_response_results_summary_instance = BatchForecastStatusResponseResultsSummary.from_json(json)
# print the JSON string representation of the object
print(BatchForecastStatusResponseResultsSummary.to_json())

# convert the object into a dict
batch_forecast_status_response_results_summary_dict = batch_forecast_status_response_results_summary_instance.to_dict()
# create an instance of BatchForecastStatusResponseResultsSummary from a dict
batch_forecast_status_response_results_summary_from_dict = BatchForecastStatusResponseResultsSummary.from_dict(batch_forecast_status_response_results_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


